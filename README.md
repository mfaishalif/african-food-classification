# Implementasi SVM pada Klasifikasi Makanan Afrika

**Tugas Ujian Akhir Semester (UAS) Pembelajaran Mesin**  
**Fakultas Sains dan Teknologi, Universitas Airlangga (2025)**

---

## 📌 Tentang Proyek
Proyek ini adalah implementasi algoritma **Support Vector Machine (SVM)** yang merujuk pada naskah ilmiah berjudul:

> **["An Explorative Analysis of SVM Classifier and ResNet50 Architecture on African Food Classification"](https://arxiv.org/pdf/2505.13923)**  
> _oleh: Chinedu Mbonu, Kenechukwu Anigbogu, Doris Asogwa, Tochukwu Belonwu_

Dalam implementasi ini, kami mengeksplorasi penggunaan SVM dengan berbagai kernel untuk mengklasifikasikan citra makanan Afrika dan membandingkan kinerjanya dengan hasil dari arsitektur ResNet50 yang dibahas dalam naskah ilmiah tersebut.

## 👥 Anggota Tim (Kelompok 16)
*   **Muhammad Faishal Islahudin Fikri** (187231108)
*   **Datok Radja Mulya** (187231110)

---

## 📂 Dataset
Sumber data yang digunakan adalah **African Food Dataset** yang tersedia di Mendeley Data, terdiri dari total **1.754 gambar**. Dataset ini mencakup 6 kategori makanan populer dari Ghana dan Kamerun:

1.  **Ekwang**
2.  **Eru**
3.  **Jollof Rice (Ghana)**
4.  **Ndole**
5.  **Palm Nut Soup**
6.  **Waakye**

Struktur dataset dibagi menjadi `train`, `val`, dan `test`.

---

## ⚙️ Metodologi

### 1. Pra-pemrosesan Data (SVM)
*   **Resize**: Citra diubah ukurannya menjadi **100x100 piksel**.
*   **Flatten**: Citra diratakan menjadi vektor fitur 1 dimensi (30.000 fitur dari RGB).
*   **Normalisasi**: Nilai piksel diskalakan ke rentang [0, 1].

### 2. Model & Evaluasi
Model SVM dilatih menggunakan library `scikit-learn` dengan berbagai konfigurasi kernel untuk menemukan performa terbaik:
*   **Linear**
*   **RBF (Radial Basis Function)**
*   **Polynomial (Poly)**
*   **Sigmoid**

Evaluasi dilakukan menggunakan metrik **Akurasi, Presisi, Recall,** dan **F1-Score**, serta visualisasi **Confusion Matrix**.

---

## 📊 Hasil Analisis

Berdasarkan percobaan mandiri yang dilakukan:

1.  **Kernel Terbaik**: Kernel **RBF** menunjukkan performa paling optimal dan seimbang.
2.  **Akurasi**:
    *   SVM (RBF) mencapai akurasi sekitar **83.67%**.
    *   ResNet50 (Fine-tuned) mencapai akurasi sekitar **81%** (berdasarkan naskah ilmiah referensi).
3.  **Kesimpulan**: Meskipun ResNet50 unggul dalam mengekstraksi fitur visual kompleks, SVM terbukti kompetitif dan bahkan lebih konsisten pada dataset yang relatif kecil dan tidak seimbang ini, terutama untuk kelas-kelas tertentu seperti Ekwang.

---

## 🔗 Referensi & Tautan Penting
*   **Artikel Ilmiah Utama**: [Arxiv Link](https://arxiv.org/pdf/2505.13923)
*   **Dataset**: [Mendeley Data / Google Drive](https://drive.google.com/drive/folders/1XiYHBExwOtgfgRa7qCxVs_UzbPe3ssof?usp=sharing)
*   **Kode Percobaan (Google Colab)**: [Link Notebook](https://colab.research.google.com/drive/162gOnC5EeB1KIjm0be1WlDQUe5flfiL1?usp=sharing)