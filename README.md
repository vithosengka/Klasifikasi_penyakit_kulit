# 🧠 Skin Disease Image Classification

Proyek ini bertujuan untuk melakukan klasifikasi citra medis penyakit kulit menggunakan pendekatan *Deep Learning* berbasis **Convolutional Neural Network (CNN)** dengan arsitektur modern yang efisien.

---

## 📂 Dataset

Program ini menggunakan dataset citra medis yang terdiri dari **5 kelas penyakit kulit**, yaitu:

* Acne (Jerawat)
* Eczema (Eksim)
* Herpes
* Tinea Versicolor (Panu)
* Rosacea

Dataset dibagi menjadi:

* **Training set**: 80%
* **Validation set**: 20%

Struktur folder dataset disusun terpisah untuk setiap kelas guna memudahkan proses training dan evaluasi model.

---

## ⚙️ Metode & Teknologi

### Framework

* **TensorFlow**
* **Keras**

### Arsitektur Model

* **EfficientNetV2-B0**
  Arsitektur *state-of-the-art* yang dirancang untuk memberikan keseimbangan optimal antara efisiensi komputasi dan akurasi.

### Teknik Pembelajaran

* **Transfer Learning**
  Menggunakan bobot awal dari *ImageNet* agar model memiliki pemahaman awal terhadap fitur visual dasar.

* **Fine-Tuning**
  Base model dibekukan pada tahap awal training, kemudian sebagian layer akhir dilatih ulang untuk menyesuaikan dengan karakteristik penyakit kulit.

* **Data Augmentation**
  Menerapkan teknik augmentasi seperti rotasi, *horizontal flip*, dan penyesuaian kontras secara acak untuk mengurangi risiko *overfitting*.

---

## 🚀 Strategi Optimasi

Untuk menangani permasalahan **imbalanced dataset** dan meningkatkan performa pada kelas minoritas (misalnya *Rosacea*), diterapkan beberapa strategi berikut:

* **Class Weighting**
  Memberikan bobot lebih besar pada *loss function* untuk kelas minoritas agar model tidak bias terhadap kelas mayoritas.

* **Global Average Pooling & Dropout**
  Digunakan pada layer akhir untuk mengurangi kompleksitas model serta meningkatkan kemampuan generalisasi.

---

## 📊 Hasil Evaluasi

Model menunjukkan performa yang baik dengan **trade-off seimbang antara Precision dan Recall**. Pendekatan *Fine-Tuning* dan *Class Weighting* terbukti efektif dalam membantu model membedakan penyakit dengan kemiripan visual tinggi, seperti **Acne** dan **Rosacea**.

---

