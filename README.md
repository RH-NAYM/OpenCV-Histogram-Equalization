# 💡 Histogram Equalization in OpenCV (Python Tutorial)
---
[![main branch](https://img.shields.io/badge/branch-main-red?style=flat&logo=git&logoColor=white)](https://github.com/RH-NAYM/OpenCV-Image-Thresholding/tree/main)
#

<p align="center">
  <a href="https://opencv.org/" target="_blank">
    <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-green?logo=opencv&logoColor=white">
  </a>
  <a href="https://www.python.org/" target="_blank">
    <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white">
  </a>
  <a href="https://jupyter.org/" target="_blank">
    <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white">
  </a>
  <a href="https://numpy.org/" target="_blank">
    <img src="https://img.shields.io/badge/Numpy-Numerical-lightblue?logo=numpy&logoColor=white">
  </a>
  <a href="https://matplotlib.org/" target="_blank">
    <img src="https://img_0.png">
  </a>
</p>



# 📌 Overview
This project provides a comprehensive guide to `Histogram Equalization` using `OpenCV` in Python. Histogram equalization is a fundamental computer vision technique used to improve the contrast of an image. It works by effectively spreading out the most frequent intensity values, stretching the dynamic range of the image.

This repository covers both global methods and advanced local adaptive methods (`CLAHE`) to handle various lighting conditions.
---

The Jupyter Notebook demonstrates:
- Global Histogram Equalization: Enhancing contrast using the entire image's intensity distribution.
- CLAHE (Contrast Limited Adaptive Histogram Equalization): Solving over-amplification of noise in local regions.
- Mathematical Intuition: Understanding Cumulative Distribution Functions (CDF).
- Color Image Processing: Equalizing color images without distorting hues.

`Whether you are dealing with medical X-rays, satellite imagery, or low-light photography, this repository serves as a practical toolkit for contrast enhancement.`

# 📁 Project Structure
```bash
.
├── 📓 Opencv-Histogram-Equalization.ipynb      # Comprehensive notebook on equalization
├── 📘 README.md                                # Project documentation
├── 📦 requirements.txt                        # Python dependencies
├── 🖼️ testImage.jpg                        # Sample image for demonstrations
└── 🛠️ tools                                        # Utility module for image handling
    ├── __pycache__                                  # Python cache directory (auto-generated)
    │   └── tools.cpython-312.pyc
    └── tools.py                                     # Helper functions for loading & visualization
```

# 📋 Table of Contents (Notebook Sections)
---
```bash
1. Introduction to Image Histograms
2. Mathematical Foundations (CDF & PDF)
3. Global Histogram Equalization (cv2.equalizeHist)
4. Histogram Comparison: Before vs. After
5. Limitations of Global Equalization
6. CLAHE (Contrast Limited Adaptive Histogram Equalization)
7. Parameter Tuning: clipLimit and tileGridSize
8. Equalizing Color Images (YUV/HSV Space)
9. Visual Comparisons and Analysis
```

# 🧠 What You’ll Learn
---
- The Math: How the transform function $h(v)$ uses the CDF to linearize the histogram.
$$h(v) = \text{round} \left( \frac{cdf(v) - cdf_{min}}{(M \times N) - cdf_{min}} \times (L - 1) \right)$$
- Global Enhancement: Using cv2.equalizeHist() for images with uniform lighting issues.
- Local Enhancement: Using cv2.createCLAHE() to prevent noise "blow-up" in dark areas.
- Histogram Visualization: Using Matplotlib to plot intensity distributions.

# 🛠️ Technologies Used
---
- `Python 3.x`
- `OpenCV` for morphological image processing
- `NumPy` for array operations
- `Matplotlib` for visualization
- `Jupyter Notebook` for interactive experimentation


# 📦 Installation
---
## 1️⃣ Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate    # Linux / macOS
venv\Scripts\activate       # Windows
```
## 2️⃣ Install dependencies
```bash
pip install -r requirements.txt
```
# 🚀 How to Run
---
**Option 1: Jupyter Notebook (Local)**
- Install Jupyter if needed: `pip install notebook`.
- Launch Jupyter: `jupyter notebook`.
- Open `Opencv-Histogram-Equalization.ipynb` and run cells sequentially.
    - Notebook will automatically download a placeholder image if testImage.jpg is missing.


**Option 2: Google Colab**
- Upload `Opencv-Histogram-Equalization.ipynb` to Colab.
- Install dependencies: `!pip install -r requirements.txt`.
- Run all cells for interactive demonstrations.


# ✅ Summary
---
- Histogram Equalization is essential for revealing hidden details in low-contrast images.
- CLAHE is generally superior for real-world images with non-uniform lighting.
- Visualizing the Histogram alongside the image is the best way to debug contrast issues.
- Always convert color images to a space like LAB or YCrCb before equalizing.


# 🍴 Real-World Applications
---
- Medical Imaging: Enhancing X-rays and MRI scans to highlight tissue structures.
- Security: Improving visibility in night-vision or foggy surveillance footage.
- Satellite Imagery: Balancing contrast in photos taken through atmospheric haze.
- Face Recognition: Normalizing lighting conditions before feature extraction.

# 📝 Contribution
`Feel free to open an issue or submit a pull request to add more advanced contrast stretching techniques or multi-spectral image examples.`
