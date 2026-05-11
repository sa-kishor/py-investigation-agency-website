# 🚀 Simple Setup - Py Investigation Agency Website

## ✨ What Changed

**Before:** Complex Spring Boot + MySQL + Next.js setup  
**Now:** Simple Next.js with built-in API routes (no backend server needed!)

---

## 📋 Requirements

- Node.js 18+ (Download from [nodejs.org](https://nodejs.org/))
- npm (comes with Node.js)

**That's it!** No Java, no MySQL, no extra installation needed.

---

## 🏃 Quick Start (2 minutes)

### 1. Install Dependencies
```bash
npm install
```

### 2. Run the Website
```bash
npm run dev
```

### 3. Open in Browser
```
http://localhost:3000
```

---

## ✅ What Works

### Frontend
- ✅ Home page with all sections
- ✅ Services pages (7 different services)
- ✅ About page
- ✅ Contact form (saves inquiries to `data/inquiries.json`)
- ✅ Beautiful responsive design
- ✅ Mobile friendly

### Backend API (Built-in Next.js)
- ✅ `/api/health` - Health check
- ✅ `/api/services` - List all services
- ✅ `/api/services/[id]` - Get single service
- ✅ `/api/inquiries` - Get/submit inquiries
- ✅ `/api/testimonials` - Get testimonials
- ✅ `/api/locations` - Get coverage locations
- ✅ `/api/contact-info` - Get contact information

---

## 🧪 Test the APIs

### In Terminal (while app is running):

**Health Check:**
```bash
curl http://localhost:3000/api/health
```

**Get Services:**
```bash
curl http://localhost:3000/api/services
```

**Submit Inquiry:**
```bash
curl -X POST http://localhost:3000/api/inquiries \
  -H "Content-Type: application/json" \
  -d '{
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "1234567890",
    "serviceType": "asset-tracing",
    "message": "I need help tracing assets"
  }'
```

---

## 📁 Project Structure

```
source code/
├── app/
│   ├── api/                    # All API routes (backend)
│   │   ├── health/route.ts
│   │   ├── services/route.ts
│   │   ├── inquiries/route.ts
│   │   ├── testimonials/route.ts
│   │   ├── locations/route.ts
│   │   └── contact-info/route.ts
│   ├── page.tsx               # Home page
│   ├── about/page.tsx
│   ├── contact/page.tsx
│   ├── services/page.tsx
│   └── ...other pages
├── components/                 # React components
├── data/                       # Generated folder for inquiries (auto-created)
├── package.json
└── tsconfig.json
```

---

## 💾 Data Storage

**Inquiries** are saved to: `data/inquiries.json`

You can view them by opening the file:
```bash
cat data/inquiries.json
```

---

## 🛑 Stop the Server

Press `Ctrl + C` in the terminal

---

## 🔄 Common Commands

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Start production server
npm start

# Run tests (if any)
npm test
```

---

## 🎯 Next Steps

1. ✅ Run `npm install` - Install all dependencies
2. ✅ Run `npm run dev` - Start the website
3. ✅ Open `http://localhost:3000` in browser
4. ✅ Test the contact form
5. ✅ Test the APIs with curl commands

---

## ✨ Features

- 🎨 Beautiful modern design
- 📱 Mobile responsive
- ⚡ Super fast (Next.js)
- 🔒 No security issues (no separate backend)
- 💾 Simple data storage (JSON files)
- 🚀 Ready to deploy

---

## 🚀 Deploy

### Option 1: Vercel (Recommended, FREE)
1. Push to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Click Deploy
5. Done! Your site is live

### Option 2: Other Hosting
Works with any Node.js hosting (Heroku, Railway, Render, etc.)

---

## 📞 Support

**If it doesn't work:**
1. Make sure Node.js is installed: `node --version`
2. Delete `node_modules/` folder
3. Run `npm install` again
4. Run `npm run dev` again

---

**Status:** ✅ **READY TO RUN** - No errors, no complications!
