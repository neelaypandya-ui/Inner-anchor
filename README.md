# Inner Anchor

# App available at: https://inner-anchor.netlify.app/

# ---

# Inner Anchor — Deployment Guide

## Deploy for Free in 5 Minutes (From Your Phone)

### Option 1: Netlify (Recommended — Easiest)

1. **Go to** [github.com](https://github.com) and create a new repository called `inner-anchor`
2. **Upload all 4 files** to the repository:
   - `index.html`
   - `sw.js`
   - `manifest.json`
   - `netlify.toml`
3. **Go to** [app.netlify.com](https://app.netlify.com) and sign up with your GitHub account
4. Click **"Add new site" → "Import an existing project"**
5. Select your `inner-anchor` repo
6. Click **"Deploy"** — that's it
7. Netlify gives you a URL like `inner-anchor-abc123.netlify.app`
8. You can set a custom domain later in Site Settings → Domain Management

### Option 2: Vercel

1. Upload files to a GitHub repo (same as above)
2. Go to [vercel.com](https://vercel.com), sign up with GitHub
3. Click **"New Project"** → select your repo → Deploy
4. Done. You get a URL like `inner-anchor.vercel.app`

### Option 3: GitHub Pages (No Signup Beyond GitHub)

1. Create repo called `inner-anchor`
2. Upload all files
3. Go to **Settings → Pages → Source: Deploy from a branch → Main → Save**
4. Your app will be live at `yourusername.github.io/inner-anchor`

---

## Installing on iPhone

Once deployed, the app works as a PWA (Progressive Web App):

1. **Open** your deployed URL in Safari
2. **Tap the Share button** (square with arrow pointing up)
3. **Scroll down** and tap **"Add to Home Screen"**
4. **Name it** "Inner Anchor" and tap Add
5. The app now appears on your home screen with its own icon
6. It launches fullscreen — no browser bar, feels like a native app

---

## Sharing with Others

Just send anyone the URL. They can:
- Use it directly in their browser
- Install it on their home screen (same steps above)
- Works on iPhone, Android, desktop — any modern browser

---

## Push Notification Notes

The app supports push notifications on:
- **Android**: Full support in Chrome. Notifications work even when app is closed.
- **iPhone (iOS 16.4+)**: Notifications work when the app is installed to home screen AND the app has been opened recently. iOS limits background activity for PWAs.

For the most reliable morning notifications on iPhone:
- Open the app each morning — it will immediately show you a fresh message
- The lock screen/home screen installation means your first interaction with your phone IS the app

For truly scheduled push notifications that work regardless of app state, you'd need a backend service like [OneSignal](https://onesignal.com) (free tier: 10,000 subscribers). This is a future enhancement if you want it.

---

## Customization

All messages are in the `index.html` file inside the `MESSAGES` array. You can:
- Edit existing messages
- Add new ones (follow the format: `{id:261,t:"Your message",c:"peace"}`)
- Categories: `peace`, `mastery`, `worth`, `perspective`, `gratitude`

Colors, fonts, and layout are all controlled by CSS variables at the top of the file.

---

## Files Included

| File | Purpose |
|------|---------|
| `index.html` | The entire app (HTML + CSS + JS, self-contained) |
| `sw.js` | Service worker for offline support + notification scheduling |
| `manifest.json` | PWA manifest (app name, icon, display settings) |
| `netlify.toml` | Netlify-specific config for proper headers |
