# GigMentor — GitHub Pages Deployment Guide

## Step 1 — Create GitHub Repository

1. Go to github.com → Sign in (or create account)
2. Click the "+" icon → "New repository"
3. Repository name: `gigmentor`
4. Set to **Public**
5. Click "Create repository"

## Step 2 — Upload index.html

1. In your new repo, click "Add file" → "Upload files"
2. Drag and drop `index.html`
3. Commit message: "Launch GigMentor landing page"
4. Click "Commit changes"

## Step 3 — Enable GitHub Pages

1. Go to repo → Settings → Pages (left sidebar)
2. Source: "Deploy from a branch"
3. Branch: `main` → folder: `/ (root)`
4. Click Save
5. Wait 2-3 minutes
6. Your site will be live at: `https://YOUR-USERNAME.github.io/gigmentor`

## Step 4 — Connect your domain gigmentor.co.in

### In GitHub Pages settings:
1. Settings → Pages → Custom domain
2. Type: `gigmentor.co.in`
3. Click Save
4. Check "Enforce HTTPS" once it appears

### In your domain registrar DNS panel:
Add these 4 A records:

| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Also add:
| Type | Name | Value |
|------|------|-------|
| CNAME | www | YOUR-USERNAME.github.io |

### Wait 24 hours for DNS propagation
Then gigmentor.co.in will show your landing page!

## Step 5 — Set up Formspree for email collection

1. Go to formspree.io → Sign up free
2. Create a new form → get your Form ID (looks like: xyzabcde)
3. In index.html, find this line:
   `fetch('https://formspree.io/f/YOUR_FORM_ID'`
4. Replace YOUR_FORM_ID with your actual ID
5. Commit the change

Now every waitlist signup emails you at founder@gigmentor.co.in

## Done! Your startup has a live landing page.
