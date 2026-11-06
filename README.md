# Modern Design of WebSite interface and transitions.

A high-performance coffee-shop web application designed with an artisanal, tactile aesthetic, super smooth physics-based animations(f.e. coffee cup filling up with coffee), an interactive beverage visualizer.

---

## Key Features

### 1. Interactive Cup Builder (`src/components/InteractiveCustomizer.tsx`)
* **Real-Time Animated Cup Simulation**: Fluid dynamics smoothly adapt with Framer Motion spring physics as you alter espresso extraction volume, milk emulsification ratio, and temperature.
* **Liquid Layers & Physics**:
  * Hot drinks generate animated drifting steam particles.
  * Iced/Nitro drinks dynamically spawn floating hand-carved ice cubes.
  * Steamed milk / oat barista emulsion layers expand and contract based on the slider ratio.
  * Single-origin extraction layer dynamically reflects the roast color profile (from light floral Geisha amber to dark obsidian).
* **Sensory Radar**: Dynamically calculates and displays **Floral Acidity**, **Mouthfeel & Body Weight**, and **Caramelized Sweetness** bars, alongside active calorie and caffeine readouts.
* **Interactive Calibrations**:
  * Micro-lot beans (Guji Highland Geisha, Huila Pink Bourbon, Antigua Los Volcanes, Mount Kerinci Peaberry)
  * Milk types (Oat Barista, Whole, Almond, Black extraction) with a percentage ratio slider.
  * Extraction temperatures (Steaming Hot 65°C, Gentle Warm 55°C, Over Hand-cut Ice, Nitro Draft)
  * Artisanal infusions (Bourbon Vanilla, Salted Brown Demerara, Cardamom Honey)
  * Foam architecture (Velvet Microfoam vs. Extra Cloud Foam)
  * Extra double-ristretto shot pull

### 2. Art of Selection Menu (`src/components/SelectionMenu.tsx`)
* **Smooth Spring-Pill Filtering**: Instant category switching (All, Single-Origin Filter, Signature Espresso, Cold Brew & Nitro, Sensory Atelier, Viennoiserie & Fare) with zero layout thrashing.
* **Instant Search & Dietary Tags**: Filter by plant-based, zero sugar, single-origin, or customer favorites.
* **Direct Customization Integration**: Clicking "Customize" on any drink loads it seamlessly into the Interactive Cup Builder.
* **Quick Add**: One-click addition to order bag with instant tactile bounce animation.

### 3. Slide-Out Order Bag & Checkout (`src/components/OrderDrawer.tsx`)
* Smooth slide-in drawer with line item quantities.
* Fulfillment selection: Barista Counter Pickup, Dine-in Table, or Curbside.
* Barista care tip presets (0%, 10%, 15%, 20%).
* Order confirmation receipt with cryptographic Order ID and live preparation countdown.

---

##  API Security Architecture
The project includes an enterprise-grade hardened API server (`server/api.js`) and an exhaustive automated security burnout suite (`server/security-audit.js`):

**Anti-CSRF Tokens**  Cryptographic 64-character hex tokens required for state-changing POST requests
**DDoS & Rate Limiting**  `express-rate-limit`: 10 requests / 10 min for checkout; 60 requests / 5 min general API


## Technology Stack

1. **Lucide React**: Clean modernist iconography.
2. **React 18 + Vite 5**: Ultra-fast hot module replacement, zero server hydration mismatch, lightweight bundle size.
3. **Tailwind CSS**: Custom Scandinavian-Japanese palette (`obsidian-950`, `crema-500`, `parchment-100`) avoiding generic AI templates.
4. **Framer Motion 11**: Physics-driven spring animations, layout morphing (`layoutId`), fluid level adjustments, and responsive modal sliding.
5. **Express + Helmet + Zod**: Hardened backend defense enforcing modern web security benchmarks.
6. **Lucide React**: Clean modernist iconography.


---

## Quickstart Commands

```bash
# Navigate to the project directory
cd coffee-shop-website

# Install dependencies
npm install

# Run the frontend dev server
npm run dev

# Run the security-hardened backend API server
npm run server

# Build production bundle
npm run build
```
