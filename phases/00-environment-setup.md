# Phase 0: Environment Setup

> Goal: Development environment ready, comfortable with terminal and Git.

## 1. Install tools

### macOS

```bash
# Install Homebrew (package manager)
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Node.js (via nvm — version manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
nvm install --lts
node -v   # should print v22.x or higher

# Install pnpm (fast package manager)
corepack enable
corepack prepare pnpm@latest --activate
pnpm -v   # should print 10.x

# Install Git
brew install git
git --version
```

### Windows

1. **Install Git + Git Bash:**
   - Download from https://git-scm.com/download/win
   - During install, select "Use Git from Git Bash only"
   - Select "Checkout as-is, commit Unix-style line endings"
   - This gives you a Unix-like terminal (Git Bash) on Windows

2. **Install Node.js:**
   - Download from https://nodejs.org (LTS version)
   - Or use nvm-windows: https://github.com/coreybutler/nvm-windows
   ```bash
   # After installing nvm-windows
   nvm install lts
   nvm use lts
   node -v   # should print v22.x or higher
   ```

3. **Install pnpm:**
   ```bash
   corepack enable
   corepack prepare pnpm@latest --activate
   pnpm -v   # should print 10.x
   ```

4. **Recommended:** Install [Windows Terminal](https://apps.microsoft.com/detail/9n0dx20hk701) for a better terminal experience. Set Git Bash as the default profile.

### VS Code

1. Download from https://code.visualstudio.com
2. Install these extensions:
   - **ESLint** — code linting
   - **Prettier** — code formatting
   - **Tailwind CSS IntelliSense** — autocomplete for Tailwind classes
   - **Error Lens** — inline error display
   - **GitLens** — Git blame and history

3. Enable format on save:
   - Open Settings (`Cmd + ,`)
   - Search "format on save"
   - Check the box

### Claude Code (AI assistant in terminal)

Claude Code is an AI coding assistant that runs in your terminal. It can read your code, suggest changes, run commands, and help you learn.

**Install:**

```bash
# Install globally via npm
npm install -g @anthropic-ai/claude-code
```

**Setup:**

```bash
# Start Claude Code in your project
cd your-project
claude

# First time: it will ask you to log in
# Follow the browser link to authenticate with your Anthropic account
```

**How to use:**

```bash
# Start a conversation
claude

# Ask questions about your code
> explain this function

# Ask it to make changes
> add a dark mode toggle to this component

# Run a slash command
> /help
```

**Tips for learning:**
- Ask Claude to explain code you don't understand: "what does this useEffect do?"
- Ask for comparisons: "show me this in JavaScript vs TypeScript"
- Ask for review: "review my code for improvements"
- Use `/help` to see all available commands

**Project setup:** When you clone a MirrorStack repo, Claude reads the `CLAUDE.md` file to understand the project conventions. You don't need to explain the project context — it already knows.

---

## 2. Terminal basics

Learn these commands — you'll use them every day:

| Command | What it does | Example |
|---------|-------------|---------|
| `pwd` | Print current directory | `pwd` → `/Users/you` |
| `ls` | List files | `ls -la` (show hidden files) |
| `cd` | Change directory | `cd projects` |
| `cd ..` | Go up one directory | `cd ..` |
| `mkdir` | Create folder | `mkdir my-project` |
| `touch` | Create file | `touch index.html` |
| `rm` | Delete file | `rm file.txt` |
| `rm -rf` | Delete folder | `rm -rf old-folder` |
| `cat` | Print file contents | `cat README.md` |
| `code .` | Open VS Code here | `code .` |

### Try it

```bash
mkdir ~/projects
cd ~/projects
mkdir hello-world
cd hello-world
touch index.html
code .
```

## 3. Git basics

Git tracks changes to your code. Think of it as "save points" for your project.

### Key concepts

| Concept | What it means |
|---------|--------------|
| **Repository (repo)** | A project folder tracked by Git |
| **Commit** | A save point — snapshot of your code at one moment |
| **Branch** | A parallel version of your code (for working on features) |
| **Pull Request (PR)** | A request to merge your branch into the main code |
| **Clone** | Download a repo to your computer |
| **Push** | Upload your commits to GitHub |
| **Pull** | Download new commits from GitHub |

### Setup Git

```bash
# Set your identity
git config --global user.name "Your Name"
git config --global user.email "your@email.com"

# Set default branch name
git config --global init.defaultBranch main
```

### Setup SSH key (for GitHub)

```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your@email.com"
# Press Enter for all prompts (default location, no passphrase for now)

# Copy the public key
cat ~/.ssh/id_ed25519.pub
# Copy the output
```

Go to https://github.com/settings/keys → **New SSH key** → paste the key.

Test it:

```bash
ssh -T git@github.com
# Should print: "Hi username! You've successfully authenticated"
```

### Essential Git commands

```bash
# Clone a repo
git clone git@github.com:mirrorstack-ai/zero-to-master.frontend.git

# Check status
git status

# Create a branch
git checkout -b my-feature

# Stage changes
git add file.txt        # stage one file
git add .               # stage all changes

# Commit
git commit -m "feat: add login page"

# Push to GitHub
git push origin my-feature

# Switch branches
git checkout main

# Pull latest changes
git pull origin main
```

### Commit message format

We use prefixes to describe what changed:

| Prefix | When to use | Example |
|--------|------------|---------|
| `feat:` | New feature | `feat: add avatar component` |
| `fix:` | Bug fix | `fix: button text color in dark mode` |
| `docs:` | Documentation | `docs: update README` |
| `test:` | Tests | `test: add button unit tests` |
| `chore:` | Tooling/config | `chore: update dependencies` |
| `refactor:` | Code change (no new feature) | `refactor: simplify dialog logic` |

## 4. GitHub account

1. Create an account at https://github.com if you don't have one
2. Ask your mentor to add you to the `mirrorstack-ai` organization
3. Set up your SSH key (see above)

## Exercise: Your first PR

This exercise proves you can use Git and GitHub.

### Steps

1. Clone this repo:
   ```bash
   git clone git@github.com:mirrorstack-ai/zero-to-master.frontend.git
   cd zero-to-master.frontend
   ```

2. Create a branch:
   ```bash
   git checkout -b phase-0/your-name
   ```

3. Add your name to `students.md`:
   ```markdown
   ## Students

   - Your Name (@github-username) — started YYYY-MM-DD
   ```

4. Commit and push:
   ```bash
   git add students.md
   git commit -m "docs: add my name to students list"
   git push origin phase-0/your-name
   ```

5. Open a Pull Request:
   - Go to https://github.com/mirrorstack-ai/zero-to-master.frontend
   - Click "Compare & pull request"
   - Title: `docs: add [your name] to students`
   - Submit

6. Wait for your mentor to review and merge

## Checkpoint

You're ready for Phase 1 when you can:

- [ ] Open VS Code and use the terminal
- [ ] Navigate directories with `cd`, `ls`, `mkdir`
- [ ] Clone a repo, create a branch, commit, push
- [ ] Open a Pull Request on GitHub
- [ ] Understand what a commit, branch, and PR are
- [ ] Run `claude` in a project and ask it a question

---

Next: [Phase 1 — HTML & CSS](./01-html-css.md)
