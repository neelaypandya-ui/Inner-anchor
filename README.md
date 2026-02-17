# Inner Anchor

App available at: https://inner-anchor.netlify.app/

**A wellness companion for anxiety, emotional mastery, and self-worth.**

Inner Anchor delivers thought-provoking messages, guided breathing exercises, and gentle mood tracking — designed especially for high-cortisol mornings when your phone should be a source of calm, not stress.

🔗 **Live App:** [grand-gaufre-f76ade.netlify.app](https://grand-gaufre-f76ade.netlify.app/)

---

## Features

### 💬 380+ Curated Messages
Thought-provoking reflections across eight categories — written to feel like a wise mentor, not a motivational poster.
- **Inner Peace** — Grounding messages for anxiety
- **Emotional Mastery** — Patience and anger management
- **Self-Worth** — Rebuilding self-esteem and identity
- **Perspective Shifts** — Stoic-inspired reframes
- **Gratitude & Presence** — Mindfulness prompts
- **Overcoming Fear** — Courage and stepping into the unknown
- **Protecting Family** — Strength, legacy, and being present for those you love
- **Rig Veda Wisdom** — Ancient Vedic insights on truth, creation, and the sacred self

Messages rotate intelligently so you rarely see repeats.

### 🛡️ Morning Shield Mode
Configurable high-cortisol window (default 7–9 AM EST) that delivers more frequent messages and transforms your first phone interaction of the day into something positive.

### 🌬️ Guided Breathing Exercises
Three research-backed techniques with animated visuals and haptic feedback:
- **4-7-8 Calm** — Deep anxiety relief
- **Box Breathing** — Focus under pressure (used by Navy SEALs)
- **Equal Breathing** — Simple centering anytime

Haptic pulses guide you through each phase — no need to watch the screen.

### 📖 Mood Journal
- Quick emotion check-in with 7 mood options
- Optional free-text reflection (500 char limit to keep it lightweight)
- Weekly mood trend chart
- Full entry history

### 📚 Message Library
- Browse all messages by category
- Save favorites with one tap
- Write and store personal mantras that join the notification rotation

### ✨ Quality of Life
- **No guilt mechanics** — missed a day? "Welcome back. There's no streak to protect here — just a practice to return to."
- **Dark mode** with warm tones (not pure black)
- **Journal export** as plain text
- **Share any message** via native share sheet or clipboard
- **Crisis resources** (988 Lifeline, Crisis Text Line, SAMHSA) built into settings
- **Fully offline** — works without internet after first load
- **Zero data collection** — everything stays on your device

---

## Install on Your Phone

Inner Anchor is a Progressive Web App (PWA). No app store needed.

### iPhone
1. Open the live URL in **Safari**
2. Tap the **Share button** (square with arrow)
3. Tap **"Add to Home Screen"**
4. Tap **Add**

### Android
1. Open the live URL in **Chrome**
2. Tap the **three-dot menu**
3. Tap **"Add to Home Screen"** or **"Install app"**

The app launches fullscreen with its own icon — no browser bar.

---

## Tech Stack

- **Pure HTML/CSS/JS** — no frameworks, no build step, no dependencies
- **Service Worker** — offline caching and notification scheduling
- **PWA Manifest** — installable on any device
- **localStorage** — all data persists on-device
- **96KB total** — loads instantly on any connection

---

## Self-Host / Deploy Your Own

The entire app is 4 files. Deploy anywhere that serves static files.

### Netlify (Recommended)
1. Fork this repo
2. Go to [app.netlify.com](https://app.netlify.com)
3. "Add new site" → "Import an existing project" → select your fork
4. Click Deploy

### Vercel
1. Fork this repo
2. Go to [vercel.com](https://vercel.com)
3. "New Project" → select your fork → Deploy

### GitHub Pages
1. Fork this repo
2. Go to Settings → Pages → Source: Deploy from branch → Main → Save

---

## Customize

### Messages
All 260 messages live in the `MESSAGES` array inside `index.html`. Add your own:
```javascript
{id: 261, t: "Your custom message here.", c: "peace"}
```
Categories: `peace`, `mastery`, `worth`, `perspective`, `gratitude`, `fear`, `family`, `veda`

### Appearance
Colors, fonts, and spacing are controlled by CSS variables at the top of `index.html`:
```css
--navy: #1a1f3d;
--cream: #f5f0e8;
--sage: #7c9a8e;
--gold: #c4a265;
```

---

## Project Structure

```
├── index.html       # The entire app (HTML + CSS + JS)
├── sw.js            # Service worker (offline + notifications)
├── manifest.json    # PWA manifest (app name, icon, display)
├── netlify.toml     # Netlify deployment config
└── README.md
```

---

## Privacy

Inner Anchor collects **zero data**. No analytics, no tracking, no network calls after initial load. Your journal entries, favorites, and settings never leave your device.

---

## Support & Crisis Resources

If you or someone you know is struggling:

- **988 Suicide & Crisis Lifeline** — Call or text **988**
- **Crisis Text Line** — Text **HOME** to **741741**
- **SAMHSA Helpline** — **1-800-662-4357**

These services are free, confidential, and available 24/7.

---

## License

MIT — Use it, fork it, share it. If it helps one person breathe easier, it was worth building.
