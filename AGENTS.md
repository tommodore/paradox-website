# Agents.md — Paradox.cat Landing Page

**Goal**  
Create **only a landing page** for paradox.cat.  
No multi-page site. No full website. Just one beautiful, immersive landing page.

**Core Theme**  
Schrödinger’s Cat and the uncertainty of quantum superposition. The cat is both alive and dead until observed. Keep this poetic uncertainty central.

**Languages**  
**English + Catalan** (bilingual).  
Add a clean language switcher (EN / CA) that changes all text on the page.

**Tech Recommendation**  
Single-file `index.html` + Tailwind via CDN + vanilla JavaScript.  
(Perfect for GitHub Pages, instant deployment, no build step.)

---

## Design Direction

**Visual Style**

- Deep cosmic black background (#0b0b12)
- Iridescent accents: cyan (#67e8f9) and purple (#6366f1)
- Elegant serif headings (Playfair Display or Georgia)
- Glassmorphism with soft quantum glows
- Subtle floating particles and smooth animations

**Key Sections (in order)**

1. **Fixed Navbar**
   - Logo: `paradox.cat`
   - Language toggle: **EN | CA | DE | JA**
   - “Observe” button (scrolls to experiment)

2. **Hero**  
   Quadrilingual headline:
   - English: “The cat is both alive and dead.”
   - Catalan: “El gat és viu i mort alhora.”
   - German: “Die Katze ist gleichzeitig lebendig und tot.”
   - Japanese: “猫は生きてもいて、死んでもいる。”  
     Subheadlines and CTAs in all four languages.

3. **The Paradox**  
   Short, poetic explanation of Schrödinger’s cat in all four languages.  
   Include a beautiful central illustration of the sealed box with the cat inside.

4. **The Experiment** (the heart of the page)  
   Interactive element:
   - A glowing box with a flickering cat silhouette
   - Big “Observe” / “Observa” / “Beobachten” / “観測する” button
   - On click: The superposition collapses (random alive/dead result)
   - Poetic quadrilingual result message appears
   - Subtle particle effects and screen flash

5. **Famous Paradoxes** (3–4 cards max)  
   Short cards in all four languages (Zeno’s, Fermi, Ship of Theseus, Grandfather Paradox).  
   Keep descriptions elegant and concise.

6. **Reflections** (optional short section)  
   2–3 poetic thoughts on uncertainty and observation in all four languages.

7. **Footer**  
   Simple with quadrilingual language note and copyright.

---

## Language Guidelines

- All main text must appear in **English, Catalan, German, and Japanese**.
- Use a prominent language switcher in the navbar that instantly changes the entire page content.
- Keep the interactive experiment results in all four languages (e.g. “The cat is alive.” / “El gat és viu.” / “Die Katze lebt.” / “猫は生きています。”).
- Use natural, beautiful translations for each language.
- Use `data-lang-content` attributes and a simple JS system to toggle visibility.
- Add `hreflang` tags for all four languages in `<head>`.

---

## Technical Requirements

- Fully responsive (mobile-first)
- Smooth scrolling
- Accessible (ARIA labels, keyboard navigation)
- Fast loading (< 2s)
- Works offline after first load
- Deploy directly to GitHub Pages as `index.html`

---

## Build Instructions for Your Pi Agent

1. Create a single `index.html` file.
2. Generate Tailwind CSS locally using the Tailwind CLI (see package.json).
3. Implement a simple JS language switcher (store preference in localStorage).
4. Build the interactive experiment first — it is the emotional center.
5. Add subtle quantum particle effects and hover animations.
6. Test on mobile and desktop.
7. Deploy to GitHub Pages and connect `paradox.cat` domain.

---

**Final Instruction for Pi Agent**  
“Build only a landing page for paradox.cat as described in Agents.md. Make it elegant, mysterious, and centered on Schrödinger’s cat uncertainty. Support English, Catalan, German, and Japanese with a clean language switcher. Keep the interactive observation experiment as the highlight. All resources must be self-hosted for DSGVO compliance.”

This Agents.md contains only original content created specifically for paradox.cat. No external material used.

---

## Git Branching Strategy for Agentic Coding

**Recommended Strategy:** Lightweight Trunk-Based Development with `agent/` branches

### Branch Structure

- `main` — Always production-ready (protected, requires PR + review)
- `agent/*` — All work done by the pi agent (short-lived)
- `experiment/*` — Quick tests or spikes (temporary)

### Branch Naming Examples

```bash
agent/landing-page
agent/landing-page-bilingual
agent/fix-observe-button
agent/add-particles
experiment/dark-variant
```

### Workflow

1. Create branch from latest `main`:
   ```bash
   git checkout main && git pull
   git checkout -b agent/landing-page
   ```
2. Let the agent work on the branch (commit frequently with clear messages).
3. Open a **Draft PR** early for visibility.
4. Review → Fix issues → Mark ready for review.
5. Merge using **Squash + Merge**.
6. Delete the branch after merge.
7. Keep branches **very short-lived** (ideally < 48 hours).

### Why This Works Best for Agentic Coding

- High speed while keeping `main` clean and safe
- Easy to see what was AI-generated vs human
- Fast iteration and easy rollback
- Perfect for frequent prompting and refinement

**Rule:** Never push directly to `main`. Always use branches + PRs
