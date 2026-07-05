# ✨ Free Image Enhancer (Real-ESRGAN on Google Colab)

Two Colab notebooks that upscale and enhance images for free using open-source
models — the same engine (Real-ESRGAN) behind tools like Upscayl, plus GFPGAN
for face restoration. The GPU runs on Google's servers, so any laptop or phone
works.

## The notebooks

| Notebook | What it is | Best for |
|---|---|---|
| `image_enhancer_colab.ipynb` | v1 — run cell-by-cell, batch-enhance multiple images, download as zip | Laptop use, batches |
| `enhancer_webapp_colab.ipynb` | v2 — launches a Gradio web app with a public link | Phone use, one-off enhancements |

## Quick start

1. Download a notebook from this folder
2. Go to [colab.research.google.com](https://colab.research.google.com) → **File → Upload notebook**
3. **Runtime → Change runtime type → T4 GPU → Save** ← the important step
4. Run the cells top to bottom (install takes ~2 min the first time)

For the web app version, Cell 2 prints a `https://xxxx.gradio.live` link —
open it on your phone, upload from your camera roll, and long-press the result
to save. The link works only while the Colab session is running; re-run Cell 2
to get a fresh one.

## Options

- **Model**: `photo` (real photos) or `anime` (illustrations/drawings)
- **Scale**: 2x or 4x
- **Face enhancement**: on for portraits, off for landscapes and objects

## Notes

- Faithful enhancement (Real-ESRGAN reconstructs likely detail); it can't
  recover truly lost information like blurry text.
- Free Colab sessions time out after a few hours of inactivity and daily GPU
  time is limited — fine for personal batches.
- Possible v2 upgrade: swap in a diffusion engine (e.g. Clarity Upscaler or
  SUPIR) on the same Colab setup for richer Krea/Magnific-style creative
  detail.
