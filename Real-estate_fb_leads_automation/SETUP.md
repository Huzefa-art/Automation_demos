# Setup Guide: Real Estate Lead Management Automation

Follow these steps to set up your automated lead management system from scratch. This system uses **Make.com**, **Google Sheets**, **HubSpot**, and **Gmail**.

---

## 1. Create Required Accounts (Free Tiers)

If you don't have these already, sign up for the free versions:
1. **Make.com**: [Sign up here](https://www.make.com/en/register).
2. **Google Account**: For Google Sheets and Gmail.
3. **HubSpot CRM**: [Sign up for Free CRM](https://www.hubspot.com/products/crm).
4. **Facebook Business Suite**: You need a Facebook Page and a Lead Ad form.

---

## 2. Prepare Your Google Sheet

1. Create a new Google Sheet named `Real Estate Leads`.
2. Rename the first tab (sheet) to `Leads`.
3. Add the following headers to the first row (A1 to E1):
   - **Full Name**
   - **Email**
   - **Phone Number**
   - **Source**
   - **Date Added**

---

## 3. Import the Scenario to Make.com

1. Log in to [Make.com](https://www.make.com).
2. Click **+ Create a new scenario** in the top right.
3. Click the **three dots (...)** at the bottom of the screen and select **Import Blueprint**.
4. Upload the `scenario.json` file provided.
5. You will see a map of modules. They will have red warning icons because they aren't connected yet.

---

## 4. Connect Your Services to Make.com

Click on each module in the scenario to set up the connection:

### A. Facebook Lead Ads (The Trigger)
- Click the module -> **Add** a connection.
- Log in to Facebook and select your Page.
- Select your **Lead Gen Form**.

### B. Google Sheets (Search Rows)
- Click the module -> **Add** a connection -> Select your Google account.
- Select the `Real Estate Leads` spreadsheet and the `Leads` sheet.
- This module checks if the email already exists to prevent duplicates.

### C. Google Sheets (Add a Row)
- Use the same connection as above.
- Map the fields from the Facebook module to the columns in your sheet.

### D. HubSpot (Create a Contact)
- Click the module -> **Add** a connection.
- Log in to HubSpot and choose your account.
- Map the Name, Email, and Phone from Facebook.

### E. Gmail (Send Email to Lead)
- Click the module -> **Add** a connection -> Select your Gmail.
- Set the **To** field to the lead's email.
- Copy the "Lead Confirmation" template into the content box.

### F. Gmail (Send Email to Agent)
- Use the same connection.
- Set the **To** field to *your* email (or the agent's).
- Copy the "Agent Notification" template into the content box.

---

## 5. Turning It On

1. Click the **Save** icon (floppy disk) at the bottom.
2. Toggle the switch at the bottom left to **ON**.
3. Select "From now on" when prompted.

---

## Common Errors & Fixes
- **Connection Expired**: If the automation stops, go to "Connections" in Make and re-authorize the service.
- **Permission Error**: Ensure you have "Admin" access to your Facebook Page.
- **Gmail Block**: If the email doesn't send, check your Gmail "Sent" folder. You may need to enable "Less secure app access" or use an App Password if you have 2FA on.
