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

**Template text to add** (must match the requested `calendar` read/write scope and the
live privacy policy at `privacy.html` — do not understate to read-only or client-side-only):
> CalWizz uses read and write access to your Google Calendar. Read access is used to
> analyze your events (titles, times, durations, and attendees) and generate calendar
> analytics. Write access is used only when you enable Focus Time or Lunch Protection,
> where CalWizz creates clearly labeled events on your behalf and only manages events it
> created. Calendar analysis runs on our servers during sync; cached calendar data may be
> temporarily stored to compute analytics and is cleared when you disconnect. We store
> encrypted OAuth tokens to enable syncing. You can revoke access anytime at
> https://myaccount.google.com/permissions.

> NOTE: The public privacy policy (`privacy.html`) is the source of truth for these
> claims. Keep this template, the consent screen, and the FAQ aligned with it.

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
The app requests these scopes (see `time-insights-app/google_calendar.py`):
- `calendar` (full read/write) — needs verification
- `userinfo.email` — no verification needed
- `userinfo.profile` — no verification needed
- `openid` — no verification needed

The `calendar` scope is read/write, not read-only. Read access powers the
analytics; write access is used to create/manage CalWizz-tagged events (Focus
Time, Lunch Protection). Full calendar access is classified as "sensitive/restricted"
and requires Google verification. Make sure the consent screen, privacy policy, and
public FAQ all describe read/write access consistently — Google reviewers cross-check
public claims against requested scopes.

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
