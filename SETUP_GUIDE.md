# Consultancy Website - Setup Guide

Welcome! This guide will help you set up your resume submission consultancy website on GitHub Pages.

## 📋 Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Setting Up Formspree (For Form Submissions)](#setting-up-formspree)
4. [Customizing Your Website](#customizing-your-website)
5. [Deploying to GitHub Pages](#deploying-to-github-pages)
6. [Testing the Form](#testing-the-form)

---

## Overview

This website allows candidates to submit their resumes/CVs which will be forwarded to your email. The platform has:

- **Home Page** - Introduction and highlights
- **About Page** - Company information
- **Services Page** - Services offered
- **Resume Submission Page** - (NEW) Where candidates submit CVs
- **Contact Page** - General inquiries
- **And more** - Blog, testimonials, team info, etc.

---

## Prerequisites

1. **GitHub Account** - Free account at [github.com](https://github.com)
2. **Formspree Account** - Free at [formspree.io](https://formspree.io)
3. **Text Editor** - VS Code or any code editor
4. **Git** - Installed on your system (if working locally)

---

## Setting Up Formspree (Recommended for GitHub Pages)

Formspree is perfect for static sites like GitHub Pages because it requires no backend server.

### Step 1: Create a Formspree Account
1. Go to [formspree.io](https://formspree.io)
2. Click "Let's Go" or "Sign Up"
3. Sign up with your email and password
4. Verify your email address

### Step 2: Create a New Form
1. Click "New Form" in your Formspree dashboard
2. Give it a name: **"Resume Submissions"**
3. Set the email address where you want to receive submissions (choose carefully!)
4. Click "Create Form"

### Step 3: Get Your Form ID
1. After creating the form, you'll see a form ID (looks like: `mnopqrst`)
2. Your form endpoint will be: `https://formspree.io/f/YOUR_FORM_ID`
3. Copy this endpoint

### Step 4: Update resume.html
1. Open `resume.html` in your text editor
2. Find this line (around line 95):
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" enctype="multipart/form-data">
   ```
3. Replace `YOUR_FORM_ID` with your actual form ID
4. Save the file

**Example:**
```html
<form action="https://formspree.io/f/mnopqrst" method="POST" enctype="multipart/form-data">
```

### Step 5: Set Up Email Forwarding
1. Go back to your Formspree dashboard
2. Go to your Resume Submissions form settings
3. Set up email notifications (it should already be set to your email)
4. (Optional) Set up auto-reply to candidates

---

## Customizing Your Website

### Update Contact Information
Replace the following across all pages:

1. **Email Address:**
   - Find: `info@example.com`
   - Replace with: `careers@consult.com` (or your email)

2. **Phone Number:**
   - Find: `+012 345 6789`
   - Replace with: Your phone number

3. **Company Name:**
   - Find: `CONSULT`
   - Replace with: Your company name

4. **Addresses:**
   - Find: `123 Street, New York, USA`
   - Replace with: Your address

### Update Site Title and Meta Tags

Edit `index.html`, `resume.html`, and all other pages:
```html
<title>YOUR COMPANY NAME - Consultancy Website</title>
<meta content="Your company keywords" name="keywords">
<meta content="Your company description" name="description">
```

### Add Your Logo
1. Place your logo image in `/img/` folder
2. Update logo reference in navbar:
   ```html
   <h1 class="m-0 text-uppercase text-primary">
       <i class="far fa-smile text-primary me-2"></i>YOUR COMPANY
   </h1>
   ```

### Customize Colors
Edit `css/style.css` to change the color scheme:
- Primary color: `#0D47A1` (blue)
- Secondary color: `#F3F6F9` (light gray)
- Dark color: `#1A1A1A` (dark)

---

## Deploying to GitHub Pages

### Option 1: Using GitHub Web Interface

1. **Push your files to GitHub:**
   ```bash
   git add .
   git commit -m "Initial consultancy website setup"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub.com
   - Click **Settings** → **Pages**
   - Under "Source", select **main** branch
   - Click **Save**
   - Your site will be available at: `https://USERNAME.github.io/Consult/`

3. **Wait 1-2 minutes** for GitHub to deploy your site

### Option 2: Custom Domain (Optional)

If you want to use a custom domain (e.g., myconsultancy.com):

1. Buy a domain from a registrar (GoDaddy, Namecheap, etc.)
2. In GitHub Settings → Pages, add your custom domain
3. Update DNS records at your registrar to point to GitHub Pages
4. Follow GitHub's CNAME instructions

---

## Testing the Form

### Test Before Going Live

1. **Test Locally (if working on your computer):**
   - Open `resume.html` in your browser
   - Fill out the form completely
   - Submit the form
   - Check your email for the submission

2. **Test on GitHub Pages:**
   - Visit your deployed site: `https://USERNAME.github.io/Consult/resume.html`
   - Fill out the form
   - Submit and check email

### Important Notes
- First submission requires email verification from Formspree
- After verification, all future submissions go directly to your email
- Formspree free tier includes 50 submissions/month (upgrade if needed)

---

## File Structure

```
/Consult
├── index.html           # Home page
├── about.html           # About page
├── service.html         # Services page
├── resume.html          # Resume submission (NEW)
├── contact.html         # Contact form
├── quote.html          # Quote form
├── blog.html           # Blog grid
├── detail.html         # Blog detail
├── feature.html        # Features
├── team.html           # Team page
├── testimonial.html    # Testimonials
├── css/                # Stylesheets
│   ├── bootstrap.min.css
│   └── style.css
├── js/                 # JavaScript files
│   └── main.js
├── img/                # Images (add your logo here)
├── lib/                # Libraries (Bootstrap, jQuery, etc.)
└── SETUP_GUIDE.md      # This file
```

---

## Next Steps

1. ✅ Set up Formspree account and form
2. ✅ Update `resume.html` with your form ID
3. ✅ Customize contact information across all pages
4. ✅ Add your logo to `/img/` folder
5. ✅ Push to GitHub
6. ✅ Enable GitHub Pages
7. ✅ Test the form submission
8. ✅ Share your site with candidates!

---

## Troubleshooting

### Form submissions not working?
- **Verify form ID** is correct in `resume.html`
- **Check email** - first submission requires verification
- **Test with Formspree** directly at [formspree.io](https://formspree.io)

### Site not appearing on GitHub Pages?
- **Wait 2-3 minutes** - GitHub needs time to deploy
- **Check Settings → Pages** - make sure it's enabled
- **Verify branch** - should be set to `main`
- **Check CNAME file** - if using custom domain

### File upload not working?
- **File size** - Max 5MB per file
- **File format** - Only PDF, DOC, DOCX allowed
- **Formspree tier** - Free tier supports file uploads

---

## Alternative Form Services

If you prefer not to use Formspree, here are alternatives:

| Service | Free Tier | File Upload | Pros | Cons |
|---------|-----------|------------|------|------|
| **Formspree** | 50 submissions/mo | ✅ Yes | Easy setup | Limited submissions |
| **Basin** | Unlimited | ✅ Yes | Very simple | Less features |
| **Getform** | Unlimited | ✅ Yes | Good for files | Fewer options |
| **Netlify Forms** | 100/mo | ❌ No | Good for static | No file uploads |
| **Form.taxi** | 100/mo | ✅ Yes | Affordable | Paid to upgrade |

---

## Support & Tips

### SEO Optimization
- Add meta descriptions to all pages
- Use relevant keywords
- Create unique page titles
- Add Open Graph tags for social sharing

### Security
- Never include your email directly in HTML (spammers find it)
- Use Formspree to protect your email
- Validate file uploads (already done with Formspree)
- Consider adding CAPTCHA on Formspree (paid feature)

### Analytics
Add Google Analytics to track:
- Visitor traffic
- Form submissions
- User behavior
- Top pages

```html
<!-- Add this to <head> of all pages -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

---

## Questions & Support

- **Formspree Support:** https://formspree.io/support
- **GitHub Pages Docs:** https://pages.github.com
- **Bootstrap Docs:** https://getbootstrap.com/docs

---

**Last Updated:** May 2026

Good luck with your consultancy website! 🚀
