# Developer Onboarding Tutorial: From Zero to Full-Stack

**A Complete Guide to Setting Up Your MacBook Air for Modern Development**

---

## Table of Contents

1. [Overview](#overview)
2. [Part 1: Setting Up Your Development Environment](#part-1-setting-up-your-development-environment)
3. [Part 2: GitHub Account & Desktop Setup](#part-2-github-account--desktop-setup)
4. [Part 3: Installing & Configuring VS Code](#part-3-installing--configuring-vs-code)
5. [Part 4: GitHub Copilot Setup (Claude & OpenAI)](#part-4-github-copilot-setup-claude--openai)
6. [Part 5: Your First Repository & Commit](#part-5-your-first-repository--commit)
7. [Part 6: The Baseball Card Collection Project](#part-6-the-baseball-card-collection-project)
8. [Part 7: Vibe Coding Prompts](#part-7-vibe-coding-prompts)
9. [Part 8: Future Enhancements](#part-8-future-enhancements)
10. [Troubleshooting](#troubleshooting)

---

## Overview

### What You'll Learn

By the end of this tutorial, you will:

- Have a fully configured MacBook Air development environment
- Understand how to use VS Code as your IDE
- Know how to create and manage GitHub repositories
- Be able to commit and push code from VS Code
- Use AI coding assistants (GitHub Copilot with Claude Sonnet 4.5 and OpenAI)
- Build a functional baseball card collection website

### What You'll Build

A **Baseball Card Collection Manager** - a web application that:
- Displays your card collection in a searchable/sortable grid
- Shows original 2009 Beckett values
- Fetches current market prices
- Calculates and displays percentage change in value

### Time Estimate

- Environment Setup: ~1-2 hours
- Project Build: ~3-4 hours (with AI assistance)
- Total: ~5-6 hours

---

## Part 1: Setting Up Your Development Environment

### Step 1.1: Install Homebrew (Mac Package Manager)

Homebrew makes installing software on your Mac much easier.

1. Open **Terminal** (press `Cmd + Space`, type "Terminal", press Enter)

2. Copy and paste this command, then press Enter:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

3. Follow the prompts (you'll need to enter your Mac password)

4. **Important**: After installation completes, Terminal will show you commands to add Homebrew to your PATH. Copy and run those commands. They'll look something like:

```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

5. Verify installation:

```bash
brew --version
```

You should see something like `Homebrew 4.x.x`

### Step 1.2: Install Node.js

Node.js is required for modern web development.

```bash
brew install node
```

Verify installation:

```bash
node --version
npm --version
```

### Step 1.3: Install Git

Git is for version control (tracking changes to your code).

```bash
brew install git
```

Verify installation:

```bash
git --version
```

### Step 1.4: Configure Git with Your Information

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## Part 2: GitHub Account & Desktop Setup

### Step 2.1: Create a GitHub Account

1. Go to [https://github.com](https://github.com)
2. Click **"Sign up"**
3. Enter your email address
4. Create a password
5. Choose a username (this will be public, so choose wisely!)
6. Solve the puzzle to verify you're human
7. Click **"Create account"**
8. Check your email and enter the verification code
9. Answer the personalization questions (or skip them)

**Tip**: Choose a professional username - this will be visible on all your projects.

### Step 2.2: Install GitHub Desktop

GitHub Desktop provides a visual interface for Git (easier than command line for beginners).

1. Go to [https://desktop.github.com](https://desktop.github.com)
2. Click **"Download for macOS"**
3. Open the downloaded file
4. Drag GitHub Desktop to your Applications folder
5. Open GitHub Desktop from Applications
6. Click **"Sign in to GitHub.com"**
7. Your browser will open - sign in with your GitHub credentials
8. Click **"Authorize desktop"**
9. Return to GitHub Desktop and complete setup

### Step 2.3: Configure GitHub Desktop

1. In GitHub Desktop, go to **Preferences** (Cmd + ,)
2. Under **Git**, verify your name and email are correct
3. Under **Integrations**, set External Editor to "Visual Studio Code" (we'll install this next)

---

## Part 3: Installing & Configuring VS Code

### Step 3.1: Download and Install VS Code

1. Go to [https://code.visualstudio.com](https://code.visualstudio.com)
2. Click **"Download for Mac"**
3. Open the downloaded `.zip` file
4. Drag **Visual Studio Code** to your Applications folder
5. Open VS Code from Applications
6. If prompted about opening an app from the internet, click **"Open"**

### Step 3.2: Add VS Code to Terminal PATH

This lets you open VS Code from Terminal by typing `code`.

1. Open VS Code
2. Press `Cmd + Shift + P` (opens Command Palette)
3. Type: `Shell Command: Install 'code' command in PATH`
4. Press Enter
5. Enter your Mac password if prompted

Verify it works:

```bash
code --version
```

### Step 3.3: Install Essential VS Code Extensions

Open VS Code and install these extensions:

1. Click the **Extensions icon** in the left sidebar (looks like 4 squares)
2. Search for and install each of these:

**Required Extensions:**
- **GitHub Copilot** - AI coding assistant (you'll configure this in Part 4)
- **GitHub Copilot Chat** - Chat interface for Copilot
- **Live Server** - Launch local dev server with live reload
- **Prettier - Code Formatter** - Auto-format your code
- **ESLint** - JavaScript linting
- **SQLite Viewer** - View SQLite databases in VS Code

**Optional but Helpful:**
- **Material Icon Theme** - Better file icons
- **Auto Rename Tag** - Rename paired HTML tags
- **GitLens** - Enhanced Git visualization

### Step 3.4: Configure VS Code Settings

1. Press `Cmd + ,` to open Settings
2. Search for and configure these settings:

- **Editor: Format On Save** - Check this box
- **Editor: Default Formatter** - Set to "Prettier - Code formatter"
- **Editor: Tab Size** - Set to 2
- **Files: Auto Save** - Set to "afterDelay"

---

## Part 4: GitHub Copilot Setup (Claude & OpenAI)

This is where the magic happens! GitHub Copilot is an AI assistant that helps you write code.

### Step 4.1: Get GitHub Copilot Subscription

1. Go to [https://github.com/settings/copilot](https://github.com/settings/copilot)
2. Click **"Enable GitHub Copilot"**
3. Choose your plan:
   - **Free trial** - 30 days free
   - **Individual** - $10/month or $100/year
   - **Pro** - $39/month (includes Copilot Chat with multiple models)
4. Enter payment information
5. Complete setup

**Note**: For access to Claude Sonnet 4.5, you'll need **GitHub Copilot Pro** or **GitHub Copilot Enterprise**.

### Step 4.2: Activate Copilot in VS Code

1. Open VS Code
2. Click the **Accounts icon** (person icon in bottom-left)
3. Click **"Sign in to use GitHub Copilot"**
4. Sign in with your GitHub account
5. Authorize VS Code to access Copilot

You should see a small Copilot icon in the bottom-right of VS Code.

### Step 4.3: Configure Copilot to Use Claude Sonnet 4.5

GitHub Copilot Pro gives you access to multiple AI models. Here's how to switch between them:

1. Click the **Copilot icon** in the bottom status bar of VS Code
2. Click **"Configure GitHub Copilot"**
3. In the Copilot Chat panel, you can select different models

**To use Claude Sonnet 4.5:**

1. Open Copilot Chat (click the chat icon in the sidebar)
2. At the bottom of the chat panel, click the model selector
3. Choose **"Claude 3.5 Sonnet"** (or the latest Claude model available)

**To use OpenAI GPT-4:**

1. Click the model selector
2. Choose **"GPT-4"** or **"GPT-4 Turbo"**

### Step 4.4: Test Both AI Models

Let's test both models to see the difference:

**Test 1: Claude Sonnet**

1. Select Claude in the model picker
2. In Copilot Chat, type:

```
Create a simple JavaScript function that calculates the percentage change between two numbers
```

**Test 2: OpenAI GPT-4**

1. Switch to GPT-4 in the model picker
2. Ask the same question

**Notice the differences!** Both will give you working code, but you'll likely notice:
- Claude tends to be more thorough in explanations
- Claude often provides cleaner, more maintainable code
- Claude better understands context and nuance

**Spoiler: Claude wins for most coding tasks!**

---

## Part 5: Your First Repository & Commit

### Step 5.1: Create a New Repository

**Option A: From GitHub.com**

1. Go to [https://github.com](https://github.com)
2. Click the **+** icon in the top-right
3. Select **"New repository"**
4. Repository name: `baseball-card-collection`
5. Description: `A web app to manage and track baseball card values`
6. Select **"Public"** or **"Private"**
7. Check **"Add a README file"**
8. Click **"Create repository"**

**Option B: From GitHub Desktop**

1. Open GitHub Desktop
2. Go to **File > New Repository**
3. Name: `baseball-card-collection`
4. Description: `A web app to manage and track baseball card values`
5. Choose a local path (e.g., `/Users/yourname/Projects`)
6. Check **"Initialize with a README"**
7. Click **"Create Repository"**
8. Click **"Publish repository"** to push to GitHub

### Step 5.2: Clone the Repository to Your Computer

If you created the repo on GitHub.com:

1. Open GitHub Desktop
2. Go to **File > Clone Repository**
3. Find `baseball-card-collection` in the list
4. Choose where to save it locally
5. Click **"Clone"**

### Step 5.3: Open the Project in VS Code

From GitHub Desktop:
1. Click **"Open in Visual Studio Code"** button

Or from Terminal:
```bash
cd ~/Projects/baseball-card-collection  # adjust path as needed
code .
```

### Step 5.4: Make Your First Commit

1. In VS Code, open `README.md`
2. Add some content:

```markdown
# Baseball Card Collection Manager

A web application to track and manage baseball card values.

## Features (Coming Soon)
- View all cards in a sortable grid
- Search by player, team, or year
- Track current market values
- Compare with historical prices
```

3. Save the file (Cmd + S)

**Commit from VS Code:**

1. Click the **Source Control icon** in the left sidebar (branch icon)
2. You'll see `README.md` listed under "Changes"
3. Click the **+** next to the file to stage it
4. Type a commit message: `Update README with project description`
5. Click the **checkmark** (Commit button)
6. Click **"Sync Changes"** to push to GitHub

**Or Commit from GitHub Desktop:**

1. Open GitHub Desktop
2. You'll see your changes listed
3. Enter a summary: `Update README with project description`
4. Click **"Commit to main"**
5. Click **"Push origin"**

**Congratulations!** You've made your first commit!

---

## Part 6: The Baseball Card Collection Project

### Project Architecture

For this beginner project, we'll use a simple but effective tech stack:

```
baseball-card-collection/
├── index.html          # Main page
├── styles/
│   └── main.css        # Styling
├── scripts/
│   ├── app.js          # Main application logic
│   ├── data.js         # Card data (converted from CSV)
│   └── api.js          # Price lookup functions
├── data/
│   └── cards.json      # Your card collection data
└── README.md
```

### Technology Choices

**Frontend:**
- HTML5, CSS3, JavaScript (vanilla)
- No framework needed for this beginner project
- Easy to understand and debug

**Data Storage:**
- JSON file (converted from your CSV)
- Could upgrade to SQLite later

**Styling:**
- CSS Grid for the card layout
- CSS Variables for easy theming

**Price API Options:**

Unfortunately, Beckett doesn't have a public API. Here are alternatives:

1. **eBay API** (Recommended for real prices)
   - Free to use
   - Shows actual market prices
   - Requires developer registration

2. **Manual Research Mode**
   - Start with static prices
   - Add current prices manually
   - Good for learning, limited for real use

3. **Sports Card Pro** (sportscardpro.com)
   - Has price guides
   - No public API, would need scraping

For this tutorial, we'll start with **manual price entry** and include code structure for an API integration you can add later.

### Step 6.1: Convert Your CSV to JSON

Your CSV file "grants baseball cards" has these columns:
- Card number
- Player Last name
- Player first name
- Year
- Team
- Becketts value as of 2/19/2009

We'll need to convert this to JSON format. Here's the structure:

```json
{
  "cards": [
    {
      "id": 1,
      "cardNumber": "123",
      "firstName": "Ken",
      "lastName": "Griffey Jr",
      "year": 1989,
      "team": "Seattle Mariners",
      "value2009": 45.00,
      "currentValue": null
    }
  ]
}
```

**Quick Conversion Method:**

1. Open your CSV in Excel or Google Sheets
2. Use an online CSV to JSON converter: https://csvjson.com/csv2json
3. Adjust the field names to match our format
4. Save as `data/cards.json`

---

## Part 7: Vibe Coding Prompts

Now the fun part! Use these prompts with GitHub Copilot (Claude Sonnet 4.5 recommended) to build your application.

### Prompt 1: Project Setup

Open Copilot Chat and use this prompt:

```
I'm building a baseball card collection website. I need you to create the basic project structure.

Create these files:
1. index.html - Main page with:
   - Header with title "Grant's Baseball Card Collection"
   - Search input field
   - Filter dropdowns for Year and Team
   - Sort buttons (by player name, year, value)
   - A container div for the card grid

2. styles/main.css - Modern styling with:
   - CSS Grid layout for the cards
   - Responsive design (works on mobile)
   - Clean, modern appearance
   - Hover effects on cards

Please create the complete HTML and CSS files. Use a clean, professional sports-themed color scheme.
```

### Prompt 2: Create the Card Display Component

```
Now I need the JavaScript to display baseball cards. Create scripts/app.js that:

1. Loads card data from data/cards.json
2. Renders each card in a grid with:
   - Card number
   - Player name (First Last)
   - Year and Team
   - 2009 Beckett Value (formatted as currency)
   - Current Value (formatted as currency, or "N/A" if not available)
   - Percentage change (calculated from 2009 to current, with + or - indicator)

3. Has functions for:
   - Searching by player name
   - Filtering by year
   - Filtering by team
   - Sorting by any column (ascending/descending)

4. Shows the total collection value at the top

Make the code well-commented so I can understand how it works.
```

### Prompt 3: Add Sample Data

```
Create a sample data/cards.json file with 10 example baseball cards. Include a mix of:
- Different years (1980s-2000s)
- Different teams
- Different value ranges ($5-$500)
- Include some famous players like Ken Griffey Jr, Derek Jeter, Cal Ripken Jr

Format each card with:
- id (number)
- cardNumber (string)
- firstName (string)
- lastName (string)
- year (number)
- team (string)
- value2009 (number - the Beckett value)
- currentValue (number or null)

For currentValue, set some as null and some with values higher or lower than 2009 to test the percentage change feature.
```

### Prompt 4: Add Search and Filter Functionality

```
Update the app.js to implement the search and filter functionality:

1. Search should filter cards in real-time as the user types
2. Search should match against firstName, lastName, and team
3. Filters should stack (year AND team filter together)
4. Include a "Clear Filters" button that resets everything
5. Show a count of "Showing X of Y cards"

Make sure the UI updates smoothly without page refresh.
```

### Prompt 5: Add Sorting Functionality

```
Add sorting to the card grid:

1. Clicking a column header should sort by that column
2. Clicking again should reverse the sort order
3. Show an arrow indicator for current sort direction
4. Sortable columns:
   - Player Name (alphabetical by lastName)
   - Year
   - Team
   - 2009 Value
   - Current Value
   - % Change

Maintain sort order when filters are applied.
```

### Prompt 6: Style the Percentage Change

```
Update the CSS to visually indicate the percentage change:

1. Positive changes should be:
   - Green text
   - Show a small up arrow icon
   - Format like "+45.5%"

2. Negative changes should be:
   - Red text
   - Show a small down arrow icon
   - Format like "-12.3%"

3. No change should be:
   - Gray text
   - Format like "0.0%"

4. No current value should show:
   - Italic gray text
   - Display "N/A"
```

### Prompt 7: Add Price Update Feature

```
Create a way to manually update current card prices:

1. Add an "Edit" button on each card
2. Clicking it opens a modal with:
   - Card info displayed
   - Input field for current value
   - Save and Cancel buttons

3. When saved:
   - Update the card data
   - Recalculate percentage change
   - Re-render the card
   - Save to localStorage so changes persist

Include basic form validation (must be a positive number).
```

### Prompt 8: Add Collection Statistics

```
Create a statistics summary section at the top of the page showing:

1. Total cards in collection
2. Total 2009 value (sum of all value2009)
3. Total current value (sum of all currentValue where not null)
4. Overall percentage change
5. Number of cards that increased in value
6. Number of cards that decreased in value
7. Most valuable card (by current value)
8. Best performer (highest % increase)

Update these stats whenever the data changes.
```

### Prompt 9: Export Functionality

```
Add the ability to export the card collection:

1. Add an "Export" button in the header
2. Options to export as:
   - CSV (for spreadsheets)
   - JSON (for backup)

3. The export should include all current data including updated prices
4. Filename should include the date, like "cards-export-2024-01-15.csv"
```

### Prompt 10: Import Functionality

```
Add the ability to import cards from a CSV file:

1. Add an "Import" button in the header
2. Show a file picker for CSV files
3. Parse the CSV with these columns:
   - Card number
   - Player Last name
   - Player first name
   - Year
   - Team
   - Becketts value

4. Convert to our JSON format
5. Add to existing collection (avoid duplicates based on cardNumber + year)
6. Show a summary of "Imported X new cards, Y duplicates skipped"
```

---

## Part 8: Future Enhancements

Once you've completed the basic project, here are ideas to level up:

### Add a Backend (FastAPI)

```
For the future: Create a FastAPI backend that:

1. Serves the card data from a SQLite database
2. Has endpoints for:
   - GET /cards - list all cards
   - GET /cards/{id} - get single card
   - POST /cards - add new card
   - PUT /cards/{id} - update card
   - DELETE /cards/{id} - delete card

3. Includes data validation with Pydantic models

This would teach me about:
- REST APIs
- Database design
- Python backend development
```

### Add Real Price API Integration

```
Research and implement a real price API:

1. Register for eBay Developer Program
2. Use the Finding API to search for completed listings
3. Calculate average sale price for each card
4. Update prices on a schedule (maybe weekly)

This would teach me about:
- Working with external APIs
- API authentication
- Data processing
```

### Add User Authentication

```
Add user accounts so multiple collectors can use the app:

1. Sign up / Login pages
2. Each user has their own collection
3. Secure password storage
4. Session management

This would teach me about:
- Security best practices
- User management
- Database relationships
```

### Deploy to the Internet

```
Deploy this app so it's accessible online:

Options:
1. Vercel - great for static sites
2. Netlify - similar to Vercel
3. GitHub Pages - free, works with GitHub

For the backend (if you add FastAPI):
1. Railway
2. Render
3. Fly.io

This would teach me about:
- Deployment pipelines
- Domain configuration
- Production environments
```

### Add a React Frontend

```
Rebuild the frontend using React:

1. Set up with Vite
2. Component structure:
   - App
   - Header
   - SearchBar
   - FilterPanel
   - CardGrid
   - CardItem
   - EditModal
   - Statistics

This would teach me about:
- Modern frontend frameworks
- Component-based architecture
- State management
```

---

## Troubleshooting

### Common Issues and Solutions

#### Homebrew Installation Fails

**Problem**: Permission denied errors

**Solution**:
```bash
sudo chown -R $(whoami) /usr/local/share/zsh /usr/local/share/zsh/site-functions
```

#### VS Code Can't Find 'code' Command

**Problem**: `code: command not found`

**Solution**:
1. Open VS Code
2. Cmd + Shift + P
3. Type "Shell Command"
4. Select "Install 'code' command in PATH"

#### GitHub Copilot Not Working

**Problem**: Copilot suggestions not appearing

**Solutions**:
1. Check you're signed into GitHub in VS Code
2. Verify your Copilot subscription is active
3. Check the Copilot icon in status bar - it should be active
4. Try restarting VS Code

#### Git Push Rejected

**Problem**: Permission denied when pushing

**Solutions**:
1. Ensure you're signed into GitHub Desktop
2. Check repository permissions on GitHub
3. Try cloning with HTTPS instead of SSH

#### JSON Parse Errors

**Problem**: Cards not loading

**Solutions**:
1. Validate JSON at https://jsonlint.com
2. Check for trailing commas
3. Ensure all strings are in double quotes

### Getting Help

1. **GitHub Copilot Chat**: Ask it to explain errors
2. **Stack Overflow**: Search for error messages
3. **GitHub Issues**: Check if others have the same problem
4. **MDN Web Docs**: Best resource for HTML/CSS/JavaScript

---

## Quick Reference Commands

### Terminal Commands

```bash
# Check versions
node --version
npm --version
git --version
code --version

# Navigate directories
cd ~/Projects          # Go to Projects folder
ls                     # List files
pwd                    # Show current directory

# Git commands
git status            # See changes
git add .             # Stage all changes
git commit -m "msg"   # Commit with message
git push              # Push to GitHub
git pull              # Pull from GitHub
```

### VS Code Shortcuts

| Action | Shortcut |
|--------|----------|
| Open Command Palette | Cmd + Shift + P |
| Open File | Cmd + P |
| Save File | Cmd + S |
| Save All | Cmd + Option + S |
| Find in File | Cmd + F |
| Find in Project | Cmd + Shift + F |
| Toggle Terminal | Ctrl + ` |
| Format Document | Shift + Option + F |
| Open Copilot Chat | Cmd + I |

### GitHub Desktop Shortcuts

| Action | Shortcut |
|--------|----------|
| Commit | Cmd + Enter |
| Push | Cmd + P |
| Pull | Cmd + Shift + P |
| View on GitHub | Cmd + Shift + G |

---

## Conclusion

Congratulations! By completing this tutorial, you've:

1. Set up a professional development environment on your MacBook Air
2. Created a GitHub account and learned version control
3. Configured VS Code with essential extensions
4. Experienced AI-assisted coding with GitHub Copilot
5. Compared Claude Sonnet 4.5 and OpenAI GPT-4 (Claude wins!)
6. Built a functional web application from scratch

### What's Next?

1. **Complete the baseball card project** using the prompts in Part 7
2. **Import your actual card data** from the CSV file
3. **Experiment with the future enhancements** in Part 8
4. **Build more projects** to reinforce your learning

Remember: The best way to learn coding is by doing. Don't be afraid to experiment, break things, and ask your AI assistant for help!

---

**Happy Coding!**

*This tutorial was created using Claude Sonnet 4.5 - proving once again that Claude wins!*
