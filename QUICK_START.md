# ⚡ QUICK START CHECKLIST

## 🎯 Setup (15 Minutes)

### Google Sheets Setup
- [ ] Create a Google Sheet
- [ ] Add tabs: `ContactSubmissions`, `CallbackRequests`, `Reviews`
- [ ] Copy the Sheet ID from the URL
- [ ] Create a service account in Google Cloud
- [ ] Share the sheet with the service account email

### Resend Setup
- [ ] Go to https://resend.com
- [ ] Create free account
- [ ] Go to API Keys
- [ ] Create new API key
- [ ] Copy key (starts with `re_`)
- [ ] Paste into `.env.local` as `RESEND_API_KEY`

### .env.local Setup
- [ ] Copy `.env.local.example` to `.env.local`
- [ ] Update `GOOGLE_SHEETS_ID`
- [ ] Update `GOOGLE_SERVICE_ACCOUNT_JSON`
- [ ] Update `RESEND_API_KEY` (from Resend)
- [ ] Update `ADMIN_EMAIL` (your email)

### Start Development
```bash
npm run dev              # [ ]
```

## ✅ Testing (10 Minutes)

### Frontend
- [ ] Visit http://localhost:3000
- [ ] Browse all pages
- [ ] Check mobile view
- [ ] Test all navigation links

### Forms
- [ ] Fill and submit contact form at /contact
- [ ] Check admin email (should receive notification)
- [ ] Check your email (should receive confirmation)
- [ ] Fill and submit callback form

## 🚀 Deployment (10 Minutes)

### GitHub
```bash
git add .                             # [ ]
git commit -m "Complete website"     # [ ]
git push origin main                 # [ ]
```

### Vercel
- [ ] Go to https://vercel.com/new
- [ ] Import from GitHub
- [ ] Select repository
- [ ] Add environment variables:
  - GOOGLE_SHEETS_ID                  # [ ]
  - GOOGLE_SERVICE_ACCOUNT_JSON       # [ ]
  - RESEND_API_KEY                   # [ ]
  - ADMIN_EMAIL                      # [ ]
  - NEXT_PUBLIC_SITE_URL             # [ ]
- [ ] Click Deploy
- [ ] Wait for deployment (3-5 min)
- [ ] Test live site

### Verification
- [ ] Website loads at https://yourdomain.com
- [ ] Forms work
- [ ] Emails send
- [ ] No console errors

## 📋 Important Files

**Must Update:**
- `.env.local` - Add your credentials
- `lib/constants.ts` - Update contact info
- `lib/data/services.ts` - Update service details

**Should Read:**
- `README.md` - Overview and troubleshooting
- `SETUP_GUIDE.md` - Detailed instructions
- `INTEGRATION_GUIDE.md` - Service setup help
- `BUILD_SUMMARY.md` - What's been built

## 🔑 Important Passwords/Keys

**Save These Securely:**
- Google Sheets ID: `________________`
- Service Account JSON: `________________`
- Resend API Key: `________________`
- Admin Notification Email: `________________`

## 🆘 If Something Goes Wrong

### Forms Not Working
```bash
npm run dev
```

### Emails Not Sending
- Verify `RESEND_API_KEY` is correct
- Check Resend dashboard for errors
- Check spam folder

### Sheets Access Error
- Make sure the sheet is shared with the service account email

## 📞 Support

1. **README.md** - Quick fixes
2. **SETUP_GUIDE.md** - Detailed help
3. **INTEGRATION_GUIDE.md** - Service help
4. Console logs - See what went wrong

## 🎉 After Launch

- [ ] Update contact information

- [ ] Customize styling if needed
- [ ] Set up analytics (Google Analytics)
- [ ] Monitor admin email inbox
- [ ] Respond to submissions
- [ ] Test regularly

---

## ⏱️ Time Breakdown

- Google Sheets setup: 5 min
- Resend setup: 3 min
- .env.local: 2 min
- Database init: 1 min
- Testing: 10 min
- Deployment: 10 min
- **Total: ~30 minutes**

---

## 🎯 You Have Everything Needed

✅ Complete frontend  
✅ Complete backend  
✅ Database schema  
✅ Email integration  
✅ Admin notifications  
✅ Documentation  

**Just add your credentials and deploy!**

---

**Status: READY TO DEPLOY** 🚀
