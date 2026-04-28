# Templates: Real Estate Lead Management

## 1. Google Sheets Template
Create your spreadsheet with these exact column names in the first row:

| A | B | C | D | E |
|---|---|---|---|---|
| **Full Name** | **Email** | **Phone Number** | **Source** | **Date Added** |

---

## 2. Email Template: Lead Confirmation
**To:** `{{1.email}}` (Lead's email)  
**Subject:** Thank you for your interest! - Real Estate Inquiry

**Body:**
```text
Hello {{1.full_name}},

Thank you for your interest in our property listings on Facebook! 

I have received your details and wanted to let you know that one of our senior agents will be reaching out to you shortly to provide more information and answer any questions you may have.

In the meantime, feel free to reply to this email if you have any urgent requests.

Best regards,

Real Estate Team
```

---

## 3. Email Template: Agent Notification
**To:** `your-email@example.com` (Your or Agent's email)  
**Subject:** 🚀 NEW LEAD: {{1.full_name}} from Facebook

**Body:**
```text
Hey Team,

We just received a new lead from our Facebook Lead Ads campaign!

Details:
- Name: {{1.full_name}}
- Email: {{1.email}}
- Phone: {{1.phone_number}}
- Source: Facebook Lead Ads

Please reach out to them within the next 15 minutes for the best conversion rate.

View in Google Sheets: [Link to your sheet]
View in HubSpot: [Link to HubSpot]

Happy selling!
```
