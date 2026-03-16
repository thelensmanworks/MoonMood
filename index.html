# 🌙 MoonMood

> **"Because love should care about every mood."**

A pastel-themed emotional support web app designed to help partners comfort their girlfriends during menstrual cycle mood swings — through AI companions, mini games, craving requests, and emotional interactions.

---

## 📁 Project Structure

```
moonmood/
├── index.html          ← Landing page
├── setup.html          ← Couple setup flow
├── mood.html           ← Mood selector
├── companion.html      ← AI companion chat
├── shop.html           ← Cravings Kiss Shop
├── games.html          ← Dopamine mini games
├── pet.html            ← Virtual pet system
├── comfort.html        ← Comfort + relaxation tools
├── request.html        ← Partner share/request page
│
├── css/
│   ├── style.css       ← Global design tokens, nav, animations
│   └── pages.css       ← Page-specific styles
│
├── js/
│   ├── app.js          ← Main application logic & state
│   └── components.js   ← Shared nav, footer, overlays
│
└── assets/             ← Images, icons (add your own)
```

---

## 🚀 Quick Start

### Option 1: Open Directly
Just open `index.html` in any modern browser. No build step required.

### Option 2: Local Server (Recommended)
```bash
# Python
python3 -m http.server 3000

# Node.js
npx serve .

# VS Code: Install "Live Server" extension → Right-click index.html → Open with Live Server
```

Then visit: `http://localhost:3000`

---

## ✨ Features

| Feature | Status | Description |
|---------|--------|-------------|
| Landing Page | ✅ | Hero, features, testimonials, donation |
| Couple Setup | ✅ | Name, nickname, partner name, animal companion |
| Mood Selector | ✅ | 6 mood options with theme adaptation |
| AI Companion Chat | ✅ | 5 animals × 7 response categories |
| Cravings Shop | ✅ | 12 items priced in kisses + share links |
| Mini Games | ✅ | Catch the Hearts (live) + 5 coming soon |
| Virtual Pet | ✅ | Feed system, XP bar, growth stages |
| Comfort Tools | ✅ | Hug, breathing, music, love messages |
| Relaxation Sounds | ✅ | 4 tracks with play/pause |
| Partner Share Page | ✅ | `/request.html?item=Dark+Chocolate&from=Priya` |
| Donation Section | ✅ | Stripe-ready UI |
| Mobile Responsive | ✅ | Full mobile-first design |
| Falling Petals | ✅ | Ambient animation on all pages |

---

## 🎨 Design System

**Color Palette:**
- Baby Pink: `#FFB6C1` / Deep: `#F06292`
- Lavender: `#C9B8F0` / Deep: `#9575CD`
- Mint Green: `#B2EBD0` / Deep: `#4CAF82`
- Peach: `#FFCCAA` / Deep: `#FF8A65`
- Cream White: `#FFF9F0`

**Typography:**
- Headings: Playfair Display (Google Fonts)
- Body: Poppins (Google Fonts)

**Custom cursor:** 🌸 petal cursor on desktop

---

## 🔧 Adding Real AI Chat (Claude API)

Replace `getLocalResponse()` in `js/app.js` with a real API call:

```javascript
async function getAIResponse(userMessage) {
  const data = COMPANIONS[MM.user.animal];
  const response = await fetch('/api/chat', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
      system: data.persona,
      message: userMessage,
      history: chatHistory.slice(-6) // Last 3 exchanges
    })
  });
  const result = await response.json();
  return result.reply;
}
```

**Backend endpoint** (Node.js/Next.js example):
```javascript
// /api/chat
import Anthropic from '@anthropic-ai/sdk';
const client = new Anthropic();

export async function POST(req) {
  const { system, message, history } = await req.json();
  const msg = await client.messages.create({
    model: 'claude-sonnet-4-6',
    max_tokens: 200,
    system,
    messages: [...history, { role: 'user', content: message }]
  });
  return Response.json({ reply: msg.content[0].text });
}
```

---

## 💳 Adding Stripe Donations

```javascript
// Replace handleDonate() in app.js
async function handleDonate() {
  const amount = document.querySelector('.amt-btn.selected')?.dataset.val || '5';
  const res = await fetch('/api/checkout', {
    method: 'POST',
    body: JSON.stringify({ amount: parseInt(amount) * 100 }) // cents
  });
  const { url } = await res.json();
  window.location.href = url;
}
```

---

## 🌐 Deployment (Vercel)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Custom domain
vercel --prod
# Then add moonmood.app in Vercel dashboard
```

**For the `/request/:slug` shareable links**, add a `vercel.json`:
```json
{
  "rewrites": [
    { "source": "/request/:slug", "destination": "/request.html" }
  ]
}
```

---

## 🗄️ Supabase Schema (for production)

```sql
-- Couples
create table couples (
  id uuid primary key default gen_random_uuid(),
  user_name text, user_nick text, partner_name text,
  animal text, created_at timestamptz default now()
);

-- Moods
create table moods (
  id uuid primary key default gen_random_uuid(),
  couple_id uuid references couples(id),
  mood text, recorded_at timestamptz default now()
);

-- Craving Requests
create table requests (
  id uuid primary key default gen_random_uuid(),
  couple_id uuid references couples(id),
  item text, kiss_cost int,
  slug text unique, fulfilled boolean default false,
  created_at timestamptz default now()
);

-- Pet State
create table pets (
  couple_id uuid primary key references couples(id),
  xp int default 0, stage text default 'baby',
  happiness int default 80, hunger int default 60,
  energy int default 90
);
```

---

## 📱 PWA Support

Add to `<head>` of all pages for installable app:
```html
<link rel="manifest" href="manifest.json">
<meta name="theme-color" content="#FFB6C1">
```

**manifest.json:**
```json
{
  "name": "MoonMood",
  "short_name": "MoonMood",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#FFF9F0",
  "theme_color": "#FFB6C1",
  "icons": [{ "src": "assets/icon-512.png", "sizes": "512x512", "type": "image/png" }]
}
```

---

## 🔮 Future Viral Features

1. **Mood Calendar** — Monthly heat map of mood patterns
2. **Partner Dashboard** — Partner sees mood alerts and pending requests
3. **Couple Streaks** — Daily check-in streaks with rewards
4. **Custom Animal Names** — Name your companion
5. **Music Integration** — Spotify/YouTube embed for real tracks
6. **Push Notifications** — "Your partner sent a hug!" via web push
7. **Mood Insights** — AI-generated monthly mood summary
8. **Gift Integration** — Direct Amazon/Swiggy links from shop
9. **Video Messages** — Short video hugs from partners
10. **Language Support** — Hindi, Spanish, French, Arabic

---

## 💕 Made With Love

MoonMood is built to be wholesome, emotionally supportive, playful, and minimalistic.  
No ads. No subscriptions. Just comfort.

**Tech Stack:** Vanilla HTML/CSS/JS → upgrade path to Next.js + Supabase + Claude API + Stripe
