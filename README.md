# Coll-Edge Connect Landing Page Redesign

A high-performance, senior-grade visual and interactive redesign concept of the [Coll-Edge Connect](https://colledgeconnect.in/) landing page. 

This project updates the page with smooth, high-frame-rate interactions, advanced CSS/JS visual effects, responsive fixes, accessibility compliance, and runtime stability corrections—achieving a locked **60 FPS** performance without adding heavy external animation frameworks.

---

## ✨ Features & Enhancements

### 🎨 Creative Interactions
* **Buttery Smooth Custom Cursor:** Interactive dual-pointer setup built using compositor-only `translate3d` transforms and linear interpolation (`lerp`) on a `requestAnimationFrame` render loop to avoid layout reflows.
* **Magnetic Spring Buttons:** UI buttons magnetically attract towards the pointer when hovered close, snapping back using a cubic-bezier transition on cursor exit.
* **Cyberpunk Text Scrambling:** On hover (and on page load for the hero badge), letters scramble and resolve in a cryptographic matrix-style decrypt effect.
* **Interactive Particle Canvas Web:** Connection lines dynamically bridge from the custom cursor trail coordinates to surrounding canvas background nodes.
* **Dynamic Parallax Hero Orbs:** Viewport pointer tracking shifts background ambient glows (`.hero-orb` and `.hero-orb2`) along opposite vectors for a 3D depth effect.
* **Dual Chromatic Glitch Aberration:** Highlights the main word "Brands" with a secondary cyan glitch layer stepping in sync with the original magenta overlay.
* **Native CSS Scroll Progress Bar:** Fixed top-viewport neon gradient bar showing current reading progress, driven natively by CSS `animation-timeline: scroll()`.

### 📱 Layout & UI Refinements
* **Concentric Navbar Capsule:** Refined padding and offsets so the outer capsule aligns concentrically with inner button components.
* **Responsive Layout Fixes:** Corrected desktop navigation squishing on narrow desktop/tablet screens (`901px` to `1050px`) using `flex-shrink` and fluid padding/margin rules.
* **Card Glow Clipping Solution:** testimony/college cards tickers vertical overflow padding adjusted to prevent neon shadows from clipping.
* **Sleek Custom Scrollbars & Selections:** Appended custom selection colors and matching styling tokens for browser scrollbars.

### 🛠️ Stability & Technical Performance
* **Webpack Chunk Hydration Fix:** Mapped broken static bundle folder structures to expected Next.js asset paths to fix runtime crash errors and blank screens.
* **Mock contact form handler:** Patched `window.fetch` to intercept submits to `/api/contact` and simulate success state animations instead of failing with 404.
* **Accessibility Enhancements:** Linked forms and inputs with mapped `<label>` identifiers, added landmark tags, and wrapped all raw emojis inside screen-reader accessible spans post-hydration.
* **Relative Nav Links:** Swapped absolute navigation redirects with local smooth anchor tags.
* **Legal Redirect Fallbacks:** Added redirect index pages for missing `/privacy` and `/terms` files to prevent broken link errors.

---

## 🛠️ Tech Stack & Architecture

* **Core Structure:** Next.js Static Export / Hydrated HTML5
* **Styles:** Native Vanilla CSS
* **Animations:** Compositor-thread CSS Keyframes, native CSS Scroll Timeline, and lightweight vanilla JS `requestAnimationFrame` loops.
* **Zero Dependencies:** No heavy libraries (Framer Motion, GSAP, etc.), keeping load times instant and bundle size tiny.

---

## 🚀 Running Locally

To run the project locally without file-origin CORS issues or path restrictions:

1. Clone or download the repository.
2. Spin up a local static server from the project's root folder:
   ```bash
   # Using Python
   python3 -m http.server 8080

   # Or using Node.js
   npx serve .
   ```
3. Open your browser and navigate to:
   ```
   http://localhost:8080
   ```

---

## 📝 Disclaimer & Credits

This repository is a **redesign and modification concept concept** created for educational and portfolio demonstration purposes. All brand names, trademarks, logos, and original layouts are the property of [Coll-Edge Connect](https://colledgeconnect.in/).
