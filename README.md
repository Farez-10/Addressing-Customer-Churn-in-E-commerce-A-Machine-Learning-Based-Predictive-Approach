# Addressing Customer Churn in E-commerce: A Machine Learning–Based Predictive Approach

## Overview

Proyek ini merupakan Capstone Project Module 3 yang berfokus pada pemanfaatan Machine Learning untuk memprediksi **customer churn** pada perusahaan e-commerce. Customer churn merupakan permasalahan bisnis yang krusial karena berdampak langsung pada penurunan pendapatan serta peningkatan biaya akuisisi pelanggan baru.

Melalui analisis data historis pelanggan, proyek ini bertujuan untuk membangun model klasifikasi yang mampu mengidentifikasi pelanggan dengan risiko churn tinggi sehingga perusahaan dapat melakukan tindakan retensi secara lebih efektif dan tepat sasaran.

---

## Business Problem

Perusahaan e-commerce memiliki basis pelanggan yang besar, namun tidak semua pelanggan dapat dipertahankan dalam jangka panjang. Kehilangan pelanggan (churn) sering kali terjadi tanpa tanda yang jelas dan baru disadari setelah pelanggan berhenti bertransaksi.

Tanpa sistem prediksi yang baik, perusahaan berisiko:

* Kehilangan pelanggan bernilai tinggi
* Mengalokasikan biaya promosi dan retensi secara tidak efisien
* Mengambil keputusan bisnis secara reaktif, bukan preventif

---

## Objectives

Tujuan utama dari proyek ini adalah:

1. Membangun model Machine Learning untuk memprediksi kemungkinan customer churn.
2. Mengidentifikasi pola dan karakteristik pelanggan yang berpotensi churn.
3. Menyediakan insight yang dapat digunakan sebagai dasar strategi retensi pelanggan.

---

## Dataset

Dataset yang digunakan adalah **data_ecommerce_customer_churn.csv**, yang berisi informasi demografis, perilaku transaksi, tingkat kepuasan, serta status churn pelanggan.

Target variabel:

* `Churn` (0 = Tidak Churn, 1 = Churn)

---

## Project Workflow

Tahapan pengerjaan proyek ini meliputi:

1. **Business Understanding**

   * Memahami permasalahan bisnis dan tujuan analisis

2. **Data Understanding**

   * Eksplorasi struktur data, tipe variabel, dan distribusi target

3. **Exploratory Data Analysis (EDA)**

   * Analisis distribusi churn
   * Analisis fitur numerik dan kategorikal terhadap churn

4. **Data Cleaning & Feature Engineering**

   * Penanganan missing value
   * Pembuatan fitur baru berbasis perilaku pelanggan

5. **Preprocessing & Pipeline**

   * Encoding fitur kategorikal
   * Scaling fitur numerik
   * Pipeline terintegrasi dengan resampling

6. **Baseline Model Benchmarking**

   * Perbandingan beberapa algoritma klasifikasi
   * Evaluasi menggunakan F2-score

7. **Handling Imbalanced Data**

   * Eksperimen teknik resampling (ROS, SMOTE, RUS, CNN)

8. **Hyperparameter Tuning**

   * Tuning model terbaik menggunakan GridSearchCV

9. **Model Evaluation**

   * Confusion Matrix
   * Classification Report

10. **Model Saving**

    * Penyimpanan model final menggunakan pickle

---

## Models Evaluated

Beberapa model yang dievaluasi dalam proyek ini antara lain:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest
* Gradient Boosting

Pemilihan model terbaik didasarkan pada performa **F2-score**, dengan fokus pada kemampuan mendeteksi pelanggan churn.

---

## Evaluation Metric

Metric utama yang digunakan adalah **F2-score**, karena:

* Customer churn merupakan kelas minoritas
* False negative (gagal mendeteksi churn) memiliki dampak bisnis yang lebih besar

Metric pendukung:

* Precision
* Recall
* Confusion Matrix

---

## Key Results

Model final menunjukkan kemampuan yang baik dalam mendeteksi pelanggan churn dengan recall yang tinggi, sehingga dapat digunakan sebagai alat bantu pengambilan keputusan untuk strategi retensi pelanggan.

---

## Business Impact

Dengan implementasi model ini, perusahaan dapat:

* Mengidentifikasi pelanggan berisiko churn lebih awal
* Memfokuskan program retensi secara lebih efisien
* Mengurangi kehilangan pendapatan akibat churn

---

## Repository Structure

```
├── Addressing Customer Churn in E-commerce.ipynb
├── data_ecommerce_customer_churn.csv
├── churn_model.pkl
└── README.md
```

---

## How to Run

1. Pastikan seluruh library yang dibutuhkan telah terinstal
2. Jalankan notebook `Addressing Customer Churn in E-commerce.ipynb`
3. Model final akan disimpan dalam format pickle

---

## Author

Capstone Project Module 3 – Machine Learning

---

## Notes

Proyek ini disusun untuk tujuan pembelajaran dan evaluasi akademik, serta dapat dikembangkan lebih lanjut dengan data tambahan dan algoritma yang lebih kompleks.
