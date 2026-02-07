# CalWizz Privacy Policy Update

**Purpose:** Add Google Calendar data disclosure to satisfy Google OAuth verification requirements.

## Current Privacy Policy Location
https://calwizz.com/privacy (or /privacy.html)

## Required Addition

Add the following section to your privacy policy. This language is required by Google for OAuth verification:

---

### Google Calendar Data

CalWizz uses Google OAuth to connect to your Google Calendar. When you connect your calendar, we access the following data:

**What We Access:**
- Calendar event titles
- Event start and end times
- Event duration
- Number of attendees per event

**How We Use This Data:**
- To calculate meeting costs based on time spent
- To generate calendar analytics and insights
- To provide schedule health scoring

**How We Store This Data:**
- Calendar data is processed in your browser session
- We do not permanently store your calendar events on our servers
- Analytics summaries may be stored in your account if you have one

**Data Sharing:**
- We do not sell your calendar data
- We do not share your calendar data with third parties
- Aggregated, anonymized statistics may be used to improve the product

**Revoking Access:**
You can disconnect CalWizz from your Google account at any time:
1. Visit https://myaccount.google.com/permissions
2. Find CalWizz in the list of connected apps
3. Click "Remove Access"

Once revoked, CalWizz will no longer be able to access your calendar data.

**Contact:**
For questions about how we handle your data, contact: [your email]

---

## Where to Add This

Option A: Add as a new section called "Google Calendar Data" in your existing privacy policy

Option B: Create a dedicated page at calwizz.com/google-data-disclosure and link to it from the main privacy policy

## After Adding

1. Note the URL of your updated privacy policy
2. Go to Google Cloud Console → APIs & Services → OAuth consent screen
3. Update the "Privacy policy URL" field
4. Proceed with verification submission

## Demo Video Reminder

Google also requires a demo video showing:
- How users initiate OAuth (the "Connect Calendar" button)
- The consent screen they see
- What your app does with the data after connection

Keep it under 2 minutes. Can be an unlisted YouTube video.
