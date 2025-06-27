# Setup Instructions for GitHub and Obsidian

This guide will help you publish your Dune: Awakening guides to GitHub and set them up in Obsidian on your Windows machine.

## 📋 Prerequisites

- GitHub account (create one at [github.com](https://github.com) if needed)
- Git installed on your system
- Obsidian installed on your Windows machine

## 🚀 Step 1: Create GitHub Repository

### Option A: Using GitHub Web Interface (Recommended)
1. **Go to GitHub.com** and sign in to your account
2. **Click the "+" icon** in the top right corner
3. **Select "New repository"**
4. **Repository settings**:
   - Repository name: `dune-awakening-guides` (or your preferred name)
   - Description: `Complete strategy guides for Dune: Awakening co-op gameplay`
   - Set to **Public** (so others can benefit from your guides)
   - **DO NOT** initialize with README, .gitignore, or license (we already have these)
5. **Click "Create repository"**

### Option B: Using GitHub CLI (Advanced)
```bash
# Install GitHub CLI first, then:
gh repo create dune-awakening-guides --public --description "Complete strategy guides for Dune: Awakening co-op gameplay"
```

## 🔗 Step 2: Connect Local Repository to GitHub

After creating the GitHub repository, you'll see a page with setup instructions. Use the "push an existing repository" section:

```bash
cd /home/solotitan/Dune_Awakening
git remote add origin https://github.com/solotitan/dune-awakening-guides.git
git branch -M main
git push -u origin main
```

**Note:** The remote URL is already configured for the `solotitan` username.

### Authentication Options

#### Option A: Personal Access Token (Recommended)
1. Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token with `repo` scope
3. Use token as password when prompted

#### Option B: SSH Key (Advanced)
1. Generate SSH key: `ssh-keygen -t ed25519 -C "your_email@example.com"`
2. Add to GitHub: Settings → SSH and GPG keys
3. Use SSH URL: `git@github.com:solotitan/dune-awakening-guides.git`

## 💻 Step 3: Set Up Obsidian on Windows

### Download and Install Obsidian
1. **Download Obsidian** from [obsidian.md](https://obsidian.md)
2. **Install** on your Windows machine
3. **Launch Obsidian**

### Clone Repository to Windows
1. **Open Command Prompt or PowerShell** on Windows
2. **Navigate to desired location** (e.g., `cd C:\Users\YourName\Documents`)
3. **Clone the repository**:
   ```cmd
   git clone https://github.com/solotitan/dune-awakening-guides.git
   ```

### Set Up Obsidian Vault
1. **Open Obsidian**
2. **Click "Open folder as vault"**
3. **Navigate to** the cloned repository folder
4. **Select the folder** and click "Open"
5. **Obsidian will automatically** detect the pre-configured settings

## 🔧 Step 4: Obsidian Configuration

### Recommended Plugins
The vault comes pre-configured, but you may want to install these community plugins:

1. **Advanced Tables** - Better table editing
2. **Checklist** - Enhanced checkbox functionality
3. **Tag Wrangler** - Better tag management
4. **Quick Switcher++** - Enhanced file navigation
5. **Templater** - Advanced template functionality

### Installing Community Plugins
1. **Settings** → **Community plugins**
2. **Turn off Safe mode**
3. **Browse** and install recommended plugins
4. **Enable** the plugins you want to use

## 🔄 Step 5: Keeping Everything Synced

### Updating from Linux to GitHub
When you make changes on your Linux machine:

```bash
cd /home/solotitan/Dune_Awakening
git add .
git commit -m "Update guides with new strategies"
git push origin main
```

### Updating Windows from GitHub
When you want to get the latest changes on Windows:

```cmd
cd C:\Users\YourName\Documents\dune-awakening-guides
git pull origin main
```

### Making Changes on Windows
If you edit guides in Obsidian on Windows:

```cmd
cd C:\Users\YourName\Documents\dune-awakening-guides
git add .
git commit -m "Update guides from Windows/Obsidian"
git push origin main
```

## 📱 Step 6: Mobile Access (Optional)

### Obsidian Mobile
1. **Install Obsidian** on your phone/tablet
2. **Use Obsidian Sync** (paid) or **Git-based sync** (free but complex)
3. **Access guides** while gaming

### GitHub Mobile
1. **Install GitHub app** on your phone
2. **Access repository** directly for quick reference
3. **View guides** in mobile browser

## 🎮 Step 7: Gaming Setup

### During Gaming Sessions
1. **Keep Obsidian open** on second monitor or alt-tab
2. **Use Quick Reference guide** for fast decisions
3. **Update progress** using checklists
4. **Take notes** on discoveries

### Sharing with Friends
1. **Share GitHub repository link** with your co-op partner
2. **They can clone** or just view online
3. **Collaborate** on strategy improvements
4. **Use Issues/Discussions** for coordination

## 🛠️ Troubleshooting

### Git Authentication Issues
- **Use Personal Access Token** instead of password
- **Check repository URL** (HTTPS vs SSH)
- **Verify permissions** on GitHub repository

### Obsidian Issues
- **Check vault folder** is correct
- **Restart Obsidian** if settings don't load
- **Check file permissions** on Windows

### Sync Issues
- **Always pull before pushing** changes
- **Resolve merge conflicts** if they occur
- **Use descriptive commit messages**

## 📋 Quick Reference Commands

### Essential Git Commands
```bash
# Check status
git status

# Add all changes
git add .

# Commit changes
git commit -m "Your message here"

# Push to GitHub
git push origin main

# Pull latest changes
git pull origin main

# View commit history
git log --oneline
```

### Obsidian Shortcuts
- **Ctrl+O** - Quick switcher
- **Ctrl+P** - Command palette
- **Ctrl+E** - Toggle edit/preview
- **Ctrl+K** - Insert link
- **Ctrl+Shift+F** - Search in all files

## 🎯 Success Checklist

### Initial Setup Complete
- [ ] GitHub repository created
- [ ] Local repository connected to GitHub
- [ ] Repository pushed to GitHub successfully
- [ ] Obsidian installed on Windows
- [ ] Repository cloned to Windows
- [ ] Obsidian vault configured and working

### Daily Usage
- [ ] Can access guides in Obsidian
- [ ] Can make changes and sync between devices
- [ ] Can share repository with friends
- [ ] Can use guides effectively during gaming

## 🆘 Getting Help

### Resources
- **GitHub Docs**: [docs.github.com](https://docs.github.com)
- **Obsidian Help**: [help.obsidian.md](https://help.obsidian.md)
- **Git Tutorial**: [git-scm.com/docs/gittutorial](https://git-scm.com/docs/gittutorial)

### Community
- **GitHub Issues**: Use repository issues for problems
- **Obsidian Forum**: [forum.obsidian.md](https://forum.obsidian.md)
- **Reddit**: r/ObsidianMD, r/DuneAwakening

---

**Note**: Replace `YOUR_USERNAME` with your actual GitHub username throughout these instructions.

Good luck with your setup, and may your guides serve you well in the desert! 🏜️
