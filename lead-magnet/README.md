# KSeF Lead Magnet System

## Overview
Email capture system for KSeF Blog with lead magnet (checklist).

## Files

```
lead-magnet/
├── index.html          # Landing page with full checklist
├── CHECKLIST_CONTENT.md # Source content (Markdown)
└── README.md           # This file
```

## How It Works

### 1. User Journey
1. User visits KSeF Blog homepage
2. Sees email capture form in footer
3. Enters email and clicks "Pobierz"
4. Data sent to Make.com webhook
5. User sees success message
6. User can access full checklist

### 2. Email Capture Flow
```
Homepage Form → Make.com Webhook → Mailchimp → Welcome Email → Checklist Access
```

### 3. Make.com Webhook Setup

**Webhook URL:**
```
https://hook.make.com/ksef-email-capture
```

**Payload:**
```json
{
  "email": "user@example.com",
  "source": "ksef-blog-homepage",
  "timestamp": "2026-02-03T10:00:00Z"
}
```

**Actions in Make.com:**
1. Webhook receives data
2. Validate email format
3. Add to Mailchimp list "KSEF Leads"
4. Send welcome email with checklist link
5. Log to Google Sheets

### 4. Mailchimp Setup

**List:** KSEF Leads (us19)
**Welcome Email Template:** KSeF Checklist Welcome

### 5. Deployment

The landing page is already HTML and can be deployed to Vercel:
```bash
cd ksef-blog/lead-magnet
vercel deploy
```

Or add to existing KSeF Blog deployment.

## Usage

### For Users
1. Enter email on KSeF Blog homepage
2. Check email for welcome message
3. Click link to full checklist
4. Download PDF or use online

### For Admin
1. Monitor Make.com webhook stats
2. Check Mailchimp for new subscribers
3. Update checklist content as needed

## Metrics to Track

| Metric | Target | Where |
|--------|--------|-------|
| Email submissions | 100/month | Make.com |
| Email delivery rate | >95% | Mailchimp |
| Checklist downloads | 80% of submissions | Make.com |

## Updates

To update the checklist:
1. Edit `CHECKLIST_CONTENT.md`
2. Generate new `index.html` if needed
3. Deploy changes

## License
Free for subscribers of KSeF Blog
