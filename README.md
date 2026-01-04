# Properties-AI-Content-Engine
Automated Social Media Marketing Intelligence Platform
<img width="1600" height="660" alt="image" src="https://github.com/user-attachments/assets/6a950cdb-20de-448a-a8ae-a8278f0a13bd" />
AQARY AI CONTENT ENGINE
Automated Social Media Marketing Intelligence Platform

## EXECUTIVE SUMMARY
• Automates content generation from property listings

• AI-powered copywriting (Investment + Luxury angles)

• Multi-platform publishing (LinkedIn, Facebook, Instagram)

• Human approval workflow (Quality control)

• ROI Tracking & Analytics ready

## RESULTS (after 30 days)
✓ 200+ posts generated (vs. 10 manual/month)

✓ 40+ hours saved on copywriting per month

✓ Brand consistency across all channels

✓ Lead response automation (upcoming phase)

## TECHNOLOGY STACK
• n8n (Workflow Automation) — Apache 2.0 Open Source

• Google Gemini (AI Content) — Free tier available

• Airtable (Content Management) — 5 seats / $20/seat

• Google Sheets (Data Source) — Free

• LinkedIn / Facebook APIs — Free


## Components

### Workflow #1: Content Generator
- **Input:** New property listings from Google Sheets
- **Processing:** AI Gemini (Chief Investment Officer persona)
- **Output:** Structured JSON (Title, Copy, Hashtags, CTA)
- **Approval:** Airtable dashboard for human review

### Workflow #2: Publisher
- **Input:** Approved records from Airtable
- **Processing:** Platform-specific formatting (LinkedIn vs. Instagram etc...)
- **Output:** Live posts on social networks
- **Tracking:** Updates Airtable status to "Posted"

## Data Security
- Credentials stored in n8n's encrypted vault
- OAuth2 for all platform integrations
- No API keys in public repos
- Audit logs in Airtable

# AQARY CONTENT ENGINE - USER GUIDE

## For Marketing Manager (Non-Technical)

### How to Add a New Property
1. Open Google Sheet: "UAE Property Dataset"
2. Add new row with: Title, Address, Bedrooms, Bathrooms, Price, Images
3. Wait 5 minutes (workflow runs every 5 mins)
4. Check Airtable "Social Media Posts" table

### How to Approve a Post
1. Open Airtable → "Posts Management"
2. Review the auto-generated content
3. Edit if needed (fix grammar, add details)
4. Choose Platform(s) to post
5. Click **"Approve"** button
6. Post goes live within 10 minutes

### How to Track Performance
1. Open Airtable → "Posts Management"
2. Filter by `post status = "Posted"`
3. View timestamp in "Post Date"

## For System Administrator (Technical)

### Monitoring Health
- **Check n8n Dashboard:** Look for red/failed executions
- **Expected Frequency:** Content Gen runs every 5 mins, Publisher every 10 mins
- **Log Storage:** All errors logged in n8n execution history

### Scaling Up
- To process more properties: Lower the batch interval
- To add new platform: Update Switch node in Workflow #2
- To change AI tone: Edit system prompt in AI Agent node
