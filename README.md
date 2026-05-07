# Consultancy Website - Resume Submission Platform

A modern consultancy website where candidates can submit their resumes/CVs that get forwarded to your HR contacts and opportunities.

![Website Preview](#) <!-- Add screenshot URL here -->

## 🎯 Features

- **Professional Design** - Modern, responsive website built with Bootstrap
- **Resume Submission** - Dedicated page for CV uploads with file validation
- **Auto Email Forwarding** - Submissions automatically sent to your email
- **Mobile Responsive** - Works perfectly on desktop, tablet, and mobile
- **GitHub Pages Ready** - Deploy instantly with zero backend required
- **No Server Needed** - Completely static site using form service

## 📋 What's Included

- **Home Page** - Company introduction and highlights
- **About Page** - Company background and information
- **Services Page** - Your service offerings
- **Resume Submission Page** ✨ **NEW** - Candidate resume upload
- **Contact Page** - General inquiry form
- **Blog Pages** - Blog grid and detailed posts
- **Team Page** - Meet your team
- **Testimonials Page** - Client feedback
- **Quote Form** - Service quote requests
- **And More!**

## 🚀 Quick Start

### 1. **Clone or Download This Repository**
```bash
git clone https://github.com/YOUR_USERNAME/Consult.git
cd Consult
```

### 2. **Set Up Formspree (For Form Submissions)**

1. Create a free account at [formspree.io](https://formspree.io)
2. Create a new form called "Resume Submissions"
3. Copy your form ID (e.g., `mnopqrst`)
4. Open `resume.html` and replace `YOUR_FORM_ID` with your actual ID:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```

### 3. **Customize Your Information**

Update across all files:
- **Email:** Replace `info@example.com` with your email
- **Phone:** Replace `+012 345 6789` with your number
- **Company Name:** Replace "CONSULT" with your company name
- **Address:** Update location details
- **Colors:** Customize colors in `css/style.css`

### 4. **Deploy to GitHub Pages**

1. Push your changes to GitHub:
   ```bash
   git add .
   git commit -m "Initial setup of consultancy website"
   git push origin main
   ```

2. Go to repository Settings → Pages
3. Select `main` branch as source
4. Your site will be live at: `https://USERNAME.github.io/Consult/`

### 5. **Test Your Form**

1. Visit `resume.html` on your deployed site
2. Fill out and submit the form
3. Check your email for the submission
4. (First time: verify the email with Formspree)

## 📁 File Structure

```
Consult/
├── index.html              # Home page
├── about.html              # About company
├── service.html            # Services offered
├── resume.html             # 🆕 Resume submission form
├── contact.html            # Contact form
├── quote.html              # Quote request form
├── blog.html               # Blog listing
├── detail.html             # Blog post detail
├── feature.html            # Features page
├── team.html               # Team members
├── testimonial.html        # Testimonials
├── css/
│   ├── bootstrap.min.css   # Bootstrap framework
│   └── style.css           # Custom styles
├── js/
│   └── main.js             # Main JavaScript
├── lib/                    # Third-party libraries
├── img/                    # Images & logo
├── SETUP_GUIDE.md          # Detailed setup instructions
└── README.md               # This file
```

## ⚙️ Configuration

### Customize Contact Information
Edit the files and replace placeholder text:

**Email Address:**
- Find: `info@example.com`
- Replace with: `your-email@company.com`

**Phone Number:**
- Find: `+012 345 6789`
- Replace with: `+1 (555) 123-4567`

**Company Name:**
- Find: `CONSULT`
- Replace with: `YOUR COMPANY`

**Address:**
- Find: `123 Street, New York, USA`
- Replace with: Your address

### Connect Your Resume Form

The resume submission page uses **Formspree** to handle submissions:

1. **Sign up** at [formspree.io](https://formspree.io)
2. **Create form** named "Resume Submissions"
3. **Copy form ID** (looks like: `abc123def`)
4. **Update** `resume.html` line ~95:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" enctype="multipart/form-data">
   ```

## 📊 How It Works

### For Candidates:
1. Visit your website
2. Click "Submit Resume" in navigation
3. Fill in their details
4. Upload their CV/Resume (PDF, DOC, or DOCX)
5. Click "Submit Resume"
6. Confirmation message sent

### For You:
1. Each submission arrives in your email
2. Review candidate information
3. Contact them directly
4. Forward qualified candidates to your HR contacts

## 🛠️ Customization Tips

### Change Primary Color
Edit `css/style.css`:
```css
:root {
  --primary: #0D47A1;      /* Change this blue */
  --secondary: #F3F6F9;
  --dark: #1A1A1A;
}
```

### Add Your Logo
1. Place logo image in `img/` folder
2. Update `navbar-brand` in all HTML files:
   ```html
   <img src="img/your-logo.png" alt="Logo" height="40">
   ```

### Modify Form Fields
Edit the form in `resume.html` to add/remove fields as needed.

## 📱 Mobile Optimization

The website is fully responsive using Bootstrap:
- Desktop view (1200px+)
- Tablet view (768px - 1199px)
- Mobile view (< 768px)

Test responsiveness by resizing your browser or using mobile devices.

## 🔒 Privacy & Security

- Your email is protected by Formspree (not exposed in HTML)
- Form submissions encrypted over HTTPS
- File uploads validated (PDF, DOC, DOCX only)
- Formspree handles security automatically

## 💬 Alternative Form Services

| Service | Free Limit | File Upload | Recommendation |
|---------|------------|------------|-----------------|
| **Formspree** | 50/month | ✅ Yes | Best overall |
| **Basin** | Unlimited | ✅ Yes | Simple, good |
| **Getform** | Unlimited | ✅ Yes | Feature-rich |
| **Netlify Forms** | 100/month | ❌ No | No file support |

## 🎨 Customization Examples

### Add Google Analytics
Add to all page `<head>` sections:
```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Add Social Media Links
Update footer social icons in HTML (already in place, just link them)

### Change Font
Edit Google Fonts import in `<head>`:
```html
<link href="https://fonts.googleapis.com/css2?family=YourFont:wght@400;600;700&display=swap" rel="stylesheet">
```

## ❓ Troubleshooting

**Q: Form submissions not working?**
- A: Verify your Formspree form ID is correct in `resume.html`
- Verify you confirmed the email in Formspree
- Test direct submission at formspree.io

**Q: Site not showing on GitHub Pages?**
- A: Wait 2-3 minutes for deployment
- Check Settings → Pages is enabled for `main` branch
- Ensure files are properly pushed to GitHub

**Q: File upload failing?**
- A: Check file size (max 5MB)
- Verify file format (PDF, DOC, DOCX only)
- Try a different browser

**Q: Want to use a custom domain?**
- A: See SETUP_GUIDE.md section on custom domains

## 📚 Additional Resources

- [Bootstrap Documentation](https://getbootstrap.com/)
- [Formspree Documentation](https://formspree.io/docs/)
- [GitHub Pages Guide](https://pages.github.com)
- [HTML5 Reference](https://developer.mozilla.org/en-US/docs/Web/HTML)

## 📝 Next Steps

- [ ] Set up Formspree account
- [ ] Update form ID in `resume.html`
- [ ] Customize contact information
- [ ] Add your logo to `img/`
- [ ] Push to GitHub
- [ ] Enable GitHub Pages
- [ ] Test form submission
- [ ] Share with candidates!

## 🤝 Support

Need help? Check the detailed [SETUP_GUIDE.md](SETUP_GUIDE.md) for step-by-step instructions.

## 📄 License

This template is free to use and modify for your consultancy business.

## 👨‍💼 Created By

Your Name / Your Company

---

**Ready to get started?**  
1. Follow the Quick Start section above
2. Refer to [SETUP_GUIDE.md](SETUP_GUIDE.md) for detailed instructions
3. Deploy to GitHub Pages and share with candidates!

**Happy recruiting! 🎉**
