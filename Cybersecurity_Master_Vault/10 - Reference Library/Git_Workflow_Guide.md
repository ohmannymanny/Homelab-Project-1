# **Git Workflow Guide for My Cybersecurity Master Vault**

This page documents how I manage version control and syncing between my local Obsidian Vault and my GitHub repository. The goal is to keep my cybersecurity notes, homelab documentation, and project logs versioned, backed up, and accessible across devices.



---

# **1. Purpose of Using Git With My Obsidian Vault**

I use Git for:

- Tracking changes in my cybersecurity notes over time
    
- Creating a permanent backup of my entire vault
    
- Syncing notes between devices without relying on cloud services
    
- Maintaining a Portfolio-quality record of my homelab, security projects, and other type of tech project I plan to do in the future.
    
- Practicing real-world version control workflows used in security, sysadmin, and cloud engineering roles
    



---

# **2. How the Sync System Works (Obsidian Git Plugin)**

My Obsidian vault is also a Git repository.  
When I update or create notes:

1. **Changes appear in the Git panel inside Obsidian.**
    
2. I manually stage → commit → sync using the plugin.
    
3. The plugin pushes to GitHub using SSH authentication.
    

I specifically avoid automatic commits to ensure I maintain intentional, meaningful commit history.

---

# **3. Daily Workflow: Commit & Sync**

### **A. Add new or modified notes**

Obsidian automatically detects file changes.  
No manual `git add` is required — the plugin handles it.

### **B. Commit changes**

I click:

**“Commit & Sync”**

This performs:

- `git add .`
    
- `git commit -m "vault backup: YYYY-MM-DD HH:mm:ss"`
    
- `git pull` (to avoid conflicts)
    
- `git push`
    

### **Why commit messages look like backups**

The purpose is to keep history clean and readable.  
For example:

`vault backup: 2025-11-19 15:06:42`

Each commit represents a snapshot in time.

---

# **4. Pulling Remote Updates**

If I work on another device or GitHub changes, I click:

**“Pull”**

Why this matters:

- Prevents merge conflicts
    
- Ensures my vault is always up-to-date before making changes
    

---

# **5. Handling Conflicts 

If I edit the _same note_ on two different devices before syncing, Git will warn me.

To fix:

1. Obsidian Git will highlight the file.
    
2. I open the file to review both versions.
    
3. I accept or merge the correct version manually.
    
4. Commit & Sync again.
    



---

# **6. Understanding the Three Git States**

This helps solidify Git fundamentals.

### **Untracked**

New files that Git has never seen.  
Obsidian Git will show these as “new”.

### **Modified**

Files that changed since last commit.

### **Staged**

Files prepared to be committed.

Obsidian Git handles this automatically when I click **Commit & Sync**, but knowing the states helps during interviews.

---

# **7. Why I Use SSH Instead of HTTPS**

**SSH Benefits:**

- No password required
    
- More secure
    
- Matches security engineering best practices
    
- Works across devices without re-authentication
    
- Recommended in enterprise environments
    

My SSH key is stored at:

`C:\Users\<USERNAME>\.ssh\<Key>`

GitHub recognizes it under my account’s SSH keys.

---

# **8. Recommended Commit Frequency**

I follow this pattern:

- **After completing a lab step**
    
- **After adding new documentation**
    
- **After updating reference notes**
    
- **Before shutting down for the day**
- or any relevant note for the homelab.
    

update my changes with my notes. want to keep everything synced up and have full control of what can be saved or not be saved, when to save it.

---

# **9. Folder Structure Managed by Git**

Every file inside:

`C:\Obsidian Vaults\Cybersecurity_Master_Vault\`

is version-controlled except for `.obsidian` config files and anything explicitly ignored.

This includes:

- Homelab setup logs
    
- Kali/Windows attack walkthrough notes
    
- Blue/Red team notes
    
- SIEM / AD / Malware lab documentation
    
- Daily logs
    
- Reference library entries
    
- Scripts and cheat sheets
    



---

# **10. What Git Does _Not_ Sync**

Git does not sync:

- Obsidian settings on other devices by default
    
- Plugin configurations
    
- Large binaries like VM files
    
- Screenshots unless I manually add them
    
- Anything ignored via `.gitignore`
    



---

# **11. Manual Git Commands I Should Know**

Obsidian Git automates Git, but knowing these commands helps:

### Check status:

`git status`

### Add all changes:

`git add .`

### Commit changes:

`git commit -m "message"`

### Push to GitHub:

`git push`

### Pull from GitHub:

`git pull`



---

# **12. Backup Strategy Using GitHub**

GitHub acts as:

- Versioned backup
    
- Offsite storage
    
- Documentation archive
    
- Portfolio asset
    
- Syncing mechanism
    

