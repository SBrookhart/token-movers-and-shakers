
# 📈 Token Movers — Microcaps & Majors

A tiny static site (no backend, no build) that shows **top gainers and losers** (24h %) for:

- **Tiny Microcaps**: market cap **< $50,000,000**
- **Major Players**: **Top‑100** by market cap

Live demo logic is fully client‑side. Optional CoinGecko Demo API key improves reliability but is **not required**.

---

## ✨ Features

- Two tabs: **Microcaps** and **Majors**
- Top **gainers** and **losers** (24h) — 15 each
- Search by name/symbol
- Auto‑refresh every **60s**
- **Key‑free** by default; **fallback** to CoinPaprika if CoinGecko rate‑limits
- Optional CoinGecko **Demo** key (stored only in your browser)

---

## 🚀 Quick Start (Local)

1. Download `index.html`
2. Double‑click it to open in your browser  
   (or run any local static server; not required)

> You can optionally append your CoinGecko Demo key to the URL once:  
> `file:///.../index.html?ck=YOUR_DEMO_KEY`  
> The page stores the key in LocalStorage and removes it from the URL.

---

## 🌐 Deploy on GitHub Pages (Public)

1. Create a **public** repo (e.g., `token-movers`)
2. Add `index.html` and `README.md`
3. Settings → **Pages** → Source: **Deploy from a branch**, Branch: **main**, Folder: **/**  
4. Open `https://YOURNAME.github.io/token-movers/`

**Optional key (recommended):**  
Open your site with `?ck=YOUR_DEMO_KEY` once, or paste the key in the top bar and click **Save**.

---

## ⚙️ Configuration

You can tweak these constants inside `index.html`:

```js
const CAP_MAX_MICRO = 50_000_000; // microcap threshold
// change the number of items shown by adjusting .slice(0, 15)
