# ⚙️ OPERATIONS Documentation

**Last Updated:** [YYYY-MM-DD]

> Documentation owner: [YOUR_OPS_LEAD]
>
> Related docs: ENGINEERING.md (what we're running), PRODUCT.md (what users see)

---

## 📋 Quick Facts

| | |
|---|---|
| **Infrastructure** | [AWS/GCP/DigitalOcean/etc] |
| **Database** | [PostgreSQL/MongoDB/etc] |
| **Monitoring** | [DataDog/New Relic/Prometheus/etc] |
| **Uptime Target** | [99.9% / 99.99% / etc] |
| **On-Call Schedule** | [Who's on call?] |

---

## 🚀 Deployment Process

### Pre-Deployment Checklist

Before deploying to production:

```
☐ All tests passing locally
☐ Code review approved
☐ No database migrations that lock tables
☐ Monitoring alerts configured
☐ Rollback plan documented
☐ Notify stakeholders
```

### Step 1: Staging Deployment

```bash
# Deploy to staging environment
[YOUR_DEPLOY_COMMAND] staging

# Run smoke tests
[YOUR_TEST_COMMAND] staging

# Verify in staging UI
# Go to: https://staging.example.com
```

### Step 2: Production Deployment

```bash
# Deploy to production
[YOUR_DEPLOY_COMMAND] production

# Verify deployment health
curl https://api.example.com/health

# Watch logs for errors
[YOUR_LOG_COMMAND] production --follow
```

### Step 3: Post-Deployment Verification

```
☐ Health check passes
☐ No spike in error rate
☐ Database migrations completed
☐ New features working as expected
☐ Logs are clean (no errors)
☐ Customers not reporting issues
```

### Rollback Procedure (If Needed)

```bash
# Rollback to previous version
[YOUR_DEPLOY_COMMAND] production rollback

# Verify rollback successful
curl https://api.example.com/health

# Notify team
```

**Time to rollback:** Should be <5 minutes

---

## 🏗️ Infrastructure Overview

```
                    ┌─ Load Balancer ─┐
                    │   (Route 53)     │
                    └────────┬─────────┘
                             │
                    ┌────────┴────────┐
                    │                 │
            ┌───────▼───────┐  ┌──────▼──────┐
            │  Web Server 1 │  │ Web Server 2 │
            │   (ECS Task)  │  │  (ECS Task)  │
            └───────┬───────┘  └──────┬───────┘
                    │                 │
                    └────────┬────────┘
                             │
                    ┌────────▼─────────┐
                    │  RDS Database    │
                    │  (PostgreSQL)    │
                    └──────────────────┘
                             │
                    ┌────────▼─────────┐
                    │   S3 Storage     │
                    │  (User uploads)  │
                    └──────────────────┘
```

### Key Services

| Service | Purpose | Provider | Cost |
|---------|---------|----------|------|
| **Load Balancer** | Distribute traffic | AWS Route 53 | $0.60/month |
| **Web Servers** | Run application | AWS ECS | $[X]/month |
| **Database** | Store data | AWS RDS | $[X]/month |
| **File Storage** | User uploads | AWS S3 | $[X]/month |
| **Monitoring** | Watch system | [Tool] | $[X]/month |
| **Log Aggregation** | Centralized logs | [Tool] | $[X]/month |

---

## 📊 Monitoring & Alerts

### Key Metrics We Monitor

| Metric | Alert Threshold | Who Gets Paged |
|--------|-----------------|---|
| **CPU Usage** | >80% | On-call engineer |
| **Memory Usage** | >85% | On-call engineer |
| **Error Rate** | >0.5% | On-call engineer |
| **API Response Time (p95)** | >2 seconds | On-call engineer |
| **Database Disk** | >80% full | DBA + on-call |
| **Request Queue** | >1000 pending | On-call engineer |

### Alert Channels

- **Page (immediate):** PagerDuty → SMS + phone call
- **Notify (30 min):** Email + Slack
- **Log (no alert):** Just in logs

### Dashboard Access

- **Main Dashboard:** [Link to monitoring dashboard]
- **Health Check:** [Link to status page]

---

## 🐛 Incident Response

### Incident Severity Levels

| Level | Response | Example |
|-------|----------|---------|
| **P1 (Critical)** | Page on-call immediately | Service completely down |
| **P2 (High)** | Page within 15 minutes | 50%+ of users affected |
| **P3 (Medium)** | Email within 1 hour | Feature broken, users can work around |
| **P4 (Low)** | No immediate response | Minor UI bug, cosmetic issue |

### When a P1 Alert Fires

```
1. On-call engineer gets paged
              ↓
2. Check monitoring dashboard
              ↓
3. Identify if it's real issue or false alarm
              ↓
4. Post in #incidents Slack channel
              ↓
5. If code-related: roll back last deployment
              ↓
6. If infrastructure: restart service
              ↓
7. Verify service recovered
              ↓
8. Post-mortem after on-call period
```

**Goal:** Detect and respond within 5 minutes

### Common Issues & Quick Fixes

| Issue | Symptom | Quick Fix |
|-------|---------|-----------|
| **Database Connection Pool Exhausted** | "connection refused" errors | Restart web servers |
| **Disk Full** | Uploads failing | Clear old logs or delete old uploads |
| **Memory Leak** | Service slow then crashes | Restart service |
| **Bad Deployment** | Sudden errors after deploy | Run rollback command |

---

## 📖 Runbook: Common Operational Tasks

### "Service is down"

**Checklist:**
```
☐ Check monitoring dashboard for alerts
☐ Verify all servers are running
☐ Check database is up
☐ Look at recent logs for errors
☐ Is it recent deployment? Rollback if needed
☐ Restart web servers if no obvious cause
☐ Check with engineering if still down
```

**Command to check status:**
```bash
kubectl get pods -n production
# Should see all pods with status "Running"
```

### "Database is slow"

**Checklist:**
```
☐ Check database CPU and memory usage
☐ Look at slowest queries in monitoring
☐ Kill any long-running queries
☐ Check for locks on tables
☐ Restart database if needed
```

**Command to find slow queries:**
```bash
[YOUR_SLOW_QUERY_COMMAND]
```

### "Out of disk space"

**Checklist:**
```
☐ Check which volume is full
☐ Clear old logs: [COMMAND]
☐ Delete old backups if safe
☐ Clear browser cache on web servers
☐ Increase volume size if needed
```

### "One server is down but service still works"

**Checklist:**
```
☐ Decide: restart it or let it scale up?
☐ If restarting: kubectl restart pod [POD_NAME]
☐ If scaling: let load balancer route around it
☐ Monitor other servers don't get overloaded
☐ Investigate why it crashed (logs)
```

---

## 🔄 Backup & Recovery

### Backup Strategy

| What | Frequency | Location | Retention |
|------|-----------|----------|-----------|
| **Database** | Daily | AWS backup, S3 copy | 30 days |
| **User Uploads** | Continuous | S3 with versioning | 30 days |
| **Configuration** | Manual | Git repo | Indefinite |

### Restoring from Backup

**If database is corrupted:**

```bash
# List available backups
[YOUR_BACKUP_LIST_COMMAND]

# Restore from timestamp
[YOUR_RESTORE_COMMAND] "2025-11-19 10:00:00"

# Verify restore worked
[YOUR_VERIFY_COMMAND]
```

**Estimated restore time:** 30 minutes to 2 hours depending on database size

---

## 🔐 Security Operations

### Access Control

| Role | Can Do | Who Has | Revoke Process |
|------|--------|---------|---|
| **On-Call Engineer** | Deploy, restart services, view logs | [3 people] | Remove from PagerDuty |
| **DevOps Engineer** | Infrastructure changes, manage servers | [2 people] | Remove SSH key |
| **Database Admin** | Restore backups, modify schema | [1 person] | Remove DB password |

### Secure Secrets Management

- Database passwords: [AWS Secrets Manager]
- API keys: [Vault / SSM Parameter Store]
- SSL certificates: [AWS Certificate Manager]

**Never commit secrets to git.** Use [YOUR_SECRETS_TOOL].

### Regular Security Tasks

```
☐ Monthly: Rotate database passwords
☐ Monthly: Review access logs for suspicious activity
☐ Quarterly: Audit who has production access
☐ Quarterly: Update SSL certificates
```

---

## 📱 On-Call Responsibilities

### Before Your On-Call Shift

```
☐ Verify you can access [Monitoring Dashboard]
☐ Test PagerDuty notifications work on your phone
☐ Know how to roll back a deployment
☐ Review recent incidents and their causes
☐ Ensure all runbooks are current
```

### During Your On-Call Shift

- Respond to pages within 5 minutes
- Assess severity immediately
- Escalate to engineering if needed
- Don't make major architectural changes
- Document what you did

### After Your On-Call Shift

- Write a quick handoff note for next person
- Update runbooks if you learned something
- Participate in post-mortems for any P1 incidents

---

## 📈 Capacity Planning

### Current Usage

| Resource | Current | Capacity | Utilization |
|----------|---------|----------|-------------|
| **CPU** | 35% | 100% | Low - plenty of headroom |
| **Memory** | 60% | 100% | Medium - watch this |
| **Disk** | 45% | 100% | Low - OK for now |
| **Database Connections** | 120 of 200 | 200 | 60% - OK |

### Scaling Plan

- **If CPU > 80%:** Add more web servers
- **If Memory > 85%:** Optimize code or add memory
- **If Disk > 80%:** Increase volume or delete old data
- **If connections > 150:** Increase connection pool

### Growth Projections

- **Users:** Projected 10K by Q2 2026
- **Storage:** Need 5TB by end of 2025
- **Bandwidth:** Expected to double by Q3 2026

---

## 🔧 Common Operational Procedures

### "Scaling up for traffic spike"

```bash
# Increase web server replicas
kubectl scale deployment web-app --replicas=10

# Watch deployment scale up
kubectl get deployment web-app --watch

# Verify load is balanced
# Check each server CPU in dashboard
```

### "Running a database migration"

```bash
# Create backup first
[BACKUP_COMMAND]

# Run migration (preferably during low traffic)
[MIGRATION_COMMAND]

# Verify migration successful
[VERIFY_COMMAND]

# Monitor for issues next hour
```

### "Deploying a hotfix"

```bash
# Deploy directly to production (no staging)
[DEPLOY_COMMAND] production

# Monitor error rate closely
watch [YOUR_MONITOR_COMMAND]

# Be ready to rollback if needed
# Issue: [ISSUE_BRIEF_DESC]
# Rollback: [ROLLBACK_COMMAND]
```

---

## 📞 Escalation Paths

**If service is down and you can't fix it:**
1. Page on-call engineer (if you're not on-call)
2. Page engineering lead if still not resolved in 10 minutes
3. Page CTO if still not resolved in 30 minutes

**If you need access you don't have:**
- Ask on-call engineer
- If urgent, ask engineering lead
- For permanent access, ask DevOps

---

## 🎓 Learning Resources

- [AWS Documentation]: [URL]
- [Kubernetes Docs]: [URL]
- [Our internal runbooks]: [Link]
- [Monitoring tool docs]: [URL]

---

## 🔮 Future Operations Improvements

- [ ] Auto-scaling based on load (not manual)
- [ ] Automated database backups to multiple regions
- [ ] Canary deployments (gradual rollout)
- [ ] Automated incident detection and initial response
- [ ] Full disaster recovery plan (geographically distributed)

---

## 📝 Operation Logs Template

When you perform major operations, document them:

```
Date/Time: 2025-11-19 14:30 UTC
Operation: [What you did]
Reason: [Why you did it]
Impact: [Service behavior before/after]
Duration: [How long it took]
Issues: [Any problems?]
Follow-up: [Anything to do next?]
```

---

**Related:**
- See ENGINEERING.md for technical details on what we're running
- See PRODUCT.md for understanding what users depend on
- See MISSION_CONTROL.md for workflow guidelines

---

**Keep this document updated with every incident. It's your operational memory.**
