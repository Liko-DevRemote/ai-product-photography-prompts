# AI Product Photography Prompts (Glass, Liquid & Studio Lighting)

A practical, copy-pasteable reference for generating studio product shots with **Qwen Image 2.1 Turbo**. 

This guide focuses on transparent materials, refractive liquids, and dark studio environments—specifically designed for indie fragrance founders and packaging designers who need rapid concept frames before committing to a physical shoot or 3D render pass.

---

## 1. Core Prompting Principles for Product Shots

When writing **AI product photography prompts**, vague aesthetic adjectives usually fail on reflective surfaces. Instead, structure your prompt around five concrete tokens:

1. **Subject:** Define the exact vessel or form factor (e.g., *perfume bottle*, *dropper bottle*).
2. **Material:** State both the outer shell and the inner contents (e.g., *faceted glass*, *amber liquid*).
3. **Light:** Specify the modifier, not just the mood (e.g., *soft box lighting*, *golden-hour rim light*).
4. **Background & Surface:** Give the light something to bounce off (e.g., *wet black stone*, *minimal background*).
5. **Aspect Ratio:** Match the placement right from generation:
   * `1:1` (default) is best for e-commerce catalog grids.
   * `9:16` works well for social Stories and adds natural top padding for UI or headline overlays.

### Label & Brand Text Rules
If you are testing typography on packaging:
* Always wrap the exact brand or label text in **English double quotes** (e.g., `"AURA"`).
* Keep the quoted text to **at most three words**. Longer ingredient lists or taglines increase character drift on curved glass.

---

## 2. Copy-Ready Prompts & Variants

### Prompt 1: The Verified Baseline (Faceted Glass on Wet Stone)
*Default Aspect Ratio: `1:1`*

```text
Studio product photo of a faceted glass perfume bottle with an amber liquid on a wet black stone, soft box lighting, water droplets, minimal background, high-end advertising look
```

**Why this prompt works:**
* **Refraction & inner glow:** Explicitly naming *faceted glass* alongside *amber liquid* forces the model to calculate refraction and produces a warm inner highlight through the center of the bottle.
* **Grounding the object:** *Wet black stone* provides a natural specular reflection at the base and pairs logically with *water droplets*.
* **Clean edges:** Combining *soft box lighting* with a *minimal background* prevents blown-out white edges on the glass shoulders.

You can inspect the reference output or run the [Perfume Bottle Product Shot Prompt](https://turboimagegen.com/prompts/perfume-bottle-product-shot/?utm_source=github&utm_medium=platform-content&utm_campaign=2026w47) directly in the browser (the online generator lets you run 2 watermarked previews with no sign-up, and generations typically take about 15–30 seconds).

---

### Prompt 2: Variant A — Dusty-Rose & Frosted Acrylic
Swaps the heavy stone and warm amber for a softer, contemporary cosmetic palette while keeping the same studio geometry.

```text
Studio product photo of a faceted glass perfume bottle with a dusty-rose pink-rose liquid on frosted acrylic, soft box lighting, water droplets, minimal background, high-end advertising look
```

**What changes:**
* Switching to *frosted acrylic* softens the bottom reflection into a diffused matte glow rather than a sharp mirror reflection.
* The *dusty-rose / pink-rose liquid* shifts the internal refraction toward pastel tones without losing contrast against the glass facets.

---

### Prompt 3: Variant B — Packaging Concept with Quoted Label Text
Adds a clean paper label to test front-of-pack hierarchy.

```text
Studio product photo of a faceted glass perfume bottle with an amber liquid and a white rectangular label reading "AURA" on a wet black stone, soft box lighting, water droplets, minimal background, high-end advertising look
```

**What changes:**
* Specifying *a white rectangular label reading "AURA"* gives the text renderer a flat, high-contrast bounding box so the letters don't warp into the glass facets.
* Stick to 1–3 words inside the English double quotes when testing your own brand names.

---

### Prompt 4: Variant C — Golden-Hour Rim / Contour Light
Moves away from neutral commercial soft boxes toward a moodier editorial contour.

```text
Studio product photo of a faceted glass perfume bottle with an amber liquid on a wet black stone, golden-hour rim contour light, water droplets, minimal background, high-end advertising look
```

**What changes:**
* *Golden-hour rim contour light* traces the outer silhouette of the stopper and bottle edges, creating warm directional streaks across the wet stone.

---

## 3. Troubleshooting: Fixing Lost Edges on Dark Glass

A common failure mode in studio product generation is **dark glass on a dark background**. When both the vessel and the backdrop share low luminance values, the bottle edges dissolve into the shadow.

If your bottle silhouette disappears into the background, apply one of these two fixes:

| Issue | Fix in the Prompt | Why It Fixes the Silhouette |
| :--- | :--- | :--- |
| Bottle center looks muddy or merges with the dark backdrop | **Keep a bright liquid inside the bottle** (e.g., *amber liquid*, *bright golden liquid*, *pink-rose liquid*) | Acts as an internal backlight, separating the front and back walls of the glass through refraction. |
| Outer glass edges vanish into a black background | **Switch to bright dual rim light** | Places symmetric highlights along both vertical edges of the bottle, carving the shape out of the dark scene. |

**Copy-ready edge-recovery tweak:**

```text
Studio product photo of a faceted glass perfume bottle with a bright amber liquid on a wet black stone, bright dual rim light, water droplets, minimal background, high-end advertising look
```

---

## 4. Related Product Prompt Index

If you are building a wider moodboard beyond fragrance bottles, the [TurboImageGen prompt library](https://turboimagegen.com/prompts/?utm_source=github&utm_medium=platform-content&utm_campaign=2026w47) also indexes these verified product setups:

* **Skincare Serum on Marble**
* **Headphones Product Shot**
* **Ceramic Mug Flat Lay**
* **Multi-Reference Product Lifestyle Scene**

---

## 5. Runtime, Pricing & License Notes

* **Speed:** Online generations with Qwen Image 2.1 Turbo typically take **15–30 seconds**.
* **Testing & Quotas:** You can test prompts online with **2 watermarked previews (no sign-up required)**. After signing up, accounts include 10 free 1K images without a watermark, and paid packs start at $9.90 for 200 images at 2K resolution without watermarks.
* **Open-Weight Licensing:** If you are running the open weights locally rather than using the hosted generator, note that the weights use the **Qwen Research License**—research and evaluation are allowed, while commercial use requires a separate license from Qwen. Also keep in mind that third-party "Uncensored GGUF" uploads circulating on community hubs are community conversions, not official releases.

