# ✅ Client Checklist - Step-by-Step Setup

## Phase 1: Local Testing (On Your Computer)
**What:** Test website before going live
**Time:** ~30 minutes
**Who:** You + Your Developer

### Getting Started
- [ ] Receive website folder from developer
- [ ] Developer starts the website (`npm run dev`)
- [ ] Opens http://localhost:3000 in browser
- [ ] Website loads successfully

### Testing Website
- [ ] Navigate to Home page
- [ ] Browse each Service page (7 total)
- [ ] Check About page
- [ ] Check Contact page
- [ ] Check Reviews page
- [ ] Check Locations page

### Testing Contact Form
- [ ] Go to Contact page
- [ ] Fill out test form:
  - Name: "Test User"
  - Email: "test@email.com"
  - Phone: "1234567890"
  - Service: Any service
  - Message: "Test message"
- [ ] Click Submit
- [ ] Confirmation appears on screen

### Testing Reviews
- [ ] Go to Reviews page
- [ ] Click "Add Review" or similar button
- [ ] Fill out test review:
  - Name: "Happy Customer"
  - Review: "Great service!"
  - Date: Today's date
- [ ] Click Submit
- [ ] Review appears on page

### Viewing Your Data
- [ ] Open browser
- [ ] Go to: http://localhost:3000/api/inquiries
- [ ] See your test contact form
- [ ] Go to: http://localhost:3000/api/testimonials
- [ ] See your test review

### All Checks Pass?
- [ ] ✅ Yes → Go to Phase 2
- [ ] ❌ No → Contact developer

---

## Phase 2: Email Setup (Optional but Recommended)
**What:** Get email notifications
**Time:** ~15 minutes
**Who:** You (follow steps below)

### Step 1: Create Resend Account
- [ ] Go to https://resend.com
- [ ] Click "Sign Up"
- [ ] Enter your email
- [ ] Enter password
- [ ] Verify your email
- [ ] You see dashboard

### Step 2: Get API Key
- [ ] In Resend dashboard, find "API Keys"
- [ ] Click "Create New API Key"
- [ ] Name: "Py Investigation Agency"
- [ ] Select: "Emails"
- [ ] Copy the key (starts with `re_`)
- [ ] Save in safe place (Word doc or notepad)

### Step 3: Tell Developer
- [ ] Share the API key with your developer
- [ ] Developer adds it to website
- [ ] Website restarts
- [ ] Test email (see next section)

### Step 4: Test Email
- [ ] Go to http://localhost:3000/contact
- [ ] Fill test form (any details)
- [ ] Submit
- [ ] Check email inbox
- [ ] ✅ Should receive confirmation

### Emails Working?
- [ ] ✅ Yes → Continue to Phase 3
- [ ] ❌ No → Ask developer to check

---

## Phase 3: Prepare for Deployment
**What:** Get ready to go live
**Time:** ~1 hour
**Who:** You + Your Developer

### Update Content
- [ ] Review all text on website
- [ ] Update contact information (phone, email, address)
- [ ] Update service descriptions if needed
- [ ] Update About page information
- [ ] Upload your logo
- [ ] Upload quality photos

### Verify All Information
- [ ] Phone number is correct
- [ ] Email address is correct
- [ ] Address is correct
- [ ] Services are all listed
- [ ] Service descriptions are accurate
- [ ] No spelling errors
- [ ] No broken images

### Final Testing
- [ ] Test all links work
- [ ] Test all forms work
- [ ] Test all pages load fast
- [ ] Test on mobile phone
- [ ] Test on tablet
- [ ] Test in different browser (Chrome, Firefox, Safari)

### Get Domain Name
- [ ] Decide on domain name
- [ ] Go to GoDaddy.com or Namecheap.com
- [ ] Search for domain (e.g., pyinvestigationagency.com)
- [ ] Purchase domain
- [ ] Note down login details
- [ ] Note down domain registrar

### Ready to Deploy?
- [ ] ✅ Everything looks good → Go to Phase 4
- [ ] ❌ Need changes → Modify and repeat Phase 3

---

## Phase 4: Deploy to Server
**What:** Make website live online
**Time:** ~2 hours
**Who:** Your Developer (handles most)

### Developer Actions
- [ ] Developer connects code to Vercel
- [ ] Website builds successfully
- [ ] Vercel generates temporary URL
- [ ] You test the temporary URL
- [ ] All systems working

### Domain Connection
- [ ] Your domain registrar settings updated
- [ ] Domain points to your website server
- [ ] DNS updated (can take up to 24 hours)
- [ ] Your custom domain now works

### Test Live Website
- [ ] Go to https://yourdomain.com
- [ ] Website loads
- [ ] All pages work
- [ ] Forms submit
- [ ] Data saves
- [ ] Emails send (if configured)

### Live Website Checklist
- [ ] ✅ Website loads at custom domain
- [ ] ✅ All pages accessible
- [ ] ✅ Forms work
- [ ] ✅ Contact form sends email
- [ ] ✅ Review form works
- [ ] ✅ Mobile looks good
- [ ] ✅ No errors in browser

### Launch!
- [ ] ✅ Announce to clients
- [ ] ✅ Share website link
- [ ] ✅ Post on social media
- [ ] ✅ Add to email signature

---

## Phase 5: Regular Maintenance
**What:** Keep website running smoothly
**Time:** ~30 min per week

### Daily (Takes 5 minutes)
- [ ] Check email for new submissions
- [ ] Read customer inquiries
- [ ] Read customer reviews
- [ ] Respond to new contacts

### Weekly (Takes 15 minutes)
- [ ] Check website loads properly
- [ ] Verify no error messages
- [ ] Back up your data (ask developer)
- [ ] Review new submissions

### Monthly (Takes 30 minutes)
- [ ] Create full backup
- [ ] Check website speed
- [ ] Update content if needed
- [ ] Review analytics (if using Google Analytics)
- [ ] Check for any technical issues

### Quarterly (Takes 1 hour)
- [ ] Review and update service descriptions
- [ ] Update pricing if needed
- [ ] Update team information
- [ ] Upload new photos/testimonials
- [ ] Check all links still work

---

## Emergency Checklist
**If something goes wrong, do this:**

### Website Not Loading
- [ ] Check internet connection
- [ ] Refresh page (F5)
- [ ] Try different browser
- [ ] Clear browser cache
- [ ] Wait 5 minutes
- [ ] Try again
- [ ] ❌ Still not working? → Contact developer

### Form Not Submitting
- [ ] Refresh page
- [ ] Check all fields filled
- [ ] Check internet connection
- [ ] Try different browser
- [ ] ❌ Still not working? → Contact developer

### Not Receiving Emails
- [ ] Check spam folder
- [ ] Verify email address correct
- [ ] Ask developer to check settings
- [ ] Test with different email

### Data Lost
- [ ] ❌ Don't panic!
- [ ] Ask developer to restore from backup
- [ ] Usually can recover within 24 hours

### Website Hacked/Compromised
- [ ] ❌ Stop using website immediately
- [ ] Contact developer immediately
- [ ] Change all passwords
- [ ] Contact hosting provider

---

## Important Information to Save

**Print or save this information somewhere safe:**

```
WEBSITE DETAILS
==============
Domain: ________________________
Hosting: ________________________
Admin Email: ________________________
Emergency Contact: ________________________
Backup Location: ________________________

RESEND EMAIL (If using)
==============
API Key: ________________________
Account Email: ________________________
Password Hint: ________________________

CONTACTS
==============
Developer: ________________________
Domain Registrar: ________________________
Hosting Support: ________________________
```

---

## Success Metrics

### After 1 Month
- [ ] Website loading fast
- [ ] No errors or issues
- [ ] Received 5+ inquiries
- [ ] Received 2+ reviews
- [ ] Emails working
- [ ] Backed up data

### After 3 Months
- [ ] Regular customer inquiries
- [ ] Building client reviews
- [ ] Website rank improving in search
- [ ] Mobile traffic growing
- [ ] No technical issues

### After 6 Months
- [ ] Strong inquiry volume
- [ ] Good client testimonials
- [ ] Website established online
- [ ] Growing client base
- [ ] All systems stable

---

## Need Help?

**Contact your developer for:**
- Technical issues
- Data recovery
- Website changes
- Performance problems
- Security concerns

**Contact domain registrar for:**
- Domain renewal
- DNS settings
- Domain transfer

**Contact hosting provider for:**
- Uptime issues
- Server performance
- Backup recovery
- Account support

---

**Status:** Ready to Launch! 🚀  
**Version:** 1.0  
**Date:** May 2025
