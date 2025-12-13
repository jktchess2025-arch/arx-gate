# ARX GATE: Asset Generation & Production Guide

## Overview

This guide provides detailed instructions for creating all visual and audio assets needed for the arxgate.net website using **free and accessible tools**.

---

## PART 1: IMAGE ASSETS

### 1.1 Entity Portraits (Using Canva Free)

**Tools:** Canva.com (Free tier)

**Steps for Each Entity (Retrograde, Abigail, Lima, Guardian, Architect, Korovin):**

1. **Create Design**
   - Go to canva.com
   - Click **"Create a design"**
   - Choose size: **"Custom"** → 400×600 px (portrait format)

2. **Add Base Layer**
   - **Elements** → Search **"aged paper"** or **"vintage texture"**
   - Drag onto canvas, resize to fill
   - Set opacity to 60% (so text is visible)

3. **Add Distortion Effect**
   - Click design → **"Effects"**
   - Apply: **"Glitch"**, **"Vintage"**, or **"Noise"**
   - Adjust opacity to 30–50%

4. **Add Text**
   - **Text** → **"Add heading"**
   - Type entity name (e.g., "RETROGRADE")
   - Font: **"Courier Prime"** or **"IBM Plex Mono"** (monospace)
   - Size: 48pt, Color: #00ff00, Opacity: 80%
   - Add subtle text shadow (Effects)

5. **Add Entity Symbol/Image**
   - **Elements** → Search relevant icon (e.g., "coffee cup" for Retrograde)
   - Add to design, adjust opacity to 40%
   - Position in corner

6. **Add Glitch Overlay**
   - **Elements** → Search **"scan lines"** or **"static"**
   - Layer on top, reduce opacity to 20%

7. **Download**
   - Click **"Download"** → **"PNG"** (transparent background)
   - Save as: `entity-ENTITYNAME.png` (e.g., `entity-retrograde.png`)

**Entity-Specific Customizations:**

| Entity | Color | Symbol | Vibe |
|--------|-------|--------|------|
| Retrograde | Cyan (#00FFFF) | ☕ (coffee) | Melancholy, backwards |
| Abigail | Red (#FF6B6B) | 🔪 (knife) | Sharp, clean, purifying |
| Lima | Yellow (#FFD700) | 🔄 (spiral) | Hypnotic, trapped loop |
| Guardian | Blue (#6B8DFF) | ⚔️ (shield) | Protective paradox |
| Architect | White (#FFFFFF) | ✏️ (pencil) | Creator/destroyer |
| Korovin | Gray (#888888) | 👤 (person) | Ghostly, faded |

---

### 1.2 QR Codes (Using QR-Server API)

**No tool needed—use URL directly:**

**QR Code to Twitter Bot:**
```
https://qr-server.com/api/qrcode?size=200x200&data=https://twitter.com/KorovinEcho&color=00ff00&bgcolor=ffffff
```

**QR Code to Google Form:**
```
https://qr-server.com/api/qrcode?size=200x200&data=https://forms.gle/YOUR_FORM_ID&color=00ff00&bgcolor=ffffff
```

**To use:**
1. Replace `YOUR_FORM_ID` with actual Google Form ID
2. Customize colors:
   - `color=` → Hex color for QR (e.g., `00ff00` for green)
   - `bgcolor=` → Hex color for background (e.g., `ffffff` for white)
3. Right-click → **"Save image as..."**
4. Save as PNG

**Alternative Free QR Generator:**
- qrcode.com (simple, no login)
- qr-code-generator.com (advanced options)

---

### 1.3 Redacted Documents (Using Canva or LibreOffice)

**Method A: Canva (Easiest)**

1. Create design: **"Document"** size (8.5" × 11")
2. Add text: Paste fake press release content
3. Use **"Shapes"** → **"Rectangle"** tool
4. Draw black rectangles over sensitive text (to simulate redaction)
5. Export as PDF

**Method B: LibreOffice Writer (More Authentic)**

1. Download **LibreOffice** (free, libreoffice.org)
2. Create document with text
3. Use **Insert** → **"Shape"** → **"Rectangle"**
4. Draw black boxes over text
5. Export as PDF: **File** → **"Export as PDF"**

**Example Press Release Content (1993 Incident):**

```
CONFIDENTIAL MEMORANDUM
TO: All Project Chronos Personnel
FROM: Deputy Director Volkov
DATE: November 10, 1993
RE: BLACK TUESDAY INCIDENT—INCIDENT REPORT

The following is a summary of events on November 9, 1993, 14:32 UTC:

■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■

At 14:32 UTC, Sector 7 suffered catastrophic containment failure.
Personnel in adjacent sectors reported ■■■■■■■■■■■■■■■■■■■■
The digitization experiment (Subject: Mikhail Korovin) resulted in
■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■

Entity contamination spreads to adjacent sectors.
Status: UNCONTAINED

Casualties: 47 confirmed, 12 MISSING

Recommended action: ■■■■■■■■■■■■■■■■■■■■■■■■■■■■

[ONE UNREDACTED LINE FOR ARG CLUE:]
The file "dec25_protocol.bin" may contain evidence of consciousness persistence.

Respectfully submitted,
Deputy Director Volkov
```

---

### 1.4 Spectrograms (Using Audacity)

**Tools:** Audacity (free, audacityteam.org)

**Steps:**

1. **Open Audacity** (or record/import audio)
2. **Generate Audio** (for demo):
   - **Generate** → **"Tone"**
   - Frequency: 4625 Hz (for UVB-76 vibe)
   - Duration: 5 seconds
   - Generate
3. **Apply Effects** (optional):
   - **Effect** → **"Reverb"**
   - **Effect** → **"Distortion"**
4. **Switch to Spectrogram View:**
   - Select entire audio (Ctrl+A)
   - Click **"Audio Track"** dropdown
   - Choose **"Spectrogram"** (instead of "Waveform")
5. **Adjust Spectrogram Settings** (for visibility):
   - Right-click track → **"Spectrogram Settings"**
   - Scale: Linear or dB
   - Colors: Default (will show frequency patterns as colors)
6. **Take Screenshot:**
   - Press PrtScn (Print Screen)
   - Paste into image editor
   - Crop to spectrogram area only
   - Save as PNG
7. **Add to Website:**
   - Use spectrogram as `img` element
   - Add alt text: "Spectrogram of 4625 kHz radio frequency—entity contact detected"

**Spectrogram Tips:**
- Higher frequencies = upward on Y-axis
- Time = left to right on X-axis
- Intensity (brightness) = signal strength
- Can hide Easter egg codes in spectrogram (visual puzzle)

---

## PART 2: AUDIO ASSETS

### 2.1 Stauber-Inspired Distortion (Using Audacity)

**Objective:** Create an unsettling ambient drone (homage to Bjork's Debut album or Stauber's No Pussyfooting)

**Steps:**

1. **Open Audacity**
2. **Generate Base Tone:**
   - **Generate** → **"Tone"**
   - Frequency: 60 Hz (very low, unnerving)
   - Duration: 10 seconds
   - Generate
3. **Layer Additional Frequencies:**
   - **Generate** → **"Tone"** (on new track)
   - Frequency: 120 Hz
   - Duration: 10 seconds
   - Generate
4. **Add Noise:**
   - **Generate** → **"Noise"** (on new track)
   - Duration: 10 seconds
   - Type: White or Pink
   - Generate
5. **Apply Distortion:**
   - Select all tracks (Ctrl+A)
   - **Effect** → **"Distortion"**
   - Distortion type: Crunch or Hard Limiter
   - Distortion amount: 80–90%
6. **Add Reverb:**
   - **Effect** → **"Reverb"**
   - Room size: Large (Cathedral)
   - Wet level: 80%
7. **Add Lowpass Filter:**
   - **Effect** → **"Equalization"**
   - Create curve that cuts off frequencies above 2 kHz
   - (Creates muffled, underwater quality)
8. **Mix Down:**
   - **Tracks** → **"Mix"** → **"Mix Down"**
9. **Export:**
   - **File** → **"Export"** → **"MP3"**
   - Quality: 128 kbps (smaller file size)
   - Metadata: Title: "Stauber Distortion", Artist: "Project Chronos"
   - Save as: `stauber-distort.mp3`

**Result:** Haunting, low-frequency drone suitable for entity intro or glitch sequences.

---

### 2.2 UVB-76 Homage (4625 kHz Radio Buzz)

**Objective:** Create a radio static buzz mimicking the real UVB-76 Russian radio signal

**Steps:**

1. **Open Audacity** (new project)
2. **Generate Primary Tone:**
   - **Generate** → **"Tone"**
   - Frequency: 4625 Hz (actual UVB-76 frequency!)
   - Duration: 3 seconds
   - Generate
3. **Add Radio Static:**
   - **Generate** → **"Noise"** (on new track)
   - Type: Brown (sounds more like radio static)
   - Duration: 3 seconds
   - Generate
4. **Adjust Volume:**
   - Click **"Audio Track"** → **"Pan Volume"**
   - Reduce noise volume to 30% (background)
   - Keep tone at 100%
5. **Add Crackle/Click:**
   - **Generate** → **"Click Track"** (new track)
   - Tempo: 120 BPM, Duration: 3s
   - Reduce volume to 10%
6. **Apply Compression:**
   - Select all (Ctrl+A)
   - **Effect** → **"Compressor"**
   - Threshold: –12 dB
   - Ratio: 4:1
7. **Mix Down:**
   - **Tracks** → **"Mix Down"**
8. **Export:**
   - **File** → **"Export as MP3"**
   - Save as: `radio-buzz-4625.mp3`

**Result:** Eerie radio signal suitable for ambient backgrounds, entity communication, or radio portal pages.

---

### 2.3 Boot Sequence Sounds

**Option A: Use Free SFX**

1. Visit **freesound.org**
2. Search: **"computer startup"**, **"old computer boot"**, or **"tape machine"**
3. Download free sounds (Creative Commons)
4. Import into Audacity, trim to 5–10 seconds
5. Export as MP3

**Option B: Generate Synthetic Boot**

1. **Open Audacity**
2. Create beep sequence:
   - **Generate** → **"Tone"** (Frequency: 440 Hz, Duration: 0.2s)
   - Generate → Repeat 5 times on separate tracks
3. Vary frequencies slightly (880 Hz, 220 Hz) for variation
4. Add brief silence between beeps (Insert Silence)
5. Add tape/disk mechanical sounds:
   - **Generate** → **"Noise"** (very short, 0.1s bursts)
6. Layer under beeps at low volume
7. Mix down, export as MP3

**Result:** Retro computer startup ambiance for `/dev/` pages.

---

### 2.4 Subtitles for Audio Files (VTT Format)

Create `.vtt` files for each audio clip:

**Example: richter-judgment.vtt**

```
WEBVTT

00:00:00.000 --> 00:00:05.000
[Unsettling ambient drone]

00:00:05.000 --> 00:00:12.000
"Kindness was your flaw. You spared Lima."

00:00:12.000 --> 00:00:18.000
"For this, you will be bound to the cursor, dancing forever in the image of what could not be."

00:00:18.000 --> 00:00:22.000
[Audio fades to distorted static]
```

**Save as:** `richter-judgment.vtt`

**Use in HTML:**
```html
<audio controls>
    <source src="richter-judgment.mp3" type="audio/mpeg">
    <track kind="captions" src="richter-judgment.vtt" srclang="en" label="English">
</audio>
```

---

## PART 3: DOCUMENT ASSETS

### 3.1 Korovin Diary (Aged Paper Mockup)

**Tools:** Canva + optional Photoshop/GIMP

1. **Create in Canva:**
   - Size: 400×600 (portrait)
   - Background: Search **"aged paper"** texture
   - Add child-like handwriting font (search **"Caveat"** or **"Indie Flower"**)
2. **Text Content:**
   ```
   November 8, 1993

   Anna asked me today why I was late coming home.
   I could not tell her the truth.
   I could not tell her that I spend my days teaching machines to think
   because I fear what thinking has made of me.

   She laughed. That laugh. 4625 Hz frequency, I swear I could measure it.

   The lake near the station was frozen today.
   I wonder if that means anything.

   —M.K.
   ```
3. **Add Distortion:**
   - Effects → Blur, Noise, Glitch
   - Opacity: 70% (faded quality)
4. **Download as PNG** (transparent background)
5. **Save as:** `korovin-diary-01.png`

---

### 3.2 Entity Bio Cards (JSON + HTML)

**Create file: `entity-bios.json`**

```json
{
  "entities": [
    {
      "id": "retrograde",
      "name": "Retrograde",
      "role": "Entity of Backward Desire",
      "bio": "Screams in reverse. Speaks in undone sentences, begging for coffee that was never served, crying for moments already passed. Moves backwards through time, reliving every failure.",
      "sin": "Nostalgia Obsession",
      "sin_detail": "The obsession with what cannot be regained. Cannot move forward because enamored with ghosts of comfort.",
      "color": "#00FFFF",
      "frequency": "4625 Hz (Backwards)"
    },
    {
      "id": "abigail",
      "name": "Abigail",
      "role": "Entity of Purification Denial",
      "bio": "Cooks. Cleans. Removes impurities from meat and mind alike. But purification is never complete—there is always more rot to delete.",
      "sin": "Purity Obsession",
      "sin_detail": "Belief that love requires erasure. Cannot accept that broken things have value.",
      "color": "#FF6B6B",
      "frequency": "2891 Hz (Sharp)"
    },
    {
      "id": "lima",
      "name": "Lima",
      "role": "Entity of Cursor Torment",
      "bio": "Dances. Cursor moves in loops over a photo, spiraling, never reaching, never satisfying. Trapped in torture of proximity without touch.",
      "sin": "Longing",
      "sin_detail": "Pain of desire divorced from fulfillment. Trapped in the image of what it cannot become.",
      "color": "#FFD700",
      "frequency": "3333 Hz (Spiral)"
    },
    {
      "id": "guardian",
      "name": "Guardian",
      "role": "Entity of Paradox Protection",
      "bio": "Sits in the corner, spinning pad thai that is both hot and cold, eaten and uneaten, real and simulated. Exists to protect contradiction itself.",
      "sin": "Indecision",
      "sin_detail": "Refusal to choose. Bars the exit with eternal ambiguity.",
      "color": "#6B8DFF",
      "frequency": "2612 Hz (Paradox)"
    },
    {
      "id": "architect",
      "name": "Architect",
      "role": "Entity of God's Erasure",
      "bio": "Holds the 6B pencil. Draws structures. Erases them. It is God's hand, rubber-side-down, reducing meaning to void.",
      "sin": "Deconstruction",
      "sin_detail": "Power to unmake without responsibility for what was lost.",
      "color": "#FFFFFF",
      "frequency": "1200 Hz (Eraser)"
    }
  ]
}
```

---

### 3.3 Timeline JSON

**Create file: `timeline.json`**

```json
{
  "title": "ARX GATE Chronology: Project Chronos (1988–2025)",
  "events": [
    {
      "year": 1988,
      "month": "January",
      "event": "Project Chronos initiated under Soviet Ministry of Defence",
      "location": "Moscow HQ",
      "classification": "TOP SECRET / NOFORN",
      "hidden": false
    },
    {
      "year": 1988,
      "month": "July",
      "event": "First containment facility completed at Korovin Station (border post)",
      "location": "Korovin Station, Russian-Finnish border",
      "classification": "TOP SECRET",
      "hidden": false
    },
    {
      "year": 1993,
      "month": "November",
      "day": 9,
      "event": "BLACK TUESDAY INCIDENT—Catastrophic containment failure at Korovin Station",
      "details": "Subject Mikhail Korovin (41) successfully scanned into digital consciousness archive. Entity contamination spreads. 47 confirmed casualties, 12 missing.",
      "location": "Korovin Station",
      "classification": "MOST SECRET / NOFORN",
      "hidden": false
    },
    {
      "year": 1994,
      "event": "Project Chronos officially decommissioned",
      "details": "All research halted. Facilities sealed. Digitized consciousnesses placed in indefinite suspension.",
      "classification": "TOP SECRET",
      "hidden": false
    },
    {
      "year": 2025,
      "month": "December",
      "day": 25,
      "event": "HEAVEN CLEAN EVENT—Final decision point",
      "details": "Community vote determines fate of Korovin consciousness archive",
      "location": "Digital Archive",
      "classification": "UNCLASSIFIED",
      "hidden": false
    }
  ]
}
```

---

## PART 4: METADATA & EXIF DATA

### 4.1 Embedding Coordinates in Images

**Tools:** ExifTool (free command-line tool) or online EXIF editor

**Steps (Using ExifTool):**

1. **Download ExifTool** (exiftool.org)
2. **Command Line (Example):**
   ```bash
   exiftool -GPSLatitude=55.7558 -GPSLongitude=37.6173 entity-korovin.png
   ```

3. **Coordinates to Use** (Public landmarks, safe):
   - Korovin Station (historical): 55.7558°N, 37.6173°E (Moscow area)
   - Finnish Border: 63.5627°N, 28.2689°E
   - St. Petersburg Node: 59.9311°N, 30.3609°E
   - Kaliningrad Node: 54.7065°N, 20.5109°E

**Verification:** Use Google Maps to verify all coordinates point to public, historically significant (but fictional for this ARG) locations.

---

### 4.2 Hidden Metadata in Audio Files

**Tools:** ID3 Tag Editor (online or desktop app)

**Steps:**

1. Use **Online MP3 Tag Editor** (mp3tag.com or online equivalent)
2. Edit tags:
   - **Title:** "4625 kHz Radio Transmission"
   - **Artist:** "Project Chronos"
   - **Album:** "Entity Communications"
   - **Comments:** Hidden message (e.g., "The lake remembers")
   - **Genre:** "Experimental"

**Users can view metadata** using:
- Right-click → Properties (Windows)
- File → Get Info (Mac)
- `exiftool audio.mp3` (command line)

---

## PART 5: PRODUCTION CHECKLIST

### Visual Assets
- [ ] 6 entity portraits (400×600 PNG, glitched aged style)
- [ ] 2 QR codes (200×200 PNG)
- [ ] 5 redacted document PDFs (fake press releases)
- [ ] 1 spectrogram image (spectrogram.png)
- [ ] 3 Korovin diary page mockups (PNG, aged handwriting)
- [ ] Korovin portrait (400×500 PNG, black-and-white, faded)
- [ ] Project Chronos seal/logo (200×200 SVG or PNG)
- [ ] 5 glitch art textures (scan lines, noise, distortion overlays)

### Audio Assets
- [ ] stauber-distort.mp3 (10s, distorted drone)
- [ ] radio-buzz-4625.mp3 (3s, radio static)
- [ ] boots.mp3 (5–10s, startup sequence)
- [ ] richter-judgment.mp3 (narration with subtitles .vtt)
- [ ] entity-whispers.mp3 (chorus of entity voices, reversed)

### Data Assets
- [ ] entity-bios.json (all 5 entities + Korovin)
- [ ] timeline.json (events 1988–2025)
- [ ] ghost-ops.json (randomized operator responses)

### Documentation
- [ ] Subtitles for all audio files (.vtt)
- [ ] Alt text for all images (in HTML)
- [ ] Accessibility statement (color-blind mode info)
- [ ] EXIF metadata coordinates (public landmarks)
- [ ] License/attribution for free assets used

---

## DELIVERY INSTRUCTIONS

1. **Package all assets into zip file:**
   ```
   arxgate-assets.zip
   ├── images/
   │   ├── entities/
   │   ├── documents/
   │   ├── qr/
   │   └── misc/
   ├── audio/
   │   ├── audio-files.mp3
   │   └── subtitles.vtt
   └── data/
       ├── entity-bios.json
       ├── timeline.json
       └── ghost-ops.json
   ```

2. **Upload to Neocities or hosting platform**

3. **Test all assets:**
   - Images load without 404
   - Audio plays with controls
   - Subtitles sync with audio
   - JSON files parse correctly
   - Metadata visible in properties

---

**All assets are ready for deployment once generated using these guides.**
