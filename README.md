# 🧫 Cell Counter App

A MATLAB GUI application for loading, enhancing, segmenting, and counting cells in microscopy images. Built using MATLAB’s `uifigure` and `uiaxes` components, this tool provides a simple, interactive interface for image-based cell analysis.

## 📸 Features

- **Load Images**: Import `.png`, `.jpg`, or `.tif` files.
- **Image Enhancement**: Convert to grayscale, apply median filtering, and adjust contrast.
- **Segmentation**: Perform binary thresholding and watershed-based segmentation.
- **Cell Counting**: Automatically detect and count segmented cell regions.
- **Threshold Control**: Adjustable size filter to remove noise or small artifacts.

---

## 🚀 Getting Started

### Prerequisites

- MATLAB R2019b or later
- Image Processing Toolbox

### Installation

1. Clone this repository or download the code.
2. Place an initial display image (optional) named `ini.png` in the same folder.
3. Run the app:

```matlab
cellCounterApp
```

---

## 🖥️ UI Overview

| UI Element         | Function                                      |
|--------------------|-----------------------------------------------|
| **Load Image**     | Select and display a microscopy image         |
| **Enhance Image**  | Grayscale, filter, and adjust contrast        |
| **Segment Image**  | Apply segmentation and remove small artifacts |
| **Count Cells**    | Count and highlight detected cells            |
| **Size Threshold** | Minimum pixel area for counting objects       |

---

## 🧠 How It Works

1. **Enhancement**:
   - Convert RGB to grayscale
   - Apply `medfilt2` and `imadjust`

2. **Segmentation**:
   - Convert to binary image using `imbinarize`
   - Clean noise with `imopen`
   - Apply `watershed` algorithm
   - Filter regions using `bwareaopen`

3. **Counting**:
   - Use `bwconncomp` to count connected regions
   - Outline and visualize cells on the original image

---

## 📂 File Structure

```
📁 CellCounterApp/
├── cellCounterApp.m       # Main application code
├── ini.png                # Optional startup image
```

---

## 📷 Sample

![image](https://github.com/user-attachments/assets/0c7fa5e8-1763-4cb3-9bb0-5fa62897e3d5)

---

## 📃 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements

- MATLAB's `Image Processing Toolbox`
- Inspiration from typical biological image segmentation workflows
