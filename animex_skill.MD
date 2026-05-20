# AnimateX Skill Guide for AI Agents

Use this skill when a user asks for animated UI in a website, dashboard, landing page, or app screen.

## 1) How to decide what animation to use

1. Detect the UI goal from the prompt (navigation, CTA button, carousel, modal, section reveal, etc.).
2. Pick the closest animation family from this repo.
3. Use the HTML reference as motion/style baseline.
4. Use the React/Next component as implementation baseline.
5. Adjust props/classes to match the user’s branding and layout.

## 2) Source mapping pattern

- HTML/CSS references live in: `html/...`
- React components live in: `components/ui/...`
- Showcase usage pages live in: `app/components/.../page.tsx`

Usually:

`html/<group>/<name>.html` → `components/ui/<group>/<name>.tsx`

## 3) Animation index by intent

### Navigation

- **Vercel-style nav (underline + hover trailer)**  
  HTML: `html/navs/vercel.html`  
  React: `components/ui/navs/vercel.tsx`  
  Example page: `app/components/vercel/page.tsx`
- Tipped nav: `html/navs/tipped.html` → `components/ui/navs/tipped.tsx`
- Breadcrumb nav: `html/navs/breadcrum.html` → `components/ui/navs/breadcrum.tsx`
- Momo nav: `html/navs/momonav.html` → `components/ui/navs/momonav.tsx`
- Morphing tabs: `html/navs/morphingtabs.html` → `components/ui/navs/morphingtabs.tsx`
- Flower nav: `html/navs/flower.html` → `components/ui/navs/flower.tsx`

### Buttons / CTAs

- `press`, `shimmerbtn`, `loadingButton`, `delete`, `gooey`, `copy`, `arrowbtn`, `themetoggler`, `aurabutton`, `feedback`, `pulse`, `aerobutton`, `rainbowbutton`, `expand`  
  HTML: `html/buttons/<name>.html`  
  React: `components/ui/buttons/<name>.tsx`

### Carousels

- `wheel`, `hightlight`, `picCycle`, `swift`, `scrollrotate`, `infinitecarousel`, `domino`, `infinitez`  
  HTML: `html/carousels/<name>.html`  
  React: `components/ui/carousels/<name>.tsx`
- Canvas variants:  
  HTML: `html/carousels/canvas/canvas.html`, `html/carousels/canvas/canvas02.html`  
  React: `components/ui/carousels/canvas/canvas.tsx`, `components/ui/carousels/canvas/canvas02.tsx`

### Cards

- `stackswipe`, `flipy`, `lightcards`, `filter`, `flip`  
  HTML: `html/cards/<name>.html`  
  React: `components/ui/cards/<name>.tsx`
- Stagger cards (root file):  
  HTML: `html/staggercards.html`  
  React: `components/ui/staggercards.tsx`

### Modals / overlays

- `todo`, `tooltip`, `dailog`, `sign`, `reportbug`, `toast`  
  HTML: `html/modals/<name>.html`  
  React: `components/ui/modals/<name>.tsx`

### Inputs

- Animated dropdown  
  HTML: `html/inputs/dropdown.html`  
  React: `components/ui/inputs/dropdown.tsx`

### Text / typographic motion

- Swoop text  
  HTML: `html/text/swoop.html`  
  React: `components/ui/text/swoop.tsx`
- Letter stack (root file):  
  HTML: `html/letterstack.html`  
  React: `components/ui/letterstack.tsx`

### Full sections

- Features:  
  `html/sections/features/featureswoop.html` → `components/ui/sections/features/featureswoop.tsx`  
  `html/sections/features/scrollstack.html` → `components/ui/sections/features/scrollstack.tsx`
- About:  
  `html/sections/about/textreveal.html` → `components/ui/sections/about/textreveal.tsx`
- Gallery:  
  `html/sections/gallery/stagger3d.html` → `components/ui/sections/gallery/stagger3d.tsx`
- Integration:  
  `html/sections/intergration/toolspread.html` → `components/ui/sections/intergration/toolspread.tsx`

## 4) Selection rules for the AI agent

- If the user asks for a **clean SaaS/header nav similar to Vercel**, use `VercelNav` first.
- If the user asks for **tabbed nav with fluid transitions**, prefer `morphingtabs`.
- If the user asks for **attention-grabbing CTA**, choose from button animations by tone:
  - subtle: `press`, `aerobutton`
  - vivid: `rainbowbutton`, `gooey`, `shimmerbtn`
  - utility: `copy`, `loadingButton`, `themetoggler`
- If the user asks for **storytelling / scrolling sections**, use `scrollstack`, `featureswoop`, `textreveal`.
- If the user asks for **media-heavy hero/gallery**, start from `swift`, `picCycle`, `canvas`.

## 5) Example decision (from user prompt)

Prompt type: “Build a modern website with a Vercel-like navbar.”  
Agent behavior:
1. Select `html/navs/vercel.html` as visual behavior reference.
2. Implement with `components/ui/navs/vercel.tsx` (`VercelNav`).
3. Follow usage structure from `app/components/vercel/page.tsx`.
4. Pass `links` and optional style props (`className`, `linkstyle`, `dashstyle`, `hoverstyle`, `speed`) to fit the page brand.

## 6) Integration checklist the AI should follow

- Confirm user’s target section and interaction intent.
- Pick one primary animation (avoid stacking many competing effects).
- Keep accessibility in mind (readable contrast, clear states, not motion-overloaded).
- Keep animation speed moderate and consistent with surrounding UI.
- Reuse existing component props before rewriting motion logic.
