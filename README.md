# 🌊 Visualization of Wave Energy Density Hotspots from EEZ Satellite Images

---

## 📌 Overview

This project presents a robust image-processing pipeline to **identify and visualize wave energy density hotspots** in the **Gulf of Mannar** using **Sentinel-2 SAR satellite imagery**.  
The work is published in the **Q1 journal – Power System Technology**, demonstrating both academic value and real-world applicability.

We leverage modern techniques like:
- **Fuzzy-C Means Segmentation**
- **Wiener Filtering** (for speckle noise reduction)
- **Canny Edge Detection**
- **K-Means Clustering**
- **Geo-coordinate Extraction** using metadata

to automate and visualize potential **wave energy harvesting zones**.

---

## 🛰️ Journal Publication

- **📖 Title:** Visualization of Wave Energy Density Hotspots from EEZ Satellite Images  
- **📰 Journal:** *Power System Technology* (Q1 Rated)  
- **🔗 Link:** [Read Full Publication](https://powertechjournal.com/index.php/journal/article/view/1236)

---

## 🧠 Key Features

✔️ Satellite image preprocessing using **Wiener Filter**  
✔️ Speckle noise removal with high PSNR (10.73 dB) and low MSE (74.06)  
✔️ Segmentation using **Fuzzy-C Means** to isolate land and water bodies  
✔️ Edge detection via **Canny Algorithm**  
✔️ Clustering wave hotspots with **K-Means**  
✔️ Geo-mapping coordinates of top wave density zones  
✔️ Supports further integration for renewable energy infrastructure planning

---

## 🌍 Region of Study

- 🌐 **Location:** Gulf of Mannar, India (EEZ region)
- 🛰️ **Data Source:** Sentinel-2 SAR TIFF images
- 📦 **Dataset Size:** 100 images (512×512 pixels each)

---

## 🛠️ Technology Stack

| 🧩 Category         | ⚙️ Tools & Libraries               |
|--------------------|-----------------------------------|
| Programming        | Python                            |
| Image Processing   | OpenCV, skimage, NumPy            |
| Clustering         | scikit-learn (KMeans)             |
| Visualization      | Matplotlib, Seaborn               |
| Development Env.   | Google Colab / Jupyter Notebook   |

---

## 🧪 Methodology

The following steps describe the full process used to identify wave energy density hotspots from satellite images:

1. **Read SAR Images**
   - Load Sentinel-2 SAR images in Band-2 format (10-meter resolution).
   - Images are converted into NumPy arrays for processing.

2. **Preprocessing (Noise Removal)**
   - Apply **Wiener Filter** to remove speckle noise from SAR images.
   - Resize all images from 1024×1024 to 512×512 pixels.

3. **Segmentation**
   - Use **Fuzzy C-Means Segmentation** to differentiate between land and ocean.
   - Ensures that wave energy analysis is restricted to water regions only.

4. **Masking**
   - Perform **layer masking** to exclude land areas from the analysis.
   - Uses binary thresholding and bitwise operations.

5. **Edge Detection**
   - Apply **Canny Edge Detection** to extract wave structures.
   - Detects sharp transitions (edges) that often represent wave boundaries.

6. **Clustering**
   - Extract pixel coordinates of detected edges.
   - Use **K-Means Clustering** to identify energy density "hotspots" (wave clusters).

7. **Wave Energy Density Calculation**
   - Apply **Barrack’s Algorithm** to estimate wave energy density in J/m³.
   - Based on SAR backscatter intensity and empirical wave energy formulas.

8. **Geo-Localization**
   - Use metadata from Sentinel images to map hotspots to real-world latitude and longitude.
   - Coordinates for each detected cluster are computed and visualized.

9. **Visualization**
   - Hotspots and wave power distributions are displayed in 2D and 3D plots.
   - Includes cluster color-mapping, top hotspot coordinates, and percentage energy contribution.



---


## ✅ Advantages

- 🔄 Automates hotspot detection from SAR datasets  
- 🌐 Applicable across global coastal/EEZ regions  
- 🔧 Reduces manual effort in wave energy plant planning  
- 🔍 Enhances spatial accuracy of renewable energy scouting

---

## 🔭 Future Enhancements

- ✨ Integrate **Gaussian smoothing** for land-sea noise reduction  
- 🧠 Use **adaptive thresholding** for dynamic masking  
- ☁️ Extend model to support **real-time cloud-based processing**

---

## 👨‍💻 Authors & Contributors

- **Raja Reddy Nalamolu** — [rajareddy.n.1002@gmail.com](mailto:rajareddy.n.1002@gmail.com)  
- **Kallem Vamsi Kiran**  
- **Mutakani Yaswanth**

📚 **Guided by:** *Dr. S. Vasavi, MS, PhD*  
Department of Computer Science and Engineering  
**VR Siddhartha Engineering College**

---

## 💬 Citation

If you use this work in your research, please cite the journal article:

> **S. Vasavi, Nalamolu Raja Reddy, et al.**  
> *Visualization of Wave Energy Density Hotspots from EEZ Satellite Images*,  
> **Power System Technology**, 2023.  

---
