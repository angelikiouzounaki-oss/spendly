# Spendly — Personal Expense Tracker

> A personal expense tracking Progressive Web App (PWA) — installable on iPhone, fully private, no App Store needed.

**Live app:** [angelikiouzounaki-oss.github.io/spendly](https://angelikiouzounaki-oss.github.io/spendly)

---

## What is Spendly?

Spendly is a personal expense tracker built as a single HTML file that runs entirely in your browser. It can be installed on your iPhone home screen where it looks and feels like a native app.

- **No App Store** — install directly from Safari
- **Fully private** — all data stays on your device, nothing is sent to any server
- **Works offline** — no internet needed after first load
- **Free forever** — hosted on GitHub Pages at no cost

---

## Install on iPhone

1. Open **Safari** on your iPhone and go to `angelikiouzounaki-oss.github.io/spendly`
2. Tap the **Share button** (box with arrow pointing up)
3. Tap **"Add to Home Screen"**
4. Tap **Add**

Spendly will appear as a full-screen app icon on your home screen.

---

## Features

### 📱 Three pages

| Page | Description |
|------|-------------|
| **Overview** | Spending summary, weekly bar chart, top 5 categories, last 10 transactions |
| **Transactions** | Full transaction list with timestamps, export & import |
| **Charts** | Spending trend line chart, pie chart by category, horizontal category totals |

---

### 🗓 Period Selector

All pages have a **Today / Week / Month / Year** selector in the header. Use the **‹ ›** arrows to navigate between past periods.

| Period | Breakdown shown |
|--------|----------------|
| Today | By hour of day |
| Week | By day of week |
| Month | By week of month |
| Year | By month of year |

---

### ➕ Adding an Expense

1. Tap **+ Add expense** at the bottom of any page
2. Enter the amount (€)
3. Pick a date (defaults to today)
4. Choose a **category**
5. Choose a **store / provider** from the pre-filled list, or add your own with **+ Add**
6. Add an optional note
7. Tap **Add expense**

> Swipe the form down or tap Cancel to discard. If you've entered an amount, you'll be asked to confirm.

---

### 🗂 Categories & Stores

| Icon | Category | Pre-filled options |
|------|----------|--------------------|
| 🛒 | Groceries | Albert Heijn, Jumbo, Lidl, Penny, Kaufland, DM, Kruidvat, Action |
| 🍽 | Restaurants | Delivery, Restaurant, Café / Bar, Fast Food |
| 🚗 | Transport | NS, DB, Taxi, Bus, GVB, Arriva + purpose tags |
| 🛍 | Shopping | Clothes & Shoes, Books, Gifts, Games, Apps, Electronics |
| 🏠 | Housing | Rent |
| 💊 | Health | Psychologist, Doctor, Medication, Health Insurance |
| 🎬 | Entertainment | Cinema, Concert, Museum, Theme Park |
| ✈️ | Travel | Accommodation, Plane, Train, Car, Activities |
| 📱 | Subscriptions | Netflix, Spotify, Lebara, Apple, Google, Bunq, ABN, Revolut |
| 📦 | Other | — |

> Custom stores can be added to any category and are saved permanently on your device.

---

### 🔍 Category Drill-Down

On the Overview page, tap any category in the **Top 5 categories** list to see a detailed breakdown of spending per store or provider within that category, including transaction counts and percentages.

---

### 📤 Export & Import

Go to **Transactions → Export expenses** to access:

| Option | Description |
|--------|-------------|
| All expenses — CSV | Every transaction ever, opens in Excel / Numbers |
| This period — CSV | Only transactions in the current view |
| Full backup — JSON | Complete data backup for safekeeping |
| Import backup — JSON | Restore data from a previously exported backup |

> ⚠️ Importing a backup will replace all current data. A confirmation prompt will appear first.

---

## Data & Privacy

| Question | Answer |
|----------|--------|
| Where is data stored? | In your browser's `localStorage` — on your device only |
| Is data sent anywhere? | No. GitHub Pages only serves the HTML file |
| What if I clear Safari cache? | Data will be wiped — export a JSON backup regularly |
| Can others see my expenses? | No — the repo is public but your data is only on your device |
| Does it work offline? | Yes, fully |

---

## Backup Guide

> Recommended: export a JSON backup at least once a month.

**To back up:**
1. Transactions → Export expenses → Full backup — JSON
2. Save to Files / iCloud Drive

**To restore:**
1. Transactions → Export expenses → Import backup — JSON
2. Select your backup file
3. Confirm — all data restored instantly

---

## Updating the App

1. Download the latest `index.html` from this repo
2. Delete the existing `index.html` on GitHub
3. Upload the new file and commit
4. Wait ~1 minute for GitHub Pages to deploy
5. Hard refresh in Safari: hold the refresh button → **Reload Without Content Blockers**

---

## Custom App Icon

1. Create a **180×180 pixel PNG** image
2. Name it `icon.png`
3. Upload it to this repo alongside `index.html`
4. Remove Spendly from your iPhone home screen
5. Re-add via Safari → Share → Add to Home Screen

---

## File Structure

```
spendly/
├── index.html        ← the entire app
├── icon.png          ← home screen icon (180×180px)
└── README.md         ← this file
```

---

## Technical Stack

- **Single HTML file** — no build tools, no dependencies to install
- **Vanilla JavaScript** — no frameworks
- **[Chart.js 4.4.1](https://cdnjs.cloudflare.com)** — for charts
- **localStorage** — for persistent on-device data storage
- **PWA meta tags** — for full-screen iPhone installation
- **GitHub Pages** — free static hosting

---

*Spendly — built for personal use · data stays on your device · hosted on GitHub Pages*
