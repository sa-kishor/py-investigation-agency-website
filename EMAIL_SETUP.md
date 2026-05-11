# 📧 Email Setup Guide - Complete

## 🎯 Where Everything Is Saved

### Reviews/Testimonials
- **Saved to:** `data/testimonials.json`
- **Emails sent to:** pyinvestigationagency@gmail.com (admin notification)

### Contact Forms (Inquiries)  
- **Saved to:** `data/inquiries.json`
- **Emails sent to:**
  - Customer email (confirmation)
  - pyinvestigationagency@gmail.com (admin notification)

---

## 📨 Email Setup (5 minutes)

### Step 1: Create Resend Account (FREE)
1. Go to https://resend.com
2. Click "Sign Up"
3. Enter your email and password
4. Verify your email
5. You'll get a dashboard

### Step 2: Get API Key
1. In Resend dashboard, go to "API Keys"
2. Click "Create New API Key"
3. Name it: `Py Investigation Agency`
4. Select: "Emails"
5. Copy the key

### Step 3: Add API Key to Your App
1. Open `.env.local` file in your project
2. Add your API key:
```
RESEND_API_KEY=re_your_api_key_here
```
3. Save the file
4. Restart the dev server: `npm run dev`

---

## 📧 Email Flow

### When Someone Submits a Contact Form:

```
Customer fills form
         ↓
Data saved to data/inquiries.json
         ↓
Email 1: Sent to Customer ✉️
         (Confirmation: "We received your inquiry")
         ↓
Email 2: Sent to Admin ✉️
         (pyinvestigationagency@gmail.com)
         (Alert: "New inquiry received")
```

### When Someone Submits a Review:

```
Customer submits review
         ↓
Data saved to data/testimonials.json
         ↓
Email: Sent to Admin ✉️
       (pyinvestigationagency@gmail.com)
       (Alert: "New testimonial received")
       ↓
Review appears on website immediately
```

---

## 📊 Email Templates

### Contact Form - Customer Email
```
Subject: "Inquiry Received - Py Investigation Agency"

Thank You for Your Inquiry

Hi [Name],

We have received your inquiry about [Service].

Your Details:
- Service: [Service Type]
- Email: [Email]
- Phone: [Phone]
- Message: [Your message]

Our team will review your inquiry and contact you soon.

Thank you,
Py Investigation Agency Team
```

### Contact Form - Admin Email
```
Subject: "New Inquiry Received"

New Inquiry Received

From: [Name]
Email: [Email]
Phone: [Phone]
Service: [Service Type]
Message: [Full message]

Inquiry ID: [ID]
```

### Review - Admin Email
```
Subject: "New Testimonial Received"

New Testimonial/Review Received

From: [Name]
Date: [Date]

Review:
"[Full review text]"

Review ID: [ID]
This review has been automatically added to your testimonials section.
```

---

## 🧪 Test Emails

### Test Contact Form Submission:
```bash
curl -X POST http://localhost:3000/api/inquiries \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Test User",
    "email": "test@example.com",
    "phone": "1234567890",
    "serviceType": "asset-tracing",
    "message": "Test inquiry"
  }'
```

**Emails sent:**
1. ✉️ To: test@example.com (confirmation)
2. ✉️ To: pyinvestigationagency@gmail.com (admin alert)

### Test Review Submission:
```bash
curl -X POST http://localhost:3000/api/testimonials \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Happy Customer",
    "quote": "Great service!",
    "date": "12 May 2025"
  }'
```

**Email sent:**
1. ✉️ To: pyinvestigationagency@gmail.com (admin alert)

---

## ✅ Verification Checklist

- [ ] Resend account created
- [ ] API key generated
- [ ] API key added to `.env.local`
- [ ] Dev server restarted (`npm run dev`)
- [ ] Test contact form submission
- [ ] Check email inbox for confirmation
- [ ] Check admin email for notification
- [ ] Test review submission
- [ ] All emails received successfully

---

## 🆘 Troubleshooting

### "Email not sent" error?

**Check 1:** Is API key in `.env.local`?
```bash
cat .env.local
```

**Check 2:** Did you restart the server after adding the key?
```bash
# Stop: Ctrl+C
# Start again:
npm run dev
```

**Check 3:** Is API key correct?
- Check it in Resend dashboard
- Copy it again carefully
- Paste into `.env.local`
- Restart server

### Email goes to spam?

- Add to Resend: In Resend dashboard → "Domains"
- Verify your domain for better deliverability

### No emails at all?

Check server logs for errors:
```
npm run dev
# Look for error messages
```

---

## 🚀 Production Email

When you deploy to production:

1. **Add environment variable** to your hosting (Vercel, Heroku, etc.)
   - Variable: `RESEND_API_KEY`
   - Value: Your API key

2. **Update sender email** (optional):
   - In code: `from: 'your-domain@emails.resend.com'`

3. **Update admin email** (optional):
   - In code: Change `pyinvestigationagency@gmail.com` to your actual email

---

## 📁 Files Modified

- `app/api/inquiries/route.ts` - Added email on form submission
- `app/api/testimonials/route.ts` - Added email on review submission
- `.env.local` - Added API key

---

## 💾 Data Locations

```
data/
├── inquiries.json      # Contact form submissions
└── testimonials.json   # Customer reviews
```

---

## ✨ Summary

✅ Reviews saved to: `data/testimonials.json`  
✅ Forms saved to: `data/inquiries.json`  
✅ Emails sent automatically (when API key configured)  
✅ Admin notifications for all submissions  
✅ Customer confirmations for inquiries  

**Everything works automatically once API key is added!**
