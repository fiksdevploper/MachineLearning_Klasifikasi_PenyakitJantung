# ❤️ Heart Disease Classification with Random Forest

## 📌 Problem Statement
Penyakit jantung merupakan penyebab kematian utama di seluruh dunia. Diagnosis dini dan akurat sangat krusial untuk mencegah komplikasi serius. Proyek ini bertujuan untuk membangun model klasifikasi menggunakan algoritma Random Forest yang mampu memprediksi risiko penyakit jantung berdasarkan data klinis.

---

## 📊 Dataset Description

- **Sumber**: [Heart Disease Dataset by mexwell (Kaggle)](https://www.kaggle.com/datasets/mexwell/heart-disease-dataset)
- **Jumlah Data**: 918 observasi
- **Target**: 
  - `0` → Tidak berisiko
  - `1` → Berisiko penyakit jantung
- **Fitur penting**:
  - `Age`, `RestingBP`, `Cholesterol`, `FastingBS`, `MaxHR`, `ExerciseAngina`, `ST_Slope`
- **Catatan khusus**:
  - Beberapa fitur memiliki missing values dan perlu preprocessing
  - Data bersifat tabular dan dapat langsung digunakan untuk supervised learning

---

## ⚙️ Model Pipeline

- **Preprocessing**:
  - Penanganan missing values dan fitur numerik
  - Encoding fitur kategorik
  - Scaling dengan `StandardScaler`
  - Pipeline menggunakan `scikit-learn`

- **Model**: 
  - `RandomForestClassifier` dengan hyperparameter tuning:
    - `n_estimators`
    - `max_depth`
    - `min_samples_split`
    - `max_features`

- **Saving Model**:
  - Model disimpan dalam format `.pkl` dengan `joblib`

---

## 📈 Model Evaluation

| Dataset         | Akurasi  | F1-score | Catatan                                   |
|-----------------|----------|----------|--------------------------------------------|
| Train Set       | 95.27%   | –        | Performa tinggi, hampir overfitting        |
| Test Set        | 91.60%   | 0.92     | Generalisasi baik, stabil                  |
| Unseen Data     | 90.34%   | 0.90     | Efektif terhadap data baru                 |
| Cross-Val       | ~89.50%  | –        | Validasi silang menunjukkan konsistensi    |

### 🧪 Evaluasi Tambahan
- Confusion Matrix
- Classification Report: Precision, Recall, F1-score
- Learning Curve
- Feature Importance: SHAP / Permutation (optional)
- ROC Curve & AUC

---


---

## 🧠 Insight & Recommendation

- Random Forest menunjukkan performa tinggi dan stabil
- Pipeline membuat proses prediksi lebih konsisten
- Model layak dipertimbangkan untuk implementasi sistem deteksi dini penyakit jantung
- Logging dan monitoring dapat ditambahkan untuk keperluan produksi

---

## 📎 Author

**Nama**: Muhammad Fikri
**Role**: Data Scientist in Progress  
**Fokus**: Membuat model machine learning yang lebih baik, evaluasi model, dan pengembangan portofolio machine learning

---
## 🗒️ Catatan
project ini mungkin belum begitu sempurna, namun saya akan selau tetap belajar dengan giat kedepannya untuk memangun model yang lebih baik dan andal
