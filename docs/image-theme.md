# Image theme: Leading Without a Script

One visual system for chapter art: **cool vs warm**, **purple at the overlap**, **textured digital illustration** (not flat stock). Reference look: [`04-empathy-candor/cover.png`](../04-empathy-candor/cover.png) in the repo, or on GitHub: [view file](https://github.com/arun-gupta/leading-without-script/blob/main/04-empathy-candor/cover.png). For tools that load image bytes by URL, use the [raw file](https://raw.githubusercontent.com/arun-gupta/leading-without-script/main/04-empathy-candor/cover.png). A path in prose alone is not an image.

---

## Workflow

Use an **image-capable** assistant (built-in image generation or an image API), not text-only chat.

1. Copy the **Single block** below into that assistant (palette and reference URLs are inside the block).
2. Paste the **book excerpt** under `PASTE BOOK EXCERPT`. Include the **title** for the overlay if it is not obvious from the excerpt. If needed, one line: **Chapter hero** (→ `cover.png`) or **inline figure** (→ `{slug}.png`).
3. Instruct: complete the **Agent tasks** and **deliver the finished image** (16:9 with title). Prefer reference-URL conditioning when the product supports **image + text**.
4. Save as **PNG** in that chapter’s folder next to `index.md`; link from `index.md` with alt text.

---

## Single block for AI

The palette lives **inside** this block so one paste is enough. Change hex here when you adjust the book colors.

Copy the **entire** fenced region below. Boundaries: line **`START AI BLOCK`** … line **`END AI BLOCK`** (banner lines mark the span; you may drop the banners in paste if they confuse the tool).

**Goal:** The assistant **renders the image** (pixels). Only if it cannot call any image generator should it fall back to a single text prompt for an external app.

```
================================================================================
START AI BLOCK
================================================================================

BOOK VISUAL BRIEF — Leading Without a Script

Primary instruction: Generate the **final image file** (bitmap) per this brief—do not stop at a text-only prompt unless image output is impossible in this environment.

Reference cover (image-aware tools): https://raw.githubusercontent.com/arun-gupta/leading-without-script/main/04-empathy-candor/cover.png · GitHub: https://github.com/arun-gupta/leading-without-script/blob/main/04-empathy-candor/cover.png · Use as reference input when the product supports **image + text**. If URLs or pixels are unavailable, rely on palette + style lines only.

Style: Same family as the reference—cool/warm split, purple/magenta blend where they meet, depth (texture, glow, light streaks), not clip art. Mood: opposites in balance, forward, grounded. Avoid random rainbows, meme look, handshake stock.

Palette (hex) — use only these:
  Cool:   deep navy #001F3F · cobalt #0047AB · cyan #00BFFF
  Warm:   burnt orange #CC5500 · orange #FF8C00 · gold #FFD700
  Blend:  purple #8A2BE2 · magenta alt #800080
  Neutrals: white #FFFFFF · charcoal #1A1A1A

Apply: cool blues on calmer / listening sides; warm oranges on direct / energetic sides; purple or magenta where they meet; white and charcoal for type and ground. Prefer dark ground (#1A1A1A or #001F3F) and light accents.

Text overlay: Put the **title** on the image (the chapter or section title supplied with the excerpt, or infer one short line from the excerpt if none given). Bold, clean **sans-serif**, **white** (#FFFFFF) or near-white; strong contrast (solid band or soft gradient behind type if needed). **Do not** paste body paragraphs into the art; title only unless the author asks for a short subtitle.

Output: PNG, 16:9, ~5% margin from edges; keep title inside safe area. Chapter folder only: cover.png (hero) or {slug}.png (kebab-case). No chapter prefix in the filename.

Agent tasks after the excerpt is pasted:
1) One strongest visual or metaphor for the passage (single focal idea).
2) Confirm the **exact title string** for the overlay (from the author or from the excerpt’s heading).
3) **Render the image:** 16:9, this palette and style, title on the art as specified, safe margins. Deliver a **downloadable or displayable image** (or attach the PNG). Use the reference URL as conditioning when supported.
4) **Fallback only:** If you cannot generate pixels here, output **one** detailed English prompt (plus negative hints if useful) for an external generator, and say which settings to use (16:9).
5) Filename: cover.png if hero; else {slug}.png from the topic.
6) One-line alt text for Markdown (describe the scene; the visible title can be mentioned briefly).

--- PASTE BOOK EXCERPT ---


================================================================================
END AI BLOCK
================================================================================
```

---

## Repo rules

| Rule | Value |
|------|--------|
| Format | PNG |
| Aspect | 16:9 (exception: `{slug}-4x5.png` etc. if you crop outside this doc’s default) |
| Location | Same folder as chapter `index.md` |
| Names | `cover.png` or `{purpose}.png` (kebab-case; optional `{name}@2x.png`) |

Shared cross-chapter assets: `assets/` with a unique name (e.g. `shared-topic-*.png`).

Print or vector masters: keep sources as you like; **in-repo figures stay PNG**.
