Garbage Classification System (CNN vs Machine Learning)

Deskripsi
Proyek ini merupakan implementasi sistem klasifikasi sampah berbasis citra dengan membandingkan performa Deep Learning (CNN) dan Machine Learning klasik (SVM, Decision Tree, Random Forest).

Penelitian ini bertujuan untuk menganalisis model mana yang paling optimal dalam kondisi dataset terbatas, serta mengevaluasi efektivitas fitur Histogram of Oriented Gradients (HOG) dibandingkan pembelajaran fitur otomatis oleh CNN.

Tujuan
Membangun sistem klasifikasi sampah otomatis berbasis citra

Membandingkan performa CNN dengan SVM, Decision Tree, dan Random Forest

Menganalisis efektivitas fitur HOG pada dataset terbatas

Mendukung implementasi sistem cerdas untuk pengelolaan sampah (SDG 12)

Dataset
Dataset yang digunakan berasal dari Kaggle:
Garbage Classification Dataset (6–7 kategori sampah seperti plastic, paper, metal, dll.)

Teknologi yang Digunakan
Python 3.10

TensorFlow & Keras (CNN)

Scikit-learn (SVM, Decision Tree, Random Forest)

OpenCV (image processing)

Scikit-image (HOG feature extraction)

Matplotlib (visualisasi)

Google Colab (eksperimen)

Pipeline Sistem
Preprocessing

Resize gambar (224×224 untuk CNN, 64×64 untuk HOG)

Normalisasi (CNN)

Grayscale (HOG)

Feature Extraction

CNN → otomatis (deep features)

ML → HOG (handcrafted features)

Split Data

Training dan testing

Model Training

CNN

SVM (RBF Kernel)

Decision Tree

Random Forest

Evaluasi

Accuracy, Precision, Recall, F1-score

Confusion Matrix

Prediksi

Upload gambar

Output dari semua model + voting mayoritas

Konfigurasi Model
🔹 SVM
Kernel: RBF

C = 10

gamma = scale

🔹 Random Forest
n_estimators = 150

🔹 Decision Tree
Criterion: Gini

Tanpa max depth

🔹 CNN
4 Conv Block (32, 64, 128, 256)

BatchNorm + ReLU + MaxPooling

Global Average Pooling

Dense 256 + Dropout 0.5

Output: Softmax

Optimizer: Adam (lr = 0.0001)

Hasil Perbandingan Model
Model Akurasi
SVM (RBF) 66.66%
Random Forest 59.90%
Decision Tree 39.13%
CNN 22.22%

Insight utama:

SVM memberikan performa terbaik pada dataset terbatas

CNN underperform karena data tidak cukup besar

HOG + SVM sangat efektif untuk klasifikasi citra sederhana

Fitur Aplikasi
Upload gambar sampah

Prediksi dari 4 model sekaligus

Confidence score tiap model

Visualisasi hasil (bar chart & voting)

Prediksi mayoritas (final decision)

Cara Menjalankan

1. Clone Repository
   Bash

git clone https://github.com/username/garbage-classification.git
cd garbage-classification 2. Install Dependencies
Bash

pip install -r requirements.txt 3. Jalankan Program
Bash

python main.py
Atau gunakan Google Colab untuk menjalankan notebook.

Struktur Folder
├── dataset/
├── output_model/
│   ├── model_cnn.h5
│   ├── model_svm.pkl
│   ├── model_rf.pkl
│   ├── model_dt.pkl
│   ├── scaler.pkl
│   └── label_encoder.pkl
├── notebooks/
├── src/
└── README.md
Kesimpulan
Model SVM dengan fitur HOG terbukti memberikan performa terbaik dalam kondisi dataset terbatas, mengungguli CNN yang memerlukan data lebih besar untuk optimal.

Acknowledgment
Penelitian ini tidak terlepas dari dukungan dosen pembimbing, institusi, serta penyedia dataset publik yang digunakan dalam eksperimen.

Lisensi
Proyek ini bersifat akademik dan digunakan untuk keperluan penelitian.

Author
Nabila Carrissa Dewi
TRPL 6A
