# Vishna Clothing — Indo-Western Modern Storefront (React)

Crafted from the Google Stitch design system, this is a production-grade e-commerce application built with **React** and **Vite**, adhering to modern full-stack architectural principles.

---

## 🏛️ Architecture & Directory Structure

This project adopts the **Page Directory Pattern** (`pages/<PageName>/<PageName>.jsx` & `<PageName>.css`) as requested:

```
frontend/
├── public/
│   └── assets/                  # Brand wordmark, editorial hero & original design assets
├── src/
│   ├── components/
│   │   ├── layout/
│   │   │   ├── Navbar/          # Announcement bar, logo, search trigger, profile & badges
│   │   │   ├── Footer/          # Trust badges, brand story, shop links, newsletter
│   │   │   └── BottomNav/       # Fixed mobile navigation bar with real-time badges
│   │   └── common/
│   │       ├── ProductCard/     # 3:4 portrait card with shade swatches & quick add
│   │       ├── QuickAddDrawer/  # Slide-up modal with shade & size selector
│   │       ├── Toast/           # Real-time feedback toast
│   │       ├── FilterPills/     # Category filter buttons
│   │       └── SearchModal/     # Instant catalog search modal
│   ├── context/
│   │   ├── CartContext.jsx      # Global cart state, item quantities, free shipping calculator
│   │   └── WishlistContext.jsx  # Global favorites state with localStorage persistence
│   ├── data/
│   │   ├── products.js          # Full catalog (Mira Co-ord, Aira Corset, Noor Dress, etc.)
│   │   ├── categories.js        # Curated edits (Indo-Western, Co-ords, Dresses, Tops, Bottoms)
│   │   ├── editorial.js         # Currently Obsessed trends & The Vishna Edit articles
│   │   └── reviews.js           # Verified customer reviews & trust credentials
│   ├── pages/                   # Dedicated directory for each page
│   │   ├── Home/                # Full editorial storefront
│   │   ├── Explore/             # All 84 pieces catalog with search, filters & sorting
│   │   ├── Categories/          # Collection showcase directory
│   │   ├── Wishlist/            # Saved items manager
│   │   ├── Bag/                 # Checkout experience, coupon code & order confirmation
│   │   └── Story/               # Atelier philosophy & style journal reader
│   ├── services/
│   │   └── api.js               # Service abstraction layer ready for backend integration
│   ├── styles/
│   │   ├── tokens.css           # Design tokens from DESIGN.md (colors, typography, spacing)
│   │   └── index.css            # Base stylesheet, typography utilities & animations
│   ├── App.jsx                  # Main application orchestrator & route switcher
│   └── main.jsx                 # React root mount
├── package.json
└── vite.config.js
```

---

## 🎨 Design System Tokens (from `DESIGN.md`)

- **Primary Heritage Wine**: `#500215` / `#6E1A29`
- **Neutral Canvas**: `#FAF8F5` / `#FBF9F6`
- **Soft Sand**: `#ECE6DC` / `#E8E2D8`
- **Champagne Gold**: `#C5A880` / `#FEDEB2`
- **Charcoal Text**: `#18181B` / `#1B1C1A`
- **Typography Pairing**: *Playfair Display* (Editorial headlines) + *Plus Jakarta Sans* (Functional UI/Pricing)
- **Sharp Architectural Borders**: 1px micro-borders (`#E3DDD2`) with 0px corner radii.

---

## 🚀 How to Run Locally

1. **Install Node.js** (if not already installed):
   ```powershell
   winget install OpenJS.NodeJS.LTS
   ```
   *Restart your terminal after installation to refresh the PATH.*

2. **Navigate to the frontend folder**:
   ```bash
   cd frontend
   ```

3. **Install dependencies**:
   ```bash
   npm install
   ```

4. **Start the local development server**:
   ```bash
   npm run dev
   ```
   Open `http://localhost:3000` in your browser.

---

## 🔌 Full-Stack Backend Integration

The frontend includes an abstraction service layer at `src/services/api.js`. When you build your backend (e.g. Express, NestJS, FastAPI, or Django), simply configure the `BASE_URL` in `src/services/api.js` to connect the frontend to live database APIs!
