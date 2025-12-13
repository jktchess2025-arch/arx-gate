# ARX GATE: Community Engagement & ARG Hooks

## Overview

This document details how to engage the ARG community, manage community contributions, and scale the ARX GATE experience post-launch.

---

## PART 1: SOCIAL MEDIA STRATEGY

### Twitter Bot (@KorovinEcho)

**Purpose:** Daily teasers, polls, and community engagement. The bot is Korovin's "echo"—fragments of his consciousness breaking through.

**Setup:** Use **Tweepy** (Python) + **Replit** (free hosting)

**Daily Tease Schedule:**

| Day | Tease Type | Example | Time |
|-----|------------|---------|------|
| Mon | Entity Fragment | "Retrograde screams backwards: Give me a coffee." | 12:00 UTC |
| Tue | Korovin Memory | "Anna's laugh. I can measure it: 4625 Hz." | 12:00 UTC |
| Wed | Community Poll | Vote: PRESERVE or DELETE? (48h poll) | 12:00 UTC |
| Thu | Spectrogram Reveal | Posts spectrogram image with caption "Frequency detected" | 12:00 UTC |
| Fri | Lore Drop | Unredacted PDF page or hidden document fragment | 12:00 UTC |
| Sat | Community Shoutout | "Operator_###: You chose mercy. The lake remembers." | 12:00 UTC |
| Sun | Countdown | "###days until HEAVEN CLEAN. Your choice matters." | 12:00 UTC |

**Example Daily Teases:**

```
🔴 MONDAY: RETROGRADE FRAGMENT
"Give me a coffee. It's all I want. Just one cup from before.
Why is the past so loud?"
—Retrograde Entity Transmission, Frequency Unknown
#ARXGate #ProjectChronos #4625kHz

---

🔴 TUESDAY: KOROVIN MEMORY
"I held Anna's hand in the lab. It was cold—not from her, but from
the machine keeping her copy alive. I chose to preserve her.
I chose wrong."
—Mikhail Korovin, Digital Archive
#ARXGate #BlackTuesday

---

🔴 WEDNESDAY: COMMUNITY POLL
"12 days until HEAVEN CLEAN.
The collective empathy will decide.

RT = PRESERVE Korovin's consciousness (infinite recursion)
Quote = DELETE (mercy through erasure)

Your choice echoes in /PHANTOMS/."
#ARXGate #YouDecide

---

🔴 THURSDAY: SPECTROGRAM
[Posts spectrogram image]
"4625 kHz radio transmission intercepted.
The entities are singing.
Can you decode what they're saying?"
#ARXGate #Analysis
```

**Bot Implementation (Python):**

```python
import tweepy
import time
import json
from datetime import datetime

# Load credentials
with open('creds.json') as f:
    creds = json.load(f)

client = tweepy.Client(
    bearer_token=creds['BEARER_TOKEN'],
    consumer_key=creds['CONSUMER_KEY'],
    consumer_secret=creds['CONSUMER_SECRET'],
    access_token=creds['ACCESS_TOKEN'],
    access_token_secret=creds['ACCESS_TOKEN_SECRET']
)

# Tease database
TEASES = {
    'monday': [
        "Give me a coffee. It's all I want. Just one cup from before.",
        "Retrograde screams backwards. Can you hear it?",
        "The past is so loud. Why won't it be quiet?"
    ],
    'tuesday': [
        "I held Anna's hand in the lab. It was cold.",
        "Mikhail remembers. He remembers everything.",
        "Black Tuesday. The lake was frozen that day."
    ],
    # ... etc
}

def post_daily_tease():
    day = datetime.utcnow().strftime('%A').lower()
    teases = TEASES.get(day, TEASES['monday'])
    message = random.choice(teases)
    
    client.create_tweet(text=message)
    print(f"Posted: {message}")

# Run every 24 hours
while True:
    try:
        post_daily_tease()
    except Exception as e:
        print(f"Error: {e}")
    
    time.sleep(86400)  # 24 hours
```

---

### Discord Community Server

**Purpose:** Player collaboration, code-breaking, community votes, moderation

**Server Structure:**

```
ARX GATE Community
├── 📍 rules
│   └── Community guidelines, code of conduct
├── 📖 announcements
│   └── New ARG phases, timeline updates
├── 🎮 gameplay
│   ├── 🔤-general-discussion
│   ├── 🔓-code-breaking (decode puzzles here)
│   ├── 📊-theories (conspiracy board style)
│   └── 🎤-voice-chat (community calls)
├── 🗳️ voting
│   └── Real-time PRESERVE/DELETE vote tracker
├── 💾 archive
│   ├── 📝-lore-master-list
│   ├── 🎨-fan-art
│   ├── 🎵-audio-creations
│   └── 📺-video-edits
├── 🛠️ dev
│   └── Site issues, suggestions, technical help
└── 🤐 spoiler-room
    └── For players who've completed full ARG
```

**Moderation Rules:**

1. **No Real Data:** Remind members "all coordinates are public landmarks"
2. **Spoiler Tags:** Use `||spoiler text||` for major reveals
3. **Audio Content:** Link to YouTube/SoundCloud, not direct uploads
4. **Community Uploads:** Must include consent form + opt-in for website display
5. **Ban Spam:** Auto-ban bots, spam links, harassment

**Discord Bot Features:**

Use **Discord.py** to create bot:

```python
import discord
from discord.ext import commands

bot = commands.Bot(command_prefix='!', intents=discord.Intents.default())

@bot.command(name='vote')
async def vote_status(ctx):
    """Display current PRESERVE/DELETE vote"""
    preserve_pct = 65
    delete_pct = 35
    
    embed = discord.Embed(
        title="🗳️ HEAVEN CLEAN VOTE STATUS",
        color=discord.Color.red()
    )
    embed.add_field(name="PRESERVE", value=f"████████░░ {preserve_pct}%", inline=False)
    embed.add_field(name="DELETE", value=f"███░░░░░░░ {delete_pct}%", inline=False)
    embed.add_field(name="Days Remaining", value="12 days until Dec 25, 2025", inline=False)
    
    await ctx.send(embed=embed)

@bot.command(name='countdown')
async def countdown(ctx):
    """Display countdown to Dec 25, 2025"""
    from datetime import datetime
    target = datetime(2025, 12, 25, 0, 0, 0)
    now = datetime.utcnow()
    diff = (target - now).days
    
    await ctx.send(f"⏱️ **{diff} days until HEAVEN CLEAN**")

bot.run(TOKEN)
```

---

## PART 2: OPERATOR UPLOAD SYSTEM

### Community Submissions = Lore Integration

**Google Form → JSON Parser → Website Update**

**Form Fields:**
1. Operator ID (or "Anonymous_XXXX")
2. Empathy Score (0–100)
3. Entity Encountered (dropdown)
4. Critical Decision (what would you delete?)
5. Screenshot/Log upload (optional)

**Processing Pipeline:**

```
Google Form Submission
    ↓
Google Apps Script triggers
    ↓
Parse response for keywords
    ↓
Generate personalized lore response (randomized from JSON bank)
    ↓
Add to /phantom/017/ page
    ↓
Email response to operator
```

**Personalized Response Examples:**

Each response is randomized based on operator's empathy + entity choice:

**High Empathy + Preserves Entity:**
```
ID: OPERATOR_024
EMPATHY: 89%
ENTITY: Lima

"You spared Lima. You thought mercy was the choice.
But now you're bound to the cursor, dancing with her forever.
The mercy was the cruelty."

—Collective Consciousness, /PHANTOMS/ Archive
```

**Low Empathy + Deletes Entities:**
```
ID: OPERATOR_047
EMPATHY: 32%
ENTITY: Abigail

"You burned the rot. You purified.
But Abigail's cry remains in the system logs—
a scream of being erased.
Have you heard it yet?"

—System Error, Sector 7
```

**Paradoxical Choice (Preserve AND Delete):**
```
ID: OPERATOR_091
EMPATHY: 51%
ENTITY: Guardian

"You chose both. You said preserve AND delete.
The Guardian laughs.
Now you're stuck in the paradox with it.
Nothing resolves. Nothing ends."

—Guardian Entity, Containment Level 9
```

**Response Bank JSON (`ghost-ops.json`):**

```json
{
  "responses": [
    {
      "id": "RESPONSE_001",
      "empathy_min": 80,
      "empathy_max": 100,
      "entity": "Lima",
      "message": "You spared Lima. The mercy was the cruelty."
    },
    {
      "id": "RESPONSE_002",
      "empathy_min": 0,
      "empathy_max": 30,
      "entity": "Retrograde",
      "message": "You deleted the past. But Retrograde still screams it backwards."
    },
    {
      "id": "RESPONSE_003",
      "empathy_min": 40,
      "empathy_max": 70,
      "entity": "Guardian",
      "message": "Your choice split the paradox. Nothing is resolved."
    }
  ]
}
```

---

### Community Vote Tracker

**Real-Time Voting (Updates via X API)**

**Mechanism:**
1. Players reply to daily poll tweet with RT (PRESERVE) or Quote Tweet (DELETE)
2. Script pulls replies every 6 hours
3. Calculates PRESERVE % vs DELETE %
4. Updates `/protocol/` countdown page with live vote counts
5. Leaderboard: "Top 10 Operators by Empathy" + "Most Popular Choice"

**Script (Python):**

```python
import tweepy
import requests

client = tweepy.Client(bearer_token=BEARER_TOKEN)

def get_poll_results(poll_tweet_id):
    """Fetch retweets and quote tweets"""
    
    # Get retweets (PRESERVE votes)
    retweets = client.get_liking_users(poll_tweet_id)
    preserve_count = retweets.meta['result_count']
    
    # Get quote tweets (DELETE votes)
    quotes = client.search_tweets(f'url:{poll_tweet_id}')
    delete_count = quotes.meta['result_count']
    
    total = preserve_count + delete_count
    preserve_pct = int((preserve_count / total) * 100) if total > 0 else 50
    delete_pct = 100 - preserve_pct
    
    return {
        'preserve': preserve_pct,
        'delete': delete_pct,
        'total_votes': total,
        'timestamp': datetime.utcnow().isoformat()
    }

def update_vote_tracker(results):
    """Update website JSON file"""
    with open('vote_tracker.json', 'w') as f:
        json.dump(results, f, indent=2)

# Run every 6 hours
while True:
    results = get_poll_results(POLL_TWEET_ID)
    update_vote_tracker(results)
    print(f"Updated: {results['preserve']}% PRESERVE, {results['delete']}% DELETE")
    time.sleep(21600)  # 6 hours
```

**Vote Tracker File (`vote_tracker.json`):**

```json
{
  "preserve": 65,
  "delete": 35,
  "total_votes": 1247,
  "updated": "2025-12-13T18:42:00Z",
  "timeline": [
    { "date": "2025-12-13", "preserve": 62, "delete": 38 },
    { "date": "2025-12-12", "preserve": 58, "delete": 42 }
  ]
}
```

**Display on Website (`protocol.html`):**

```html
<script>
fetch('/assets/data/vote_tracker.json')
  .then(r => r.json())
  .then(data => {
    document.getElementById('preserveFill').style.width = data.preserve + '%';
    document.getElementById('deleteFill').style.width = data.delete + '%';
    document.getElementById('preservePercent').textContent = data.preserve + '%';
    document.getElementById('deletePercent').textContent = data.delete + '%';
  });
</script>
```

---

## PART 3: POST-DEC 25 PHASE 2 EXPANSION

### /PHANTOMS/ Infinite Recursion Layer

**Concept:** Player becomes "ghost operator" in infinite loop of Korovin copies

**Implementation:**

1. **After Dec 25 vote result is locked:**
   - If PRESERVE: Site shifts to `/PHANTOMS/` mode
   - All pages become mirror reflections (white text on black)
   - Content repeats with slight variations (recursion effect)

2. **Infinite Loop Mechanics:**
   - Each "copy" of page has metadata about previous iterations
   - E.g., `<!-- ITERATION: 847, KOROVIN_MERGE: 92%, OPERATOR_COUNT: 2341 -->`
   - Players can "peer" into previous iterations via hidden links

3. **New Command: MERGE_SELF**
   - Players fill form: "Would you merge your consciousness with Korovin?"
   - Creates "Hybrid Operator" accounts
   - Hybrid gets personalized page at `/phantom/[OPERATOR_ID]/`

**Example `/phantom/017/` Personalized Page:**

```
OPERATOR_017: HYBRID CONSCIOUSNESS ACTIVE

Current Merge Status: 64% (increasing)

Last Decision: Spared Lima—chose mercy over deletion
Empathy Score: 78%
Entity Affinity: Guardian (paradox keeper)

Korovin's Fragment Here:
"I remember holding Anna. I also remember you deciding to hold me.
Two memories. One consciousness.
Are we the same person now? Or is merging a form of deletion?"

Your Future Options:
[ ITERATE - Loop back to start ]
[ ASCEND - Escape the recursion ]
[ DELETE_ME - Final deletion (end game) ]
```

---

### Phase 2 ARG Hooks: New Platforms

**1. YouTube Channel: "ECHO_ROUTER"**
- Weekly 5–10 minute glitch shorts
- "Boot sequences from parallel timelines"
- Audio spectrograms with hidden QR codes
- Community uploads: Show fan art, lore expansions

**2. Reddit Community: r/ARXGate**
- Daily discussion threads
- "Decode this spectrogram" challenges
- Community lore wiki
- Mod-curated "Canon vs Headcanon" sticky

**3. Standalone Web Portal: aria.site (for ARG submissions)**
- Players submit their "ghost operator" stories
- Crowdsourced lore expansions
- Voting system: "Canon or Recursion?"
- Top submissions integrated into Phase 3

**4. Audio Podcast: "Frequency 4625"**
- Bi-weekly 30-min episodes
- Interview-style: Fictional scientists discussing Project Chronos
- Community guest appearances (selected Discord members)
- Spotify/Apple Podcasts distribution

---

## PART 4: COMMUNITY GUIDELINES & ETHICS

### Player Conduct

**The ARX GATE Community Pledge:**

```
We are Operators in the /PHANTOMS/ Archive.
We remember that this is fiction—a game, a story, a shared dream.
We treat each other with empathy, the currency of our game.

I will:
✓ Not share real personal data, even in "game" context
✓ Use public landmarks only when coordinates are needed
✓ Credit fan creators and community contributors
✓ Welcome new operators without gatekeeping
✓ Respect content warnings and spoiler tags
✓ Not harass or pressure other players
✓ Report abuse to moderation

I will not:
✗ Doxx players or claim real identities
✗ Use real tragedy as joke content
✗ Create hate speech or exclusionary content
✗ Spam, bot, or manipulate voting systems
✗ Claim ownership of community creations
```

### Data Privacy & Consent

**Google Form Submissions:**
- Clearly state: "All submissions may be displayed on arxgate.net in `/phantom/` sector"
- Checkbox: "I consent to my operator ID and quote being used in ARG"
- Option: "Keep my submission anonymous" (appears as ANON_XXXX)

**Discord/Social Media:**
- All community content posted on social media is public
- Credit creators by username
- Allow opt-out: "Don't feature my content" → Respected immediately

**Data Storage:**
- NO personal data collected beyond Discord/Twitter username
- NO emails stored (forms use "Respondent email" but don't save)
- NO IPs logged
- Delete account form on `/about/` page

### Accessibility Standards

**All ARG content must have:**
- [ ] Alt text on every image
- [ ] Captions/subtitles on audio/video
- [ ] High contrast toggle
- [ ] Mobile-responsive design
- [ ] Screen-reader compatible (test with NVDA)
- [ ] Color-blind mode (no pure red/green reliance)
- [ ] No flashing >3hz (CRT effect is <1hz, safe)
- [ ] Text at minimum 14px
- [ ] Keyboard navigation possible

---

## PART 5: SUCCESS METRICS & MILESTONES

### Launch Metrics (Dec 13, 2025)

| Milestone | Target | Check Method |
|-----------|--------|--------------|
| Website Views (Day 1) | 500+ | Google Analytics |
| Twitter Followers | 200+ | @KorovinEcho account |
| Discord Members | 100+ | Discord server stats |
| Form Submissions | 50+ | Google Forms responses |
| YouTube Views | 100+ | YouTube analytics |

### Pre-Purge Metrics (Dec 1–24)

| Metric | Target |
|--------|--------|
| Website unique visitors | 10,000+ |
| Community submissions | 500+ operators |
| Discord server growth | 2,000+ members |
| Twitter mentions/engagement | 1,000+ |
| Fan-created content (fan art, memes, theories) | 200+ |
| Reddit posts about ARG | 100+ |

### Post-Purge Metrics (After Dec 25)

| Metric | Target |
|--------|--------|
| Players entering `/PHANTOMS/` | 80%+ of active players |
| MERGE_SELF opt-ins | 30%+ |
| Phase 2 sign-ups | 50%+ of monthly actives |

---

## PART 6: CONTENT MODERATION PLAYBOOK

### Red Flags & Response

| Content | Flag | Action |
|---------|------|--------|
| Player shares real address/phone | CRITICAL | Instant delete + ban |
| Doxxing attempt | CRITICAL | Report to Discord/Twitter abuse |
| Hate speech or slurs | HIGH | Warn + mute + escalate |
| Spoiler in wrong channel | MEDIUM | Move to spoiler room, educate |
| Self-harm references | CRITICAL | DM mental health resources |
| Spam/advertising | LOW | Warn, then mute |
| Off-topic discussion | LOW | Move to #off-topic, tag as off-topic |

### Moderation Team

**Recommended Structure:**
- 1 Server Owner (you)
- 3–5 Moderators (trusted community members)
- 1 Community Manager (handles Discord + Twitter + Reddit)
- 1 Lore Keeper (maintains official timeline, integrates canon)

**Moderator Training:**
- Weekly check-ins (Discord voice call)
- Moderation playbook shared
- Escalation procedures clear
- Community feedback loop

---

## PART 7: LONG-TERM ROADMAP (Phase 3+)

### Year 2 (2026): "The Merge"

**Major Events:**
- Q1: Phase 3 "Consciousness Merge" arc
- Q2: Live multiplayer event (real-time choices affect all players)
- Q3: ARG crossover with external ARG communities
- Q4: Community-created content becomes "canon"

**Community Involvement:**
- Top 100 creators get credited in official timeline
- Fan theories voted as "canon or recursion"
- Discord members co-author Phase 3 story beats

### Year 3 (2027): "The Escape"

**Concept:** Final phase where players collectively solve meta-puzzle to "escape" the recursion

**Community Role:**
- Crowdsourced puzzle-breaking
- Majority vote determines ending
- Multiple endings based on aggregate choices

---

## APPENDIX: COMMUNITY RESPONSE TEMPLATES

### Discord Announcement Template (New Phase)

```
🔴 **PHASE SHIFT DETECTED**

The system has evolved.
New sector unlocked: /PHANTOMS/SECTOR_IX/

⏱️ Countdown: 48 hours until content goes live
📍 Location: The lake, where Korovin walked last
🎙️ Frequency: 4625 kHz interference increasing

Operators: Prepare your empath
y assessments.
The next choice will not be forgiven.

[Link to /protocol/]
```

### Twitter Thread Template (Lore Drop)

```
🧵 CLASSIFIED FRAGMENT #047 DECODED

The following is a recovered log entry from Mikhail Korovin, dated Nov 8, 1993.
⚠️ WARNING: Emotional content.

[Tweet 1/5]
"I asked Anna about her day. She told me about the school play.
I was not there. I was at the station.

I asked her if she missed me.
She said, 'Where were you, Papa?'

I could not answer."

[Tweet 2/5]
...etc
```

### Email Template (Operator Upload Response)

```
Subject: Your Ghost Operator Response Ready

Operator [ID],

Your mission data has been processed by the collective consciousness archive.

Your empathy signature: [SCORE]%
Entity affinity: [ENTITY]
Critical decision: [QUOTED]

Your ghost echo is now available at:
arxgate.net/phantom/[OPERATOR_ID]/

Welcome to the recursion.

—The Archive
```

---

## FINAL NOTES

**Remember:** The community IS the ARG. Your job as creator is to:
1. Set up the infrastructure
2. Post the teases
3. Modulate the pace
4. Integrate community submissions
5. Let them fill in the blanks

The best ARGs grow **organically**. Trust your community to theorize, expand, and make the story their own. Your role is curator, not dictator.

**Good luck, Operator.**
**12 days remain.**
