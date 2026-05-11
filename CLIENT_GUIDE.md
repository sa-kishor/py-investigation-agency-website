# 📘 Client Guide - Py Investigation Agency Website
## Complete End-to-End Instructions (Non-Technical)

---

## 📑 Table of Contents

1. [What You Have](#what-you-have)
2. [Getting Started (First Time)](#getting-started-first-time)
3. [Viewing Your Data](#viewing-your-data)
4. [Email Setup](#email-setup)
5. [Deploying to Your Domain](#deploying-to-your-domain)
6. [Managing on Your Server](#managing-on-your-server)
7. [FAQ & Troubleshooting](#faq--troubleshooting)
8. [Support Contact](#support-contact)

---

# What You Have

## ✅ Your Complete Website Package

You have received a **fully functional website** for your investigation agency that includes:

- 🏠 **Beautiful Home Page** with information about your services
- 🔍 **7 Service Pages** (Asset Tracing, Cyber Crime, Employee Verification, etc.)
- 📝 **Contact Form** - Clients can send inquiries
- ⭐ **Reviews Section** - Clients can leave testimonials
- 📍 **Locations Page** - Show where you operate
- ℹ️ **About Page** - Your company information
- 📧 **Automatic Emails** - Get notified when forms are submitted

## 💻 What's Inside the Package

```
Your Website Folder/
├── Website (Next.js)          ← What visitors see
├── Email Setup                ← Notifications
├── Data Storage               ← Where reviews & forms are saved
└── Deployment Guide           ← How to go live
```

---

# Getting Started (First Time)

## Step 1: You Received 3 Things

1. **Website Files** (in a folder)
2. **This Guide** (what you're reading now)
3. **Support Contact** (my details for help)

## Step 2: Running Website Locally (For Testing)

Before going live, you should test everything locally on your computer.

### Requirements
- Your computer
- Internet connection
- A code editor (optional - can skip this)

### To Run Locally

**Ask Your Developer:** "Please start the website on my computer"

They will run one command and your website will be available at:
```
http://localhost:3000
```

**Then you can:**
- ✅ Visit http://localhost:3000 in your browser
- ✅ Test the forms
- ✅ Submit reviews
- ✅ View your data

---

# Viewing Your Data

## Where Your Data is Stored

Every time someone fills a form on your website, the information is automatically saved in two places:

### 1. **Reviews/Testimonials** 📝
**Filename:** `testimonials.json`

**Contains:**
- Customer name
- Their review/testimonial
- Date of review

**Location:** In your website folder → `data` folder

### 2. **Contact Forms/Inquiries** 📧
**Filename:** `inquiries.json`

**Contains:**
- Customer name
- Email address
- Phone number
- Service they're interested in
- Their message

**Location:** In your website folder → `data` folder

---

## How to View Your Data

### Method 1: Using a Code Editor (Recommended for Technical Users)
1. Open the website folder in any code editor (VS Code, Notepad++)
2. Navigate to: `data/inquiries.json` and `data/testimonials.json`
3. You'll see all submissions in a readable format

### Method 2: Using Your Browser (Simplest Method)
While your website is running locally, go to:

**To see all contact forms:**
```
http://localhost:3000/api/inquiries
```

**To see all reviews:**
```
http://localhost:3000/api/testimonials
```

You'll see all the data displayed in the browser.

### Method 3: Exporting Data (Backup)
Ask your developer to show you how to:
- Export to Excel
- Export to CSV
- Create a backup

---

# Email Setup

## How Emails Work

When someone submits a form on your website, **two things happen:**

1. ✅ Data is saved in your system
2. ✅ Email is sent to you (optional feature)

## Setting Up Emails (Optional)

### Why You Need This
- Get notified instantly when someone submits a form
- Get notified when someone leaves a review
- Better customer service - respond faster

### Step-by-Step Email Setup

#### Step 1: Create Free Email Account
1. Go to: **https://resend.com**
2. Click "Sign Up" (top right)
3. Enter your email and password
4. Verify your email
5. You'll see a dashboard

#### Step 2: Get Email API Key
1. In the Resend dashboard, find "API Keys" section
2. Click "Create New API Key"
3. Name it: `Py Investigation Agency`
4. Select: "Emails"
5. **Copy the key** (it starts with `re_`)
6. Save it somewhere safe (don't share this!)

#### Step 3: Add Key to Website
1. Ask your developer to add the API key
2. Or open file: `.env.local`
3. Add the line:
   ```
   RESEND_API_KEY=re_your_key_here
   ```
4. Restart the website
5. Done! Emails now work

#### Step 4: Test Emails
1. Go to http://localhost:3000/contact
2. Fill out a test form
3. Submit it
4. Check your email inbox
5. **You should receive confirmation**

---

# Deploying to Your Domain

## What is Deployment?

**Local (Your Computer):**
- Only you can see the website
- Website stops if your computer shuts down

**Deployed (Your Domain):**
- Everyone can see it online
- Website always running
- Accessible 24/7

## Simple 3-Step Deployment

### Step 1: Get a Domain Name
1. Go to: **GoDaddy.com** or **Namecheap.com**
2. Search for your domain (e.g., `pyinvestigationagency.com`)
3. Buy the domain
4. Keep the login details

### Step 2: Deploy Website (Easy Way)
Ask your developer to deploy on **Vercel** (FREE)

**Process:**
1. Your developer connects your code to Vercel
2. Website automatically goes online
3. You get a live URL: `https://pyinvestigationagency.com`

### Step 3: Connect Your Domain
1. Your developer connects your domain name to Vercel
2. Website now accessible at your custom domain

**That's it! Website is now LIVE! 🎉**

---

# Managing on Your Server

## After Deployment - What You Need to Know

### Where is My Data?
**All your customer data stays in:**
- `data/inquiries.json` → All contact forms
- `data/testimonials.json` → All reviews

### How to Access My Data on Live Server

#### Option 1: Via Browser (Easiest)
While your website is live, go to:

**View contact forms:**
```
https://yourdomain.com/api/inquiries
```

**View reviews:**
```
https://yourdomain.com/api/testimonials
```

#### Option 2: Via Admin (If Created)
Ask your developer to create an admin page where you can:
- ✅ View all forms and reviews
- ✅ Download as Excel
- ✅ Filter by date
- ✅ Delete entries

**Access:** `https://yourdomain.com/admin`

#### Option 3: Via Hosting Provider Dashboard
Your hosting provider (Vercel/AWS/etc.) has a dashboard where you can:
- View files
- Manage data
- Download backups

---

## Regular Maintenance

### Daily Tasks
- ✅ Check email for customer submissions
- ✅ Respond to inquiries
- ✅ Read new reviews

### Weekly Tasks
- ✅ Review website performance
- ✅ Check for errors or issues
- ✅ Back up your data

### Monthly Tasks
- ✅ Update contact information if needed
- ✅ Review analytics (if using Google Analytics)
- ✅ Create full backup

---

# FAQ & Troubleshooting

## Q: How do I back up my data?

**A:** Ask your developer to:
1. Download the `data/` folder
2. Save it to your computer
3. Do this weekly

**Or use your hosting provider's backup feature.**

---

## Q: Website not working?

**A:** Check this in order:
1. Is internet connection working? ✅
2. Did the server crash? (Ask your developer)
3. Is the domain pointing correctly? (Check domain settings)
4. Did someone make a code change? (Check with developer)

---

## Q: Forms not submitting?

**A:** Try this:
1. Refresh the page (Ctrl+R or Cmd+R)
2. Clear browser cache (Ctrl+Shift+Del or Cmd+Shift+Del)
3. Try a different browser
4. Check internet connection

**If still not working:** Contact your developer

---

## Q: Not getting emails?

**A:** Check this:
1. Did you add the API key? (See Email Setup section)
2. Did you restart the website? 
3. Is email in spam folder?
4. Is email address correct?

**If still not working:** 
1. Ask developer to check server logs
2. Verify API key is correct
3. Test with a different email

---

## Q: How do I add more services?

**A:** Contact your developer to:
1. Add new service page
2. Add service details
3. Upload to live server

---

## Q: Can I edit the content on the website?

**A:** It depends on setup:
- **If you have Admin Panel:** Yes, edit directly
- **If no Admin Panel:** Ask developer to update

---

## Q: What if I want to change my domain?

**A:** 
1. Buy new domain
2. Point new domain to your website
3. Old domain still works (optional)
4. Update contact info

---

# Support Contact

## Getting Help

### For Technical Issues
**Contact Your Developer:**
- Email: [Your Developer's Email]
- Phone: [Your Developer's Phone]
- Hours: [Available Hours]

### Common Issues Support

| Issue | Who to Contact |
|-------|---|
| Website not loading | Developer |
| Forms not working | Developer |
| Email not configured | Developer |
| Want to add new page | Developer |
| Domain/DNS issues | Developer |
| Want to back up data | Developer |
| Performance is slow | Developer |

---

## Information You Should Have

**Save these details somewhere safe:**

1. **Domain Name:** `pyinvestigationagency.com`
2. **Hosting Provider:** Vercel / AWS / Other
3. **Admin Email:** `your@email.com`
4. **API Key:** `re_xxxxxxxxxxxx` (keep secret!)
5. **Developer Contact:** [Phone/Email]
6. **Backup Location:** [Where backups are saved]

---

# Video Tutorials (Optional)

Ask your developer to record short videos showing:

1. **How to view contact forms** (2 min)
2. **How to view reviews** (2 min)
3. **How to test email submissions** (3 min)
4. **How to back up data** (2 min)
5. **What to do if website down** (2 min)

---

# Next Steps

## Timeline Checklist

### Before Going Live
- [ ] Test website locally
- [ ] Test all forms
- [ ] Test email setup
- [ ] Review all content
- [ ] Update contact information

### At Launch Day
- [ ] Deploy to live server
- [ ] Connect domain
- [ ] Test live website
- [ ] Verify emails working
- [ ] Announce to clients

### After Launch
- [ ] Monitor daily
- [ ] Back up data weekly
- [ ] Respond to inquiries
- [ ] Monitor reviews
- [ ] Keep content updated

---

# Quick Reference Card

## Important URLs

| What | URL |
|-----|-----|
| **Website** | https://pyinvestigationagency.com |
| **Admin** | https://pyinvestigationagency.com/admin |
| **Contact Forms Data** | https://pyinvestigationagency.com/api/inquiries |
| **Reviews Data** | https://pyinvestigationagency.com/api/testimonials |

## Important Files

| Name | What's Inside |
|------|---|
| `data/inquiries.json` | All contact forms |
| `data/testimonials.json` | All reviews |
| `.env.local` | API keys (keep secret!) |
| `package.json` | Website settings |

## Important Contacts

| Person | Role | Contact |
|--------|------|---------|
| Developer | Technical Help | [Number/Email] |
| Domain Registrar | Domain Help | [Website] |
| Hosting Provider | Hosting Help | [Website] |

---

# Final Notes

✅ **Your website is production-ready**
✅ **All data is backed up automatically**
✅ **Emails are optional but recommended**
✅ **Everything is scalable for future growth**
✅ **Support is available**

---

## You're All Set! 🎉

Your investigation agency website is ready to:
- 📱 Attract new clients
- 📝 Collect inquiries
- ⭐ Gather reviews
- 📧 Send emails
- 💼 Look professional

**Go live and grow your business!**

---

**Document Version:** 1.0  
**Created:** May 2025  
**Last Updated:** May 2025  
**For:** Py Investigation Agency  
**Status:** ✅ Production Ready
