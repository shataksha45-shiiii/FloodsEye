# FloodEye: Satellite-Based Disaster Analysis System 

**FloodEye** is a deep learning-based flood severity detection system that utilizes Synthetic Aperture Radar (SAR) imagery from the Sentinel-1 satellite constellation.

![Flood Result](assam_flood_result.png)
*(Above: Real-world detection of flood expansion in the Brahmaputra River, Assam, July 2024)*

##  Key Features
- **Satellite Integration:** Automated pipeline fetching real-time SAR data via Google Earth Engine (GEE).
- **Deep Learning Core:** Custom U-Net architecture with a ResNet34 backbone for semantic segmentation.
- **Robustness:** Trained on global datasets (Sen1Floods11) and successfully tested on unseen Indian geographies (Assam/Brahmaputra).
- **Quantifiable Impact:** Calculates exact flood area expansion (e.g., 1.64 km² detected in test cases).

##  Tech Stack
- **Frameworks:** PyTorch, Segmentation Models PyTorch (SMP)
- **Data Source:** Google Earth Engine (Copernicus Sentinel-1 Data)
- **Processing:** Rasterio, OpenCV, NumPy
- **Visualization:** Matplotlib

## Methodology
1. **Data Acquisition:** Sentinel-1 (VV/VH polarization) data is pulled for the target region/date.
2. **Preprocessing:** Speckle filtering and normalization (-50dB to 0dB clipping).
3. **Inference:** The U-Net model segments water vs. land.
4. **Severity Logic:** Permanent water channels are subtracted from the prediction to isolate *flood* waters.

##  Author
**Shataksha Raj Sharma** *Electronics & Communication Engineering, IIIT Naya Raipur* ```

