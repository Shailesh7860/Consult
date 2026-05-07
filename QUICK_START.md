# Consultancy Website - Quick Setup Checklist

Follow these steps in order to get your resume submission website live in under 30 minutes!

## ✅ Phase 1: Preparation (5 minutes)

- [ ] **Sign Up for Formspree** 
  - Go to https://formspree.io
  - Create free account
  - Verify your email

## ✅ Phase 2: Create Your Resume Form (5 minutes)

- [ ] **Create Form in Formspree Dashboard**
  - Click "New Form"
  - Name it: "Resume Submissions"
  - Set receiver email to YOUR email address
  - Copy your **Form ID** (e.g., `abc123def`)

- [ ] **Update `resume.html` with Your Form ID**
  - Open `resume.html` in your editor
  - Find line ~95: `<form action="https://formspree.io/f/YOUR_FORM_ID"`
  - Replace `YOUR_FORM_ID` with your actual ID
  - **Example:** `https://formspree.io/f/mnopqrst`
  - Save the file

## ✅ Phase 3: Customize Your Website (10 minutes)

### Update Contact Information
Use Find & Replace in your editor:

| Find | Replace With | Files |
|------|--------------|-------|
| `info@example.com` | Your email | ALL |
| `+012 345 6789` | Your phone | ALL |
| `CONSULT` | Your company name | ALL |
| `123 Street, New York, USA` | Your address | ALL |

**Quickest way:**
1. Open each HTML file
2. Use Ctrl+H (Cmd+H on Mac) - Find & Replace
3. Replace all occurrences

### (Optional) Add Your Logo
- Save your logo to: `img/your-logo.png`
- Update navbar in all pages if desired

## ✅ Phase 4: Deploy to GitHub (5 minutes)

### If Using Git in Terminal:
```bash
# Stage all changes
git add .

# Commit with message
git commit -m "Setup consultancy website with resume submission"

# Push to GitHub
git push origin main
```

### If Using GitHub Web (No Terminal):
1. Go to your GitHub repository
2. Click "Upload files"
3. Select all HTML, CSS, JS, and img files
4. Click "Commit changes"

### Enable GitHub Pages
1. Go to your GitHub repository
2. Click **Settings** (top right)
3. Click **Pages** (left sidebar)
4. Under "Source", select **main** branch
5. Click **Save**
6. Wait 2-3 minutes

**Your site will be live at:**  
`https://YOUR_USERNAME.github.io/Consult/`

## ✅ Phase 5: Test Everything (5 minutes)

- [ ] **Visit Your Website**
  - Go to: `https://YOUR_USERNAME.github.io/Consult/`
  - Wait up to 5 minutes if it's your first deployment

- [ ] **Test the Resume Form**
  - Click "Submit Resume" in navigation
  - Fill out all fields
  - Upload a test PDF/DOC
  - Click "Submit Resume"

- [ ] **Check Email**
  - Look for confirmation email from Formspree
  - (First time) Click link to verify email
  - Resume submission should arrive in your inbox

- [ ] **Verify Navigation**
  - All pages should have "Submit Resume" link
  - All links should work
  - Website should look good on mobile

## ✅ Phase 6: Go Live! (Done!)

- [ ] **You're Ready!**
  - Test with real resume submission
  - Share link with candidates
  - Monitor email for submissions
  - Contact promising candidates

---

## 📋 Troubleshooting Quick Reference

### ❌ Form Not Submitting?
- [ ] Check form ID is correct in `resume.html`
- [ ] Verify you verified Formspree email
- [ ] Try in different browser
- [ ] Check file size (max 5MB)

### ❌ Website Not Showing?
- [ ] Wait 2-3 minutes for GitHub deployment
- [ ] Refresh browser (Ctrl+F5 or Cmd+Shift+R)
- [ ] Check Settings → Pages is enabled
- [ ] Check branch is set to "main"

### ❌ Links Not Working?
- [ ] Make sure you're on GitHub Pages URL
- [ ] Check all files were pushed to GitHub
- [ ] Verify file names match HTML links

---

## 🎯 Form Fields in Resume Submission

When candidates submit, you'll receive:
- Full Name
- Email Address
- Phone Number
- Position of Interest
- Professional Summary (textarea)
- Resume/CV File (PDF/DOC/DOCX)
- Consent agreement checkbox

---

## 📞 Quick Reference

**Formspree Form ID Location:**
- Dashboard → Your Form → Look for form ID in URL or settings

**GitHub Pages URL:**
- `https://USERNAME.github.io/Consult/`

**Resume Submission Page:**
- `https://USERNAME.github.io/Consult/resume.html`

---

## 🚀 Next Steps After Setup

1. **Share Your Site**
   - Email link to potential candidates
   - Post on LinkedIn
   - Share on social media
   - Add to email signature

2. **Monitor Submissions**
   - Check email for submissions
   - Review candidate profiles
   - Contact qualified candidates
   - Forward to HR contacts

3. **Customize Further** (Optional)
   - Add more job positions
   - Update your services
   - Add team photos
   - Add testimonials
   - Create blog posts

4. **Add Analytics** (Optional)
   - Set up Google Analytics
   - Track visitor traffic
   - Monitor form submissions
   - See popular pages

---

## 💡 Pro Tips

✨ **Tip 1:** Add your photo to the team page  
✨ **Tip 2:** Write a blog post about career tips  
✨ **Tip 3:** Add specific job titles in position dropdown  
✨ **Tip 4:** Include your LinkedIn profile links  
✨ **Tip 5:** Update testimonials from past placements  

---

## 📱 Website Preview Checklist

Before sharing with candidates, verify:

- [ ] All pages load correctly
- [ ] Navigation works on all pages
- [ ] Submit Resume link visible everywhere
- [ ] Resume form loads without errors
- [ ] File upload field is working
- [ ] Submit button works
- [ ] Mobile view looks good
- [ ] All contact info is current
- [ ] No broken images or links
- [ ] No placeholder text remaining

---

## 🎓 Learning Resources

Want to customize further? Check these guides:

- **Detailed Setup:** See `SETUP_GUIDE.md`
- **Full Info:** See `README.md`
- **Bootstrap Help:** https://getbootstrap.com/
- **GitHub Pages:** https://pages.github.com/
- **Formspree:** https://formspree.io/docs/

---

**You've got this! 🚀**

Having trouble? Check the detailed guides in this repository:
- SETUP_GUIDE.md - Step-by-step instructions
- README.md - Complete documentation

Good luck with your consultancy website!
