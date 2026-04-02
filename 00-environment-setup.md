# Phase 0: Environment Setup

> Goal: All development tools installed and verified.

## 1. Node.js & pnpm

### macOS

```bash
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Node.js via nvm
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.4/install.sh | bash
nvm install --lts

# Download and install Homebrew
curl -o- https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh | bash

# Download and install Node.js:
brew install node@25

# Verify the Node.js version:
node -v # Should print "v25.9.0".

# Install Corepack:
npm install -g corepack

# Download and install pnpm:
corepack enable pnpm

# Verify pnpm version:
pnpm -v
```

### Windows

1. Download and install Node.js from https://nodejs.org (LTS version)
   - Or use [nvm-windows](https://github.com/coreybutler/nvm-windows):
   ```bash
   nvm install lts
   nvm use lts
   ```

2. Install pnpm:
   ```bash
   corepack enable
   corepack prepare pnpm@latest --activate
   ```

## 2. Git

### macOS

```bash
brew install git
```

### Windows

Download from https://git-scm.com/download/win
- Select "Use Git from Git Bash only"
- Select "Checkout as-is, commit Unix-style line endings"
- Recommended: Install [Windows Terminal](https://apps.microsoft.com/detail/9n0dx20hk701), set Git Bash as default profile

### Configure

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global init.defaultBranch main
```

## 3. GitHub CLI

### macOS

```bash
brew install gh
```

### Windows

```bash
winget install GitHub.cli
```

### Login

```bash
gh auth login
# Select: GitHub.com → SSH → Yes → Login with a web browser
```

## 4. VS Code

1. Download from https://code.visualstudio.com
2. Install extensions:
   - **ESLint**
   - **Prettier**
   - **Tailwind CSS IntelliSense**
   - **Error Lens**
   - **GitLens**
3. Enable format on save:
   - Settings (`Cmd + ,` / `Ctrl + ,`) → search "format on save" → check the box

## 5. Docker Desktop

Download and install from https://www.docker.com/products/docker-desktop/

After install, verify:

```bash
docker --version   # 27.x
```

## 6. Claude Code

### macOS

```bash
brew install claude-code
```

### Windows

```bash
winget install Anthropic.ClaudeCode
```

### Login

```bash
claude
# Follow the browser link to authenticate
```

### Install Everything Claude Code plugin

```bash
# Inside Claude Code, run:
/plugin marketplace add affaan-m/everything-claude-code
/plugin install everything-claude-code@everything-claude-code
```

## Checkpoint

Verify everything works:

```bash
node -v          # v24.x or higher
pnpm -v          # 10.x
git --version    # 2.53+
gh --version     # 2.88+
docker --version # 27.x
claude --version # 2.x
code --version   # 1.113+
```

- [ ] All commands above print a version
- [ ] VS Code opens with extensions installed
- [ ] `claude` starts and shows the prompt

---

Next: [Phase 01 — Terminal & Git](./01-terminal-git.md)
