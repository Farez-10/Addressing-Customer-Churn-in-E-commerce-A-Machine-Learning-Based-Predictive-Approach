# Addressing Customer Churn in E-commerce: A Machine Learning–Based Predictive Approach

## 1. Project Overview

Proyek ini bertujuan untuk **memprediksi customer churn pada platform e-commerce** menggunakan pendekatan machine learning. Customer churn didefinisikan sebagai kondisi ketika pelanggan berhenti menggunakan layanan atau tidak lagi melakukan transaksi.

Dengan membangun model prediktif yang akurat, perusahaan dapat:

* Mengidentifikasi pelanggan yang berisiko churn lebih awal
* Menyusun strategi retensi pelanggan yang lebih efektif
* Mengurangi kerugian bisnis akibat kehilangan pelanggan

**Tujuan utama proyek:**

* Melakukan eksplorasi dan pemahaman data (Data Understanding & EDA)
* Membangun feature engineering yang relevan dengan perilaku pelanggan
* Membandingkan beberapa algoritma machine learning sebagai baseline model
* Melakukan penanganan data imbalance dengan teknik resampling
* Melakukan hyperparameter tuning untuk meningkatkan performa model
* Mengevaluasi model menggunakan metrik yang sesuai (F2-score)

---

## 2. Data Sources

Dataset yang digunakan merupakan data pelanggan e-commerce yang berisi informasi:

* Demografi pelanggan
* Perilaku transaksi dan penggunaan layanan
* Status churn (target variable)

Setiap baris data merepresentasikan **satu pelanggan unik**.

**Target Variable:**

* `Churn` (0 = Tidak Churn, 1 = Churn)

---

## 3. Data Understanding

### 3.1 Struktur Data

Dataset terdiri dari fitur numerik dan kategorikal, di antaranya:

* **Demografi:** Age, MaritalStatus, dll
* **Perilaku Pelanggan:** Tenure, DaySinceLastOrder, CashbackAmount
* **Preferensi:** PreferedOrderCat
* **Interaksi Layanan:** Complaint

### 3.2 Permasalahan Data

* Data imbalance pada target `Churn`
* Nilai kosong (missing values)
* Variabel kategorikal dengan banyak kategori

---

## 4. Exploratory Data Analysis (EDA)

EDA dilakukan untuk memahami pola dan karakteristik data, meliputi:

* Distribusi customer churn (menunjukkan data tidak seimbang)
* Analisis fitur numerik terhadap churn menggunakan histogram
* Analisis fitur kategorikal menggunakan churn rate per kategori

**Insight utama dari EDA:**

* Pelanggan dengan frekuensi komplain lebih tinggi cenderung churn
* Kategori produk tertentu memiliki churn rate lebih tinggi
* Pelanggan dengan jarak waktu transaksi terakhir yang lama lebih berisiko churn

---

## 5. Feature Engineering

Beberapa fitur baru dibuat untuk meningkatkan performa model:

* `RecencyFlag` → indikator pelanggan lama tidak bertransaksi
* `EngagementScore` → interaksi pelanggan dengan platform
* `HighCashback` → indikator insentif tinggi
* Transformasi dan encoding fitur kategorikal

Seluruh proses feature engineering dibungkus dalam **pipeline** menggunakan `ColumnTransformer`.

---

## 6. Modeling Approach

### 6.1 Baseline Models

Model yang dibandingkan:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Decision Tree
* Random Forest
* Gradient Boosting

Evaluasi menggunakan **Stratified K-Fold Cross Validation (5-fold)**.

### 6.2 Evaluation Metric

Digunakan **F2-score** karena:

* Lebih menekankan pada **Recall**
* Lebih sesuai untuk kasus churn, di mana kehilangan pelanggan (False Negative) lebih mahal dibanding False Positive

---

## 7. Handling Imbalanced Data

Untuk mengatasi data imbalance, dilakukan eksperimen dengan:

* Random Over Sampling (ROS)
* SMOTE
* Random Under Sampling (RUS)
* Condensed Nearest Neighbour (CNN)

Resampling diintegrasikan langsung ke dalam pipeline menggunakan `imblearn.Pipeline`.

---

## 8. Hyperparameter Tuning

Model terbaik (Gradient Boosting) ditingkatkan performanya menggunakan:

* GridSearchCV
* Tuning parameter utama seperti:

  * `n_estimators`
  * `learning_rate`
  * `max_depth`
  * `subsample`

---

## 9. Model Evaluation

Evaluasi akhir dilakukan menggunakan:

* Confusion Matrix
* Precision, Recall, F1-score

**Hasil utama:**

* Model mampu menangkap sebagian besar pelanggan churn (recall tinggi)
* Cocok digunakan sebagai sistem peringatan dini churn

---

## 10. Conclusion & Recommendation

### 10.1 Conclusion

Model machine learning berhasil mengidentifikasi pelanggan berisiko churn dengan performa yang baik, terutama setelah penerapan resampling dan hyperparameter tuning.

### 10.2 Business Recommendation

* Terapkan program retensi untuk pelanggan dengan risiko churn tinggi
* Fokus pada peningkatan pengalaman pelanggan yang sering komplain
* Gunakan model ini sebagai bagian dari sistem CRM

---

## 11. Technologies Used

* Python (Pandas, NumPy)
* Scikit-learn
* Imbalanced-learn
* Matplotlib & Seaborn
* Jupyter Notebook

---

## 12. Contact

* **Name:** Fahrezy Maulana Haz
* **Email:** [farez007100@gmail.com](mailto:farez007100@gmail.com)
* **LinkedIn:** [https://www.linkedin.com/in/fahrezy-maulana-haz](https://www.linkedin.com/in/fahrezy-maulana-haz)
