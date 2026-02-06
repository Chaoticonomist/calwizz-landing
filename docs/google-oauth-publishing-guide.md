# CalWizz Google OAuth Publishing Guide

## Current Status
App is in "Testing" mode — limited to 100 test users you manually add.

## Goal
Move to "Production" so anyone with a Google account can connect their calendar.

---

## Steps to Publish

### 1. Update Privacy Policy ⚡ REQUIRED
Your privacy policy at calwizz.com/privacy must include:

- [ ] What data you access (Google Calendar events: title, time, duration, attendees)
- [ ] How you use the data (calculate meeting costs, show analytics)
- [ ] How you store the data (or don't — if processed in-browser only)
- [ ] How users can revoke access (link to Google account permissions)
- [ ] Contact information

**Template text to add:**
> CalWizz accesses your Google Calendar data (event titles, times, durations, and attendee counts) solely to calculate meeting costs and provide calendar analytics. We do not store your calendar data on our servers — analysis happens in your browser. You can revoke access anytime at https://myaccount.google.com/permissions.

### 2. Create Demo Video ⚡ REQUIRED FOR SENSITIVE SCOPES
Google requires a video showing:
- [ ] How users initiate OAuth (click "Connect Calendar")
- [ ] The consent screen they see
- [ ] What your app does with the data
- [ ] That you're not doing anything sketchy

**Tips:**
- Under 2 minutes
- Can be unlisted YouTube video
- Screen recording with simple narration
- Show the actual user flow

### 3. Fill Out OAuth Consent Screen
Go to: [Google Cloud Console](https://console.cloud.google.com/) → APIs & Services → OAuth consent screen

Fill in:
- [ ] App name: CalWizz
- [ ] User support email
- [ ] App logo (optional but professional)
- [ ] App homepage: https://calwizz.com
- [ ] Privacy policy: https://calwizz.com/privacy
- [ ] Terms of service: https://calwizz.com/terms (optional)
- [ ] Authorized domains: calwizz.com, app.calwizz.com
- [ ] Developer contact email

### 4. Verify Scopes
You're likely using:
- `calendar.readonly` — needs verification
- `userinfo.email` — no verification needed
- `userinfo.profile` — no verification needed

Calendar scopes = "sensitive" = requires verification.

### 5. Submit for Verification
- Click "Publish App" in OAuth consent screen
- Google will review (can take 1-4 weeks)
- They may ask clarifying questions

### 6. Common Rejection Reasons & Fixes
| Issue | Fix |
|-------|-----|
| Privacy policy doesn't mention Google data | Add specific Google Calendar disclosure |
| No demo video | Create and upload video |
| Scopes too broad | Request minimum necessary scopes |
| Branding mismatch | App name must match consent screen |

---

## Timeline Estimate
- Privacy policy update: 30 min
- Demo video: 1-2 hours
- Form filling: 30 min
- Google review: 1-4 weeks
- Q&A with reviewer: 1-2 days per round

**Total: ~3 hours of work, then wait for Google**

---

## Quick Start Checklist
1. [ ] Update privacy policy TODAY
2. [ ] Record demo video
3. [ ] Submit for verification
4. [ ] While waiting: continue marketing the calculator (no OAuth needed)

The calculator at calculator.calwizz.com works without Google OAuth — promote that immediately while the app verification is pending!
