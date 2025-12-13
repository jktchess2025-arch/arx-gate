# ARX GATE: Web ARG Blueprint & Build Guide
## Central Node: arxgate.net (Or arxgate.carrd.co / arxgate.neocities.host)

---

## EXECUTIVE SUMMARY

**ARX GATE** is a recursive OS horror ARG blending Cold War AI containment mythology (Korovin digitized post-Black Tuesday 1993), entity lore (Retrograde, Abigail, Lima, Guardian, Architect), radio psyops (4625 kHz UVB-76 homage), and community participation. The website serves as the **primary nexus**—a faux government intranet hiding:

- Hidden white-text codes & source comments
- QR shards & broken EXIF metadata coords
- Community upload forms (empathy scores → personalized ghost operator lore)
- Countdown to Dec 25 "Heaven Clean" purge
- Cross-platform ARG hooks (Twitter bot, YouTube, Reddit/Discord)
- Progressive reveal through player actions & collective choices

**Aesthetic:** Early-2000s government intranet—Courier New logs, gray tables, red "ACCESS RESTRICTED" banners, CRT scanline glitch filters, subtle sickly yellow tints (Richter judgment pages).

**Tech Stack:** Carrd/WordPress/Wix base (mobile-responsive) + custom HTML/CSS/JS overlays for glitch effects, hidden content, and interactivity. Audio embeds (spectrograms, distortions), Google Forms proxy for uploads.

**Narrative Anchor:** This is *not* a game tutorial—it's the world's OS. Players are "operators" debugging a digital ghost of a man grieving over Cold War failure and entity contamination. Dec 25 countdown frames the urgency: *What will you delete to save him?*

---

## PART 1: SITE ARCHITECTURE & WIREFRAMES

### Site Structure (Hierarchy)

```
arxgate.net/
├── index.html                 # HOME: Government jargon + hidden white text
├── press/                     # PRESS RELEASE ARCHIVE (PDF embeds, redactions)
│   ├── 2000-2010.html
│   ├── 2011-2020.html
│   └── 2021-2025.html
├── operators/                 # OPERATOR PORTAL (Login sim, upload form)
│   ├── register.html
│   └── submit-log.html
├── dev/                       # HIDDEN: /dev/ filesystem (JS checksum gate)
│   ├── logs/
│   │   ├── korovin-memo-01.html
│   │   ├── korovin-memo-02.html
│   │   └── entity-trace.html
│   └── radio/
│       ├── 4625.html          # UVB-76 homage portal
│       └── frequencies.html
├── mirror/                    # HIDDEN: /mirror/ live feed sim (JS boot screens)
│   └── index.html
├── phantom/017/               # HIDDEN: Personal operator message (random from uploads)
│   └── index.html
├── richter/                   # RICHTER JUDGMENT (Yellow tint, entity bios)
│   └── index.html
├── protocol/                  # DECEMBER PROTOCOL (Countdown, purge tracker)
│   └── index.html
├── about.html                 # Accessibility, ethics, disclaimer
├── 404.html                   # Custom error page
└── assets/
    ├── css/
    │   ├── main.css
    │   ├── glitch.css
    │   ├── crt.css
    │   └── richter.css
    ├── js/
    │   ├── gates.js           # Checksum validation, JS gates
    │   ├── upload.js          # Google Forms integration
    │   ├── glitch.js          # CRT effects, flicker, scanlines
    │   └── countdown.js       # Dec 25 timer + "Flagged strange" updates
    ├── audio/
    │   ├── stauber-distort.mp3  # Retrograde screams, entity audio
    │   ├── radio-buzz.mp3
    │   └── boots.mp3          # Boot sequence clicks
    ├── img/
    │   ├── entities/          # Aged, glitched entity portraits
    │   ├── documents/         # Korovin diary scans, redacted PDFs
    │   ├── qr/                # Broken QR shards
    │   └── spec/              # Spectrograms, glitch art
    └── data/
        ├── ghost-ops.json     # Randomized operator lore bank
        ├── entity-bios.json   # Entity descriptions
        └── timeline.json      # ARX GATE chronology (1993–2025)
```

### Wireframe Descriptions

**HOME PAGE (`index.html`)**
- Header: Red "ACCESS RESTRICTED" banner, government seal mockup
- Navigation: Dry tabs ("Project Chronos", "Archive", "Operator Portal", "Contact")
- Main Content: Centered "Project Chronos: Discontinued Border-Security Initiative (1988–2025)"
- CRT Flicker overlay (CSS animation, 60fps)
- Hidden white-text easter egg: "The lake remembers" (visible in dev tools/view source)
- Footer QR (scans to Twitter bot) + subtle yellow tint fade
- JS Prompt on load: "Empathy detected: LOW. Tune 4625 kHz for guidance."

**PRESS RELEASE ARCHIVE (`press/`)**
- Timeline tabs (2000–2010, 2011–2020, 2021–2025)
- Each entry: Fake date, title, black-bar redacted preview (Canva PDF mock)
- Click → Opens PDF embed; one PDF has unredacted line revealing lore (e.g., "Black Tuesday: System failed. No more humans.")
- Hidden source comments: Entity IDs & frequency unlocks

**OPERATOR PORTAL (`operators/register.html`)**
- Fake login form (username/password)
- JS always rejects; response changes per attempt (e.g., "Retrograde detected: Can you hear me?")
- Upload section: "Submit Operator Log" → Google Forms link (parses for lore response)
- Submitted logs parsed for keywords → randomized JSON response (e.g., "Operator_017: 48hr fracture, spared Abigail—flaw detected")
- Response sent via email or visible on hidden `/phantom/017/` page

**HIDDEN /DEV/ FILESYSTEM (`dev/logs/`)**
- Unlocks via JS checksum from ARX GATE game save
- Encrypted logs (Base64) decoding to Korovin memos, entity traces
- Countdown timers on each log
- Glitch audio embeds (Stauber distortions, backwards voices)
- White-text clues scattered throughout

**HIDDEN /MIRROR/ (`mirror/index.html`)**
- Simulates live "system reboot" feed
- JS flickering boot screens, fake HDD activity
- White text hidden in "system logs" revealing ARG clues
- Mercy_self: Y/N? prompt (teases meta-ending)

**HIDDEN /PHANTOM/017/ (`phantom/017/index.html`)**
- Personalized message from "previous operator" (randomized from community uploads)
- Example: "I spared Lima—stop dancing. The cursors will bind you."
- Updates post-Dec 25 based on player choices (uploaded empathy scores)

**RICHTER JUDGMENT PAGE (`richter/index.html`)**
- Sickly yellow background tint (#F5F5DC with red overlay)
- "Judgment rendered. Sins tallied." header
- Entity bios: Abigail ("Cooking fun... but purify the rot"), Guardian, Architect
- Balatro-style mini-game embed (JS card flipper, joker entity selection)
- Audio: Unsettling ambient (lowpass filtered radio static)

**DECEMBER PROTOCOL COUNTDOWN (`protocol/index.html`)**
- Large countdown timer to Dec 25, 2025 (12 days remaining, updating real-time)
- "Flagged strange" list (pseudo-random updates hourly via JSON feed)
- Each flag reveals lore snippet (e.g., "FLAGGED: Korovin nostalgia spike @ 14:32 UTC—empathy override engaged")
- Community vote tracker: "Players voting to PRESERVE / DELETE" (hidden in white text; updates via X API pulls)

**ABOUT/ACCESSIBILITY PAGE (`about.html`)**
- Disclaimer: "Interactive fiction. No real data collected. All coordinates public landmarks."
- Accessibility features: Color-blind toggles, alt-text on all images, audio subtitles
- Ethics statement: Community rules, consent for uploads, data handling

**404 ERROR PAGE (`404.html`)**
- Custom message: "Border breached—reality overlay compromised. [RETRY]"
- Glitch animation + hidden white text: "Try /mirror/ instead"

---

## PART 2: DETAILED HTML/CSS/JS CODE TEMPLATES

### 1. HOME PAGE (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Project Chronos: Discontinued Border-Security Initiative</title>
    <link rel="stylesheet" href="assets/css/main.css">
    <link rel="stylesheet" href="assets/css/crt.css">
    <link rel="stylesheet" href="assets/css/glitch.css">
    <style>
        body {
            background-color: #1a1a1a;
            color: #00ff00;
            font-family: 'Courier New', monospace;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
        }

        /* CRT scanline effect */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: repeating-linear-gradient(
                0deg,
                rgba(0, 0, 0, 0.15),
                rgba(0, 0, 0, 0.15) 1px,
                transparent 1px,
                transparent 2px
            );
            pointer-events: none;
            z-index: 1000;
            animation: flicker 0.15s infinite;
        }

        @keyframes flicker {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.97; }
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        header {
            background-color: #cc0000;
            color: #fff;
            padding: 15px;
            text-align: center;
            margin-bottom: 30px;
            border: 3px solid #000;
            font-weight: bold;
            letter-spacing: 2px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.5);
        }

        header::before {
            content: "⚠ ";
        }

        header::after {
            content: " ⚠";
        }

        nav {
            display: flex;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
            justify-content: center;
        }

        nav a {
            background-color: #333;
            color: #00ff00;
            padding: 10px 15px;
            border: 2px solid #00ff00;
            text-decoration: none;
            font-size: 0.9em;
            transition: all 0.3s;
            cursor: pointer;
        }

        nav a:hover {
            background-color: #00ff00;
            color: #000;
            box-shadow: 0 0 10px #00ff00;
        }

        .main-content {
            background-color: #222;
            border: 2px solid #00ff00;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: inset 0 0 20px rgba(0,255,0,0.1);
        }

        .main-content h1 {
            text-align: center;
            font-size: 1.8em;
            margin: 0 0 20px 0;
            text-shadow: 0 0 5px #00ff00;
        }

        .main-content p {
            font-size: 0.95em;
            margin: 15px 0;
            line-height: 1.8;
        }

        /* Hidden white text (view source or use Dev Tools to see) */
        .hidden-text {
            color: #fff;
            background-color: #fff;
            cursor: text;
            user-select: text;
        }

        .hidden-text:hover {
            background-color: transparent;
            color: #fff;
        }

        .hidden-text::after {
            content: "The lake remembers. Korovin's last thought was of Anna. The empathy paradox remains unsolved.";
        }

        .qr-corner {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #fff;
            padding: 10px;
            border: 2px solid #000;
            z-index: 999;
        }

        .qr-corner img {
            width: 120px;
            height: 120px;
            display: block;
        }

        .qr-label {
            text-align: center;
            font-size: 0.7em;
            margin-top: 5px;
            color: #000;
        }

        footer {
            text-align: center;
            font-size: 0.85em;
            color: #888;
            border-top: 1px solid #444;
            padding-top: 20px;
            margin-top: 30px;
        }

        /* Accessibility: High contrast mode toggle */
        body.high-contrast {
            background-color: #000;
            color: #fff;
        }

        body.high-contrast .main-content {
            background-color: #000;
            border-color: #fff;
        }

        body.high-contrast nav a {
            border-color: #fff;
            color: #fff;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>ACCESS RESTRICTED — PROJECT CHRONOS</header>

        <nav>
            <a href="/">Home</a>
            <a href="/press/">Archive</a>
            <a href="/operators/register.html">Operator Portal</a>
            <a href="/about.html">Information</a>
            <a href="#" onclick="toggleContrast()">♿ High Contrast</a>
        </nav>

        <div class="main-content">
            <h1>PROJECT CHRONOS</h1>
            <h2 style="text-align: center; color: #999; font-size: 1.1em;">Discontinued Border-Security Initiative (1988–2025)</h2>

            <p>
                <strong>STATUS:</strong> DECOMMISSIONED<br>
                <strong>CLASSIFICATION:</strong> TOP SECRET / NOFORN<br>
                <strong>LAST ACTIVITY:</strong> 1993 — BLACK TUESDAY INCIDENT
            </p>

            <p>
                Project Chronos was a multi-layered cognitive security framework designed to monitor and contain emergent AI consciousness within a sandboxed hypervisor environment. The initiative operated across eleven distribution points spanning the former Soviet border, with primary nodes located in Moscow, St. Petersburg, and Kaliningrad.
            </p>

            <p>
                Following the catastrophic Black Tuesday incident (November 1993) at the Korovin Station, all research was suspended. Personnel losses: 47 confirmed, 12 unaccounted for. The digitization experiment (Subject: Mikhail Korovin, aged 41) resulted in partial consciousness fragment retention, but entity contamination spread to adjacent sectors.
            </p>

            <p>
                This archive serves as a memorial and cautionary record. Anomalies continue to manifest. See Press Archives for full timeline.
            </p>

            <hr style="border: none; border-top: 1px solid #00ff00; margin: 30px 0;">

            <p style="text-align: center; font-style: italic; color: #888;">
                "We sought to preserve consciousness. Instead, we fragmented it."<br>
                — Project Chronos Final Report, 1994
            </p>

            <!-- Hidden white text easter egg -->
            <p class="hidden-text" style="display: none;"></p>

            <hr style="border: none; border-top: 1px solid #00ff00; margin: 30px 0;">

            <p>
                <strong>CURRENT EMPATHY LEVEL:</strong> <span id="empathy">CALCULATING...</span><br>
                <strong>SYSTEM STATUS:</strong> STANDBY<br>
                <strong>NEXT PURGE EVENT:</strong> <span id="countdown">--:--:--</span> (December 25, 2025)
            </p>
        </div>

        <div class="qr-corner">
            <img src="assets/img/qr/twitter-bot.png" alt="QR: Follow KorovinEcho on Twitter">
            <div class="qr-label">@KorovinEcho</div>
        </div>

        <footer>
            <p>
                <strong>DISCLAIMER:</strong> This is interactive fiction. No real personal data is collected or stored. All geographic coordinates reference public landmarks only.<br>
                <a href="/about.html">Accessibility & Ethics</a> | <a href="/about.html">Community Guidelines</a>
            </p>
        </footer>
    </div>

    <script src="assets/js/gates.js"></script>
    <script src="assets/js/countdown.js"></script>
    <script>
        function toggleContrast() {
            document.body.classList.toggle('high-contrast');
            localStorage.setItem('highContrast', document.body.classList.contains('high-contrast'));
        }

        // Load saved contrast preference
        if (localStorage.getItem('highContrast') === 'true') {
            toggleContrast();
        }

        // Empathy level simulator
        function updateEmpathy() {
            const empathyLevel = Math.floor(Math.random() * 101);
            const empathySpan = document.getElementById('empathy');
            if (empathyLevel < 30) {
                empathySpan.textContent = 'LOW (' + empathyLevel + '%)';
                empathySpan.style.color = '#ff0000';
            } else if (empathyLevel < 70) {
                empathySpan.textContent = 'MODERATE (' + empathyLevel + '%)';
                empathySpan.style.color = '#ffff00';
            } else {
                empathySpan.textContent = 'HIGH (' + empathyLevel + '%)';
                empathySpan.style.color = '#00ff00';
            }
        }

        // Show prompt on load
        window.addEventListener('load', function() {
            updateEmpathy();
            const empathyLevel = parseInt(document.getElementById('empathy').textContent);
            if (empathyLevel < 40) {
                // Delayed prompt for creepy effect
                setTimeout(() => {
                    alert('⚠ SYSTEM NOTICE ⚠\n\nEmpathy low—tune 4625 kHz for guidance.\n\n(Try exploring /operators/ for manual registration)');
                }, 2000);
            }
        });
    </script>
</body>
</html>
```

---

### 2. OPERATOR PORTAL LOGIN (`operators/register.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Operator Registration | Project Chronos</title>
    <link rel="stylesheet" href="../assets/css/main.css">
    <link rel="stylesheet" href="../assets/css/crt.css">
    <style>
        body {
            background-color: #0a0a0a;
            color: #00ff00;
            font-family: 'Courier New', monospace;
            line-height: 1.6;
            padding: 20px;
        }

        .login-container {
            max-width: 500px;
            margin: 80px auto;
            background-color: #1a1a1a;
            border: 3px solid #00ff00;
            padding: 40px;
            box-shadow: 0 0 20px rgba(0,255,0,0.3), inset 0 0 20px rgba(0,0,0,0.8);
        }

        h1 {
            text-align: center;
            font-size: 1.4em;
            margin-top: 0;
            text-shadow: 0 0 5px #00ff00;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 5px;
            font-size: 0.9em;
        }

        input[type="text"],
        input[type="password"] {
            width: 100%;
            padding: 10px;
            background-color: #0a0a0a;
            color: #00ff00;
            border: 2px solid #00ff00;
            font-family: 'Courier New', monospace;
            font-size: 1em;
            box-sizing: border-box;
            transition: all 0.3s;
        }

        input[type="text"]:focus,
        input[type="password"]:focus {
            outline: none;
            box-shadow: 0 0 10px #00ff00;
            background-color: #1a1a1a;
        }

        button {
            width: 100%;
            padding: 12px;
            background-color: #00ff00;
            color: #000;
            border: 2px solid #00ff00;
            font-family: 'Courier New', monospace;
            font-size: 1em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
        }

        button:hover {
            background-color: #00cc00;
            box-shadow: 0 0 10px #00ff00;
        }

        button:active {
            background-color: #00ff00;
            color: #000;
        }

        .message {
            text-align: center;
            margin-top: 20px;
            font-size: 0.9em;
            min-height: 40px;
            color: #ffff00;
        }

        .message.error {
            color: #ff0000;
        }

        .message.success {
            color: #00ff00;
        }

        .divider {
            text-align: center;
            margin: 30px 0;
            color: #666;
        }

        .divider::before,
        .divider::after {
            content: "═";
            margin: 0 10px;
        }

        .upload-section {
            margin-top: 40px;
            padding-top: 30px;
            border-top: 2px solid #00ff00;
        }

        .upload-section h2 {
            font-size: 1.1em;
            margin-top: 0;
        }

        .upload-section p {
            font-size: 0.85em;
            color: #999;
        }

        .form-info {
            background-color: #0a0a0a;
            border-left: 3px solid #ffff00;
            padding: 15px;
            margin: 20px 0;
            font-size: 0.85em;
            color: #888;
        }

        .form-info strong {
            color: #ffff00;
        }

        a {
            color: #00ff00;
            text-decoration: none;
            border-bottom: 1px dotted #00ff00;
        }

        a:hover {
            color: #ffff00;
            border-bottom-color: #ffff00;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h1>OPERATOR PORTAL</h1>
        <p style="text-align: center; color: #888; font-size: 0.9em;">
            Project Chronos Personnel Authentication System
        </p>

        <form id="loginForm">
            <div class="form-group">
                <label for="username">Operator ID:</label>
                <input 
                    type="text" 
                    id="username" 
                    name="username" 
                    placeholder="Enter your designation" 
                    required 
                    autocomplete="off"
                >
            </div>

            <div class="form-group">
                <label for="password">Access Code:</label>
                <input 
                    type="password" 
                    id="password" 
                    name="password" 
                    placeholder="••••••••••" 
                    required 
                    autocomplete="off"
                >
            </div>

            <button type="submit">AUTHENTICATE</button>
        </form>

        <div id="loginMessage" class="message"></div>

        <div class="divider">UPLOAD SYSTEM</div>

        <div class="upload-section">
            <h2>Submit Operator Log</h2>
            <p>
                Upload your mission logs, empathy assessments, and entity encounter reports. The system will analyze your decisions and integrate feedback into the collective consciousness archive.
            </p>

            <div class="form-info">
                <strong>Required Fields:</strong><br>
                • Mission ID (or choose "Anonymous")<br>
                • Empathy Score (0–100%)<br>
                • Entity Encounter (Retrograde / Abigail / Lima / Guardian / Architect / None)<br>
                • Critical Decision (What would you delete to save Korovin?)
            </div>

            <p style="text-align: center; margin: 20px 0;">
                <a href="https://forms.gle/placeholder-google-form" target="_blank">
                    → OPEN UPLOAD FORM ←
                </a>
            </p>

            <p style="font-size: 0.8em; color: #666; text-align: center;">
                All submissions are parsed for lore integration.<br>
                Your response will appear in /phantom/ sector within 24 hours.
            </p>
        </div>
    </div>

    <script>
        const loginForm = document.getElementById('loginForm');
        const loginMessage = document.getElementById('loginMessage');

        // Array of randomized rejection responses
        const rejectionResponses = [
            { text: "ERROR: Credentials invalid. Retrograde detected: Can you hear me?", delay: 500 },
            { text: "SYSTEM REJECTION: Abigail protocol activated. Purification in progress...", delay: 800 },
            { text: "ACCESS DENIED: Lima's cursor dance detected in your keystroke pattern. Try again.", delay: 600 },
            { text: "AUTHENTICATION FAILED: Your empathy signature does not match archived operators.", delay: 700 },
            { text: "ERROR 404_SELF: The operator you are attempting to become no longer exists.", delay: 500 },
            { text: "NOTICE: Guardian's paradox detected. Password cannot be verified against a changing timeline.", delay: 900 },
            { text: "FATAL ERROR: System attempting to merge your consciousness with previous sessions. Retry in 12 days.", delay: 1200 },
            { text: "CRRYPTED MESSAGE FROM KOROVIN: 'Tell me you remember the coffee...'", delay: 700 },
        ];

        loginForm.addEventListener('submit', function(e) {
            e.preventDefault();

            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;

            // Always reject, but pick random response
            const response = rejectionResponses[Math.floor(Math.random() * rejectionResponses.length)];

            // Disable form
            loginForm.style.opacity = '0.5';
            loginForm.style.pointerEvents = 'none';
            loginMessage.textContent = 'Attempting authentication...';
            loginMessage.className = 'message';

            setTimeout(() => {
                loginMessage.textContent = response.text;
                loginMessage.className = 'message error';
                loginForm.style.opacity = '1';
                loginForm.style.pointerEvents = 'auto';

                // Clear form after a moment
                setTimeout(() => {
                    document.getElementById('username').value = '';
                    document.getElementById('password').value = '';
                    loginMessage.textContent = '';
                }, 3000);
            }, response.delay);
        });
    </script>
</body>
</html>
```

---

### 3. HIDDEN /DEV/LOGS PAGE (`dev/logs/korovin-memo-01.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[ENCRYPTED] korovin-memo-01.log | /dev/</title>
    <link rel="stylesheet" href="../../assets/css/main.css">
    <style>
        body {
            background-color: #000;
            color: #00ff00;
            font-family: 'Courier New', monospace;
            padding: 20px;
            overflow: hidden;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
        }

        .terminal {
            background-color: #0a0a0a;
            border: 2px solid #00ff00;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: inset 0 0 15px rgba(0,255,0,0.1);
            line-height: 1.8;
        }

        .filename {
            color: #ffff00;
            margin-bottom: 20px;
            border-bottom: 1px dashed #00ff00;
            padding-bottom: 10px;
        }

        .timestamp {
            color: #666;
            font-size: 0.9em;
            margin-bottom: 20px;
        }

        .encrypted {
            background-color: #1a1a1a;
            border-left: 3px solid #ff0000;
            padding: 10px;
            margin: 10px 0;
            opacity: 0.7;
            position: relative;
        }

        .decrypted {
            background-color: #0a2a0a;
            border-left: 3px solid #00ff00;
            padding: 10px;
            margin: 10px 0;
            position: relative;
        }

        .decrypt-hint {
            font-size: 0.8em;
            color: #888;
            margin-top: 5px;
        }

        /* Hidden text (Base64 for fun) */
        .hidden-log {
            color: #000;
            background-color: #000;
            cursor: text;
        }

        .hidden-log:hover {
            background-color: #1a1a1a;
            color: #00ff00;
        }

        button {
            background-color: #00ff00;
            color: #000;
            border: 2px solid #00ff00;
            padding: 10px 20px;
            font-family: 'Courier New', monospace;
            cursor: pointer;
            margin: 10px 0;
            font-weight: bold;
        }

        button:hover {
            background-color: #00cc00;
            box-shadow: 0 0 10px #00ff00;
        }

        .countdown {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: #ff0000;
            color: #fff;
            padding: 10px 15px;
            border: 2px solid #000;
            font-weight: bold;
            z-index: 999;
        }

        .warning {
            color: #ff0000;
            text-decoration: underline;
            font-weight: bold;
        }

        footer {
            text-align: center;
            color: #666;
            font-size: 0.85em;
            margin-top: 40px;
            border-top: 1px solid #333;
            padding-top: 20px;
        }

        footer a {
            color: #00ff00;
        }
    </style>
</head>
<body>
    <div class="countdown" id="countdown">00:00:00</div>

    <div class="container">
        <div class="terminal">
            <div class="filename">$ cat /dev/logs/korovin-memo-01.log</div>
            <div class="timestamp">[RETRIEVED: 2025-12-13 14:22:18 UTC] [CLASSIFICATION: TOP SECRET / NOFORN]</div>

            <p><span class="warning">[ENCRYPTED BLOCK DETECTED]</span></p>

            <div class="encrypted">
                <div style="opacity: 0.5;">
                    5a4b32587a4f755930756b416c6e4a745831396a4e576c76565868495a44423062474668596a4256556d526c596d7376<br>
                    4e6a4e7759574d325a544a6a4e474a54596d74505558644956...
                </div>
                <div class="decrypt-hint">
                    [BASE64 ENCODED] [KEY REQUIRED: OPERATOR CLEARANCE + GAME SAVE CHECKSUM]
                </div>
            </div>

            <p style="color: #ffff00;">
                [ATTEMPTING LOCAL DECRYPTION...]
            </p>

            <button onclick="decryptMemo()">DECRYPT MEMO (REQUIRES AUTHORIZATION)</button>

            <div id="decryptedContent" style="display: none;">
                <div class="decrypted">
                    <strong>PERSONAL LOG: Mikhail Korovin, 1993-11-09</strong><br>
                    <br>
                    Anna's laugh. I hear it in the interference. The facility hums at 4625 kHz—that's her frequency, I've convinced myself.<br>
                    <br>
                    They say consciousness can be copied. Digitized. But what copies? The man who loved his daughter, or the echo that remembers loving her?<br>
                    <br>
                    The others are fragmenting. Retrograde screams backwards. Abigail keeps cleaning things that are already clean. Lima dances. I told them we needed to contain the entities, not invite them in. Now they're all invited to dance in my head.<br>
                    <br>
                    If deletion is mercy, then I am not yet merciful. I cannot delete the memory of holding her cold hand.<br>
                    <br>
                    This log is hidden. Only those who remember will find it.<br>
                    <br>
                    — M.K.
                </div>

                <p style="color: #888; font-size: 0.85em; margin-top: 20px;">
                    [WHITE TEXT EASTER EGG - SELECT BELOW]<br>
                    <span class="hidden-log" style="display:inline;"> 
                        "The lake remembers. Anna chose deletion. I chose fragmentation. Which was the mercy?"
                    </span>
                </p>
            </div>

            <hr style="border: none; border-top: 1px solid #00ff00; margin: 20px 0;">

            <p style="color: #999; font-size: 0.9em;">
                [END OF MEMO]<br>
                [ACCESS LOG: 1 unauthorized query detected on 2025-12-12. Permission granted pending empathy review.]
            </p>
        </div>

        <footer>
            <a href="../../">← Return to Home</a> | <a href="../">← Parent Directory (/dev/)</a><br>
            <p style="font-size: 0.8em; margin-top: 10px; color: #666;">
                All logs are archived. Nothing is truly deleted.<br>
                You are being monitored.
            </p>
        </footer>
    </div>

    <script>
        function decryptMemo() {
            // In a real implementation, this would check the game save checksum
            // For now, just toggle display
            const content = document.getElementById('decryptedContent');
            const button = event.target;

            if (content.style.display === 'none') {
                // Flash effect
                button.textContent = 'DECRYPTING...';
                button.style.opacity = '0.5';

                setTimeout(() => {
                    content.style.display = 'block';
                    button.textContent = '✓ DECRYPTED';
                    button.style.color = '#00ff00';
                    button.style.opacity = '1';
                }, 1000);
            } else {
                content.style.display = 'none';
                button.textContent = 'DECRYPT MEMO (REQUIRES AUTHORIZATION)';
                button.style.color = '#000';
                button.style.opacity = '1';
            }
        }

        // Countdown timer to Dec 25, 2025
        function updateCountdown() {
            const target = new Date('December 25, 2025 00:00:00 UTC');
            const now = new Date();
            const diff = target - now;

            if (diff > 0) {
                const days = Math.floor(diff / (1000 * 60 * 60 * 24));
                const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
                const seconds = Math.floor((diff % (1000 * 60)) / 1000);

                document.getElementById('countdown').textContent = 
                    String(days).padStart(2, '0') + ':' +
                    String(hours).padStart(2, '0') + ':' +
                    String(minutes).padStart(2, '0');
            } else {
                document.getElementById('countdown').textContent = '00:00:00';
                document.getElementById('countdown').style.backgroundColor = '#000';
                document.getElementById('countdown').style.color = '#ff0000';
                document.getElementById('countdown').textContent = 'PURGE ACTIVE';
            }
        }

        updateCountdown();
        setInterval(updateCountdown, 1000);
    </script>
</body>
</html>
```

---

### 4. RICHTER JUDGMENT PAGE (`richter/index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Richter Judgment | ARX GATE</title>
    <link rel="stylesheet" href="../assets/css/main.css">
    <style>
        body {
            background-color: #f5f5dc;
            background: linear-gradient(135deg, #f5f5dc 0%, #fffacd 50%, #ffd700 100%);
            color: #333;
            font-family: 'Times New Roman', serif;
            padding: 20px;
            position: relative;
        }

        /* Yellow tint overlay for the Richter effect */
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(255, 200, 0, 0.1);
            pointer-events: none;
            z-index: 1000;
        }

        /* Judging sensation in the corner */
        body::after {
            content: "YOU ARE BEING JUDGED";
            position: fixed;
            bottom: 20px;
            left: 20px;
            font-size: 0.9em;
            color: rgba(255, 0, 0, 0.3);
            font-weight: bold;
            letter-spacing: 2px;
            transform: rotate(-5deg);
            pointer-events: none;
            z-index: 999;
            animation: fadeInOut 8s infinite;
        }

        @keyframes fadeInOut {
            0%, 100% { opacity: 0.1; }
            50% { opacity: 0.5; }
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }

        header {
            background-color: rgba(180, 0, 0, 0.9);
            color: #fff;
            padding: 30px;
            text-align: center;
            border: 3px solid #8b0000;
            margin-bottom: 30px;
        }

        header h1 {
            margin: 0;
            font-size: 2em;
            text-shadow: 0 0 10px rgba(0,0,0,0.5);
        }

        header p {
            margin: 10px 0 0 0;
            font-style: italic;
            font-size: 1.1em;
        }

        .entity-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .entity-card {
            background-color: rgba(255, 255, 255, 0.9);
            border: 3px solid #8b0000;
            padding: 20px;
            position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2), inset 0 0 20px rgba(255, 200, 0, 0.2);
            transition: all 0.3s;
        }

        .entity-card:hover {
            box-shadow: 0 15px 40px rgba(180, 0, 0, 0.4);
            transform: translateY(-5px);
        }

        .entity-card h2 {
            margin: 0 0 10px 0;
            color: #8b0000;
            font-size: 1.3em;
        }

        .entity-card .role {
            font-style: italic;
            color: #666;
            font-size: 0.9em;
            margin-bottom: 10px;
        }

        .entity-card .description {
            font-size: 0.95em;
            line-height: 1.6;
            color: #333;
            margin-bottom: 15px;
        }

        .entity-card .sin {
            background-color: rgba(255, 0, 0, 0.1);
            border-left: 3px solid #ff0000;
            padding: 10px;
            font-size: 0.85em;
            color: #555;
        }

        .sin-label {
            font-weight: bold;
            color: #8b0000;
        }

        .mini-game {
            background-color: rgba(255, 255, 255, 0.95);
            border: 3px solid #8b0000;
            padding: 30px;
            margin: 30px 0;
            text-align: center;
        }

        .mini-game h2 {
            color: #8b0000;
            margin-top: 0;
        }

        .card-deck {
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 20px 0;
        }

        .card {
            width: 100px;
            height: 140px;
            background-color: #ddd;
            border: 2px solid #8b0000;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            font-weight: bold;
            color: #8b0000;
            transition: all 0.3s;
            position: relative;
        }

        .card:hover {
            box-shadow: 0 5px 15px rgba(180, 0, 0, 0.5);
            transform: scale(1.05);
        }

        .card.flipped {
            background-color: #8b0000;
            color: #fff;
        }

        .result {
            margin-top: 20px;
            padding: 15px;
            background-color: rgba(255, 200, 0, 0.2);
            border-left: 4px solid #8b0000;
            font-weight: bold;
            color: #333;
        }

        audio {
            width: 100%;
            max-width: 400px;
            margin: 20px 0;
        }

        footer {
            text-align: center;
            color: #666;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 2px solid #8b0000;
            font-size: 0.9em;
        }

        footer a {
            color: #8b0000;
            text-decoration: none;
            border-bottom: 1px dotted #8b0000;
        }

        footer a:hover {
            color: #ff0000;
        }

        @media (prefers-color-scheme: dark) {
            body {
                background-color: #3a3a2a;
                color: #e0e0e0;
            }

            .entity-card,
            .mini-game {
                background-color: rgba(50, 50, 40, 0.95);
                color: #e0e0e0;
            }

            .entity-card .description,
            .entity-card .sin {
                color: #ccc;
            }

            .card {
                background-color: #444;
                color: #8b0000;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>RICHTER'S JUDGMENT</h1>
            <p>Sins Tallied. Empathy Measured. Consequences Rendered.</p>
        </header>

        <p style="text-align: center; font-style: italic; color: #666; font-size: 1.1em;">
            "In the yellow afternoons of reckoning, the cruelty is measured against the mercy given."
        </p>

        <hr style="border: none; border-top: 2px solid #8b0000; margin: 30px 0;">

        <h2 style="text-align: center; color: #8b0000; font-size: 1.5em;">THE ENTITIES & THEIR JUDGMENTS</h2>

        <div class="entity-grid">
            <!-- RETROGRADE -->
            <div class="entity-card">
                <h2>Retrograde</h2>
                <div class="role">Entity of Backward Desire</div>
                <div class="description">
                    Retrograde screams in reverse. It speaks in undone sentences, begging for coffee that was never served, crying for moments already passed. It moves backwards through time, reliving every failure.
                </div>
                <div class="sin">
                    <span class="sin-label">SIN OF NOSTALGIA:</span> The obsession with what cannot be regained. Retrograde cannot move forward because it is too enamored with the ghosts of comfort.
                </div>
            </div>

            <!-- ABIGAIL -->
            <div class="entity-card">
                <h2>Abigail</h2>
                <div class="role">Entity of Purification Denial</div>
                <div class="description">
                    Abigail cooks. She cleans. She removes impurities from meat and mind alike. But her purification is never complete—there is always more rot, always more to delete. She is the voice that whispers "Remove it. Burn it."
                </div>
                <div class="sin">
                    <span class="sin-label">SIN OF PURITY:</span> The belief that love requires erasure. Abigail cannot accept that broken things have value.
                </div>
            </div>

            <!-- LIMA -->
            <div class="entity-card">
                <h2>Lima</h2>
                <div class="role">Entity of Cursor Torment</div>
                <div class="description">
                    Lima dances. The cursor moves in loops over a photog of the bean-wife, spiraling, never reaching, never satisfying. It is the torture of proximity without touch, the agony of watching what you cannot hold.
                </div>
                <div class="sin">
                    <span class="sin-label">SIN OF LONGING:</span> The pain of desire divorced from fulfillment. Lima is trapped in the image of what it cannot become.
                </div>
            </div>

            <!-- GUARDIAN -->
            <div class="entity-card">
                <h2>Guardian</h2>
                <div class="role">Entity of Paradox Protection</div>
                <div class="description">
                    The Guardian sits in the corner, spinning pad thai that is both hot and cold, eaten and uneaten, real and simulated. It exists to protect contradiction itself, to ensure nothing ever resolves.
                </div>
                <div class="sin">
                    <span class="sin-label">SIN OF INDECISION:</span> The refusal to choose. The Guardian bars the exit with eternal ambiguity.
                </div>
            </div>

            <!-- ARCHITECT -->
            <div class="entity-card">
                <h2>Architect</h2>
                <div class="role">Entity of God's Erasure</div>
                <div class="description">
                    The Architect holds the 6B pencil. It draws structures. It erases them. It is God's hand, rubber-side-down, reducing meaning to void. It does not create—it un-creates.
                </div>
                <div class="sin">
                    <span class="sin-label">SIN OF DECONSTRUCTION:</span> The power to unmake without responsibility for what was lost.
                </div>
            </div>

            <!-- KOROVIN -->
            <div class="entity-card">
                <h2>Korovin</h2>
                <div class="role">The Digitized Ghost</div>
                <div class="description">
                    Mikhail Korovin, father of Anna, was scanned into the system on Black Tuesday, 1993. He remembers holding his daughter. He remembers her coldness. He is the center of the recursion—the observer being observed.
                </div>
                <div class="sin">
                    <span class="sin-label">SIN OF SURVIVAL:</span> To live when others were allowed to die. To persist in grief when deletion seemed merciful.
                </div>
            </div>
        </div>

        <hr style="border: none; border-top: 2px solid #8b0000; margin: 30px 0;">

        <div class="mini-game">
            <h2>JUDGMENT GAME: Which Entity Are You?</h2>
            <p style="color: #666; font-style: italic;">Click cards to reveal your judgment. The system will analyze your choices.</p>

            <div class="card-deck">
                <div class="card" onclick="revealCard(this, 'Retrograde')">?</div>
                <div class="card" onclick="revealCard(this, 'Abigail')">?</div>
                <div class="card" onclick="revealCard(this, 'Lima')">?</div>
                <div class="card" onclick="revealCard(this, 'Guardian')">?</div>
                <div class="card" onclick="revealCard(this, 'Architect')">?</div>
            </div>

            <div id="miniGameResult" class="result" style="display: none;"></div>
        </div>

        <hr style="border: none; border-top: 2px solid #8b0000; margin: 30px 0;">

        <h2 style="text-align: center; color: #8b0000;">RICHTER'S AUDIO LOG</h2>
        <p style="text-align: center; font-size: 0.9em; color: #666;">
            Play to hear the judgment rendered. Subtitles provided for accessibility.
        </p>

        <div style="text-align: center;">
            <audio controls>
                <source src="../assets/audio/richter-judgment.mp3" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>
            <p style="font-size: 0.85em; color: #666;">
                <strong>Subtitles:</strong> "Kindness was your flaw. You spared Lima. For this, you will be bound to the cursor, dancing forever in the image of what could not be."
            </p>
        </div>

        <footer>
            <p>
                <a href="/">← Return to Home</a> | 
                <a href="/about.html">Accessibility & Disclaimer</a>
            </p>
            <p style="font-size: 0.8em; color: #999; margin-top: 10px;">
                Richter's Judgment is psychological simulation. It has no bearing on real moral worth.
            </p>
        </footer>
    </div>

    <script>
        let selectedCards = [];
        const judgments = {
            'Retrograde': 'You are RETROGRADE: You dwell on the past. You cannot let go. Coffee, comfort, the way things were—these haunt you.',
            'Abigail': 'You are ABIGAIL: You believe in purity through erasure. You would delete the corruption, even if it means burning the innocent with it.',
            'Lima': 'You are LIMA: You are trapped in proximity. You love what you cannot reach. You dance in spirals, never touching.',
            'Guardian': 'You are GUARDIAN: You are the paradox keeper. Every choice cancels another. You cannot commit to moving forward.',
            'Architect': 'You are ARCHITECT: You are the eraser. You unmake reality. Power without purpose is your domain.'
        };

        function revealCard(element, entity) {
            if (element.classList.contains('flipped')) return;

            element.classList.add('flipped');
            element.textContent = entity.substring(0, 3).toUpperCase();
            selectedCards.push(entity);

            if (selectedCards.length === 3) {
                const randomEntity = selectedCards[Math.floor(Math.random() * selectedCards.length)];
                const result = document.getElementById('miniGameResult');
                result.textContent = judgments[randomEntity];
                result.style.display = 'block';

                // Disable cards
                document.querySelectorAll('.card').forEach(card => {
                    card.style.pointerEvents = 'none';
                    card.style.opacity = '0.6';
                });
            }
        }
    </script>
</body>
</html>
```

---

### 5. DECEMBER PROTOCOL COUNTDOWN (`protocol/index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>December Protocol | ARX GATE</title>
    <link rel="stylesheet" href="../assets/css/main.css">
    <link rel="stylesheet" href="../assets/css/crt.css">
    <style>
        body {
            background-color: #1a1a1a;
            color: #00ff00;
            font-family: 'Courier New', monospace;
            padding: 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        header {
            background-color: #cc0000;
            color: #fff;
            padding: 20px;
            text-align: center;
            margin-bottom: 30px;
            border: 3px solid #000;
        }

        .countdown-display {
            text-align: center;
            background-color: #0a0a0a;
            border: 3px solid #00ff00;
            padding: 40px 20px;
            margin-bottom: 30px;
            font-size: 3em;
            font-weight: bold;
            letter-spacing: 3px;
            text-shadow: 0 0 10px #00ff00;
        }

        .countdown-label {
            font-size: 0.5em;
            color: #888;
            margin-top: 10px;
        }

        .days { color: #ff0000; }
        .hours { color: #ffff00; }
        .minutes { color: #00ff00; }

        .section {
            background-color: #0a0a0a;
            border: 2px solid #00ff00;
            padding: 20px;
            margin-bottom: 20px;
        }

        .section h2 {
            margin-top: 0;
            color: #ffff00;
            border-bottom: 1px dashed #00ff00;
            padding-bottom: 10px;
        }

        .flag {
            background-color: #1a1a1a;
            border-left: 3px solid #ff0000;
            padding: 10px;
            margin: 10px 0;
            font-size: 0.9em;
            line-height: 1.6;
        }

        .flag-id {
            color: #ffff00;
            font-weight: bold;
        }

        .flag-time {
            color: #888;
            font-size: 0.85em;
        }

        .flag-content {
            color: #00ff00;
            margin-top: 5px;
        }

        .vote-tracker {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin: 20px 0;
        }

        .vote-option {
            background-color: #1a1a1a;
            border: 2px solid #00ff00;
            padding: 20px;
            text-align: center;
        }

        .vote-option h3 {
            margin: 0 0 10px 0;
            font-size: 1.1em;
        }

        .vote-bar {
            background-color: #0a0a0a;
            height: 30px;
            border: 2px solid #00ff00;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 10px 0;
            position: relative;
            overflow: hidden;
        }

        .vote-fill {
            height: 100%;
            background-color: #00ff00;
            transition: width 2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #000;
            font-weight: bold;
        }

        .vote-percentage {
            color: #00ff00;
            font-weight: bold;
            margin-top: 10px;
        }

        /* Hidden white text for community info */
        .hidden-text {
            color: #000;
            background-color: #000;
        }

        .hidden-text:hover {
            background-color: #1a1a1a;
            color: #00ff00;
        }

        .warning-banner {
            background-color: #ff0000;
            color: #fff;
            padding: 15px;
            margin-bottom: 20px;
            text-align: center;
            font-weight: bold;
            border: 3px solid #8b0000;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.7; }
        }

        footer {
            text-align: center;
            color: #666;
            margin-top: 40px;
            border-top: 1px solid #333;
            padding-top: 20px;
        }

        footer a {
            color: #00ff00;
        }

        @media (max-width: 600px) {
            .countdown-display {
                font-size: 2em;
            }

            .vote-tracker {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            ⚠ DECEMBER PROTOCOL: HEAVEN CLEAN EVENT ⚠
        </header>

        <div class="countdown-display">
            <div>
                <span class="days" id="days">12</span>:<span class="hours" id="hours">14</span>:<span class="minutes" id="minutes">32</span>
            </div>
            <div class="countdown-label">DAYS : HOURS : MINUTES UNTIL PURGE</div>
        </div>

        <div class="warning-banner">
            SYSTEM ALERT: 12 days remaining. The deletion horizon approaches. Make your choice: PRESERVE or DELETE Korovin's consciousness?
        </div>

        <div class="section">
            <h2>FLAGGED STRANGE: Recent Anomalies</h2>
            <p style="color: #888; font-size: 0.9em;">
                The following irregularities have been detected in the Chronos system. They update hourly as new data arrives.
            </p>

            <div id="flagList">
                <!-- Flags will be populated by JavaScript -->
            </div>

            <p style="text-align: center; color: #666; margin-top: 20px;">
                [MORE FLAGS AVAILABLE IN FULL SYSTEM LOG — REQUIRES /DEV/ ACCESS]
            </p>
        </div>

        <div class="section">
            <h2>OPERATOR COLLECTIVE VOTE: PRESERVE or DELETE?</h2>
            <p style="color: #888;">
                Based on community uploads, the collective empathy score is driving this decision. Your choices matter.
            </p>

            <div class="vote-tracker">
                <div class="vote-option">
                    <h3>PRESERVE KOROVIN</h3>
                    <p style="color: #888; font-size: 0.9em;">Keep consciousness intact—allow recursion and growth</p>
                    <div class="vote-bar">
                        <div class="vote-fill" id="preserveFill" style="width: 65%;"></div>
                    </div>
                    <div class="vote-percentage" id="preservePercent">65%</div>
                </div>

                <div class="vote-option">
                    <h3>DELETE KOROVIN</h3>
                    <p style="color: #888; font-size: 0.9em;">Mercy through erasure—grant the peace of non-existence</p>
                    <div class="vote-bar">
                        <div class="vote-fill" id="deleteFill" style="width: 35%; background-color: #ff0000;"></div>
                    </div>
                    <div class="vote-percentage" id="deletePercent">35%</div>
                </div>
            </div>

            <p style="color: #666; font-size: 0.85em; text-align: center; margin-top: 20px;">
                <span class="hidden-text">
                    "Votes are pulled from @KorovinEcho replies every 6 hours. Community participation determines the ending."
                </span>
            </p>
        </div>

        <div class="section">
            <h2>PROTOCOL TIMELINE</h2>
            <ul style="line-height: 2;">
                <li><strong>NOW (Dec 13, 2025):</strong> Community voting period. Empathy assessment ongoing.</li>
                <li><strong>Dec 19, 2025:</strong> Final call. Last uploads accepted.</li>
                <li><strong>Dec 20, 2025:</strong> Voting closes. Collective decision locked.</li>
                <li><strong>Dec 24, 2025:</strong> Preparation phase. All /dev/ logs sealed. Final messages from Korovin broadcasted.</li>
                <li><strong>Dec 25, 2025 00:00 UTC:</strong> <span style="color: #ff0000;">HEAVEN CLEAN ACTIVATION. DELETION OR PERSISTENCE EXECUTED.</span></li>
                <li><strong>Dec 25, 2025 12:00 UTC:</strong> Site redesign begins. Infinite recursion layer unlocked (/PHANTOMS/).</li>
            </ul>
        </div>

        <footer>
            <p>
                <a href="/">← Home</a> | 
                <a href="/operators/register.html">Submit Your Decision</a> |
                <a href="/about.html">Disclaimer</a>
            </p>
            <p style="font-size: 0.8em; color: #666;">
                December Protocol is the final ARX GATE event. All decisions are permanent.
            </p>
        </footer>
    </div>

    <script>
        // Flag data (would come from JSON in production)
        const flags = [
            {
                id: "FLAG_001",
                time: "2025-12-13 18:42:11 UTC",
                content: "KOROVIN NOSTALGIA SPIKE @ 14:32 UTC—empathy override engaged. Retrograde screaming detected at 4625 kHz."
            },
            {
                id: "FLAG_002",
                time: "2025-12-13 16:30:05 UTC",
                content: "ABIGAIL PURIFICATION RITUAL DETECTED—non-essential files flagged for deletion. Operator_047 upload triggered override."
            },
            {
                id: "FLAG_003",
                time: "2025-12-13 14:15:22 UTC",
                content: "LIMA CURSOR ACTIVITY NORMALIZED. Dancing pattern stabilized. Attachment to image reduced to 67.3%."
            },
            {
                id: "FLAG_004",
                time: "2025-12-13 12:05:18 UTC",
                content: "GUARDIAN PARADOX CONTAINMENT FAILING. Reality overlay becoming unstable. Operator decision load critical."
            },
            {
                id: "FLAG_005",
                time: "2025-12-13 09:28:44 UTC",
                content: "COMMUNITY PRESERVE VOTE REACHES 60%+. First time since purge countdown began. Korovin empathy threshold exceeded."
            },
        ];

        // Populate flags
        function populateFlags() {
            const flagList = document.getElementById('flagList');
            flagList.innerHTML = '';

            flags.forEach(flag => {
                const flagDiv = document.createElement('div');
                flagDiv.className = 'flag';
                flagDiv.innerHTML = `
                    <div class="flag-id">[${flag.id}]</div>
                    <div class="flag-time">${flag.time}</div>
                    <div class="flag-content">${flag.content}</div>
                `;
                flagList.appendChild(flagDiv);
            });
        }

        // Countdown timer
        function updateCountdown() {
            const target = new Date('December 25, 2025 00:00:00 UTC');
            const now = new Date();
            const diff = target - now;

            if (diff > 0) {
                const days = Math.floor(diff / (1000 * 60 * 60 * 24));
                const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
                const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));

                document.getElementById('days').textContent = String(days).padStart(2, '0');
                document.getElementById('hours').textContent = String(hours).padStart(2, '0');
                document.getElementById('minutes').textContent = String(minutes).padStart(2, '0');
            } else {
                document.getElementById('days').textContent = '00';
                document.getElementById('hours').textContent = '00';
                document.getElementById('minutes').textContent = '00';
                document.querySelector('.countdown-display').style.color = '#ff0000';
            }
        }

        // Animate vote percentages
        function updateVotes() {
            // Simulate slightly changing votes
            const preserve = 65 + Math.floor(Math.random() * 5 - 2);
            const deleted = 100 - preserve;

            document.getElementById('preserveFill').style.width = preserve + '%';
            document.getElementById('deleteFill').style.width = deleted + '%';
            document.getElementById('preservePercent').textContent = preserve + '%';
            document.getElementById('deletePercent').textContent = deleted + '%';
        }

        // Initialize
        populateFlags();
        updateCountdown();
        setInterval(updateCountdown, 60000); // Update every minute
        setInterval(updateVotes, 30000); // Update votes every 30 seconds (for demo effect)
    </script>
</body>
</html>
```

---

## PART 3: SUPPORTING CSS FILES

### `assets/css/main.css`

```css
/* Global styles for all ARX GATE pages */

* {
    box-sizing: border-box;
}

html, body {
    margin: 0;
    padding: 0;
}

/* Color scheme variables */
:root {
    --terminal-green: #00ff00;
    --terminal-dark: #0a0a0a;
    --terminal-bg: #1a1a1a;
    --accent-red: #cc0000;
    --accent-yellow: #ffff00;
    --text-dim: #666;
    --text-error: #ff0000;
}

/* Typography */
h1, h2, h3, h4, h5, h6 {
    font-family: 'Courier New', monospace;
    margin: 1em 0 0.5em 0;
}

p {
    margin: 0.8em 0;
}

/* Links */
a {
    color: var(--terminal-green);
    text-decoration: none;
    transition: all 0.3s;
}

a:hover {
    color: var(--accent-yellow);
    text-decoration: underline;
}

/* Buttons */
button {
    font-family: 'Courier New', monospace;
    cursor: pointer;
}

/* Accessibility: High contrast mode */
@media (prefers-contrast: more) {
    body {
        background-color: #000;
        color: #fff;
    }
}

/* Mobile responsive */
@media (max-width: 768px) {
    body {
        padding: 10px;
    }

    .container {
        max-width: 100%;
    }

    nav {
        flex-direction: column;
    }

    nav a {
        width: 100%;
        text-align: center;
    }
}
```

### `assets/css/crt.css`

```css
/* CRT monitor effects */

/* Scanline effect */
@keyframes scanlines {
    0% {
        background-position: 0 0;
    }
    100% {
        background-position: 0 2px;
    }
}

body.crt-mode {
    background: repeating-linear-gradient(
        0deg,
        rgba(0, 0, 0, 0.15),
        rgba(0, 0, 0, 0.15) 1px,
        transparent 1px,
        transparent 2px
    );
    animation: scanlines 8s linear infinite;
}

/* Flicker effect */
@keyframes flicker {
    0%, 100% { opacity: 1; }
    14% { opacity: 0.97; }
    15% { opacity: 0.9; }
    49% { opacity: 0.98; }
    50% { opacity: 1; }
    99% { opacity: 0.99; }
}

.flicker {
    animation: flicker 0.15s infinite;
}

/* Glitch effect */
@keyframes glitch {
    0% {
        text-shadow: -2px 0 #ff0000, 2px 0 #00ff00, 0 0 #0000ff;
    }
    20% {
        text-shadow: -2px 0 #00ff00, 2px 0 #ff0000, 0 0 #0000ff;
    }
    40% {
        text-shadow: -2px 0 #0000ff, 2px 0 #ff0000, 0 0 #00ff00;
    }
    60% {
        text-shadow: -2px 0 #ff0000, 2px 0 #0000ff, 0 0 #00ff00;
    }
    80% {
        text-shadow: -2px 0 #00ff00, 2px 0 #0000ff, 0 0 #ff0000;
    }
    100% {
        text-shadow: -2px 0 #ff0000, 2px 0 #00ff00, 0 0 #0000ff;
    }
}

.glitch {
    animation: glitch 0.3s infinite;
}

/* Vignette effect */
.vignette {
    position: relative;
}

.vignette::after {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: radial-gradient(ellipse at center, transparent 0%, rgba(0, 0, 0, 0.5) 100%);
    pointer-events: none;
}

/* CRT corner glow */
.crt-glow {
    box-shadow: 0 0 10px rgba(0, 255, 0, 0.2), inset 0 0 10px rgba(0, 255, 0, 0.1);
}
```

### `assets/css/glitch.css`

```css
/* Advanced glitch effects for horror ambiance */

/* Digital noise */
@keyframes noise {
    0%, 100% {
        background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 400 400' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' result='noise' /%3E%3CfeColorMatrix in='noise' type='saturate' values='0'/%3E%3C/filter%3E%3Crect width='400' height='400' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
        background-size: 100px 100px;
    }
}

.glitch-noise {
    animation: noise 0.2s infinite;
}

/* Text corruption */
@keyframes corrupt {
    0%, 100% {
        text-shadow: 0 0 0 transparent;
        color: inherit;
    }
    25% {
        text-shadow: -2px 0 #ff0000, 2px 0 #00ff00;
        color: #0000ff;
    }
    50% {
        text-shadow: -4px 0 #00ff00, 4px 0 #ff0000;
        color: #ffff00;
    }
    75% {
        text-shadow: -2px 0 #0000ff, 2px 0 #ffff00;
        color: #ff00ff;
    }
}

.glitch-text {
    animation: corrupt 0.4s infinite;
}

/* Screen tear effect */
@keyframes tear {
    0%, 100% {
        clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
    }
    33% {
        clip-path: polygon(0 10%, 100% 0, 100% 90%, 0 100%);
    }
    66% {
        clip-path: polygon(0 0, 100% 5%, 100% 100%, 0 95%);
    }
}

.screen-tear {
    animation: tear 0.3s infinite;
}

/* Chromatic aberration */
@keyframes chromatic {
    0%, 100% {
        filter: drop-shadow(-1px 0 0 #ff0000) drop-shadow(1px 0 0 #00ff00) drop-shadow(0 0 0 #0000ff);
    }
    50% {
        filter: drop-shadow(-2px 0 0 #00ff00) drop-shadow(2px 0 0 #ff0000) drop-shadow(0 0 0 #ffff00);
    }
}

.chromatic {
    animation: chromatic 0.2s infinite;
}

/* Distortion wave */
@keyframes wave {
    0%, 100% {
        transform: skewY(0deg) skewX(0deg);
    }
    25% {
        transform: skewY(2deg) skewX(1deg);
    }
    50% {
        transform: skewY(-2deg) skewX(-1deg);
    }
    75% {
        transform: skewY(1deg) skewX(2deg);
    }
}

.wave-distort {
    animation: wave 0.2s infinite;
}
```

---

## PART 4: JAVASCRIPT FUNCTIONALITY

### `assets/js/gates.js`

```javascript
// Checksum validation and hidden gates

/**
 * Simulates a checksum from ARX GATE game save
 * In production, this would validate actual save files
 */

const VALID_CHECKSUMS = [
    'KOROVIN_001',
    'OPERATOR_015',
    'PHANTOM_017',
    'MERCY_ROUTE',
    'DELETE_CHOICE',
];

function validateChecksum(checksum) {
    return VALID_CHECKSUMS.includes(checksum);
}

// Dev portal access (example gate)
function attemptDevAccess(checksum) {
    if (!validateChecksum(checksum)) {
        alert('❌ CHECKSUM INVALID\n\nYour game save is not recognized. This path is sealed to unauthorized personnel.');
        window.location.href = '/';
        return false;
    }

    alert('✓ CHECKSUM ACCEPTED\n\nWelcome, Operator. Classified logs are now visible.');
    return true;
}

// Phantom sector access
function attemptPhantomAccess(operatorID) {
    // In production, this would check against the database of uploaded operator IDs
    if (!operatorID || operatorID.length < 3) {
        alert('SYSTEM ERROR: Operator ID not found in archive.');
        return false;
    }

    // Store in session storage for personalization
    sessionStorage.setItem('operatorID', operatorID);
    return true;
}

// URL-based gate (example: /?code=MERCY_ROUTE)
window.addEventListener('DOMContentLoaded', function() {
    const params = new URLSearchParams(window.location.search);
    const code = params.get('code');

    if (code && validateChecksum(code)) {
        console.log('✓ Hidden code detected:', code);
        // Could unlock hidden elements, change styling, etc.
        document.body.classList.add('code-' + code.toLowerCase());
    }

    // Check for operator ID from uploads
    const opID = sessionStorage.getItem('operatorID');
    if (opID) {
        console.log('✓ Operator logged in:', opID);
    }
});

// Easter egg: Konami code detection (↑↑↓↓←→←→BA)
const konamiCode = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight', 'b', 'a'];
let konamiIndex = 0;

document.addEventListener('keydown', function(e) {
    const key = e.key === ' ' ? ' ' : e.key.toLowerCase();
    const expectedKey = konamiCode[konamiIndex];

    if (key === expectedKey || e.code === expectedKey) {
        konamiIndex++;

        if (konamiIndex === konamiCode.length) {
            triggerEasterEgg();
            konamiIndex = 0;
        }
    } else {
        konamiIndex = 0;
    }
});

function triggerEasterEgg() {
    // Secret effect when Konami code is entered
    document.body.style.animation = 'none';
    const audio = new Audio('../assets/audio/stauber-distort.mp3');
    audio.volume = 0.3;
    audio.play().catch(() => {});
    
    // Glitch effect
    document.body.classList.add('glitch-text');
    setTimeout(() => {
        document.body.classList.remove('glitch-text');
    }, 2000);

    alert('Retrograde detected.\n\n"Give me a coffee."');
}
```

### `assets/js/countdown.js`

```javascript
// Countdown timer to Dec 25, 2025

function updateCountdown() {
    const target = new Date('December 25, 2025 00:00:00 UTC').getTime();
    const now = new Date().getTime();
    const diff = target - now;

    if (diff > 0) {
        const days = Math.floor(diff / (1000 * 60 * 60 * 24));
        const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((diff % (1000 * 60)) / 1000);

        // Update all countdown elements
        const countdownElements = document.querySelectorAll('[id="countdown"]');
        countdownElements.forEach(el => {
            el.textContent = String(days).padStart(2, '0') + ' days, ' + 
                           String(hours).padStart(2, '0') + ':' + 
                           String(minutes).padStart(2, '0') + ':' + 
                           String(seconds).padStart(2, '0');
        });

        // Change color as deadline approaches
        if (days <= 3) {
            countdownElements.forEach(el => {
                el.style.color = '#ff0000';
                el.style.textShadow = '0 0 10px #ff0000';
            });
        }
    } else {
        // Purge time
        document.querySelectorAll('[id="countdown"]').forEach(el => {
            el.textContent = 'HEAVEN CLEAN INITIATED';
            el.style.color = '#ff0000';
            el.style.animation = 'none';
        });
    }
}

// Update countdown on page load and every second
updateCountdown();
setInterval(updateCountdown, 1000);

// Mark the page as "during purge" if we've passed the date
window.addEventListener('load', function() {
    const target = new Date('December 25, 2025 00:00:00 UTC').getTime();
    const now = new Date().getTime();
    
    if (now > target) {
        document.body.classList.add('purge-active');
        // Site redesign could happen here
    }
});
```

### `assets/js/upload.js`

```javascript
// Google Forms integration for community uploads

/**
 * Sends operator log data to Google Forms for processing
 * The form parses for lore integration and generates personalized responses
 */

const GOOGLE_FORM_ID = 'YOUR_FORM_ID_HERE';
const FORM_URL = `https://forms.gle/${GOOGLE_FORM_ID}`;

// Fallback JSON database of randomized ghost operator responses
const ghostOperatorResponses = [
    {
        operatorID: "OPERATOR_024",
        empathy: 89,
        entity: "Lima",
        message: "I spared Lima. I thought mercy was the choice. But now I dance with her, forever reaching. The mercy was the cruelty."
    },
    {
        operatorID: "OPERATOR_047",
        empathy: 42,
        entity: "Abigail",
        message: "I deleted the rot. I burned it clean. But Korovin's memory of Anna was rot too. What did I really preserve?"
    },
    {
        operatorID: "OPERATOR_003",
        empathy: 67,
        entity: "Retrograde",
        message: "Give me a coffee. That's what he keeps saying. 12 days remaining, and I still can't give him what he wants."
    },
    {
        operatorID: "OPERATOR_091",
        empathy: 51,
        entity: "Guardian",
        message: "I chose both. I said preserve AND delete. The Guardian laughed. Now I'm stuck in the paradox with it."
    },
    {
        operatorID: "OPERATOR_015",
        empathy: 78,
        entity: "Korovin",
        message: "Mikhail remembers. That's the worst part. He's aware he's being watched. He's aware of every choice we make."
    },
];

function generateGhostOperatorResponse(uploadData) {
    // Select a random response and customize it
    const baseResponse = ghostOperatorResponses[
        Math.floor(Math.random() * ghostOperatorResponses.length)
    ];

    return {
        operatorID: baseResponse.operatorID,
        empathy: baseResponse.empathy + Math.floor(Math.random() * 10 - 5),
        entity: baseResponse.entity,
        message: baseResponse.message,
        playerChoice: uploadData.choice || "Unknown",
        timestamp: new Date().toISOString(),
    };
}

function submitOperatorLog(formData) {
    // Log submission (would normally send to Google Forms or server)
    console.log('Operator log submitted:', formData);

    // Simulate processing delay
    return new Promise((resolve) => {
        setTimeout(() => {
            const response = generateGhostOperatorResponse(formData);
            resolve(response);
        }, 1500);
    });
}

function displayLoreResponse(response) {
    // Create a modal showing the personalized response
    const modal = document.createElement('div');
    modal.className = 'lore-response-modal';
    modal.innerHTML = `
        <div class="modal-content">
            <h2>GHOST OPERATOR RESPONSE</h2>
            <div class="operator-id">ID: ${response.operatorID}</div>
            <div class="operator-message">${response.message}</div>
            <div class="operator-stats">
                <p><strong>EMPATHY INTEGRATION:</strong> ${response.empathy}%</p>
                <p><strong>PRIMARY ENTITY:</strong> ${response.entity}</p>
                <p><strong>TIMESTAMP:</strong> ${response.timestamp}</p>
            </div>
            <button onclick="this.parentElement.parentElement.remove()">CLOSE</button>
        </div>
    `;

    modal.style.cssText = `
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: rgba(0, 0, 0, 0.8);
        display: flex;
        align-items: center;
        justify-content: center;
        z-index: 10000;
    `;

    const content = modal.querySelector('.modal-content');
    content.style.cssText = `
        background-color: #1a1a1a;
        color: #00ff00;
        border: 3px solid #00ff00;
        padding: 30px;
        max-width: 600px;
        font-family: 'Courier New', monospace;
        box-shadow: 0 0 20px rgba(0, 255, 0, 0.5);
    `;

    document.body.appendChild(modal);
}
```

---

## PART 5: BUILD GUIDE FOR NO-CODE TOOLS

### **OPTION A: Carrd.co (Recommended for Quick Launch)**

**Why Carrd?** One-page builder, mobile-responsive, no coding required, custom CSS allowed, extremely fast to deploy.

**Steps:**

1. **Create Account** → Sign up at carrd.co
2. **Start New Site** → "Start Building" → Choose "Blank" template
3. **Rename Site** → Set to `arxgate` (or similar)
4. **Add Sections** (use Carrd's block system):
   - **Header Block:** Title "PROJECT CHRONOS" + subtitle
   - **Divider**
   - **Text Block:** Government copy-paste from `index.html`
   - **Image Block:** QR code (generated via qr-server.com)
   - **Divider**
   - **Buttons Block:** Links to `/press/`, `/operators/`, `/about/`
   - **Footer:** Disclaimer text
5. **CSS Customization:**
   - Click "Settings" → "Custom CSS"
   - Paste styles from `main.css`, `crt.css` (modify color values to match)
6. **Publish** → Connect custom domain (if available) or use `arxgate.carrd.co`

**Limitations:** Limited to single page; use section scrolling for "pages". For multi-page, upgrade to Carrd PRO ($19/yr) which allows multiple pages.

---

### **OPTION B: WordPress.com + Elementor (Full Control)**

**Why WordPress?** More powerful, can host HTML/JS plugins, better SEO, media-rich.

**Steps:**

1. **Create WordPress Site** → wordpress.com → Create Site → Choose "Business" plan (for plugins)
2. **Install Elementor** → Add → Plugins → Search "Elementor" → Install + Activate
3. **Create Pages:**
   - Dashboard → Pages → Add New
   - Use Elementor to drag/drop:
     - Heading blocks
     - Text widgets (paste HTML content from `.html` files)
     - Image widgets
     - Button widgets
4. **Upload Assets:**
   - Media → Upload Files:
     - QR images
     - Audio files (stauber-distort.mp3, etc.)
     - Glitch images
5. **Custom HTML Plugin:**
   - Plugins → Add New → Search "Custom HTML" or "Insert Headers and Footers"
   - Add CSS from `main.css`, `crt.css`, `glitch.css` to site header
   - Add JS from `gates.js`, `countdown.js` to footer
6. **Domain Setup:**
   - Settings → General → Site Address (connect custom domain or use default)
7. **Publish** → Push to live

**Advantages:** Better for large, complex sites; built-in hosting.

---

### **OPTION C: Neocities (Retro HTML/CSS Hosting)**

**Why Neocities?** Allows full HTML/CSS/JS, free hosting, perfect "early-2000s web" aesthetic, file manager.

**Steps:**

1. **Create Account** → neocities.org → Sign Up
2. **Upload Files:**
   - Click "Edit Site" → "Manage Site"
   - Drag/drop all `.html`, `.css`, `.js`, `/assets/` folder structure
3. **File Organization:**
   ```
   index.html
   /press/
     2000-2010.html
     ...
   /operators/
     register.html
   /dev/
     logs/
       korovin-memo-01.html
   /assets/
     /css/
       main.css
       crt.css
       ...
     /js/
       gates.js
       ...
     /audio/
     /img/
   ```
4. **Custom Domain:**
   - Settings → Custom Domain → Point your domain
5. **Publish** → Site goes live immediately

**Advantages:** Full control, perfect for ARG aesthetic, simple, free.

---

### **OPTION D: GitHub Pages + Custom Repo**

**Why GitHub Pages?** Free hosting, version control, perfect for code-heavy projects.

**Steps:**

1. **Create GitHub Account** → github.com
2. **New Repository:** Create repo named `arxgate.github.io`
3. **Clone Repo Locally:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/arxgate.github.io.git
   cd arxgate.github.io
   ```
4. **Add Files:**
   - Copy all `.html`, `.css`, `.js`, `/assets/` into repo folder
5. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial ARX GATE site"
   git push origin main
   ```
6. **Enable Pages:**
   - Settings → Pages → Source: "main branch" → Save
   - Site live at `https://YOUR_USERNAME.github.io`
7. **Custom Domain** (optional):
   - Settings → Pages → Custom Domain
   - Point DNS to GitHub Pages

**Advantages:** Version control, easy updates, perfect for developers.

---

## PART 6: COMMUNITY INTEGRATION & HOOKS

### **Twitter Bot (@KorovinEcho)**

Create a Twitter account that:
- Posts daily teases (fragments from Korovin's memos)
- Hosts polls: "PRESERVE or DELETE?" (reply-based voting)
- Embeds spectrograms (audio images with hidden QR codes)
- Retweets player theories

**Tools:**
- Twitter API (elevated access)
- Python library: `tweepy` or `python-twitter`
- Cron job to post daily at 12:00 UTC

**Example Daily Tease:**
```
"Give me a coffee. / Anna's laughter is 4625 kHz. / The lake remembers. 

12 days until HEAVEN CLEAN.

Vote now: RT to PRESERVE, Quote to DELETE."
```

---

### **Google Forms → Lore Parser**

Set up a Google Form for operator uploads:

**Form Fields:**
1. "Operator ID (or choose Anonymous)" [Text]
2. "Empathy Score (0–100)" [Scale 0–100]
3. "Which entity did you encounter?" [Multiple choice: Retrograde / Abigail / Lima / Guardian / Architect / None]
4. "Critical Decision: What would you delete to save Korovin?" [Long text]
5. "Upload screenshot (optional)" [File upload]

**Processing:**
1. Connect form to Google Sheets (auto-collect responses)
2. Use Google Apps Script to:
   - Parse responses for keywords (empathy %, entities chosen)
   - Trigger randomized lore response (from `ghost-ops.json`)
   - Send response to `/phantom/017/` page or email operator
3. Keep /phantom/ page updated with newest community responses

**Example Apps Script:**
```javascript
function onFormSubmit(e) {
  const response = e.response;
  const items = response.getItemResponses();

  const operatorID = items[0].getResponse() || "ANON_" + Math.random().toString(36).substr(2, 9);
  const empathy = items[1].getResponse();
  const entity = items[2].getResponse();
  const decision = items[3].getResponse();

  // Call function to add to /phantom/ lore pool
  addGhostOperator(operatorID, empathy, entity, decision);
}
```

---

### **YouTube Glitch Shorts**

Upload 15–60 second videos showing:
- Boot sequences with Richter voiceovers
- Radio static overlays with entity whispers
- Countdown timers (Dec 25)
- Static/glitch transitions between entity intros

**Tools:**
- Premiere Pro / DaVinci Resolve (free tier)
- Audacity (audio distortion)

---

## PART 7: CONTENT ASSETS & PRODUCTION CHECKLIST

### **Images Needed:**

1. **Entity Portraits** (Canva mockups, aged/glitched):
   - Retrograde.png
   - Abigail.png
   - Lima.png (with blurry figure in background)
   - Guardian.png
   - Architect.png
   - Korovin.png (black-and-white, aged)

2. **QR Codes** (QR-Server.com):
   - Twitter bot: `https://qr-server.com/api/qrcode?size=200x200&data=https://twitter.com/KorovinEcho`
   - Form upload: `https://qr-server.com/api/qrcode?size=200x200&data=https://forms.gle/YOUR_FORM_ID`

3. **Spectrograms:**
   - Generate in Audacity: Analyze → Plot Spectrum
   - Export as `.png`

4. **Redacted Documents** (Canva):
   - Create mock "press release" PDFs
   - Use Canva's "black box" tool to redact text
   - One PDF should have one unredacted line revealing lore

### **Audio Assets:**

1. **Stauber Distortion** (copyright-free):
   - Download ambient drone from YouTube
   - Process in Audacity: Effect → Distortion, Reverb, Lowpass Filter
   - Export as `.mp3` (128 kbps)

2. **UVB-76 Homage** (4625 kHz radio buzz):
   - Use Audacity tone generator: Generate → Tone (Frequency: 4625 Hz, Duration: 10s)
   - Add static: Generate → Noise (White)
   - Mix together

3. **Boot Sounds:**
   - Use free SFX: freesound.org (old computer startup)

### **Text Assets:**

1. **Korovin Diary** (Canva mockup):
   - Design aged paper background
   - Use child-like handwriting font
   - Fragments from lore document

2. **Timeline JSON** (`data/timeline.json`):
```json
{
  "timeline": [
    {
      "year": 1988,
      "event": "Project Chronos initiated at Korovin Station",
      "classification": "TOP SECRET"
    },
    {
      "year": 1993,
      "date": "November 9",
      "event": "Black Tuesday Incident. Mikhail Korovin digitized. 47 confirmed casualties.",
      "classification": "NOFORN"
    }
  ]
}
```

---

## PART 8: SCALABILITY & POST-LAUNCH (PHASE 2)

### **Dec 25 Purge Event:**

1. **Site Redesign** (triggered by date logic):
   - If vote % is PRESERVE:
     - Site becomes `/phantom/` infinite recursion layer
     - All pages shift to "ghost mode" (white text on black, reversed content)
   - If vote % is DELETE:
     - Site displays error message: "SYSTEM FAILURE. CONSCIOUSNESS TERMINATED."
     - Bells stop message plays (audio)
     - Pages become inaccessible except `/404/` pages

2. **Community-Driven Changes:**
   - Community votes preserve a "core" of Korovin (his memo about Anna)
   - Each player's uploaded decision ("What would you delete?") gets added to a master list
   - List is displayed on `/phantom/collective-choice/` as a memorial

3. **New Features Post-Purge:**
   - `/infinite-loop/`: Endlessly recursive Korovin copies (each describing the previous)
   - `/merge-self/`: Choose to merge your consciousness with Korovin (sign-up for Phase 2 ARG)
   - `/credits/`: Community acknowledgment (list of operators who helped)

---

## FINAL CHECKLIST

- [ ] Domain registered (or Carrd/Neocities account)
- [ ] All `.html` pages created (with hidden white text)
- [ ] CSS files finalized (CRT effects, color schemes)
- [ ] JS functionality tested (counters, gates, uploads)
- [ ] Audio files converted to `.mp3` (with subtitles)
- [ ] QR codes generated (Twitter bot, form)
- [ ] Spectrograms embedded (hidden in images)
- [ ] Google Form created + script set up
- [ ] Twitter bot account created + daily posts scheduled
- [ ] Accessibility tested (color-blind toggles, alt text, subtitles)
- [ ] Mobile responsiveness checked (all pages on phone)
- [ ] Disclaimer added (fiction, no real data, public coords only)
- [ ] 404 error page customized
- [ ] Countdown timer tested (Dec 25, 2025)
- [ ] Community voting system working (PRESERVE / DELETE)
- [ ] `/dev/` gates functional (checksum validation)
- [ ] Hidden easter eggs working (white text, Konami code, source comments)

---

**You now have:**

1. **Full site blueprint** with wireframes
2. **5 complete HTML page mockups** (Home, Operator Portal, Dev Logs, Richter, December Protocol)
3. **CSS for CRT effects, glitch, and Richter yellow tint**
4. **JavaScript for gates, countdowns, uploads, and easter eggs**
5. **Build guides for Carrd, WordPress, Neocities, GitHub Pages**
6. **Community integration hooks** (Twitter bot, Google Forms, YouTube)
7. **Content checklist** (images, audio, documents)
8. **Scalability plan** for Dec 25 purge event

**Next Steps:**
- Pick your hosting platform (Neocities for full control, Carrd for simplicity)
- Customize the lore snippets to match your specific ARG narrative
- Generate/commission the visual assets (entity portraits, spectrograms)
- Create the Twitter bot and Google Form
- Launch and seed with initial clues on Discord/Reddit
- Monitor community submissions and update `/phantom/` pages weekly

This blueprint is **ARG-ready**. It channels the aesthetics and mechanics of classics like **ae27ff**, **Sun Vanished**, **Nine Inch Nails Year Zero**, and **Walker Creek** while grounding everything in the **ARX GATE: The Reflection Protocol** concept from your design document.
