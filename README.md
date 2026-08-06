# XDeepFake
<img width="1394" height="921" alt="image" src="https://github.com/user-attachments/assets/fc069193-5f85-4b28-bcb0-09e7e5328828" />

Browser-based, real-time deepfake image detector. It runs a Vision Transformer (ViT) model directly in your browser using ONNX Runtime Web, so images are analyzed locally and are not uploaded to any server by the page.

## Overview

XDeepFake lets you check whether an image is likely REAL or FAKE (AI-generated or manipulated). You can either upload an image or use a live camera feed, and inference is performed client-side in the browser.

## Features

- Real-time deepfake detection on uploaded images or a live camera feed
- Fully client-side inference via ONNX Runtime Web (no server upload from the page)
- Adjustable decision threshold to balance false positives and missed detections
- Reports prediction, confidence, fake score, and inference time
- Light and dark mode

## Files

- index.html - The web app (UI plus in-browser inference logic)
- vit_deepfake.onnx - The ViT deepfake detection model used for inference
- vit_tiny_student.pt - PyTorch checkpoint of the trained (distilled) student model

## Usage

1. Serve the repository over HTTP (for example, GitHub Pages or a local static server). Opening index.html directly from the file system may block model loading.
2. Open index.html in a modern browser.
3. Choose an input mode: Image upload or Live camera.
4. Load the model, then analyze an image or camera frame.
5. Adjust the decision threshold as needed. Higher values reduce false positives but can miss manipulated images.

The app expects the model at the path ./vit_deepfake.onnx relative to index.html.

## Model Export Note

ONNX Runtime Web does not support every quantized operator. If you see an error such as "Could not find an implementation for ConvInteger", re-export vit_deepfake.onnx as fp32, or use QDQ quantization (QuantFormat.QDQ) so the graph uses web-supported ops.

## Disclaimer

Research and educational use only. Predictions can be wrong, especially on compressed images, screenshots, or unseen editing styles.
