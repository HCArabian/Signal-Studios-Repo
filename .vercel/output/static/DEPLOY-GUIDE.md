# GitHub + Vercel Deployment Guide

## Step-by-Step Instructions

### STEP 1: Create GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Name it: `signal-studios` (or whatever you want)
3. Keep it **Public** or **Private** (your choice)
4. **DO NOT** check any boxes (no README, no .gitignore, no license)
5. Click **Create repository**

---

### STEP 2: Upload Files to GitHub (Easy Way - No Command Line)

After creating the repo, you'll see a page with setup instructions. Look for:

**"uploading an existing file"** link - click it

OR go to: `https://github.com/YOUR_USERNAME/signal-studios/upload/main`

Then:
1. **Drag ALL the files** from the extracted folder into the upload area:
   - index.html
   - vercel.json
   - .gitignore
   - README.md
   - css/ (entire folder)
   - js/ (entire folder)
   - images/ (entire folder)
   - projects/ (entire folder)

2. Scroll down and click **"Commit changes"**

---

### STEP 3: Connect Vercel to GitHub

1. Go to [vercel.com/new](https://vercel.com/new)
2. Click **"Import Git Repository"**
3. Select **GitHub** (authorize if needed)
4. Find and select your `signal-studios` repository
5. Click **Import**

---

### STEP 4: Configure & Deploy

On the configuration screen:
- **Framework Preset:** Select `Other`
- **Root Directory:** Leave as `.` (or empty)
- **Build Command:** Leave empty
- **Output Directory:** Leave as `.` (or empty)

Click **Deploy**

Wait ~30 seconds... **Done!** 🎉

---

## Alternative: Command Line Method

If you prefer using terminal:

```bash
# 1. Navigate to your extracted folder
cd path/to/signal-studios-vercel

# 2. Initialize git
git init

# 3. Add all files
git add .

# 4. Commit
git commit -m "Initial commit - Signal Studios website"

# 5. Add your GitHub repo as remote (replace with YOUR repo URL)
git remote add origin https://github.com/YOUR_USERNAME/signal-studios.git

# 6. Push to GitHub
git branch -M main
git push -u origin main
```

Then connect Vercel to GitHub (Step 3 above).

---

## Troubleshooting

### "Files not showing in GitHub"
- Make sure you uploaded the FILES, not the ZIP
- Extract the ZIP first, then upload the contents

### "Vercel says no framework detected"
- That's fine! Select "Other" as framework
- This is a static HTML site, no framework needed

### "Styles not loading after deploy"
- Check that `/css/styles.css` exists in your repo
- Make sure the folder structure is correct (see below)

### Correct folder structure in GitHub:
```
your-repo/
├── index.html          ← At root level!
├── vercel.json
├── .gitignore
├── README.md
├── css/
│   └── styles.css
├── js/
│   └── main.js
├── images/
│   └── favicon.svg
└── projects/
    └── morrison.html
```

### WRONG structure (nested folder):
```
your-repo/
└── signal-studios-vercel/    ← ❌ This extra folder breaks paths
    ├── index.html
    └── ...
```

---

## After Deployment

### Add Custom Domain
1. Vercel Dashboard → Your Project → Settings → Domains
2. Add your domain
3. Follow DNS instructions

### Setup Contact Form
1. Go to [formspree.io](https://formspree.io)
2. Create form, get ID
3. Edit index.html in GitHub
4. Replace `YOUR_FORM_ID` with actual ID
5. Commit - Vercel auto-redeploys!

---

## Making Future Updates

Once connected, any push to GitHub auto-deploys to Vercel:

1. Edit files in GitHub (click file → pencil icon → edit)
2. Or push changes via git
3. Vercel automatically rebuilds and deploys!
