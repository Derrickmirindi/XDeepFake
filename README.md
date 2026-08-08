# XDeepFake
<img width="1401" height="953" alt="image" src="https://github.com/user-attachments/assets/d2250af2-c245-4f64-abba-411ffaeec7db" />

## Live Demo

**Try it now:** https://derrickmirindi.github.io/XDeepFake/?v=6/

Browser-based, real-time deepfake image detector. It runs a Vision Transformer (ViT) model directly in your browser using ONNX Runtime Web, so images are analyzed locally and are not uploaded to any server by the page.

## Overview

XDeepFake lets you check whether an image is likely REAL or FAKE (AI-generated or manipulated). You can either upload an image or use a live camera feed, and inference is performed client-side in the browser.
<img width="1220" height="430" alt="image_ViT_new" src="https://github.com/user-attachments/assets/a52afa47-bf59-4f58-9302-33436c6f5fb2" />

## Features

- Real-time deepfake detection on uploaded images or a live camera feed
- Fully client-side inference via ONNX Runtime Web (no server upload from the page)
- Adjustable decision threshold to balance false positives and missed detections
- Reports prediction, confidence, fake score, and inference time
- Light and dark mode

## Development

The tool cannot be used for commercial purposes. Only can be used to foster education.
By Derrick Mirindi, Frederic Mirindi & David Sinkhonde



## Disclaimer

Research and educational use only. Predictions can be wrong, especially on compressed images, screenshots, or unseen editing styles.
