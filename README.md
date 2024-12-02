# About Project
Machine Learning model for Bank Marketing Campaign.

This project was created as a capstone project for Purwadhika Data Science Class Module 3.

## Introduction
Bank PWDK memiliki beberapa produk finansial, salah satunya adalah deposito. Dalam mengadakan campaign untuk menawarkan deposito sering kali Bank tidak mencapai target dan tidak tepat sasaran karena belum memanfaatkan profil nasabah. Oleh karena itu dibuatlah model machine learning untuk mengidentifikasi nasabah yang cenderung membuka deposito dengan harapan campaign berjalan secara efisien dan tepat sasaran sehingga bisa menghemat biaya, waktu dan sumber daya.

## Data Understanding
| Attribute | Data Type, Length | Description |
| --- | --- | --- |
| age | Int | Usia nasabah |
| job | String | Pekerjaan nasabah |
| balance | Int | Saldo nasabah |
| housing | String | Pinjaman nasabah untuk rumah|
| loan | String | Pinjaman nasabah |
| contact | String | Tipe komunikasi |
| month | String | Bulan terakhir dikontak |
| campaign | Int | Banyaknya kontak selama campaign sebelumnya |
| pdays | Int | Jumlah hari setelah terakhir dihubungi dari campaign sebelumnya|
| poutcome | String | Hasil campaign sebelumnya |
| deposit | String | Keputusan nasabah deposit |

## Data Cleaning
- Missing Values
- Duplication
- Outliers

## Data Analysis

### Feature Categorical
Hasil analisis kolom kategorikal `job`, `housing`, `loan`, `contact`, dan `month`:
- Nasabah terbanyak berdasarkan profesi: manajemen dan blue clollar
- Bulan Mei merupakan bulan terbanyak nasabah dihubungi sementara paling sedikit di Desember
- Mayoritas nasabah tidak memiliki pinjaman untuk cicilan rumah
- Mayoritas nasabah tidak memiliki pinjaman bank
- Nasabah paling sering dihubungi melalui telepon seluler
- Tingkat keberhasilan kampanye sebelumnya tidak diketahui

### Imbalance Check
| Deposit Status | Percentage  |
| -------------- | ----------- |
| No             | 52.23%      |
| Yes            | 47.77%      |

Data cenderung seimbang

## Data Preparation

### Encoding
1. Fitur `job` dan `poutcome`: binary encoding
2. Fitur `housing`, `loan`, dan `contact`: one hot encoding
3. Fitur `month`: ordinal encoding 

### Scaling
- Robust Scaler

## Modeling & Evaluation

### Model
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Trees
- Random Forest
- Extreme Gradient Boosting (XGB)
- Light Gradient Boosting Machine (LGBM)

### Evalulation
- Classification Report
- F1-Score
- ROC AUC
- Accuracy
- Recall
- Precision

### Hyperparameter Tuning
- Grid Search

### Feature Importance
- Month
- Balance
- Age

## Conclusion

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 0.70      | 0.82   | 0.76     | 741     |
| 1     | 0.77      | 0.64   | 0.70     | 711     |
| **Accuracy** |           |        |          | 0.69    |
| **Macro Avg** | 0.69      | 0.68   | 0.69     | 1603    |
| **Weighted Avg** | 0.69   | 0.69   | 0.69     | 1603    |
