Addressing Customer Churn in E-commerce:
A Machine Learning–Based Predictive Approach
Project Overview

Customer churn merupakan salah satu tantangan utama dalam bisnis e-commerce. Kehilangan pelanggan tidak hanya berdampak pada penurunan pendapatan, tetapi juga meningkatkan biaya akuisisi pelanggan baru.

Proyek ini bertujuan untuk membangun model Machine Learning yang mampu memprediksi pelanggan yang berpotensi churn, sehingga perusahaan dapat melakukan tindakan preventif secara lebih efektif dan tepat sasaran.

Business Problem

Perusahaan e-commerce mengalami kesulitan dalam mengidentifikasi pelanggan yang berisiko berhenti menggunakan layanan. Tanpa sistem prediksi yang akurat, strategi retensi pelanggan menjadi tidak optimal dan cenderung reaktif.

Project Goals

Membangun model klasifikasi untuk memprediksi customer churn

Mengidentifikasi faktor-faktor utama yang memengaruhi churn

Membantu perusahaan memprioritaskan strategi retensi pelanggan

Analytic Approach

Pendekatan analitik yang digunakan dalam proyek ini meliputi:

Data Understanding

Exploratory Data Analysis (EDA)

Feature Engineering

Model Benchmarking (beberapa algoritma)

Handling Imbalanced Data (Resampling)

Hyperparameter Tuning

Model Evaluation & Selection

Data Understanding

Setiap baris pada dataset merepresentasikan satu pelanggan e-commerce yang unik. Tahap ini bertujuan untuk memahami struktur data, karakteristik fitur, serta relevansinya terhadap permasalahan churn.

Target Variable

Churn

0 : Pelanggan tidak churn

1 : Pelanggan churn

Kelompok Fitur dan Artinya
1. Customer & Transaction Information

Tenure : Lama pelanggan bergabung (bulan)

CityTier : Tingkat kota tempat pelanggan tinggal

PreferredLoginDevice : Perangkat yang paling sering digunakan pelanggan

PreferredPaymentMode : Metode pembayaran utama pelanggan

PreferedOrderCat : Kategori produk yang paling sering dipesan

SatisfactionScore : Tingkat kepuasan pelanggan

2. Behavioral & Engagement Features

NumberOfDeviceRegistered : Jumlah perangkat yang terdaftar

OrderCount : Jumlah transaksi pelanggan

DaySinceLastOrder : Jarak waktu sejak transaksi terakhir

CashbackAmount : Total cashback yang diterima pelanggan

3. Customer Support Indicator

Complaint : Menunjukkan apakah pelanggan pernah mengajukan komplain

Tahap Data Understanding memastikan setiap fitur memiliki makna bisnis yang jelas dan relevan untuk memprediksi churn.

Exploratory Data Analysis (EDA)

EDA dilakukan untuk mengeksplorasi pola dan hubungan antara fitur dengan churn.

Insight Utama dari EDA

Dataset bersifat imbalanced, pelanggan tidak churn lebih dominan

Pelanggan dengan jarak waktu transaksi terakhir yang lama memiliki kecenderungan churn lebih tinggi

Pelanggan dengan engagement rendah (order sedikit, device terbatas) lebih berisiko churn

Beberapa kategori produk dan karakteristik pelanggan menunjukkan churn rate yang lebih tinggi

Insight ini menjadi dasar untuk feature engineering, pemilihan metrik evaluasi, dan strategi resampling.

Modeling & Evaluation

Algoritma yang digunakan:

Logistic Regression

KNN

Decision Tree

Random Forest

Gradient Boosting

Evaluasi menggunakan F2-score untuk memprioritaskan recall (mengurangi false negative churn)

Penanganan imbalance menggunakan teknik resampling

Hyperparameter tuning dilakukan untuk meningkatkan performa model terbaik

Final Output

Model terbaik disimpan dalam format pickle dan dapat digunakan untuk:

Prediksi churn pelanggan baru

Mendukung strategi retensi pelanggan berbasis data

Author

Fahrezy Maulana Haz
📧 Email: farez007100@gmail.com

🔗 LinkedIn: https://www.linkedin.com/in/fahrezy-maulana-haz
