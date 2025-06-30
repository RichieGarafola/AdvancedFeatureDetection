
# Advanced Marker Detection Using SIFT, ORB, and AKAZE

This project uses OpenCV to detect a reference **marker image** within a set of **scene images** using local keypoint descriptors such as **SIFT**, **ORB**, and **AKAZE**. It applies feature detection and brute-force matching to identify whether the marker is present and classifies each scene accordingly.

> Developed for Capella University's CSC-FPX4040  
> Combines classic computer vision with performance-tuned feature descriptors.

---

## Features

- Use SIFT, ORB, or AKAZE descriptors for flexible detection
- Visualize keypoints and matched features
- Classify images into `Positives` and `Negatives`
- Save annotated results into organized output folders

---

## Project Structure

```bash
.
├── AdvancedFeatureDetection.ipynb         # Main notebook
├── marker.png                             # Input marker image
├── scenes/                                # Folder of scene images to scan
├── output/
│   ├── Positives/                         # Images containing marker
│   └── Negatives/                         # Images without marker
├── requirements.txt
└── README.md
```

---

## Setup & Usage

### 1. Install Required Packages

```bash
pip install -r requirements.txt
```

Or manually:

```bash
pip install opencv-python matplotlib numpy
```

### 2. Run the Notebook

```bash
jupyter notebook Assessment5_FeatureDetection.ipynb
```

Follow the prompts to:
- Enter the **marker image path**
- Choose the **descriptor type**: `sift`, `orb`, or `akaze`
- Provide the **scene images folder**
- Specify an **output directory**

---

## Algorithm Details

- **Descriptors**: Extract keypoints using chosen algorithm
- **Matcher**: Brute-Force with Lowe’s Ratio Test
- **Threshold**: Images with ≥10 good matches are classified as `Positives`
- **Overlay**: Matching images are optionally displayed using `cv2.drawMatches`

---

## Output Example

| Match Type | Description |
|------------|-------------|
| Positive   | Marker found in the scene (≥10 matches) |
| Negative   | No sufficient keypoint matches |

Images are saved under `output/Positives` and `output/Negatives`.

---

## Learning Objectives

- Understand the application of different keypoint detectors
- Evaluate matching performance using real-world scenes
- Apply thresholding logic to automate classification
- Learn modular OpenCV practices for image matching

---

## Acknowledgements

- Developed as part of **CSC‑FPX4040: Computer Vision**
- Thanks to OpenCV contributors for robust descriptor APIs

---

## License

This repository is for academic and learning use.  
Reuse and contributions welcome with attribution.

---
