# YOLO Object Detection Web App

An interactive web application built with **Gradio** and powered by the Hugging Face **YOLOS** (`hustvl/yolos-small`) model, designed for real-time object detection and visualization with customizable confidence thresholds.

---

## Features

* **Interactive Image Upload:** Upload any custom image or test using built-in COCO dataset examples.
* **Adjustable Confidence Threshold:** Fine-tune detection sensitivity on-the-fly using a dynamic Gradio slider.
* **Bounding Box Rendering:** Automatically overlays bounding boxes, class labels, and confidence scores directly onto detected objects using Matplotlib.
* **Public URL Generation:** Easily launch and share temporary public web demos directly from a Google Colab notebook.

---

## Requirements

1. Python
2. PyTorch
3. Transformers (`hustvl/yolos-small`)
4. Pillow (PIL)
5. Matplotlib
6. Gradio

---

## Installation & Setup

1. Open the project notebook in Google Colab or clone the repository locally.
2. Install the required dependencies:
```bash
pip install -q gradio transformers torch pillow matplotlib

```



---

## Usage

Run the notebook cells sequentially to initialize the YOLOS image processor, load the model, and launch the interactive Gradio interface.