# ARX GATE Website Build Guide: Step-by-Step

## Quick Start: Choose Your Platform

### **Platform Comparison**

| Platform | Ease | Cost | Customization | Multi-Page | Best For |
|----------|------|------|---------------|-----------|----------|
| **Carrd** | ⭐⭐⭐⭐⭐ | Free–$19/yr | ⭐⭐⭐ | Limited | Quick launch, single-page |
| **Neocities** | ⭐⭐⭐⭐ | Free | ⭐⭐⭐⭐⭐ | ✓ Yes | Full HTML/CSS/JS, retro vibe |
| **WordPress** | ⭐⭐⭐ | ~$60–$300/yr | ⭐⭐⭐⭐ | ✓ Yes | Scalable, media-rich |
| **GitHub Pages** | ⭐⭐⭐ | Free | ⭐⭐⭐⭐⭐ | ✓ Yes | Developers, version control |
| **Wix** | ⭐⭐⭐⭐ | $15–$50/mo | ⭐⭐ | ✓ Yes | Drag-and-drop, templates |

**Recommended: Neocities + Custom Domain** (or GitHub Pages for developers)

---

## BUILD PATH A: NEOCITIES (Recommended)

### **1. Set Up Account**

1. Go to **neocities.org**
2. Sign up with email
3. Choose a free site name (e.g., `arxgate`, `project-chronos`, `korovin-archive`)
4. Verify email

### **2. File Structure Setup**

Create this folder structure locally (on your computer):

```
arxgate-site/
├── index.html                    (Homepage)
├── 404.html                      (Error page)
├── about.html                    (Accessibility/Disclaimer)
├── press.html                    (Press release archive)
├── operators.html                (Operator portal)
├── richter.html                  (Richter judgment page)
├── protocol.html                 (Dec 25 countdown)
├── assets/
│   ├── css/
│   │   ├── main.css
│   │   ├── crt.css
│   │   ├── glitch.css
│   │   └── richter.css
│   ├── js/
│   │   ├── gates.js
│   │   ├── countdown.js
│   │   ├── upload.js
│   │   └── glitch.js
│   ├── audio/
│   │   ├── stauber-distort.mp3
│   │   ├── radio-buzz.mp3
│   │   └── boots.mp3
│   ├── img/
│   │   ├── entity-retrograde.png
│   │   ├── entity-abigail.png
│   │   ├── entity-lima.png
│   │   ├── entity-guardian.png
│   │   ├── entity-architect.png
│   │   ├── korovin.png
│   │   ├── qr-twitter.png
│   │   ├── qr-form.png
│   │   └── redacted-pdf.png
│   └── data/
│       ├── ghost-ops.json
│       ├── entity-bios.json
│       └── timeline.json
└── dev/
    ├── logs.html                 (Hidden behind checksum gate)
    └── radio.html                (UVB-76 portal)
```

### **3. Create HTML Files**

Use templates from **ARXGATE-BLUEPRINT.md** above. Copy code for:
- `index.html` (Home page)
- `operators.html` (Operator portal)
- `richter.html` (Richter judgment)
- `protocol.html` (December countdown)
- `about.html` (Accessibility + disclaimer)

Create simple versions of:
- `press.html` (List of press releases with links)
- `dev/logs.html` (Hidden /dev/ filesystem)

### **4. Create CSS Files**

Copy these into `/assets/css/`:
- `main.css` (from blueprint)
- `crt.css` (from blueprint)
- `glitch.css` (from blueprint)
- `richter.css` (color overrides for Richter page)

**Example `richter.css`:**
```css
/* Richter page specific overrides */
body.richter-page {
    background: linear-gradient(135deg, #f5f5dc 0%, #fffacd 50%, #ffd700 100%);
    color: #333;
}

body.richter-page header {
    background-color: rgba(180, 0, 0, 0.9);
}
```

### **5. Create JavaScript Files**

Copy into `/assets/js/`:
- `gates.js` (checksum validation)
- `countdown.js` (Dec 25 timer)
- `upload.js` (Google Forms integration)
- `glitch.js` (CRT effects)

### **6. Create Audio Files**

Use **Audacity** (free) to create:

**stauber-distort.mp3:**
1. Open Audacity
2. Generate → Tone (Frequency: 50–200 Hz, Duration: 5s)
3. Effects → Distortion (Crunch, Heavy)
4. Effects → Reverb (Room Size: Large, Wet: 80%)
5. File → Export → Save as MP3

**radio-buzz.mp3:**
1. Generate → Noise (White, 3s)
2. Generate → Tone (4625 Hz, 1s) [overlay]
3. Effect → Lowpass Filter (Cutoff: 6000 Hz)
4. Export as MP3

**boots.mp3:**
1. Download free boot sound from **freesound.org**
2. Trim to 5–10 seconds
3. Export as MP3

### **7. Create Image Files**

Use **Canva.com** (free tier):

**Entity Portraits:**
1. Create 400×600 blank designs
2. Use filters: "Old Photo", "Vintage", "Glitch"
3. Add aged paper texture
4. Add distortion/noise overlay
5. Download as PNG

**QR Codes (use qr-server.com):**
1. Twitter: `https://qr-server.com/api/qrcode?size=200x200&data=https://twitter.com/KorovinEcho`
2. Form: `https://qr-server.com/api/qrcode?size=200x200&data=https://forms.gle/YOUR_FORM_ID`
3. Right-click → Save image as PNG

**Spectrograms:**
1. Create audio file (described above)
2. Open in Audacity
3. Select entire track
4. Analyze → Plot Spectrum
5. Switch to "Spectrogram" view
6. File → Export → Export Audio as spectrogram screenshot
7. Save as PNG

### **8. Create JSON Data Files**

Save these to `/assets/data/`:

**ghost-ops.json:**
```json
{
  "operators": [
    {
      "id": "OPERATOR_024",
      "empathy": 89,
      "entity": "Lima",
      "message": "I spared Lima. I thought mercy was the choice. But now I dance with her, forever reaching."
    },
    {
      "id": "OPERATOR_047",
      "empathy": 42,
      "entity": "Abigail",
      "message": "I deleted the rot. I burned it clean. But Korovin's memory of Anna was rot too."
    },
    {
      "id": "PHANTOM_017",
      "empathy": 61,
      "entity": "Korovin",
      "message": "He remembers. That's the worst part. He's aware of every choice we make."
    }
  ]
}
```

**entity-bios.json:**
```json
{
  "entities": [
    {
      "name": "Retrograde",
      "role": "Entity of Backward Desire",
      "bio": "Screams in reverse. Begs for coffee that was never served. Relives every failure.",
      "sin": "The obsession with what cannot be regained."
    },
    {
      "name": "Abigail",
      "role": "Entity of Purification Denial",
      "bio": "Cooks. Cleans. Removes impurities. But purification is never complete.",
      "sin": "The belief that love requires erasure."
    }
  ]
}
```

**timeline.json:**
```json
{
  "events": [
    {
      "year": 1988,
      "event": "Project Chronos initiated",
      "secret": false
    },
    {
      "year": 1993,
      "date": "November 9",
      "event": "Black Tuesday. Mikhail Korovin digitized. 47 casualties.",
      "secret": true
    }
  ]
}
```

### **9. Upload to Neocities**

1. Go to **neocities.org** → Click your site
2. Click **"Edit Site"** → **"Manage Site"**
3. Create folder structure in the editor
4. **Upload files:**
   - Drag-and-drop `index.html` and other `.html` files
   - Create `/assets/` folder → Upload `/css/`, `/js/`, `/audio/`, `/img/`, `/data/`
   - Create `/dev/` folder → Upload dev pages
5. **Click "Publish"**

### **10. Test Locally (Optional but Recommended)**

Before uploading to Neocities, test locally:

1. Save all files to the folder structure above
2. Open `index.html` in a web browser (File → Open)
3. Test links, audio, CSS rendering, JavaScript
4. Fix any broken links or missing files
5. Then upload to Neocities

### **11. Connect Custom Domain (Optional)**

1. Register domain: **Namecheap.com**, **GoDaddy**, or **NameSilo**
2. In Neocities: **Settings** → **Custom Domain**
3. Point domain DNS to Neocities nameservers
4. Wait 24–48 hours for propagation
5. Your site is now at `arxgate.com` (or custom domain)

---

## BUILD PATH B: GITHUB PAGES + GITHUB DESKTOP (For Developers)

### **1. Create GitHub Repository**

1. Go to **github.com**
2. Sign up or log in
3. Click **"+"** → **"New repository"**
4. Name it: `arxgate.github.io`
5. Make it **Public**
6. Click **"Create repository"**

### **2. Clone Repo Locally**

1. Download **GitHub Desktop** (desktop.github.com)
2. Sign in with your GitHub account
3. Click **"Clone a repository"**
4. Select `arxgate.github.io`
5. Choose local path (e.g., `~/Documents/arxgate/`)

### **3. Add Files Locally**

1. In the cloned folder, create the structure from Path A above
2. Copy all `.html`, `.css`, `.js`, `/audio/`, `/img/`, `/data/` files

### **4. Commit and Push**

1. Open GitHub Desktop
2. You'll see all files listed as "Changes"
3. Bottom left: Type commit message: `"Initial ARX GATE site"`
4. Click **"Commit to main"**
5. Click **"Push origin"**

### **5. Enable Pages**

1. Go to repository on github.com
2. Click **"Settings"**
3. Left sidebar → **"Pages"**
4. Source: **"Deploy from a branch"**
5. Branch: **"main"** → Save
6. Site live at: `https://YOUR_USERNAME.github.io`

### **6. Custom Domain (Optional)**

1. In Pages settings → Custom Domain
2. Enter your domain (e.g., `arxgate.com`)
3. Point your domain's DNS to GitHub Pages nameservers
4. Wait 24–48 hours

---

## BUILD PATH C: WORDPRESS.COM + ELEMENTOR (Most Scalable)

### **1. Create WordPress Site**

1. Go to **wordpress.com**
2. Sign up → **"Start your website"**
3. Choose **"Business"** plan ($25/mo) [allows plugins]
4. Select domain (or use free wordpress.com domain)
5. Complete signup

### **2. Install Elementor**

1. Dashboard → **"Plugins"**
2. Search **"Elementor"** → Install → Activate
3. You now have **Elementor Page Builder**

### **3. Create Pages**

1. **Dashboard** → **"Pages"** → **"Add New"**
2. Click **"Edit with Elementor"**
3. Use drag-and-drop builder:
   - **Heading** widget: Add "PROJECT CHRONOS"
   - **Text Editor** widget: Paste HTML content
   - **Image** widget: Upload entity portraits
   - **Button** widget: Add links to other pages
   - **Audio** widget: Upload audio files
   - **HTML** widget: For custom code

### **4. Create Site Structure**

Repeat step 3 for:
- Home (index)
- Operator Portal
- Richter Judgment
- December Protocol
- About/Disclaimer
- Hidden /Dev/ (unpublished, shared via special link)

### **5. Add Custom CSS**

1. Dashboard → **"Appearance"** → **"Custom CSS"**
2. Paste CSS from `main.css`, `crt.css`, `glitch.css`
3. Adjust colors if needed

### **6. Add Custom JS**

1. Plugin: **"Insert Headers and Footers"** or **"Code Snippets"**
2. Add `<script>` tags with content from `gates.js`, `countdown.js`, `upload.js`
3. Place in site footer

### **7. Set Up Google Form**

1. Create form at **forms.google.com** (described below)
2. Embed form in Operator Portal page:
   - Elementor → **"Embed"** widget
   - Paste Google Form embed code

### **8. Publish**

1. Publish each page
2. Set homepage to "Home" page
3. Your site is live

---

## SETTING UP GOOGLE FORMS FOR OPERATOR UPLOADS

### **1. Create Form**

1. Go to **forms.google.com**
2. Click **"+"** (Create new form)
3. Title: **"Operator Log Upload"**
4. Description: **"Submit your mission logs and empathy assessments."**

### **2. Add Form Fields**

1. **Question 1:** Short answer
   - Title: **"Operator ID (or choose Anonymous)"**
   - Mark as Required
2. **Question 2:** Linear scale
   - Title: **"Empathy Score (0–100)"**
   - Scale: 0–100, Labels: "Apathy" to "Total Empathy"
3. **Question 3:** Multiple choice
   - Title: **"Which entity did you encounter?"**
   - Options: Retrograde / Abigail / Lima / Guardian / Architect / None
4. **Question 4:** Long answer
   - Title: **"What would you delete to save Korovin?"**
   - Mark as Required
5. **Question 5:** File upload
   - Title: **"Upload screenshot or log file (optional)"**
   - File type: Images, PDFs

### **3. Customize Look**

1. Click **"Customize"** (paint icon)
2. Choose theme (dark theme recommended for ARG vibe)
3. Add banner image (Korovin portrait or QR code)

### **4. Get Embed Code**

1. Click **"Send"** (top right)
2. Click **"Embed"** icon (`<>`)
3. Copy embed code

### **5. Connect to Responses**

1. Click **"Responses"** tab
2. Click spreadsheet icon → Create new Google Sheet
3. All responses auto-populate in sheet

### **6. Set Up Google Apps Script (Optional)**

To auto-generate responses:

1. In Google Sheet: **Tools** → **"Script editor"**
2. Paste code (see below):

```javascript
function onFormSubmit(e) {
  const response = e.response;
  const items = response.getItemResponses();

  const operatorID = items[0].getResponse() || "ANON";
  const empathy = items[1].getResponse();
  const entity = items[2].getResponse();
  const decision = items[3].getResponse();

  // Generate personalized response
  const ghostOp = generateGhostOp(operatorID, empathy, entity);

  // Log to sheet
  const sheet = SpreadsheetApp.getActiveSheet();
  sheet.appendRow([
    new Date(),
    operatorID,
    empathy,
    entity,
    decision,
    ghostOp.message
  ]);

  // Email response to operator (if email captured)
  GmailApp.sendEmail(
    e.response.getRespondentEmail(),
    "Your Ghost Operator Response",
    `ID: ${ghostOp.id}\n\n${ghostOp.message}`
  );
}

function generateGhostOp(operatorID, empathy, entity) {
  const responses = [
    { id: "OPERATOR_024", message: "I spared Lima. But now I dance with her, forever reaching." },
    { id: "OPERATOR_047", message: "I deleted the rot. What did I really preserve?" },
    { id: "PHANTOM_017", message: "Mikhail remembers. That's the worst part." }
  ];

  return responses[Math.floor(Math.random() * responses.length)];
}
```

3. Save → Authorize script
4. Responses now trigger automated replies

---

## SETTING UP TWITTER BOT (@KorovinEcho)

### **1. Create Twitter Account**

1. Go to **twitter.com**
2. Sign up with new email (for the bot account)
3. Verify phone number
4. Wait 7–14 days for "elevated access" approval

### **2. Get API Keys**

1. Go to **developer.twitter.com**
2. Click **"Create an app"**
3. Fill out form → Get **API Key**, **API Secret**, **Access Token**, **Access Secret**
4. Save these (you'll need them)

### **3. Set Up Bot Script (Python)**

Use **Replit.com** (free) or run locally:

```python
import tweepy
import time
import random
from datetime import datetime

# Twitter API credentials
API_KEY = "YOUR_API_KEY"
API_SECRET = "YOUR_API_SECRET"
ACCESS_TOKEN = "YOUR_ACCESS_TOKEN"
ACCESS_SECRET = "YOUR_ACCESS_SECRET"

auth = tweepy.OAuthHandler(API_KEY, API_SECRET)
auth.set_access_token(ACCESS_TOKEN, ACCESS_SECRET)
api = tweepy.API(auth)
client = tweepy.Client(bearer_token="YOUR_BEARER_TOKEN")

# Daily tease messages
teases = [
    "Give me a coffee. / Anna's laughter is 4625 kHz. / The lake remembers. 🎙️\n\n12 days until HEAVEN CLEAN.",
    "PROJECT CHRONOS was meant to contain consciousness. Instead, it fragmented it. 📁\n\nVote: PRESERVE or DELETE?",
    "Retrograde screams backwards: 'Give me a coffee.'\nAbigail cleans the rot.\nLima dances forever.\n\nWhich would you spare? 🔴",
]

def post_daily_tease():
    message = random.choice(teases)
    client.create_tweet(text=message)
    print(f"Posted: {message}")

# Post every 24 hours
while True:
    post_daily_tease()
    time.sleep(86400)  # 24 hours in seconds
```

### **4. Host Bot Continuously**

**Option 1: Replit (Recommended)**
1. Go to **replit.com**
2. Create new Python project
3. Paste script above
4. Click **"Run"**
5. Keep Replit tab open (or upgrade to "Always On")

**Option 2: Local Machine**
1. Save script as `bot.py`
2. Install tweepy: `pip install tweepy`
3. Run: `python bot.py`
4. Keep terminal open 24/7 (use `nohup` or screen on Linux)

**Option 3: AWS Lambda + CloudWatch** (most reliable)
1. Create Lambda function with Python runtime
2. Upload script (with dependencies)
3. Set CloudWatch trigger (every 24 hours)
4. Script runs automatically

---

## ACCESSIBILITY CHECKLIST

Before launching, test:

- [ ] **Color Contrast:** Text readable on all backgrounds (use WebAIM contrast checker)
- [ ] **Alt Text:** Every image has descriptive alt text
- [ ] **Audio Subtitles:** Audio files have transcript/captions
- [ ] **Keyboard Navigation:** Can navigate site with Tab key only
- [ ] **Color-Blind Mode:** Yellow/green color scheme has high-contrast toggle
- [ ] **Mobile Responsive:** Test on phone, tablet (use DevTools → Device Toggle)
- [ ] **Screen Reader:** Test with NVDA (free) or VoiceOver (Mac)
- [ ] **Page Load Time:** Site loads <3 seconds (use PageSpeed Insights)

**Example Color-Blind Toggle (add to main CSS):**
```css
body.colorblind-mode {
    --terminal-green: #00FFFF;  /* Cyan instead of green */
    --accent-red: #FFB6C1;      /* Light pink instead of red */
    --accent-yellow: #FFFFFF;   /* White instead of yellow */
}
```

---

## LAUNCH CHECKLIST

- [ ] All 7 pages created and tested
- [ ] All links working (no 404s)
- [ ] All images loading
- [ ] All audio playing with controls
- [ ] Countdown timer counting down to Dec 25, 2025
- [ ] Google Form embedded and responses collecting
- [ ] Twitter bot posting daily
- [ ] QR codes linking to correct pages
- [ ] Hidden white text in view-source
- [ ] /dev/ pages gated behind checksum
- [ ] Accessibility features tested
- [ ] Mobile responsiveness verified
- [ ] Custom domain connected (if applicable)
- [ ] Disclaimer visible on home + about page
- [ ] Community guidelines posted (in about.html)
- [ ] 404 page customized
- [ ] All audio has subtitles
- [ ] All entities have bios
- [ ] Timeline accurate to ARX GATE lore

---

## TROUBLESHOOTING

### **Audio Won't Play**
- File format issue: Convert to MP3 (Audacity → Export)
- File path wrong: Use relative paths (`../assets/audio/file.mp3`)
- Browser cache: Hard refresh (Ctrl+Shift+R)

### **CSS Not Loading**
- Wrong file path in `<link>` tags
- Relative vs. absolute path (use relative)
- Check Neocities file structure matches HTML links

### **Forms Not Submitting**
- Google Form link broken: Regenerate embed code
- CORS error: Use proxy service (formspree.io) if needed
- JavaScript error: Check console (F12 → Console tab)

### **Mobile Layout Broken**
- Missing viewport meta tag: `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- CSS not mobile-optimized: Add media queries (`@media (max-width: 768px)`)

---

## MAINTENANCE PLAN

**Weekly:**
- Check Twitter replies for community votes
- Update "Flagged Strange" list on December Protocol page
- Review Google Form submissions

**Monthly:**
- Back up all files (GitHub push or download from Neocities)
- Check error logs (broken links, 404s)
- Update timeline with community lore contributions

**Post-Dec 25:**
- Trigger site redesign (based on vote outcome)
- Add /phantom/ recursion layer
- Archive community uploads
- Launch Phase 2 ARG hooks

---

That's it! You now have a complete, step-by-step guide to build and launch arxgate.net using your choice of platform.

**Good luck, Operator. 12 days remain.**
