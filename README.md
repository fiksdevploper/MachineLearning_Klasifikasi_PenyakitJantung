# ❤️ Heart Disease Classification with Random Forest

## 📌 Problem Statement
Penyakit jantung merupakan penyebab kematian utama di seluruh dunia. Diagnosis dini dan akurat sangat krusial untuk mencegah komplikasi serius. Proyek ini bertujuan untuk membangun model klasifikasi menggunakan algoritma Random Forest yang mampu memprediksi risiko penyakit jantung berdasarkan data klinis.

---

## 📊 Dataset Description

- **Sumber**: [Heart Disease Dataset by mexwell (Kaggle)](https://www.kaggle.com/datasets/mexwell/heart-disease-dataset)
- **Jumlah Data**: 918 observasi
- **Target**: 
  - `0` → Normal
  - `1` → Mengidap penyakit jantung

### 🧬 Fitur dan Penjelasan

| Fitur | Kode | Tipe | Deskripsi |
|------|------|------|-----------|
| Age | `age` | Numerik | Usia pasien dalam tahun |
| Sex | `sex` | Binary | `1`: Pria, `0`: Wanita |
| Chest Pain Type | `chest pain type` | Nominal | `1`: Typical angina, `2`: Atypical angina, `3`: Non-anginal pain, `4`: Asymptomatic |
| Resting BP | `resting bp s` | Numerik | Tekanan darah istirahat (mm Hg) |
| Cholesterol | `cholesterol` | Numerik | Kadar kolesterol (mg/dl) |
| Fasting Blood Sugar | `fasting blood sugar` | Binary | `1`: >120 mg/dl, `0`: <=120 mg/dl |
| Resting ECG | `resting ecg` | Nominal | `0`: Normal, `1`: ST-T abnormality, `2`: LV hypertrophy |
| Max Heart Rate | `max heart rate` | Numerik | Denyut jantung maksimal |
| Exercise Angina | `exercise angina` | Binary | `1`: Ya, `0`: Tidak |
| ST Depression | `oldpeak` | Numerik | Penurunan ST saat latihan |
| ST Slope | `ST slope` | Nominal | `1`: Upsloping, `2`: Flat, `3`: Downsloping |

---

## ⚙️ Model Pipeline

- **Preprocessing**:
  - Penanganan missing values
  - Encoding fitur kategorikal
  - Scaling numerik (`StandardScaler`)
  - Pipeline dengan `scikit-learn`

- **Model**:
  - `RandomForestClassifier`
  - Tuning: `n_estimators`, `max_depth`, `min_samples_split`, `max_features`

- **Model Saving**:
  - Model disimpan sebagai `.pkl` menggunakan `joblib`

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
- Classification Report
- Learning Curve
- ROC & AUC
- Feature Importance: SHAP / Permutation (opsional)

---

---

## 📎 Author

**Nama**: Muhammad Fikri
**Role**: Data Scientist  
**Fokus**: API deployment, model evaluation, machine learning portfolio projects

---
