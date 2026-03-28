# Image theme: Leading Without a Script

One visual system for chapter art: **cool vs warm**, **purple at the overlap**, **textured digital illustration** (not flat stock). Reference look: [`04-empathy-candor/cover.png`](../04-empathy-candor/cover.png) in the repo, or on GitHub: [view file](https://github.com/arun-gupta/leading-without-script/blob/main/04-empathy-candor/cover.png). For tools that load image bytes by URL, use the [raw file](https://raw.githubusercontent.com/arun-gupta/leading-without-script/main/04-empathy-candor/cover.png). A path in prose alone is not an image.

---

## Workflow

1. Copy the **Single block** below into your agent (it includes the palette). Include the **raw** reference URL from the intro when the tool can load images from a URL.
2. Paste the **book excerpt** under `PASTE BOOK EXCERPT`. If needed, one line: **Chapter hero** (→ `cover.png`) or **inline figure** (→ `{slug}.png`).
3. Run the **Agent tasks** in the block; generate from the prompt you get.
4. Save **PNG**, **16:9**, in that chapter’s folder next to `index.md`; link from `index.md` with alt text.

---

## Single block for AI (copy through “End of block”)

The palette lives **inside** this block so one paste is enough. Change hex here when you adjust the book colors.

```
BOOK VISUAL BRIEF — Leading Without a Script

Reference cover (image-aware tools): https://raw.githubusercontent.com/arun-gupta/leading-without-script/main/04-empathy-candor/cover.png · GitHub: https://github.com/arun-gupta/leading-without-script/blob/main/04-empathy-candor/cover.png · If the tool cannot load URLs, use palette + style lines below.

Style: Same family as the reference—cool/warm split, purple/magenta blend where they meet, depth (texture, glow, light streaks), not clip art. Mood: opposites in balance, forward, grounded. Avoid random rainbows, meme look, handshake stock.

Palette (hex) — use only these:
  Cool:   deep navy #001F3F · cobalt #0047AB · cyan #00BFFF
  Warm:   burnt orange #CC5500 · orange #FF8C00 · gold #FFD700
  Blend:  purple #8A2BE2 · magenta alt #800080
  Neutrals: white #FFFFFF · charcoal #1A1A1A

Apply: cool blues on calmer / listening sides; warm oranges on direct / energetic sides; purple or magenta where they meet; white and charcoal for type and ground. Prefer dark ground (#1A1A1A or #001F3F) and light accents. No text on image unless essential; then bold white sans, minimal.

Output: PNG, 16:9, ~5% margin from edges. Chapter folder only: cover.png (hero) or {slug}.png (kebab-case). No chapter prefix in the filename.

Agent tasks after the excerpt is pasted:
1) One strongest visual or metaphor for the passage (single focal idea).
2) Full image-generation prompt applying the brief; end with 16:9 widescreen.
3) Filename: cover.png if hero; else {slug}.png from the topic.
4) One-line alt text for Markdown.

--- PASTE BOOK EXCERPT ---


--- End of block ---
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
