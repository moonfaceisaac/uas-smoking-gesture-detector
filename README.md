

# Smoking Gesture Detection System

**Proyek UAS Pembelajaran Mesin**

## Deskripsi Proyek

Smoking Gesture Detection System adalah aplikasi berbasis web yang memanfaatkan **Deep Learning** untuk melakukan klasifikasi citra guna mendeteksi apakah seseorang sedang **merokok (Smoking)** atau **tidak merokok (NotSmoking)** berdasarkan gambar yang diunggah pengguna.

Proyek ini dikembangkan sebagai bagian dari **Ujian Akhir Semester (UAS)** mata kuliah Deep Learning, dengan fokus pada penerapan model CNN yang telah dilatih, dievaluasi, dan dideploy ke lingkungan nyata sehingga dapat digunakan secara langsung oleh pengguna.

---

## Tujuan Proyek

* Mengimplementasikan model Deep Learning berbasis CNN untuk klasifikasi citra
* Menerapkan model hasil training ke dalam aplikasi web yang dapat diakses publik
* Menunjukkan keterkaitan antara proses **training model, evaluasi, dan deployment**
* Menghasilkan artefak UAS yang berdampak nyata dan dapat digunakan secara praktis

---

## Fitur Aplikasi

* **Image Classification**
  Pengguna dapat mengunggah gambar dan sistem akan memprediksi apakah gambar tersebut mengandung perilaku merokok atau tidak.

* **Confidence Score**
  Setiap prediksi disertai dengan nilai confidence untuk menunjukkan tingkat keyakinan model.

* **Web-based Interface**
  Aplikasi dapat diakses melalui browser tanpa instalasi tambahan.

* **Cache-based Prediction History (UI-side)**
  Riwayat gambar dan hasil prediksi dapat ditampilkan selama sesi berjalan (tanpa login).

---

## Arsitektur Sistem

Aplikasi menggunakan arsitektur sederhana dengan fokus pada kemudahan deployment dan penggunaan.

* **Frontend & Backend**
  Menggunakan **Gradio** sebagai antarmuka web sekaligus handler input-output inferensi.

* **Model Deployment**
  Model dideploy menggunakan **Hugging Face Spaces**, sehingga dapat diakses secara online tanpa server mandiri.

* **Model**
  Model CNN berbasis **MobileNetV2** yang digunakan sebagai feature extractor dengan lapisan klasifikasi tambahan untuk klasifikasi biner.

---

## Model Deep Learning

* Arsitektur: **Convolutional Neural Network (CNN)**
* Backbone: **MobileNetV2 (pretrained ImageNet)**
* Tipe Klasifikasi: Biner (Smoking vs NotSmoking)
* Format Model: `.keras`

Model menggunakan pendekatan **transfer learning** dengan MobileNetV2 sebagai feature extractor untuk meningkatkan efisiensi dan performa.

---

## Dataset

* Dataset berupa kumpulan gambar dengan dua kelas:

  * Smoking
  * NotSmoking
* Dataset dibagi menjadi:

  * Training
  * Validation
  * Testing
* Preprocessing meliputi:

  * Resize gambar ke 224×224
  * Normalisasi menggunakan keras.rescaler dari [0,255] ke [-1,1]
  * Data augmentation (flip, rotation, zoom, dll.)

---

## Evaluasi Model

Evaluasi performa model dilakukan menggunakan:

* Accuracy
* Loss
* Confusion Matrix
* Precision, Recall, dan F1-score

Hasil evaluasi menunjukkan bahwa model mampu mendeteksi perilaku merokok dengan performa yang baik, terutama dalam hal sensitivitas terhadap kelas Smoking.

---

## Teknologi yang Digunakan

* **Python**
* **TensorFlow / Keras**
* **NumPy**
* **Google Colab**
* **Pillow (PIL)**
* **Gradio**
* **Hugging Face Spaces**

---


---

## Deployment

Aplikasi dideploy menggunakan **Hugging Face Spaces** dan dapat diakses secara publik.

**Link Deployment:**
*https://huggingface.co/spaces/moonfaceisaac/CNN-MODEL*

---

## Catatan

Proyek ini dikembangkan untuk keperluan akademik dan belum ditujukan sebagai sistem pengawasan resmi. Hasil prediksi model bergantung pada kualitas dan variasi data yang digunakan selama training.

---
