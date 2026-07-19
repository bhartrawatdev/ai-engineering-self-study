# MA101 — Main Project: Image Compression via SVD

This is the standalone spec for MA101's Main Project (also summarized in `MA101.md`). Use this file as your working checklist while building.

## Description

A from-scratch (NumPy-only) tool that compresses a grayscale image using Singular Value Decomposition. This project exists to make SVD — the most broadly useful decomposition in this course — into something you've watched work on a real, visual example, not just a formula you can recite.

## Requirements

- [ ] Load a grayscale image as a 2D NumPy array (a matrix of pixel intensities).
- [ ] Compute its SVD using `numpy.linalg.svd`.
- [ ] Reconstruct an approximation of the image using only the top-*k* singular values/vectors, for at least 4 different values of *k* (e.g. 5, 20, 50, 100).
- [ ] Display or save the original image alongside each compressed reconstruction.
- [ ] Label each reconstruction with its compression ratio (original data size vs. reconstructed data size at that *k*).
- [ ] Write a short explanation (in this project's README) of what the top singular values represent, in your own words, and why keeping only a few still produces a recognizable image.

## Suggested File Layout

```
svd-image-compression/
├── compress.py          ← SVD logic, reconstruction at a given k
├── main.py               ← CLI entry point, loads image, runs comparisons, saves outputs
├── sample_image.png      ← the image you're compressing
├── outputs/               ← saved before/after comparison images
├── requirements.txt
└── README.md               ← how to run it + your explanation of the singular values
```

## Stretch Goals

- [ ] Extend the tool to work on color images (apply SVD independently per color channel, then recombine).
- [ ] Plot the singular values in descending order and use the plot to justify a "good" choice of *k* for this specific image (where the curve visibly flattens).
- [ ] Compare your from-scratch SVD compression against standard JPEG compression at a roughly equivalent file size, visually and via mean squared error.

## What "Done" Looks Like

- The tool runs end-to-end on at least one real image you provide, producing a clear before/after comparison at multiple compression levels.
- You can explain, without notes, why a low-rank approximation using only the top-*k* singular values still resembles the original image.
- The code is organized into functions across at least two files, pushed to this repo's `Projects/` folder with a README including the compressed output images.

## Notes on Getting a Test Image

Any grayscale (or grayscale-converted) image works — a photo you take yourself, a public domain image, or a simple generated test pattern. Keep the resolution modest (e.g. under 500×500) while developing so SVD computation stays fast; scale up once the pipeline works end-to-end.
