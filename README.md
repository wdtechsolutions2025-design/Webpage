# WD Tech Solutions — Official Website

> Dar es Salaam's trusted phone dealer. New, used & non-active smartphones with delivery, trade-in, and phone loan options.

---

## 📌 About

This is the official website for **WD Tech Solutions**, a phone retail business based in **Dar es Salaam, Tanzania**. The site serves as a live product catalogue and customer engagement platform, allowing customers to browse available phones, check prices, calculate loan repayments, and reach out instantly via WhatsApp.

The site is built as a **single-file HTML application** — no frameworks, no backend, no database. Everything runs in the browser.

---

## ✨ Features

- **Live Phone Catalogue** — 150+ phones listed with brand, model, storage, colour, condition and price
- **Brand & Condition Filters** — customers can filter by iPhone, Samsung, Pixel, Xiaomi / New Fullbox, Used, Non-Active
- **WhatsApp Integration** — every phone card has direct WhatsApp links pre-filled with the phone name and price for instant purchase or trade-in enquiry
- **Phone Loan Calculator** — customers enter a phone price and instantly see the deposit (40%), loan amount, interest, and weekly repayment schedule over 12 weeks
- **Loan Modal** — clicking MKOPO on any phone card opens a detailed loan breakdown for that specific phone
- **Top-Up (Trade-In)** — dedicated WhatsApp button on every card for customers who want to trade in their current phone
- **Delivery Section** — covers delivery options across Tanzania
- **Testimonials** — customer reviews section
- **Policies Section** — warranty, return and purchase policies clearly stated
- **Locations** — store locations listed (Kariakoo & Mabibo NIT)
- **Fully Responsive** — works on mobile and desktop
- **Animated UI** — smooth scroll animations, floating phone cluster, live badge pulse

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (custom, no framework) |
| Logic | Vanilla JavaScript |
| Fonts | Google Fonts — Bebas Neue, Nunito |
| Hosting | GitHub Pages |
| Domain | Custom CNAME |
| Images | GSMArena CDN + base64 embedded |

No npm. No build step. No dependencies to install. Open the file and it works.

---

## 📁 File Structure

```
Webpage/
├── index.html        ← The entire website (single file)
├── CNAME             ← Custom domain configuration for GitHub Pages
├── README.md         ← This file
└── not needed.html   ← Previous version (archived, not served)
```

---

## 📦 How to Update the Phone Catalogue

All phones are listed inside the `<!-- CATALOGUE -->` section of `index.html`. Each phone card follows this structure:

```html
<div class="pc" data-brand="iphone" data-condition="new">
  <div class="pci">
    <span class="cb new">New · Fullbox</span>
    <img src="IMAGE_URL" alt="Phone Name" loading="lazy">
  </div>
  <div class="pcb">
    <div class="pbt">Brand · Series</div>
    <div class="pn">Phone Name</div>
    <div class="ps">
      <span class="sc">Storage</span>
      <span class="sc">Colour</span>
      <span class="sc">Chip</span>
      <span class="sc">Condition</span>
    </div>
    <div class="pp"><span class="tsh">TSh </span>PRICE/=</div>
    <div class="cbs-3">
      <a href="WHATSAPP_NUNUA_LINK" class="bb" target="_blank">NUNUA SASA</a>
      <a href="WHATSAPP_TOPUP_LINK" class="bt" target="_blank">TOP UP</a>
      <a href="#" class="bl" onclick="openLoan('Phone Name', PRICE); return false;">MKOPO</a>
    </div>
  </div>
</div>
```

**Condition classes:**
- `data-condition="new"` + `class="cb new"` → New · Fullbox
- `data-condition="used"` + `class="cb used"` → Imetumika (Used)
- `data-condition="nonactive"` + `class="cb nonactive"` → Non-Active

**To change a price**, update:
1. The display price in `.pp`
2. The WhatsApp NUNUA SASA link (encoded price in URL)
3. The WhatsApp TOP UP link (encoded price in URL)
4. The `openLoan()` function call (numeric price)

---

## 💰 Loan Calculation Formula

The loan calculator uses the following formula:

```
Deposit    = Price × 40%
Loan       = Price − Deposit
Total      = Loan × 1.5  (50% interest)
Weekly     = Total ÷ 12
Grand Total = Deposit + Total
```

Repayment period: **12 weeks**

---

## 📞 Contact & Business Info

| | |
|---|---|
| 📱 WhatsApp / Phone | 0612 199 342 |
| 📍 Location 1 | Kariakoo, Dar es Salaam |
| 📍 Location 2 | Mabibo NIT, Dar es Salaam |
| ⌚ Hours | Every day, 8:00 AM – 7:00 PM |
| 🌐 Website | Deployed via GitHub Pages |

---

## 🚀 Deployment

This site is hosted on **GitHub Pages** from the `main` branch. Any commit pushed to `main` triggers an automatic deployment — changes are usually live within **1–2 minutes**.

To update the live site:
1. Edit `index.html`
2. Upload/replace the file on GitHub
3. Wait ~1 minute
4. Hard refresh the browser (`Ctrl + Shift + R`)

---

## 👤 Owner

**WD Tech Solutions**
Owned and operated by Fighter — entrepreneur, forex trader & digital builder based in Dar es Salaam, Tanzania.

---

© 2025 WD Tech Solutions · All Rights Reserved · Dar es Salaam, Tanzania
