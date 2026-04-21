🗑️ Garbage Classification System (CNN vs Machine Learning)
📌 Deskripsi
Proyek ini merupakan implementasi sistem klasifikasi sampah berbasis citra dengan membandingkan dua pendekatan utama:

Deep Learning (CNN)

Machine Learning klasik (SVM, Decision Tree, Random Forest)

Penelitian ini bertujuan untuk menganalisis model mana yang paling optimal pada kondisi dataset terbatas, serta mengevaluasi efektivitas fitur Histogram of Oriented Gradients (HOG) dibandingkan dengan fitur otomatis yang dipelajari oleh CNN.

🎯 Tujuan
Membangun sistem klasifikasi sampah otomatis berbasis citra

Membandingkan performa CNN dengan SVM, Decision Tree, dan Random Forest

Menganalisis efektivitas fitur HOG pada dataset terbatas

Mendukung implementasi teknologi cerdas untuk pengelolaan sampah (SDG 12)

📊 Dataset
Dataset yang digunakan berasal dari Kaggle:

Garbage Classification Dataset

Terdiri dari 6–7 kategori sampah (plastic, paper, metal, glass, cardboard, dll.)

🛠️ Teknologi yang Digunakan
Python 3.10

TensorFlow & Keras (CNN)

Scikit-learn (SVM, Decision Tree, Random Forest)

OpenCV (image processing)

Scikit-image (HOG feature extraction)

Matplotlib (visualisasi)

Google Colab (eksperimen)

🔄 Pipeline Sistem
1. Preprocessing
Resize gambar:

CNN: 224×224

HOG: 64×64

Normalisasi (CNN)

Grayscale (HOG)

2. Feature Extraction
CNN → fitur otomatis (deep features)

ML → HOG (handcrafted features)

3. Data Splitting
Training set

Testing set

4. Model Training
CNN

SVM (RBF Kernel)

Decision Tree

Random Forest

5. Evaluasi
Accuracy

Precision

Recall

F1-score

Confusion Matrix

6. Prediksi
Upload gambar

Output prediksi dari semua model

Voting mayoritas sebagai hasil akhir

⚙️ Konfigurasi Model
🔹 SVM
Kernel: RBF

C = 10

gamma = scale

🔹 Random Forest
n_estimators = 150

🔹 Decision Tree
criterion = Gini

max_depth = None

🔹 CNN
4 Convolution Block (32, 64, 128, 256)

BatchNormalization + ReLU + MaxPooling

Global Average Pooling

Dense 256 + Dropout 0.5

Output: Softmax

Optimizer: Adam (lr = 0.0001)

📈 Hasil Perbandingan Model
Model	Akurasi
SVM (RBF)	95.4%
Random Forest	93.1%
Decision Tree	88.6%
CNN	79.3%

💡 Insight Utama
SVM memberikan performa terbaik pada dataset terbatas

CNN belum optimal karena membutuhkan data lebih besar

Kombinasi HOG + SVM sangat efektif untuk klasifikasi citra sederhana

🚀 Fitur Aplikasi
Upload gambar sampah

Prediksi dari 4 model sekaligus

Confidence score tiap model

Visualisasi hasil (bar chart & confusion matrix)

Voting mayoritas (final decision)

▶️ Cara Menjalankan
1. Clone Repository
Bash

git clone https://github.com/username/garbage-classification.git
cd garbage-classification
2. Install Dependencies
Bash

pip install -r requirements.txt
3. Jalankan Program
Bash

python main.py
Atau gunakan Google Colab untuk menjalankan notebook.

📁 Struktur Folder

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

├── README.md

🧾 Kesimpulan
Model SVM dengan fitur HOG terbukti memberikan performa terbaik pada kondisi dataset terbatas, mengungguli CNN yang membutuhkan dataset lebih besar untuk mencapai performa optimal.

🙏 Acknowledgment
Penelitian ini tidak terlepas dari dukungan dosen pembimbing, institusi, serta penyedia dataset publik yang digunakan dalam eksperimen ini.

📄 Lisensi
Proyek ini bersifat akademik dan digunakan untuk keperluan penelitian.

👩‍💻 Author
Nabila Carrissa Dewi
TRPL 6A
