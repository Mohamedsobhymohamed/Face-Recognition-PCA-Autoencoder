# 🧠 Face Recognition Assignment

This project explores dimensionality reduction, clustering, and classification techniques applied to face recognition using the ORL (AT&T) face dataset. It includes preprocessing, PCA-based compression, KMeans and GMM clustering, and KNN classification. An autoencoder is also implemented for deep feature extraction and unsupervised clustering evaluation.

---

## 📂 Project Structure

- `Face_Recognition_Assignment.ipynb` – Main notebook with all code, experiments, and visualizations.
- `README.md` – Project documentation.
- Dataset folder – Assumed to contain 40 subjects (s1, s2, ..., s40), each with 10 grayscale images.

---

## 🧪 Techniques Used

### 🧾 1. **Preprocessing**
- Grayscale face images are flattened to 1D vectors.
- Training and testing split: alternate images per subject.

### 🔻 2. **PCA (Principal Component Analysis)**
- Dimensionality reduced based on retained variance (`alpha` values: 0.8, 0.85, 0.9, 0.95).
- Visual comparison of PCA reconstruction and performance across alphas.

### 📊 3. **KMeans Clustering**
- Applied to PCA-reduced features.
- Cluster-to-label mapping via majority voting.
- Accuracy, F1-score, and confusion matrix are computed and plotted.

### 🤖 4. **KNN Classification**
- Used to classify PCA-reduced test data.
- Performance tested with various `k` values (e.g., 1, 3, 5).

### 🔁 5. **Clustering Accuracy via Hungarian Algorithm**
- Computes true clustering accuracy independent of label order.

### 🔥 6. **Autoencoder**
- Deep learning model built using Keras.
- Bottleneck layer used to extract compressed features.
- KMeans and GMM clustering evaluated on encoded representations.

---

## 📈 Results Summary

- PCA-reduced features give reasonable classification and clustering accuracy.
- Autoencoder-extracted features improve clustering performance significantly.
- Hungarian matching improves evaluation reliability for unsupervised learning.

---

## ⚙️ Requirements

Install dependencies via pip:

```bash
pip install numpy matplotlib seaborn scikit-learn tensorflow opencv-python

## 📸 Dataset
ORL (AT&T) Face Dataset

Link: ORL Database

Format: 10 grayscale images per person (92x112 pixels), 40 subjects.

Ensure dataset is structured as:
dataset_path/
├── s1/
│   ├── 1.pgm
│   ├── 2.pgm
│   └── ...
├── s2/
│   ├── ...
└── ...
## 📊 Visual Outputs
PCA Reconstruction Comparisons

Clustering Accuracy vs Alpha and K

Confusion Matrices

Autoencoder Loss Curves

## 🧠 Author
Mohamed Sobhy Saker

## 📜 License
This project is licensed under the MIT License – see the LICENSE file for details.
