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

### Step 1.2: Install R

R is a programming language for statistical computing and data visualization.

```bash
brew install r
```

Verify installation:

```bash
R --version
```

### Step 1.3: Install RStudio

RStudio is the most popular IDE for R development.

1. Go to [https://posit.co/download/rstudio-desktop/](https://posit.co/download/rstudio-desktop/)
2. Click **"Download RStudio Desktop"**
3. Download the macOS version
4. Open the downloaded `.dmg` file
5. Drag RStudio to your Applications folder

**Note**: You'll use both VS Code (for GitHub Copilot AI assistance) and RStudio (for running R code). They work great together!

### Step 1.4: Install Git

Git is for version control (tracking changes to your code).

```bash
brew install git
```

Verify installation:

```bash
git --version
```

### Step 1.5: Configure Git with Your Information

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
- **R** - R language support (by REditorSupport)
- **R Debugger** - Debug R code in VS Code
- **SQLite Viewer** - View SQLite databases in VS Code

**Optional but Helpful:**
- **Material Icon Theme** - Better file icons
- **GitLens** - Enhanced Git visualization
- **Rainbow CSV** - Colorize CSV columns

### Step 3.4: Configure VS Code Settings

1. Press `Cmd + ,` to open Settings
2. Search for and configure these settings:

- **Editor: Tab Size** - Set to 2
- **Files: Auto Save** - Set to "afterDelay"
- **R: Bracketed Paste** - Check this box (better R console experience)

**Note**: Most R code formatting will be done in RStudio, so VS Code settings are minimal.

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
5. Description: `An R Shiny app to manage and track baseball card values`
6. Select **"Private"** (keep your collection data private!)
7. Check **"Add a README file"**
8. Click **"Create repository"**

**Option B: From GitHub Desktop**

1. Open GitHub Desktop
2. Go to **File > New Repository**
3. Name: `baseball-card-collection`
4. Description: `An R Shiny app to manage and track baseball card values`
5. Choose a local path (e.g., `/Users/yourname/Projects`)
6. Check **"Initialize with a README"**
7. Click **"Create Repository"**
8. Click **"Publish repository"** to push to GitHub
9. **Important**: Make sure "Keep this code private" is checked (it should be checked by default)

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

For this beginner project, we'll use R Shiny - a framework that lets you build interactive web apps using R:

```
baseball-card-collection/
├── app.R               # Main Shiny application
├── data/
│   └── cards.csv       # Your card collection data
├── www/
│   └── styles.css      # Custom styling (optional)
├── R/
│   └── helpers.R       # Helper functions
└── README.md
```

### Technology Choices

**Framework:**
- R Shiny - creates interactive web apps with pure R
- Perfect since you already know R!
- Handles both frontend and backend

**Data Storage:**
- CSV file (your existing format works great!)
- Could upgrade to SQLite database later

**Key R Packages:**
- `shiny` - web application framework
- `DT` - interactive data tables
- `dplyr` - data manipulation
- `ggplot2` - visualizations (optional)

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

### Step 6.1: Prepare Your CSV Data

Great news - R reads CSV files directly! Your CSV file "grants baseball cards" has these columns:
- Card number
- Player Last name
- Player first name
- Year
- Team
- Becketts value as of 2/19/2009

**Clean up your CSV headers:**

Make sure your CSV has clean column names (no spaces). Rename them to:
```
card_number,last_name,first_name,year,team,value_2009
```

You can do this in Excel/Google Sheets:
1. Open your CSV
2. Rename the header row to match above
3. Add a new column: `current_value` (leave it empty for now)
4. Save as `data/cards.csv`

**Example format:**
```csv
card_number,last_name,first_name,year,team,value_2009,current_value
123,Griffey Jr,Ken,1989,Seattle Mariners,45.00,
456,Jeter,Derek,1993,New York Yankees,125.00,
```

---

## Part 7: Vibe Coding Prompts

Now the fun part! Use these prompts with GitHub Copilot (Claude Sonnet 4.5 recommended) to build your R Shiny application.

**Workflow**: Write prompts in VS Code with Copilot, then copy the R code to RStudio to run it.

### Prompt 1: Project Setup - Basic Shiny App

Open Copilot Chat and use this prompt:

```
I'm building a baseball card collection app using R Shiny. Create an app.R file that:

1. Has a UI with:
   - Title: "Grant's Baseball Card Collection"
   - A search text input
   - Dropdown filters for Year and Team
   - A data table to display the cards
   - A statistics summary section at the top

2. Uses these R packages:
   - shiny
   - DT (for interactive tables)
   - dplyr (for data manipulation)

3. Reads card data from "data/cards.csv"

4. The data table should show:
   - Card Number
   - Player Name (First Last combined)
   - Year
   - Team
   - 2009 Value (formatted as currency)
   - Current Value (formatted as currency)
   - % Change (calculated column)

Please create a complete, working app.R file with comments explaining each section.
```

### Prompt 2: Create Sample Data

```
Create a sample CSV file for testing at data/cards.csv with 10 baseball cards.

Columns needed:
- card_number
- last_name
- first_name
- year
- team
- value_2009
- current_value

Include:
- Different years (1980s-2000s)
- Different teams
- Values ranging from $5 to $500
- Famous players like Ken Griffey Jr, Derek Jeter, Cal Ripken Jr
- Some current_value entries empty (NA), some higher than 2009, some lower

This will help test the percentage change calculations.
```

### Prompt 3: Add Search and Filter Functionality

```
Update my Shiny app to add reactive search and filtering:

1. The search box should filter cards as the user types
2. Search should match against first_name, last_name, and team
3. The Year dropdown should populate with unique years from the data
4. The Team dropdown should populate with unique teams from the data
5. Filters should stack together (year AND team AND search)
6. Add a "Clear Filters" button that resets everything
7. Show "Displaying X of Y cards" below the filters

Use reactive expressions for efficient filtering.
```

### Prompt 4: Style the Data Table

```
Update the DT datatable in my Shiny app to:

1. Format the value columns as currency ($XX.XX)
2. Color-code the % Change column:
   - Green for positive values (with + sign)
   - Red for negative values
   - Gray for zero or NA
3. Make the table sortable by clicking column headers
4. Add pagination (show 25 cards per page)
5. Make rows highlight on hover

Use DT's formatCurrency and formatStyle functions.
```

### Prompt 5: Add Collection Statistics

```
Add a statistics summary panel to my Shiny app that shows:

1. Total cards in collection
2. Total 2009 value (sum)
3. Total current value (sum, excluding NAs)
4. Overall % change in collection value
5. Cards that increased in value (count)
6. Cards that decreased in value (count)
7. Most valuable card (name and current value)
8. Best performer (name and % increase)

Display these in a nice grid of value boxes at the top of the app.
Use shinydashboard or bslib for styled value boxes.
```

### Prompt 6: Add Price Update Feature

```
Add the ability to update current card prices in my Shiny app:

1. Add an "Edit" action button in each row of the data table
2. When clicked, show a modal dialog with:
   - Card info displayed (read-only)
   - Numeric input for current value
   - Save and Cancel buttons

3. When saved:
   - Update the reactive data
   - Recalculate the % change
   - Refresh the table and statistics

4. Add validation (must be a positive number)

Use showModal() and modalDialog() for the popup.
```

### Prompt 7: Save Changes to CSV

```
Add the ability to persist changes in my Shiny app:

1. When a card price is updated, save the changes back to the CSV file
2. Add a "Save All Changes" button in the header
3. Show a notification when changes are saved
4. Add a "Discard Changes" button that reloads the original data

Use write.csv() to save and showNotification() for feedback.
```

### Prompt 8: Export Functionality

```
Add export features to my Shiny app:

1. Add a "Download CSV" button that exports all card data
2. Add a "Download Report" button that creates a summary PDF
3. Include the current filter state in the export
4. Filename should include today's date (e.g., "cards-2024-01-15.csv")

Use downloadHandler() for the downloads.
```

### Prompt 9: Add Visualizations

```
Add a visualization tab to my Shiny app with these charts:

1. Bar chart: Top 10 most valuable cards (current value)
2. Pie chart: Cards by team
3. Line chart: Average card value by year
4. Scatter plot: 2009 value vs current value (to see correlation)

Use ggplot2 for the charts and make them reactive to filters.
Add a new tab or panel to hold these visualizations.
```

### Prompt 10: Polish the UI

```
Improve the look and feel of my Shiny app:

1. Use a sports-themed color scheme (blues and grays)
2. Add a custom CSS file in www/styles.css
3. Make the layout responsive for different screen sizes
4. Add icons to buttons using shiny::icon()
5. Improve spacing and typography
6. Add a footer with "Last updated: [date]"

Use bslib or shinythemes for a modern look.
```

---

## Part 8: Future Enhancements

Once you've completed the basic project, here are ideas to level up your R skills:

### Add a SQLite Database

```
Upgrade from CSV to a proper database:

1. Use RSQLite package to create a local database
2. Create tables for:
   - cards (your collection)
   - price_history (track changes over time)
   - teams (reference data)

3. Add functions to:
   - Query cards efficiently
   - Track price updates with timestamps
   - Generate historical reports

This would teach you about:
- Database design and SQL
- Data persistence
- Relational data modeling
```

### Add Real Price API Integration

```
Research and implement a real price API:

1. Register for eBay Developer Program
2. Use httr2 package to call the Finding API
3. Search for completed listings by player/year
4. Calculate average sale price for each card
5. Schedule weekly updates with cronR

This would teach you about:
- Working with REST APIs in R
- API authentication (OAuth)
- Data processing and cleaning
```

### Add Plumber API Backend

```
Create a REST API for your card data using Plumber:

1. Install plumber package
2. Create endpoints:
   - GET /cards - list all cards
   - GET /cards/{id} - get single card
   - POST /cards - add new card
   - PUT /cards/{id} - update card
   - DELETE /cards/{id} - delete card

3. Connect your Shiny app to the API

This would teach you about:
- Building APIs with R
- RESTful design patterns
- Separating frontend from backend
```

### Deploy to shinyapps.io

```
Deploy your app so it's accessible online:

1. Create account at shinyapps.io (free tier available)
2. Install rsconnect package
3. Configure your account credentials
4. Deploy with: rsconnect::deployApp()

Alternative: Deploy to your own server with Shiny Server

This would teach you about:
- Cloud deployment
- Environment configuration
- Sharing R applications
```

### Add Machine Learning Price Predictions

```
Use R's ML capabilities to predict card values:

1. Use tidymodels for ML workflow
2. Features: year, team, player stats, condition
3. Train a model on historical price data
4. Predict future values for your collection
5. Add a "Predicted Value" column

This would teach you about:
- Machine learning in R
- Feature engineering
- Model evaluation
```

### Create an R Package

```
Package your card collection tools as an R package:

1. Use usethis to create package structure
2. Document functions with roxygen2
3. Add unit tests with testthat
4. Create vignettes with example usage
5. Share on GitHub for others to use

This would teach you about:
- R package development
- Documentation best practices
- Software engineering in R
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

#### R Package Installation Errors

**Problem**: Can't install packages

**Solutions**:
1. Make sure R is properly installed: `R --version`
2. Try installing from RStudio instead of terminal
3. Check for error messages about missing system libraries
4. On Mac, you may need Xcode tools: `xcode-select --install`

#### CSV Loading Errors

**Problem**: Cards not loading in Shiny app

**Solutions**:
1. Check the file path is correct (relative to app.R)
2. Ensure column names match what your code expects
3. Look for encoding issues (save as UTF-8)
4. Check for missing values - use `na.strings` in read.csv()

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
R --version
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

# R commands (in R console)
install.packages("shiny")     # Install a package
library(shiny)                # Load a package
runApp()                      # Run Shiny app in current directory
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
