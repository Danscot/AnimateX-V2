# AnimateX HTML/CSS Skill Guide for AI Agents

This skill is **HTML/CSS-only**.  
Do not use React references from this guide.

Use this skill when the user asks for:
- website animations,
- UI micro-interactions,
- motion-heavy layouts,
- or reusable animation ideas that can later be converted into motion-graphics video scenes.

---

## 1) Core rule for this skill

Always use files inside `html/` as the source of truth.

- Reference only: structure, styling, timing, easing, keyframes, hover/click behavior.
- Output goal: CSS animation instructions/components that can be reused or transformed into motion design pipelines.

---

## 2) Source map (HTML only)

### Navigation
- `html/navs/vercel.html` (vercel-style underline/trailer feel)
- `html/navs/tipped.html`
- `html/navs/breadcrum.html`
- `html/navs/momonav.html`
- `html/navs/morphingtabs.html`
- `html/navs/flower.html`

### Buttons
- `html/buttons/press.html`
- `html/buttons/shimmerbtn.html`
- `html/buttons/loadingButton.html`
- `html/buttons/delete.html`
- `html/buttons/gooey.html`
- `html/buttons/copy.html`
- `html/buttons/arrowbtn.html`
- `html/buttons/themetoggler.html`
- `html/buttons/aurabutton.html`
- `html/buttons/feedback.html`
- `html/buttons/pulse.html`
- `html/buttons/aerobutton.html`
- `html/buttons/rainbowbutton.html`
- `html/buttons/expand.html`

### Carousels
- `html/carousels/wheel.html`
- `html/carousels/hightlight.html`
- `html/carousels/picCycle.html`
- `html/carousels/swift.html`
- `html/carousels/scrollrotate.html`
- `html/carousels/infinitecarousel.html`
- `html/carousels/domino.html`
- `html/carousels/infinitez.html`
- `html/carousels/canvas/canvas.html`
- `html/carousels/canvas/canvas02.html`

### Cards
- `html/cards/stackswipe.html`
- `html/cards/flipy.html`
- `html/cards/lightcards.html`
- `html/cards/filter.html`
- `html/cards/flip.html`
- `html/staggercards.html`

### Modals / overlays
- `html/modals/todo.html`
- `html/modals/tooltip.html`
- `html/modals/dailog.html`
- `html/modals/sign.html`
- `html/modals/reportbug.html`
- `html/modals/toast.html`

### Inputs
- `html/inputs/dropdown.html`

### Text / typography
- `html/text/swoop.html`
- `html/letterstack.html`

### Sections
- `html/sections/features/featureswoop.html`
- `html/sections/features/scrollstack.html`
- `html/sections/about/textreveal.html`
- `html/sections/gallery/stagger3d.html`
- `html/sections/intergration/toolspread.html`

Note: keep legacy filenames exactly as written (for example `breadcrum`, `hightlight`, `dailog`, `intergration`).

---

## 3) Agent workflow (HTML/CSS animation extraction)

When a user asks for animation work:

1. Identify intent: nav, button, modal, card, carousel, text, or section animation.
2. Pick the closest `html/...` reference file.
3. Extract motion logic:
   - keyframes
   - animation duration/delay
   - easing curve
   - transform path (translate/scale/rotate/skew)
   - opacity/blur/filter behavior
   - trigger type (hover/click/scroll/loop)
4. Rewrite as reusable CSS blocks with clear class naming.
5. Preserve behavior fidelity first, then theme/colors/layout.
6. If asked for video-ready design direction, convert animation into:
   - scene timeline,
   - in/out transitions,
   - loop points,
   - camera-safe composition notes (centering, spacing, rhythm).

---

## 4) Selection rules by request type

- If user asks for a **Vercel-like navbar**: start from `html/navs/vercel.html`.
- If user asks for **minimal modern nav tabs**: compare `morphingtabs.html` and `tipped.html`.
- If user asks for **high-attention CTA**: pick from `rainbowbutton.html`, `gooey.html`, `shimmerbtn.html`.
- If user asks for **functional button states**: pick `loadingButton.html`, `copy.html`, `delete.html`.
- If user asks for **animated content storytelling on scroll**: pick `scrollstack.html`, `textreveal.html`, `stagger3d.html`.
- If user asks for **carousel hero motion**: pick from `swift.html`, `picCycle.html`, `wheel.html`, `canvas/*.html`.
- If user asks for **overlay feedback/toast/dialog flow**: pick from `toast.html`, `dailog.html`, `tooltip.html`, `todo.html`.

---

## 5) Example behavior (requested by user)

Prompt example:  
“Make me a website with a Vercel-type navbar.”

AI should:
1. Open `html/navs/vercel.html`.
2. Recreate the visual behavior in CSS:
   - clean horizontal nav layout,
   - animated underline indicator/trailer,
   - smooth timing and spacing.
3. Keep it modular so the same motion can be reused in other headers/scene compositions.
4. If needed for video pipeline, describe timeline beats:
   - idle state,
   - hover sweep,
   - active tab lock.

---

## 6) Output standards for future motion-graphics conversion

When generating final answers from this skill, the AI should provide:
- semantic HTML structure,
- scoped CSS animation classes,
- named keyframes,
- trigger logic (hover/click/auto/scroll),
- tunable timing tokens (`--duration`, `--delay`, `--easing`),
- optional scene notes for timeline/video adaptation.

Keep outputs deterministic, modular, and easy to convert into motion-graphics scenes later.
