# 💾 Data Storage Guide

## Where Is Everything Saved?

All data is saved in the **`data/`** folder as simple JSON files:

```
data/
├── inquiries.json      # Contact form submissions
└── testimonials.json   # Customer reviews/testimonials
```

This folder is **automatically created** when you first run the app.

---

## 📊 What Gets Saved

### 1. **Inquiries** (`data/inquiries.json`)
Saved when someone submits the contact form.

**Example:**
```json
[
  {
    "id": 1,
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "1234567890",
    "serviceType": "asset-tracing",
    "message": "I need help tracing assets",
    "status": "PENDING",
    "createdAt": "2025-05-11T10:30:00Z"
  }
]
```

### 2. **Testimonials/Reviews** (`data/testimonials.json`)
Saved when someone submits a review.

**Example:**
```json
[
  {
    "id": 1,
    "quote": "Great service! Highly recommended!",
    "name": "Jane Smith",
    "date": "12 May 2025",
    "createdAt": "2025-05-12T14:22:00Z"
  }
]
```

---

## 📝 How to Submit Data

### Submit a Review (Testimonial)

**Using curl:**
```bash
curl -X POST http://localhost:3000/api/testimonials \
  -H "Content-Type: application/json" \
  -d '{
    "quote": "Excellent investigation service!",
    "name": "Your Name",
    "date": "12 May 2025"
  }'
```

**Response:**
```json
{
  "success": true,
  "data": {
    "id": 2,
    "quote": "Excellent investigation service!",
    "name": "Your Name",
    "date": "12 May 2025",
    "createdAt": "2025-05-12T14:22:00Z"
  },
  "message": "Testimonial added successfully"
}
```

### Submit a Contact Form (Inquiry)

**Using curl:**
```bash
curl -X POST http://localhost:3000/api/inquiries \
  -H "Content-Type: application/json" \
  -d '{
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "9876543210",
    "serviceType": "employee-verification",
    "message": "I need employee background checks"
  }'
```

---

## 👀 View Your Data

### Open Files in VS Code
1. Open the `data` folder in VS Code
2. Click on `inquiries.json` or `testimonials.json`
3. See all submissions

### View in Terminal

**View inquiries:**
```bash
cat data/inquiries.json
```

**View testimonials:**
```bash
cat data/testimonials.json
```

### View in Browser

**Get all inquiries:**
Visit: `http://localhost:3000/api/inquiries`

**Get all testimonials:**
Visit: `http://localhost:3000/api/testimonials`

**Get specific inquiry by ID:**
Visit: `http://localhost:3000/api/inquiries` (view the JSON to get ID)

---

## 🔄 APIs Available

| Endpoint | Method | Purpose | Saves To |
|----------|--------|---------|----------|
| `/api/inquiries` | GET | Get all contact submissions | `data/inquiries.json` |
| `/api/inquiries` | POST | Submit contact form | `data/inquiries.json` |
| `/api/testimonials` | GET | Get all reviews | `data/testimonials.json` |
| `/api/testimonials` | POST | Submit review | `data/testimonials.json` |
| `/api/services` | GET | Get all services | (hard-coded) |
| `/api/locations` | GET | Get locations | (hard-coded) |
| `/api/contact-info` | GET | Get contact info | (hard-coded) |
| `/api/health` | GET | Health check | (no save) |

---

## 📤 Export Your Data

### Backup inquiries:
```bash
cp data/inquiries.json backups/inquiries_backup.json
```

### Share testimonials:
```bash
cat data/testimonials.json > testimonials_list.txt
```

---

## 🗑️ Clear Data

### Delete all inquiries:
```bash
rm data/inquiries.json
```

### Delete all testimonials:
```bash
rm data/testimonials.json
```

(Files will be recreated with default data when needed)

---

## 📁 Example Workflow

1. **User submits contact form** on website
2. **Data is saved** to `data/inquiries.json`
3. **You review** the submission in the file
4. **You respond** to the customer

Similarly for reviews:

1. **Customer submits review** on website
2. **Review is saved** to `data/testimonials.json`
3. **Review appears** on testimonials section
4. **All reviews are displayed** to future customers

---

## 🎯 Next Steps

- ✅ Website is running
- ✅ Users can submit inquiries
- ✅ Users can submit reviews
- ✅ All data is saved locally
- 📌 **TODO:** Migrate to database if you need more features later

---

**Everything works locally! No database setup needed.**
