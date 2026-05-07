# Configuration & Customization Guide

This guide shows you how to customize your website without needing coding knowledge.

## 📝 Easy Text Replacements

### Step 1: Open Find & Replace
- **Windows/Linux:** Press `Ctrl + H` in your editor
- **Mac:** Press `Cmd + H` in your editor

### Step 2: Replace These Items

Use this table to customize your website:

| Item | Find (Original) | Replace With | Which Files |
|------|-----------------|--------------|-------------|
| **Company Email** | `info@example.com` | your-email@company.com | ALL HTML files |
| **Company Phone** | `+012 345 6789` | +1 (555) 123-4567 | ALL HTML files |
| **Company Name** | `CONSULT` | Your Company Name | ALL HTML files |
| **Address** | `123 Street, New York, USA` | Your Address | ALL HTML files |
| **Site Title** | `CONSULT - Consultancy Website Template` | Your Company - Your Tagline | title tags in all files |

### Common Replacements in Detail

#### Email Address
- **Old:** `info@example.com`
- **New:** `careers@mycompany.com`
- **Where:** Found in:
  - Top bar (topbar section)
  - Footer (footer section)
  - Contact page
  - Resume page

#### Phone Number
- **Old:** `+012 345 6789`
- **New:** `+1 (555) 123-4567`
- **Where:** Found in:
  - Top bar (topbar section)
  - Footer (footer section)

#### Company Name
- **Old:** `<h1>CONSULT</h1>` or just `CONSULT`
- **New:** `<h1>YOUR COMPANY NAME</h1>`
- **Where:** Navigation bar on every page

---

## 🎨 Quick Visual Customizations

### Add Your Logo Image

**Step 1:** Save your logo
- Format: PNG or JPG
- Recommended size: 200x50 pixels
- Filename: Any name (e.g., `my-logo.png`)
- Location: Save to `img/` folder

**Step 2:** Update Navigation Navbar
- Find in every HTML file (around line 70):
  ```html
  <h1 class="m-0 text-uppercase text-primary">
      <i class="far fa-smile text-primary me-2"></i>CONSULT
  </h1>
  ```

- Replace with:
  ```html
  <img src="img/my-logo.png" alt="Logo" height="50">
  ```

---

### Change Primary Color

The default color is blue (`#0D47A1`). To change it:

**Method 1: Simple Color Replacement (Easy)**
1. Open `css/style.css`
2. Find: `.btn-primary` or `.bg-primary`
3. Replace color code `#0D47A1` with your color
4. Save

**Color Codes:**
- Blue (default): `#0D47A1`
- Green: `#10B981`
- Red: `#EF4444`
- Purple: `#8B5CF6`
- Orange: `#F97316`
- Navy: `#001F3F`

**Find your color at:** [colorhexa.com](https://www.colorhexa.com)

---

## 🏢 Customize Business Information

### Contact Information

**Top Bar (Found in all pages, around line 40-52):**

```html
<!-- BEFORE -->
<p class="m-0"><i class="fa fa-envelope-open me-2"></i>info@example.com</p>
<p class="m-0"><i class="fa fa-phone-alt me-2"></i>+012 345 6789</p>

<!-- AFTER -->
<p class="m-0"><i class="fa fa-envelope-open me-2"></i>careers@mycompany.com</p>
<p class="m-0"><i class="fa fa-phone-alt me-2"></i>+1 (555) 123-4567</p>
```

### Footer Information

**Footer Section (Found at the bottom of every page):**

```html
<!-- BEFORE -->
<div class="col-lg-3 col-md-6">
    <h5 class="text-white mb-4">Our Office</h5>
    <p class="mb-2"><i class="fa fa-map-marker-alt me-3"></i>123 Street, New York, USA</p>
    <p class="mb-2"><i class="fa fa-phone-alt me-3"></i>+012 345 67890</p>
    <p class="mb-0"><i class="fa fa-envelope me-3"></i>info@example.com</p>
</div>

<!-- AFTER -->
<div class="col-lg-3 col-md-6">
    <h5 class="text-white mb-4">Our Office</h5>
    <p class="mb-2"><i class="fa fa-map-marker-alt me-3"></i>Your Address, City, State, Zip</p>
    <p class="mb-2"><i class="fa fa-phone-alt me-3"></i>+1 (555) 123-4567</p>
    <p class="mb-0"><i class="fa fa-envelope me-3"></i>careers@mycompany.com</p>
</div>
```

---

## 📄 Customize Page Content

### Home Page (index.html)

Main content sections:
1. **Hero Section** - Large banner with title
   - **Location:** Lines 90-120
   - **Edit:** Main heading and description

2. **About Section** - Company introduction
   - **Location:** Around line 150
   - **Edit:** Company description and highlights

3. **Services Section** - Services offered
   - **Location:** Around line 250
   - **Edit:** Service descriptions

### Resume Submission Page (resume.html)

**Modify Form Fields:**

```html
<!-- Add a new field -->
<div class="col-12">
    <div class="form-floating">
        <input type="text" class="form-control" id="newfield" name="newfield" placeholder="Label">
        <label for="newfield">Your Label Here</label>
    </div>
</div>
```

**Modify Section Text:**

```html
<!-- Around line 95 -->
<h1 class="display-5 mb-4">Share Your CV with Us</h1>
<p class="mb-4">UPDATE THIS TEXT with your own message...</p>
```

---

## 📧 Form Setup (Formspree)

### Get Your Form ID

1. Visit [formspree.io](https://formspree.io)
2. Log in to your account
3. Go to "Resumes Submissions" form
4. Copy the Form ID (in URL bar or settings)
   - **Format:** Looks like `mnopqrst` or `abc123def`

### Update Form ID in resume.html

**Line ~95 in resume.html:**

```html
<!-- BEFORE -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">

<!-- AFTER - Replace YOUR_FORM_ID -->
<form action="https://formspree.io/f/mnopqrst" method="POST">
```

---

## 🔗 Link Social Media

**Footer Social Icons (Bottom of every page):**

```html
<!-- Add your social links here -->
<a class="btn btn-outline-light btn-social" href="https://twitter.com/yourhandle">
    <i class="fab fa-twitter"></i>
</a>
<a class="btn btn-outline-light btn-social" href="https://linkedin.com/company/yourcompany">
    <i class="fab fa-linkedin-in"></i>
</a>
<a class="btn btn-outline-light btn-social" href="https://facebook.com/yourpage">
    <i class="fab fa-facebook-f"></i>
</a>
```

---

## 🎯 Recommended Configuration Order

1. **First:** Update company information
   - Email, phone, address, name
   - Go through all pages

2. **Second:** Set up Formspree
   - Create form, get ID
   - Update resume.html form ID

3. **Third:** Add logo (optional)
   - Save to `img/` folder
   - Update navbar

4. **Fourth:** Customize colors (optional)
   - Update CSS color codes

5. **Fifth:** Customize content (optional)
   - Update service descriptions
   - Update about section
   - Add team info

---

## 📱 Test Your Changes

After making changes:

1. **In Terminal/Command Line:**
   ```bash
   git add .
   git commit -m "Updated customization"
   git push origin main
   ```

2. **Wait 2-3 minutes** for GitHub Pages to update

3. **Refresh your site:**
   - Navigate to: `https://USERNAME.github.io/Consult/`
   - Press Ctrl+F5 (hard refresh) to see changes

---

## File Editing Tips

### Finding Content to Edit

**Use Find (Ctrl+F):**
- Search for text you want to change
- Edit the file
- Save (Ctrl+S)

**Example:** Search for "info@example.com" to find all instances

### Making Changes Safely

1. **Before editing:** Create backup copy
   - Copy the entire `Consult` folder
   - Keep original

2. **Always test changes:**
   - Check locally if possible
   - Test on GitHub Pages after pushing

3. **Use Find & Replace:**
   - Ctrl+H (Find & Replace)
   - Review changes before replacing all

---

## 🎨 Color Scheme Reference

Current colors used:

| Name | Color Code | Where Used |
|------|-----------|-----------|
| Primary | `#0D47A1` | Buttons, links, highlights |
| Secondary | `#F3F6F9` | Background sections |
| Dark | `#1A1A1A` | Dark backgrounds, text |
| Light | `#FFFFFF` | White backgrounds |
| Success | `#10B981` | Success messages |
| Danger | `#EF4444` | Errors, warnings |

**Change color scheme in:** `css/style.css`

---

## 📚 HTML Tags Cheat Sheet

**For editing content safely:**

| What You Want | HTML Code | Example |
|--------------|-----------|---------|
| **Bold text** | `<strong>text</strong>` | `<strong>Important</strong>` |
| **Italics** | `<em>text</em>` | `<em>Emphasized</em>` |
| **Link** | `<a href="url">text</a>` | `<a href="https://example.com">Visit</a>` |
| **Heading 1** | `<h1>text</h1>` | `<h1>Main Title</h1>` |
| **Heading 2** | `<h2>text</h2>` | `<h2>Subtitle</h2>` |
| **Paragraph** | `<p>text</p>` | `<p>This is a paragraph</p>` |

---

## ✅ Customization Checklist

Before going live:

- [ ] Email address updated everywhere
- [ ] Phone number updated everywhere
- [ ] Company name updated
- [ ] Address updated
- [ ] Form ID added to resume.html
- [ ] Logo added (if desired)
- [ ] Colors customized (if desired)
- [ ] All links tested
- [ ] Responsive design checked
- [ ] Form submissions tested
- [ ] On GitHub Pages and live

---

## ⚠️ Common Mistakes to Avoid

❌ **Mistake 1:** Forgetting to update Form ID
- **Fix:** Check form ID matches in resume.html

❌ **Mistake 2:** Not saving files after editing
- **Fix:** Always Ctrl+S (Cmd+S on Mac)

❌ **Mistake 3:** Forgetting to push to GitHub
- **Fix:** Remember to `git push origin main`

❌ **Mistake 4:** Changing code tags by accident
- **Fix:** Only change text between `>` and `<`

---

## 📞 Need Help Customizing?

**Quick Reference:**
- **QUICK_START.md** - Get up and running
- **SETUP_GUIDE.md** - Detailed setup
- **README.md** - Overview everything

**External Help:**
- **Bootstrap:** https://getbootstrap.com/docs/
- **HTML:** https://www.w3schools.com/html/
- **CSS:** https://www.w3schools.com/css/

---

**Happy customizing! 🎉**

Now that your website is configured, remember to:
1. Push changes to GitHub
2. Test everything thoroughly
3. Share with candidates!

Good luck with your consultancy business! 🚀
