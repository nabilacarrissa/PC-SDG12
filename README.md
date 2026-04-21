# 🗑️ Klasifikasi Sampah Menggunakan Citra

## Machine Learning & Deep Learning (CNN vs SVM, Decision Tree, Random Forest)

---

## 👤 Informasi

- **Nama:** Nabila Carrissa Dewi
- **Repository:** https://github.com/username/garbage-classification
- **Platform:** Google Colab / Python Environment

---

## 1. 🎯 Ringkasan Proyek

Proyek ini bertujuan untuk **melakukan klasifikasi jenis sampah berbasis citra menggunakan pendekatan Machine Learning dan Deep Learning, serta membandingkan performa beberapa model untuk mengetahui algoritma terbaik pada kondisi dataset terbatas.**

Tahapan utama dalam proyek ini meliputi:

1. Melakukan preprocessing citra
2. Ekstraksi fitur menggunakan:
   - CNN (Deep Learning features)
   - HOG (Handcrafted features)
3. Membangun beberapa model klasifikasi:
   - CNN
   - SVM
   - Decision Tree
   - Random Forest
4. Melakukan evaluasi performa model
5. Menentukan model terbaik berdasarkan hasil evaluasi

---

## 2. 📄 Problem & Goals

### **Problem Statements**

1. Klasifikasi sampah secara manual tidak efisien dan membutuhkan waktu.
2. Diperlukan sistem otomatis untuk mengenali jenis sampah berbasis citra.
3. Perlu analisis perbandingan antara CNN dan machine learning klasik pada dataset terbatas.

### **Goals**

1. Mengembangkan sistem klasifikasi sampah berbasis citra.
2. Membandingkan performa CNN dengan SVM, Decision Tree, dan Random Forest.
3. Menganalisis efektivitas fitur HOG dibandingkan fitur otomatis CNN.
4. Menentukan model terbaik untuk klasifikasi sampah.

---

## 📁 Struktur Folder
```
Garbage-Classification-System/
├── dataset/
│
├── output_model/
│   ├── model_cnn.h5
│   ├── model_svm.pkl
│   ├── model_rf.pkl
│   ├── model_dt.pkl
│   ├── scaler.pkl
│   └── label_encoder.pkl
│
├── notebooks/
│
├── src/
│
└── README.md
---

## 3. 📊 Dataset

- **Nama Dataset:** Garbage Classification Dataset
- **Sumber:** Kaggle
- **Jumlah Data:** 2.527 Data Gambar
- **Kategori:** 7 jenis sampah (plastic, paper, metal, glass, cardboard, dll.)

### **Fitur Utama**

| Komponen               | Deskripsi                               |
| -----------------------| --------------------------------------- |
| Jenis Data             | Iamge ( citra Sampah )                  |
| Format                 | JPG/PNG                                 |
| Task                   | Multi-class classification              |
| Jumlah Kelas           |  7 Kategori                             |  

---

## 4. 🔧 Data Preparation

Tahapan data preparation yang dilakukan:

- **Resize gambar:**  
  1. CNN : 224x224
  2. HOG : 64x64
- **Normalisasi pixel (CNN)**  
- **Konversi grayscale (HOG)**
- **Feature Extraction**
- **Data Splitting (train-test split)**

---

## 5. 🤖 Modeling

Model yang digunakan dalam proyek ini:

- **Model 1 – Deep Learning:**  
  Convolutional Neural Network (CNN)

- **Model 2 – Machine Learning:**  
  1. Support Vector Machine ( SVM - RBF Kernel )
  2. Decision Tree
  3. Random Forest

- **Model 3 – Feature Engineering:**  
  HOG (Histogram of Oriented Gradients)

---

## 6. 🧪 Evaluation

### **Metrik Evaluasi**

- Accuracy
- Precision
- Recall
- F1-Score

### **Hasil Evaluasi**

Metrik yang digunakan: Accuracy
| Model         | Score (Accuracy) | 
| --------------| -----------------| 
| SVM (HOG)     | 66.67%           | 
| Random Forest | 59.90%           | 
| Decision Tree | 39.13%           |
| CNN           | 22.22%           |

---

## 7. 🏁 Kesimpulan

- **Model Terbaik:** SVM dengan Fitur HOG
- **Alasan:**  
  Dataset relatif kecil membuat model klasik lebih stabil dibanding CNN.
  CNN belum optimal karena membutuhkan dataset yang lebih besar untuk belajar fitur secara maksimal.

---

## 8. 🔮 Future Work

- Menambahkan jumlah dataset agar CNN lebih Optimal 
- Mengubah arsitektur CNN yang lebih dalam ( ResNet / MobileNet)
- Implementasi sistem real-time berbasis web atau mobile
- Optimasi hyperparameter seluruh model

---

## 9. 🔁 Reproducibility

Untuk mereproduksi proyek ini:

- Gunakan **Python 3.9+**
- Jalankan notebook `ML_Project.ipynb` secara berurutan

---

## 🛠️ Tools & Libraries

- Python
- scikit-image
- Scikit-learn
- Matplotlib & Seaborn
- TensorFlow / Keras

---

## 👩‍🎓 Author

**Nabila Carrissa Dewi**  
Program Studi: Teknologi Rekayasa Perangkat Lunak
Mata Kuliah: Pegolahan Citra
