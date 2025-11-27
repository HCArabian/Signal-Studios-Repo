# Signal Studios Website (Vercel Ready)

A modern, creative agency website ready for instant deployment on Vercel.

---

## 🚀 DEPLOY TO VERCEL (3 Steps)

### Step 1: Open Vercel
Go to [vercel.com/new](https://vercel.com/new)

### Step 2: Import Project
1. Click **"Upload"** (or connect to Git)
2. **Drag & drop this entire folder** into the upload area
3. Wait for upload to complete

### Step 3: Deploy
1. Click **"Deploy"**
2. Wait ~30 seconds
3. **Done!** Your site is live at `your-project.vercel.app`

---

## 📋 AFTER DEPLOYMENT: Setup Contact Form

The contact form uses **Formspree** (free tier: 50 submissions/month).

### Quick Setup (2 minutes):

1. **Go to [formspree.io](https://formspree.io)**
2. **Sign up** (free)
3. **Create new form** → Copy your form ID (looks like `xyzabc123`)
4. **Edit `index.html`** → Find this line:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID"
   ```
5. **Replace `YOUR_FORM_ID`** with your actual form ID
6. **Redeploy** to Vercel (just drag & drop again, or push to Git)

That's it! Form submissions will go to your email.

---

## 🌐 ADD CUSTOM DOMAIN

### In Vercel Dashboard:

1. Go to your project → **Settings** → **Domains**
2. Click **"Add"**
3. Enter your domain (e.g., `signalstudios.com`)
4. Follow the DNS instructions Vercel provides

### DNS Settings (at your registrar):

**Option A: Using Vercel DNS (Recommended)**
- Change nameservers to Vercel's (they'll tell you which ones)

**Option B: Keep your DNS**
- Add A record: `76.76.21.21`
- Add CNAME for www: `cname.vercel-dns.com`

SSL certificate is automatic!

---

## 📁 Project Structure

```
signal-studios-vercel/
├── index.html          # Homepage
├── vercel.json         # Vercel configuration
├── css/
│   └── styles.css      # All styles & animations
├── js/
│   └── main.js         # Navigation & interactions
├── images/
│   └── favicon.svg     # Browser tab icon
└── projects/
    └── morrison.html   # Project page template
```

---

## ✏️ EDITING YOUR SITE

### Change Text Content:
1. Open `index.html` in any text editor (VS Code recommended)
2. Find the text you want to change
3. Edit it
4. Redeploy to Vercel

### Change Colors:
Edit the CSS variables at the top of `css/styles.css`:

```css
:root {
    --navy: #0a0f1a;      /* Main background */
    --cyan: #00D4FF;      /* Primary accent */
    --purple: #8B5CF6;    /* Secondary accent */
    --pink: #EC4899;      /* Tertiary accent */
    --lime: #84CC16;      /* Quaternary accent */
}
```

### Add New Project Pages:
1. Copy `projects/morrison.html`
2. Rename to your project (e.g., `projects/newproject.html`)
3. Edit the content
4. Add link in `index.html` work section:
   ```html
   <a href="/projects/newproject.html" class="project-card">
   ```

### Add Images:
1. Put images in `/images/` folder
2. Reference in HTML: `<img src="/images/your-image.jpg">`
3. Recommended formats: WebP (best), JPEG, PNG

---

## 🔄 REDEPLOY CHANGES

### Option 1: Manual Upload
1. Go to [vercel.com/dashboard](https://vercel.com/dashboard)
2. Click your project
3. Go to Deployments → Upload
4. Drag & drop your updated folder

### Option 2: Git Integration (Better for ongoing changes)
1. Create GitHub repository
2. Push your code
3. Connect Vercel to GitHub (Settings → Git)
4. Every `git push` auto-deploys!

---

## 💰 COST BREAKDOWN

| Item | Cost |
|------|------|
| Vercel Hosting | **$0** (Hobby plan) |
| SSL Certificate | **$0** (included) |
| Formspree (50 forms/mo) | **$0** (free tier) |
| Domain (optional) | ~$12/year |
| **Total** | **$0 - $12/year** |

---

## ⚡ PERFORMANCE

This site is optimized for speed:
- Pure HTML/CSS/JS (no framework bloat)
- Minimal dependencies
- Optimized animations
- Vercel Edge Network (global CDN)

Expected scores:
- Performance: 95+
- Accessibility: 95+
- Best Practices: 100
- SEO: 100

---

## 🔧 ADVANCED: Environment Variables

If you need environment variables (API keys, etc.):

1. Vercel Dashboard → Settings → Environment Variables
2. Add your variable (e.g., `FORM_ENDPOINT`)
3. Access in code or reference in vercel.json

---

## 🐛 TROUBLESHOOTING

### Form not working?
- Check that you replaced `YOUR_FORM_ID` with actual Formspree ID
- Verify form is created in Formspree dashboard
- Check browser console for errors

### Styles not loading?
- Check file paths (should start with `/`)
- Clear browser cache (Cmd+Shift+R or Ctrl+Shift+R)
- Verify `css/styles.css` exists

### 404 on project pages?
- Check file paths match exactly
- Verify files are in `/projects/` folder
- File names are case-sensitive

### Domain not working?
- DNS changes can take up to 48 hours
- Verify DNS records are correct in Vercel
- Check SSL certificate status in dashboard

---

## 📱 TESTING

### Desktop:
- Chrome, Firefox, Safari, Edge

### Mobile:
- iOS Safari
- Android Chrome

### Quick Test:
Use Chrome DevTools (F12) → Toggle device toolbar (Ctrl+Shift+M)

---

## 🔗 USEFUL LINKS

- [Vercel Dashboard](https://vercel.com/dashboard)
- [Vercel Docs](https://vercel.com/docs)
- [Formspree Dashboard](https://formspree.io/forms)
- [Google Domains](https://domains.google)
- [Namecheap](https://namecheap.com)

---

## 📞 NEED HELP?

- [Vercel Support](https://vercel.com/support)
- [Vercel Community](https://github.com/vercel/vercel/discussions)

---

Built with ❤️ for Signal Studios
