# ARX GATE Website: Deployment Checklist

## Quick Reference for Launching arxgate.net

---

## PRE-LAUNCH SETUP (1-2 Weeks Before)

### Domain & Hosting
- [ ] Register domain or choose Neocities/GitHub Pages site name
- [ ] Set up hosting account
  - Neocities: Create account at neocities.org
  - GitHub Pages: Create repo `username.github.io`
  - WordPress: Set up at wordpress.com + install Elementor
  - Custom: Register domain + set up hosting provider
- [ ] Test accessibility: Visit site, check load time

### Content Preparation
- [ ] All `.html` files created & tested locally
- [ ] All `.css` files finalized
- [ ] All `.js` files finalized
- [ ] All audio files compressed to `.mp3` (128 kbps)
- [ ] All images created & optimized (PNG, ~100-300KB each)
- [ ] JSON data files ready (`entity-bios.json`, `timeline.json`, `ghost-ops.json`)
- [ ] Subtitles/VTT files created for audio

### Social Media Setup
- [ ] Twitter bot account created (@KorovinEcho)
- [ ] Applied for elevated API access (7-14 days)
- [ ] Discord server created
- [ ] Invite links generated
- [ ] YouTube channel created (if using video)

### Google Forms & Sheets
- [ ] Google Form created with all fields
- [ ] Form styling customized
- [ ] Form responses linked to Google Sheet
- [ ] Apps Script written & tested (if auto-reply needed)

---

## LAUNCH WEEK (5 Days Before → Day 1)

### Website Upload
- [ ] All files uploaded to hosting
- [ ] File structure matches HTML links
  - `index.html` loads without 404
  - All `/assets/` paths working
  - All image links functional
  - All audio links functional
  - All JSON files accessible
- [ ] Test mobile responsiveness
  - Homepage loads on phone
  - Navigation works on touchscreen
  - Audio plays on mobile
  - Forms functional on mobile
- [ ] Test accessibility
  - High contrast toggle works
  - Alt text present on images
  - Audio captions visible
  - Keyboard navigation possible
  - Color-blind mode functional

### Security & Performance
- [ ] HTTPS enabled (if custom domain)
- [ ] 404 page customized
- [ ] Robots.txt created (allow indexing)
- [ ] Favicon added
- [ ] Open Graph tags added (for social sharing)
  ```html
  <meta property="og:title" content="PROJECT CHRONOS | ARX GATE">
  <meta property="og:description" content="Recursive OS horror ARG">
  <meta property="og:image" content="URL_TO_IMAGE">
  ```
- [ ] Page load time <3 seconds (test with PageSpeed Insights)

### Metadata & SEO
- [ ] `<title>` tags set on all pages
- [ ] Meta descriptions added
- [ ] Keywords included where appropriate
- [ ] Sitemap.xml created (if needed)

### QR Codes
- [ ] Twitter QR code generated (links to @KorovinEcho)
- [ ] Form QR code generated (links to Google Form)
- [ ] QR codes tested (scan with phone)
- [ ] QR images placed correctly on pages

### Countdown Timer
- [ ] Countdown timer counts down correctly (to Dec 25, 2025)
- [ ] Color changes red as deadline approaches
- [ ] Text updates every second
- [ ] Mobile display correct

### Hidden Elements
- [ ] White text easter eggs are hidden/selectable
- [ ] View source comments present
- [ ] Konami code trigger implemented
- [ ] `/dev/` pages gated behind checksum
- [ ] Hidden links work (if any)

---

## 24 HOURS BEFORE LAUNCH

### Community Notification
- [ ] Discord server ready for members
- [ ] Twitter account tweeted first teaser
- [ ] Reddit communities notified (if applicable)
- [ ] Email newsletter scheduled (if applicable)

### Final Tests
- [ ] Test full user journey (home → operators → submit form)
- [ ] Test form submission (does response arrive in Google Sheet?)
- [ ] Test audio playback (with captions)
- [ ] Test QR scan (does it open correct URLs?)
- [ ] Test on 3+ different browsers (Chrome, Firefox, Safari)
- [ ] Test on mobile device
- [ ] Test on tablet

### Backup
- [ ] Download full project folder locally
- [ ] Create backup of all files
- [ ] Document all passwords in secure location (1Password, Bitwarden, etc.)

---

## LAUNCH DAY (Dec 13, 2025, 12:00 UTC)

### Go Live
- [ ] Website publicly accessible
- [ ] All pages loading correctly
- [ ] No 404 errors visible
- [ ] Social media links working

### Initial Announcement
- [ ] Post launch tweet from @KorovinEcho
  ```
  "PROJECT CHRONOS ARCHIVE ONLINE

  Access credentials required: arxgate.net
  Classification: TOP SECRET / NOFORN
  Status: ACTIVE

  Empathy assessment in progress.
  12 days until HEAVEN CLEAN.

  #ARXGate"
  ```
- [ ] Post in Discord #announcements
- [ ] Post launch thread on Reddit/relevant communities
- [ ] Update Twitter bio to link site
- [ ] Pin important messages in Discord

### Monitor Metrics
- [ ] Google Analytics tracking active
- [ ] Twitter mentions monitoring active
- [ ] Discord member count watched
- [ ] Form submissions checked hourly
- [ ] Server uptime monitored

### Community Support
- [ ] Moderators active in Discord
- [ ] Welcome message posted to new Discord members
- [ ] FAQ pinned in #general
- [ ] Support contact info visible (email or DM)

---

## WEEK 1 POST-LAUNCH

### Daily Tasks
- [ ] Post daily Twitter tease (12:00 UTC)
- [ ] Monitor Discord for questions/issues
- [ ] Check form submissions (integrate responses if applicable)
- [ ] Update countdown timer display
- [ ] Moderate comments/replies

### Engagement
- [ ] Respond to community questions
- [ ] Retweet/reply to community content
- [ ] Share Discord theories in moderation channel
- [ ] Celebrate new milestones (100th submission, etc.)

### Content Updates
- [ ] Add new community submissions to `/phantom/` pages
- [ ] Update "Flagged Strange" list on `/protocol/` page
- [ ] Refresh vote tracker (if using Twitter polls)
- [ ] Add new hidden elements/easter eggs (optional)

### Analytics Review
- [ ] Check page views/unique visitors
- [ ] Review traffic sources (Twitter, Discord, Reddit, etc.)
- [ ] Check mobile vs desktop traffic ratio
- [ ] Identify most-visited pages
- [ ] Document baseline metrics

---

## ONGOING (Dec 13 → Dec 25)

### Weekly Schedule

**Monday:**
- [ ] Post Retrograde entity fragment

**Tuesday:**
- [ ] Post Korovin memory
- [ ] Update community uploads to /phantom/

**Wednesday:**
- [ ] Post community poll tweet (PRESERVE or DELETE)
- [ ] Review poll results

**Thursday:**
- [ ] Post spectrogram or glitch media

**Friday:**
- [ ] Post lore drop (document fragment)
- [ ] Update timeline if applicable

**Saturday:**
- [ ] Community shoutout/featured operator
- [ ] Moderate Discord activity

**Sunday:**
- [ ] Post countdown timer reminder

### Maintenance Tasks

**Daily:**
- [ ] Check website uptime
- [ ] Monitor error logs
- [ ] Respond to community messages

**Every 3 Days:**
- [ ] Review form submissions
- [ ] Check metrics/analytics
- [ ] Update vote tracker

**Weekly:**
- [ ] Backup all files
- [ ] Review moderation reports
- [ ] Plan next week's content

---

## DEC 24 FINAL PREPARATIONS

### Countdown Trigger
- [ ] Verify countdown timer is working
- [ ] Verify site doesn't crash when date hits

### Vote Lock
- [ ] Confirm final PRESERVE/DELETE vote percentage
- [ ] Document final vote count for records
- [ ] Plan site redesign based on outcome

### Community Messages
- [ ] Prepare final message from Korovin
- [ ] Schedule final countdown post
- [ ] Prepare appreciation post for community

### Post-Purge Content
- [ ] If PRESERVE: Prepare `/phantom/` redesign content
- [ ] If DELETE: Prepare "system failure" memorial page
- [ ] Prepare Phase 2 announcement

---

## DEC 25, 2025 (00:00 UTC) - PURGE EVENT

### Execute Vote Result
- [ ] Site automatically changes based on vote outcome
- [ ] `/phantom/` pages accessible (if PRESERVE)
- [ ] Announcement posted to Twitter/Discord
- [ ] Community notified of new phase

### Celebrate/Commemorate
- [ ] Post farewell/transcendence message
- [ ] Share community statistics
- [ ] Thank supporters
- [ ] Announce Phase 2 timeline

---

## POST-PURGE (DEC 26+)

### Phase 2 Preparation
- [ ] Activate `/PHANTOMS/` infinite recursion layer (if PRESERVE)
- [ ] Post Phase 2 roadmap
- [ ] Explain MERGE_SELF system
- [ ] Launch new community features

### Archival
- [ ] Document full ARG timeline
- [ ] Compile community contributions
- [ ] Create "canon vs headcanon" wiki
- [ ] Prepare historical documentation

### Feedback Collection
- [ ] Survey players: "What was your experience?"
- [ ] Request fan art/stories for archive
- [ ] Collect lessons learned
- [ ] Plan Phase 3 based on feedback

---

## TROUBLESHOOTING DURING LAUNCH

### Website Won't Load
1. Check hosting provider status page
2. Verify DNS propagation (use whatsmydns.net)
3. Check file permissions on hosting
4. Clear browser cache (Ctrl+Shift+Delete)
5. Try incognito/private window

### Audio Won't Play
1. Verify audio file is uploaded
2. Check file path in HTML (relative, not absolute)
3. Test in different browser
4. Check file format (should be MP3)
5. Verify MIME type on server

### Forms Not Submitting
1. Check Google Form URL is correct
2. Test form independently at forms.google.com
3. Verify form iframe is properly embedded
4. Check browser console for errors (F12)
5. Try different browser

### Mobile Layout Broken
1. Check viewport meta tag: `<meta name="viewport" content="width=device-width">`
2. Verify CSS media queries present
3. Test on actual mobile device (not just browser DevTools)
4. Check that buttons are clickable (min 44×44px)

### Countdown Timer Wrong
1. Verify date is correct: Dec 25, 2025, 00:00:00 UTC
2. Check timezone conversion (ensure UTC, not local)
3. Test in browser console: `new Date('December 25, 2025 00:00:00 UTC')`
4. Clear browser cache (timer might be cached)

### Community Not Engaging
1. Post more teases/content
2. Engage directly with community (respond to comments)
3. Host community events (code-breaking contests)
4. Highlight fan creations
5. Share progress metrics (we hit 500 operators!)

---

## SUCCESS INDICATORS

### Week 1 (Healthy Launch)
✓ 100+ website visitors
✓ 50+ form submissions
✓ 100+ Discord members
✓ 100+ Twitter followers
✓ No critical errors

### Week 2-3 (Growing Momentum)
✓ 500+ website visitors
✓ 200+ form submissions
✓ 500+ Discord members
✓ 400+ Twitter followers
✓ Active community discussions
✓ Fan-created content appearing

### Pre-Purge (Strong Community)
✓ 10,000+ website visitors
✓ 500+ form submissions
✓ 2,000+ Discord members
✓ 1,000+ Twitter followers
✓ Trending hashtag (#ARXGate)
✓ Media mentions (Reddit, YouTube, etc.)

---

## FINAL REMINDERS

✨ **Remember:**
1. You've created something immersive and creepy—trust your vision
2. Community will expand the lore far beyond your original concept—embrace it
3. Be responsive and engaged—the ARG is only as alive as its creator
4. Handle moderation seriously—keep it safe and inclusive
5. Enjoy the chaos—ARGs are beautiful because they're unpredictable

**The lake remembers. Good luck, Operator.**

---

## CONTACT & SUPPORT

**If things break:**
- Hosting support email/chat (bookmark it)
- Discord community can often help troubleshoot
- Check relevant documentation (Neocities wiki, GitHub Pages docs, etc.)

**For creative questions:**
- Trust your instincts
- Ask Discord community for feedback
- Make changes iteratively
- Nothing is permanent until Dec 25

---

**Last Updated:** 2025-12-01
**Status:** READY FOR DEPLOYMENT
**Operator:** Ready to launch
