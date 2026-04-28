# Testing Guide: How to Verify Your Automation

Once you have connected all services, follow these steps to ensure everything is working correctly without spending any money or using real ads.

---

## 1. Use the Facebook Lead Ads Testing Tool
Facebook provides a free tool to "simulate" a lead submission.

1. Go to the [Lead Ads Testing Tool](https://developers.facebook.com/tools/lead-ads-testing).
2. Select your **Page** and the **Form** you connected in Make.com.
3. Click **Create Lead**. 
   - *Note: If you have already created a lead, click "Delete Lead" first, then "Create Lead".*
4. Click **Preview Form** if you want to fill in custom data (like your own email to see the Gmail notification).

---

## 2. Monitor Make.com
1. Go back to your Make.com scenario.
2. Ensure the scenario is **ON**.
3. You should see a "bubble" with the number **1** appear over the Facebook module. This means it caught the lead.
4. Watch the flow move through the modules:
   - It will check the Google Sheet.
   - It will add the row.
   - It will create the contact in HubSpot.
   - It will send the two emails.

---

## 3. Verify the Results
Check each of your services to confirm the data arrived:

1. **Google Sheets**: A new row should be added at the bottom with the lead's name and details.
2. **HubSpot**: Go to **CRM > Contacts**. Search for the email address you used in the test.
3. **Gmail (Lead)**: If you used your own email in the test, check your Inbox.
4. **Gmail (Agent)**: Check the inbox of the email address you set as the "Agent" in the final Gmail module.

---

## 4. How to Fix If It Fails
- **Module stays red**: Click the red icon in Make.com. It will tell you the exact error (e.g., "Spreadsheet not found").
- **No lead arrives**: Make sure you clicked "Create Lead" in the Facebook Testing Tool and that the scenario is actually switched **ON**.
- **HubSpot error**: Usually means a field mapping is wrong (e.g., trying to put a phone number into an email field).
