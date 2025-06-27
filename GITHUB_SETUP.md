# GitHub Setup and Authentication Guide

This guide will help you set up GitHub authentication and use Lazygit to manage your Gaming Guides repository.

## 🔐 GitHub Authentication Setup

GitHub no longer accepts passwords for Git operations. You need a Personal Access Token (PAT).

### Step 1: Create Personal Access Token

1. **Go to GitHub.com** and sign in
2. **Click your profile picture** → Settings
3. **Developer settings** → Personal access tokens → Tokens (classic)
4. **Generate new token** → Generate new token (classic)
5. **Configure the token**:
   - **Note**: `Gaming Guides Repository Access`
   - **Expiration**: 90 days (or No expiration for convenience)
   - **Scopes**: Check `repo` (Full control of private repositories)
6. **Generate token** and **COPY IT IMMEDIATELY** (you won't see it again!)

### Step 2: Test Authentication

```bash
cd "/home/solotitan/Gaming Guides"
git push -u origin main
```

When prompted:
- **Username**: `solotitan`
- **Password**: `[paste your Personal Access Token here]`

## 🚀 Using Lazygit

Lazygit is a terminal UI for Git that makes repository management much easier.

### Basic Lazygit Usage

```bash
cd "/home/solotitan/Gaming Guides"
lazygit
```

### Lazygit Key Bindings

#### Navigation
- **Tab** / **Shift+Tab** - Switch between panels
- **↑/↓** - Navigate within panels
- **Enter** - Select/expand item
- **Esc** - Go back/cancel

#### Common Operations
- **Space** - Stage/unstage files
- **c** - Commit (opens commit message editor)
- **P** - Push to remote
- **p** - Pull from remote
- **f** - Fetch from remote
- **R** - Refresh
- **q** - Quit

#### Pushing to GitHub (First Time)
1. **Open Lazygit**: `lazygit`
2. **Navigate to Local Branches** panel (Tab to switch panels)
3. **Press 'P'** to push
4. **Enter credentials** when prompted:
   - Username: `solotitan`
   - Password: `[your Personal Access Token]`

### Lazygit Workflow for Updates

#### Making Changes
1. **Edit files** in your preferred editor
2. **Open Lazygit**: `cd "/home/solotitan/Gaming Guides" && lazygit`
3. **Stage changes**: Navigate to Files panel, press Space on changed files
4. **Commit**: Press 'c', write commit message, save and close
5. **Push**: Press 'P' to push to GitHub

#### Pulling Updates
1. **Open Lazygit**: `lazygit`
2. **Fetch**: Press 'f' to fetch latest changes
3. **Pull**: Press 'p' to pull changes to local repository

## 🔧 Alternative: Git Credential Helper

To avoid entering your token every time, you can use Git's credential helper:

### Option 1: Store Credentials (Less Secure)
```bash
git config --global credential.helper store
```
After this, Git will save your credentials after the first successful authentication.

### Option 2: Cache Credentials (More Secure)
```bash
git config --global credential.helper 'cache --timeout=3600'
```
This caches credentials for 1 hour (3600 seconds).

## 📋 Complete Setup Checklist

### Initial Setup
- [ ] Create GitHub repository named `gaming-guides`
- [ ] Generate Personal Access Token with `repo` scope
- [ ] Test authentication with `git push -u origin main`
- [ ] Verify repository appears on GitHub

### Daily Workflow with Lazygit
- [ ] Make changes to guides
- [ ] Open Lazygit: `cd "/home/solotitan/Gaming Guides" && lazygit`
- [ ] Stage changes (Space key)
- [ ] Commit changes ('c' key)
- [ ] Push to GitHub ('P' key)

## 🎯 Repository Structure

Your repository is now organized as:

```
Gaming Guides/
├── .obsidian/                    # Obsidian configuration
├── .gitignore                    # Git ignore rules
├── README.md                     # Main repository overview
├── LICENSE                       # MIT license
├── GITHUB_SETUP.md              # This file
└── Dune Awakening/              # Game-specific guides
    ├── README.md                # Game overview
    ├── Mentat_Sniper_Leveling_Guide.md
    ├── Comprehensive_Farming_Strategy.md
    ├── Quick_Reference_Guide.md
    ├── GUIDE_USAGE.md
    └── SETUP_INSTRUCTIONS.md
```

## 🚀 Next Steps

### 1. Create GitHub Repository
- Go to GitHub.com
- Create new repository: `gaming-guides`
- Description: `Comprehensive gaming strategy guides collection optimized for Obsidian`
- Set to Public
- **Don't** initialize with README (we have everything)

### 2. Push Your Guides
```bash
cd "/home/solotitan/Gaming Guides"
git push -u origin main
```
Use your Personal Access Token as the password.

### 3. Set Up Obsidian (Optional)
- Install Obsidian on your Windows machine
- Clone repository: `git clone https://github.com/solotitan/gaming-guides.git`
- Open folder as Obsidian vault

## 🛠️ Troubleshooting

### Authentication Failed
- **Problem**: `Authentication failed for 'https://github.com/...'`
- **Solution**: Make sure you're using your Personal Access Token as the password, not your GitHub password

### Lazygit Won't Push
- **Problem**: Lazygit asks for credentials repeatedly
- **Solution**: Set up credential helper (see above) or use SSH keys

### Repository Not Found
- **Problem**: `repository not found`
- **Solution**: Make sure you've created the repository on GitHub first

### Permission Denied
- **Problem**: `Permission denied`
- **Solution**: Check that your Personal Access Token has `repo` scope

## 📞 Quick Commands Reference

```bash
# Navigate to repository
cd "/home/solotitan/Gaming Guides"

# Open Lazygit
lazygit

# Manual Git commands (if needed)
git status                    # Check status
git add .                     # Stage all changes
git commit -m "Your message"  # Commit changes
git push origin main          # Push to GitHub
git pull origin main          # Pull from GitHub

# Check remote configuration
git remote -v
```

## 🎮 Adding Future Games

When you want to add guides for new games:

1. **Create new directory**: `mkdir "New Game Name"`
2. **Add guides** to the new directory
3. **Update main README.md** to include the new game
4. **Use Lazygit** to commit and push changes

---

**Ready to push your guides to GitHub!** 🚀

*Remember: Your Personal Access Token is like a password - keep it secure!*
