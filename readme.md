# ❤️ Prediksi Penyakit Jantung Menggunakan Decision Tree & KNN

<p align="center">
  <img src="https://img.shields.io/badge/Status-Selesai-brightgreen?style=for-the-badge" alt="Status Selesai"/>
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python" alt="Python 3.10"/>
  <img src="https://img.shields.io/badge/Scikit--Learn-1.3.0-orange?style=for-the-badge&logo=scikit-learn" alt="Scikit-Learn"/>
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License MIT"/>
  <img src="https://img.shields.io/badge/Accuracy-85.25%25-success?style=for-the-badge" alt="Accuracy 85.25%"/>
</p>

---

## 📋 Deskripsi Proyek

Proyek ini bertujuan untuk mengembangkan sistem prediksi risiko penyakit jantung berbasis *machine learning* menggunakan dataset **Cleveland Heart Disease**. Dua algoritma klasifikasi diterapkan dan dibandingkan:

- **Decision Tree** — interpretatif dan mudah divisualisasikan.
- **K-Nearest Neighbor (KNN)** — sederhana dan efektif untuk data non-linear.

Hasil evaluasi menunjukkan bahwa **KNN dengan k=11** mencapai akurasi terbaik sebesar **85.25%**.

---

## 📁 Struktur Folder

```
UAS-KecerdasanBuatan/
├── README.md                 ← Deskripsi proyek & panduan
├── Laporan_uas.md            ← Laporan lengkap UAS
├── uas_model.ipynb           ← Notebook implementasi
├── data/
│   ├── heart_disease.csv     ← Dataset asli
│   └── Jurnal/               ← 5 referensi jurnal (PDF)
├── dist/                     ← Gambar hasil plotting (opsional)
│   ├── distribusi_target.png
│   ├── distribusi_usia.png
│   ├── heatmap_korelasi.png
│   ├── confusion_matrix.png
│   └── decision_tree_visualization.png
└── .gitignore
```

---

## 📊 Dataset

- **Sumber**: Kaggle – [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)
- **Jumlah Sampel**: 303
- **Fitur**: 13 fitur klinis + 1 target
- **Target**: Biner (0 = Tidak Sakit, 1 = Sakit)

Fitur utama yang digunakan:
`age`, `sex`, `cp`, `trestbps`, `chol`, `fbs`, `restecg`, `thalach`, `exang`, `oldpeak`, `slope`, `ca`, `thal`

---

## 🧠 Metode & Algoritma

| Algoritma | Kelebihan | Kekurangan |
|-----------|-----------|------------|
| **Decision Tree** | Interpretabilitas tinggi, mudah divisualisasikan | Rentan overfitting |
| **KNN** | Sederhana, menangkap pola non-linear | Sensitif terhadap skala data, lambat pada data besar |

---

## 🚀 Cara Menjalankan

### 1. Clone Repository
```bash
git clone https://github.com/username/UAS-KecerdasanBuatan.git
cd UAS-KecerdasanBuatan
```

### 2. Instal Dependensi
```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

### 3. Jalankan Notebook
- Buka **Google Colab** atau **Jupyter Notebook**.
- Upload file `uas_model.ipynb`.
- Upload dataset `heart_disease.csv` ke environment.
- Jalankan semua *cell* secara berurutan.


---

## 👥 Tim Penyusun

| Nama | NIM | Peran |
|------|-----|-------|
| Moch Azriel Naufan H | 2406046 | Data Preparation & Modeling |
| Muhamad Thor!q Mustaqim | 2406045 | Evaluation & Analisis Hasil |

## 📈 Hasil Evaluasi

| Model | Akurasi | Precision (Sakit) | Recall (Sakit) | F1-Score (Sakit) |
|-------|---------|-------------------|----------------|------------------|
| Decision Tree | **80.33%** | 0.6087 | 0.8235 | 0.7000 |
| KNN (k=11) | **85.25%** | 0.7500 | 0.7059 | 0.7273 |

**Kesimpulan:** Model KNN dengan k=11 memberikan performa terbaik secara keseluruhan, dengan akurasi 85.25% dan precision yang lebih baik.

---

## 📚 Referensi Jurnal

1. Kohsasih, K. L., et al. (2025). *IT Journal Research and Development*. [DOI](https://doi.org/10.25299/itjrd.2025.24703)
2. Muttakin, M., et al. (2025). *Journal of System & Technology (SYSTEC)*. [Link](https://systec.ejournal.unri.ac.id/index.php/systec/article/view/18)
3. Coronary heart disease prediction (2024). *Journal of Advances in Information Technology*. [DOI](https://doi.org/10.12720/jait.15.1.27-32)
4. Balhaf, K., et al. (2025). *IEEE Xplore*. [DOI](https://doi.org/10.1109/ACDSA65407.2025.11166082)
5. Regen, R., & Setiawan, H. (2024). *Journal of Electrical Technology UMY*. [Link](https://journal.umy.ac.id/index.php/jet/article/view/25208)



---

## 📝 Catatan Penting

- Proyek ini dikembangkan sebagai tugas **Ujian Akhir Semester** mata kuliah **Kecerdasan Buatan**.
- Model ini **bukan** pengganti diagnosis medis profesional, hanya sebagai alat bantu skrining awal.
- Dataset yang digunakan merupakan dataset publik, sehingga dapat diakses dan direproduksi oleh siapa saja.

---

## 📄 Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).

---

<div align="center">
  <sub>Dibuat dengan ❤️ oleh Tim Kecerdasan Buatan - Institut Teknologi Garut</sub>
</div>
