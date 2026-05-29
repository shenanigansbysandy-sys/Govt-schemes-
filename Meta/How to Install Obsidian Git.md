# 📱 How to Install Obsidian Git on Your Phone & Sync My Edits

## 🔗 The Plugin (Official)
- **Plugin Name:** Obsidian Git
- **Author:** Vinzent
- **GitHub:** https://github.com/Vinzent03/obsidian-git
- **Download inside Obsidian:** Settings → Community Plugins → Browse → Search "Git"

---

## 🅰️ For Android

### Method 1: No Termux Needed (Easiest - Recommended)

1. **Install Termux** from [F-Droid](https://f-droid.org/packages/com.termux/) (NOT from Play Store — Play Store version is outdated)

2. **Open Termux** and run:
```bash
pkg update && pkg upgrade -y
pkg install git -y
termux-setup-storage
```
*(Allow storage permission when prompted)*

3. **Clone your repo** (use your PAT):
```bash
cd /storage/emulated/0
git clone https://github.com/shenanigansbysandy-sys/Govt-schemes-.git
```

4. **Open Obsidian** → Click "Open folder as vault" → select the `Govt-schemes-` folder

5. **Install the Git plugin inside Obsidian:**
   - Settings ⚙️ → **Community plugins**
   - Turn off **Restricted mode**
   - Click **Browse** → Search **"Git"**
   - Find **"Obsidian Git"** by Vinzent → **Install** → **Enable**

6. **Configure the plugin:**
   - Go to Plugin Settings
   - **GitHub username:** `shenanigansbysandy-sys`
   - **Personal access token:** *(paste your PAT here)*
   - **Auto-pull on startup:** ✅ ON
   - **Auto-commit & push:** ✅ ON (set interval to 30 min or manual)

### Method 2: Using Obsidian Git Plugin Directly (No Termux)

The Obsidian Git plugin on mobile uses **isomorphic-git** (built-in JS git). You can skip Termux entirely!

1. **Open Obsidian** → Create a new empty vault (any name)
2. **Install "Obsidian Git" plugin** as described in Step 5 above
3. **Open Command Palette** (Cmd/Ctrl+P or swipe down)
4. Run **"Obsidian Git: Clone an existing remote repository"**
5. Paste: `https://github.com/shenanigansbysandy-sys/Govt-schemes-.git`
6. Enter your **username** and **PAT** when prompted
7. ✅ Open the cloned folder as your vault

---

## 🅱️ For iPhone/iOS

1. **Install iSH** from App Store (free Linux terminal)

2. **Open iSH** and run:
```bash
apk add git
```

3. **Mount your Obsidian vault folder:**
```bash
mkdir obsidian
mount -t ios . obsidian
```
*(Select your Obsidian vault folder when prompted)*

4. **Clone the repo:**
```bash
cd obsidian
git clone https://github.com/shenanigansbysandy-sys/Govt-schemes-.git .
```

5. **Open Obsidian** → Open the folder as vault

6. **Install Obsidian Git plugin:**
   - Settings → Community Plugins → Search "Git" → Install & Enable

7. **Configure:**
   - Username: `shenanigansbysandy-sys`
   - PAT: *(paste your token)*
   - Auto-pull on startup: ON

---

## ✅ After Setup — Sync My Edits Instantly

| You Say to Me | What Happens |
|---------------|--------------|
| *"Fix the budget in PM-KISAN"* | I edit → commit → push to GitHub |
| *"Add National Quantum Mission"* | I create card → commit → push |
| **Your phone (auto-pull on startup)** | Opens vault with my latest edits! |

### Or pull manually anytime:
- **Command Palette** → `Obsidian Git: Pull from remote`
- Or just **close & reopen Obsidian** (if auto-pull is ON)

---

## 🔐 Need to Reset Your Remote?

If you ever need to re-enter your PAT:
- Open Obsidian → Settings → **Obsidian Git** → Scroll to **"Authentication/Commit Author"**
- Update the **Personal access token** field

---

## ❓ Troubleshooting

| Problem | Fix |
|---------|-----|
| "Not a git repository" | Run `Obsidian Git: Initialize a new repo` first |
| "Authentication failed" | PAT expired? Regenerate at GitHub Settings → Tokens |
| "Push rejected" | Pull first → then push |
| Plugin not visible | Disable Restricted mode in Community plugins |

---

## 🚀 Now You're Ready!

Once the Git plugin is set up, every time you:
1. Open Obsidian → Auto-pull → Get my latest edits
2. Edit a note → Auto-commit → Saved to GitHub
3. Tell me to make changes → I push → You pull → Instant sync! 🎉
