# 📸 Visual Deployment Guide

## Step-by-Step Visual Guide for Deploying on GitHub Pages

This guide provides detailed visual instructions for deploying your portfolio website.

---

## 🟢 GitHub Pages Deployment (Recommended)

### Step 1: Access Repository Settings

1. Go to your GitHub repository: `https://github.com/vrund-addatech/testing-AI`
2. Click on the **"Settings"** tab (look for the gear icon ⚙️ in the top navigation)

```
[Repository Name]
┌─────────────────────────────────────────────────────┐
│ <> Code  Issues  Pull requests  Actions  [Settings] │ ← Click here
└─────────────────────────────────────────────────────┘
```

---

### Step 2: Navigate to Pages

1. In the left sidebar, scroll down to find **"Pages"**
2. Click on **"Pages"**

```
Left Sidebar:
├── General
├── Collaborators
├── ...
├── [Pages]  ← Click here
├── Environments
└── ...
```

---

### Step 3: Configure Source

1. Under **"Source"** section:
   - Click the dropdown that says **"None"**
   - Select **"main"** branch

```
Source
┌─────────────────┐
│ None ▼          │ ← Click to open dropdown
├─────────────────┤
│ main            │ ← Select this
└─────────────────┘
```

2. In the folder dropdown next to it:
   - Keep it as **"/ (root)"**

```
┌─────────────────┐
│ / (root) ▼      │ ← Keep this selected
└─────────────────┘
```

3. Click **"Save"** button

```
┌─────────┐
│  Save   │ ← Click this button
└─────────┘
```

---

### Step 4: Wait for Deployment

1. You'll see a message: **"Your site is ready to be published"**
2. Wait 1-2 minutes for GitHub to build and deploy your site
3. Refresh the page

---

### Step 5: Get Your Live URL

1. After deployment, you'll see:

```
┌──────────────────────────────────────────────────────┐
│ ✅ Your site is live at                              │
│ https://vrund-addatech.github.io/testing-AI/         │
└──────────────────────────────────────────────────────┘
```

2. Click on the URL or copy it
3. Open it in a new browser tab
4. **Congratulations! Your site is live!** 🎉

---

## 🔷 Vercel Deployment

### Quick Deploy Button Method

1. Go to [DEPLOYMENT.md](./DEPLOYMENT.md)
2. Click the blue **"Deploy with Vercel"** button
3. Sign in with GitHub (if not already signed in)
4. Click **"Deploy"**
5. Wait 30 seconds
6. Your site is live! 🎉

### Manual Method

#### Step 1: Create Vercel Account

1. Go to [vercel.com](https://vercel.com)
2. Click **"Sign Up"**
3. Choose **"Continue with GitHub"**
4. Authorize Vercel to access your repositories

---

#### Step 2: Import Project

1. On Vercel dashboard, click **"Add New..."**
2. Select **"Project"**
3. Find and click on `vrund-addatech/testing-AI` repository
4. Click **"Import"**

```
Your GitHub Repositories
┌────────────────────────────────────┐
│ vrund-addatech/testing-AI          │
│                        [Import]    │ ← Click Import
└────────────────────────────────────┘
```

---

#### Step 3: Configure Project

1. Project name: Keep default or change
2. Framework Preset: **"Other"** (it's auto-detected)
3. Root Directory: **"./"** (leave as is)
4. Build settings: **Leave empty** (static site)

```
Configure Project
┌────────────────────────────────────┐
│ Project Name: testing-ai           │
│ Framework: Other                   │
│ Root Directory: ./                 │
│ Build Command: [leave empty]      │
│ Output Directory: [leave empty]    │
└────────────────────────────────────┘

        [Deploy] ← Click this
```

---

#### Step 4: Deploy

1. Click **"Deploy"** button
2. Watch the deployment progress (30-60 seconds)
3. You'll see confetti 🎊 when it's done!

```
┌────────────────────────────────────┐
│  🎉 Congratulations!                │
│  Your project is live!              │
│                                     │
│  https://testing-ai-abc123.        │
│  vercel.app                         │
│                                     │
│         [Visit Site]                │
└────────────────────────────────────┘
```

---

## 🌐 Netlify Deployment

### Quick Deploy Button Method

1. Go to [DEPLOYMENT.md](./DEPLOYMENT.md)
2. Click the blue **"Deploy to Netlify"** button
3. Sign in with GitHub
4. Click **"Deploy site"**
5. Wait 30 seconds
6. Your site is live! 🎉

### Manual Method

#### Step 1: Create Netlify Account

1. Go to [netlify.com](https://www.netlify.com)
2. Click **"Sign up"**
3. Choose **"GitHub"** sign-in option
4. Authorize Netlify

---

#### Step 2: Add New Site

1. Click **"Add new site"** button
2. Select **"Import an existing project"**

```
┌────────────────────────────────────┐
│   Add new site ▼                   │
├────────────────────────────────────┤
│ → Import an existing project       │ ← Click this
│   Start from a template             │
│   Deploy manually                   │
└────────────────────────────────────┘
```

---

#### Step 3: Connect to GitHub

1. Click **"GitHub"** button
2. Authorize Netlify to access repositories
3. Search for `testing-AI`
4. Click on the repository

```
Connect to Git provider
┌─────────┬─────────┬─────────┐
│ GitHub  │ GitLab  │ Bitbucket│
└─────────┴─────────┴─────────┘
     ↑ Click this

Search: testing-AI
┌────────────────────────────────────┐
│ vrund-addatech/testing-AI          │ ← Click this
└────────────────────────────────────┘
```

---

#### Step 4: Configure Build Settings

1. Keep all settings at default:
   - Branch to deploy: **main**
   - Build command: **(leave empty)**
   - Publish directory: **(leave empty)**

```
Site settings
┌────────────────────────────────────┐
│ Branch: main                       │
│ Build command: [empty]             │
│ Publish directory: [empty]         │
└────────────────────────────────────┘

      [Deploy site] ← Click this
```

---

#### Step 5: Deploy and Access

1. Click **"Deploy site"**
2. Wait 30-60 seconds for deployment
3. Your site will be live at: `https://random-name.netlify.app`

```
┌────────────────────────────────────┐
│ ✅ Site is live                    │
│ https://amazing-name-123456.       │
│ netlify.app                         │
│                                     │
│    [Visit site]  [Change name]     │
└────────────────────────────────────┘
```

4. Optionally, click **"Change name"** to customize your URL

---

## 🎯 Troubleshooting

### Issue: "404 - Not Found" after deployment

**Solution:**
1. Wait 2-5 minutes (first deployment takes time)
2. Clear browser cache (Ctrl+Shift+R or Cmd+Shift+R)
3. Check deployment status in the platform dashboard

---

### Issue: Images or CSS not loading

**Solution:**
1. Verify all file paths are relative (not absolute)
2. Check file names match exactly (case-sensitive on Linux servers)
3. Re-deploy by pushing a small change to GitHub

---

### Issue: "Build failed" error

**Solution:**
1. This shouldn't happen for static sites
2. Check if you accidentally added build commands
3. Clear build settings and redeploy
4. Contact support if issue persists

---

### Issue: Custom domain not working

**Solution:**
1. Wait 24-48 hours for DNS propagation
2. Verify DNS records are correct
3. Check SSL certificate is issued
4. Use platform's DNS verification tool

---

## ✅ Verification Checklist

After deployment, verify:

```
Website Functionality:
[ ] Site loads successfully
[ ] All pages are accessible
[ ] Images load correctly
[ ] CSS styles are applied
[ ] JavaScript works (theme toggle, etc.)
[ ] Navigation works
[ ] All links work
[ ] Mobile view looks good

SEO & Performance:
[ ] SSL certificate active (https://)
[ ] Meta tags present
[ ] Fast load time (< 3 seconds)
[ ] No console errors

Contact Information:
[ ] Email link works
[ ] LinkedIn link works
[ ] GitHub link works
[ ] Other social links work
```

---

## 🎊 Success!

If you can see your portfolio live on the internet:
- ✅ You've successfully deployed!
- ✅ Share your URL with potential employers
- ✅ Add it to your LinkedIn profile
- ✅ Include it in your resume

**Your portfolio is now live 24/7!** 🚀

---

## 📱 Share Your Site

Share your portfolio on:
- LinkedIn: Add to featured section
- Twitter: Pin a tweet with your portfolio
- Email signature: Add your portfolio URL
- Resume: Include as a link
- GitHub profile: Add to README

---

## 🔄 Making Updates

After initial deployment, any changes you push to GitHub will automatically redeploy:

1. Make changes to your code locally
2. Commit: `git add . && git commit -m "Update content"`
3. Push: `git push origin main`
4. Wait 1-2 minutes
5. Refresh your live site - changes are live!

**It's that easy!** 🎉

---

## 📞 Need Help?

If you're stuck:
1. Read [DEPLOYMENT.md](./DEPLOYMENT.md) for detailed text instructions
2. Check [HOSTING-COMPARISON.md](./HOSTING-COMPARISON.md) to choose the best platform
3. Contact: vrundpatel99240@gmail.com

---

Made with ❤️ by Vrund Patel
