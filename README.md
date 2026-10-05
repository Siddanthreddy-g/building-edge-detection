# 🏢 Building Edge Detection

This project uses a **deep learning U-Net model** to detect the **edges of buildings** from aerial or satellite images, so disaster-response teams can plan an optimised path through affected areas.

---

## 📂 Project Structure

- `dataset/`
  - `images/` — Input images for segmentation.
  - `masks/` — Ground truth masks for segmentation.
- `training.ipynb` — Jupyter Notebook used to train the improved model (`segmentation_model.h5`).
- `unet_model_training.py` — Script for training the initial U-Net model.
- `border.py` — Main script to perform edge detection.
- `segmentation_model.h5` — Trained model used by `border.py`.
- `image1.png`, `image2.png`, `image3.png`, `extra.png` — Sample satellite images.

---

## ⚙️ How to Run

1. **Install the required libraries**:

   ```bash
   pip install tensorflow opencv-python numpy
   ```

2. **Run edge detection** from the repository root (uses `segmentation_model.h5` on `image1.png`):

   ```bash
   python border.py
   ```

3. *(Optional)* Retrain the model with `training.ipynb` or `unet_model_training.py`.
