<style>
  body {
    font-family: 'Georgia', 'Times New Roman', serif;
    line-height: 1.5;
    color: #232323;
    background-color: #fdfdfb;
    max-width: 880px;
    margin: 0 auto;
    padding: 40px 30px;
  }

  h1, h2, h3, h4 {
    font-family: 'Helvetica Neue', Arial, sans-serif;
    color: #12233d;
    letter-spacing: 0.2px;
    animation: fadeSlideIn 0.6s ease-in-out;
  }

  h1 {
    border-bottom: 3px solid #c99a3c;
    padding-bottom: 10px;
    margin-top: 55px;
  }

  h2 {
    border-left: 5px solid #c99a3c;
    padding-left: 12px;
    margin-top: 40px;
  }

  h3 {
    color: #1d3a5f;
    margin-top: 28px;
  }

  @keyframes fadeSlideIn {
    from { opacity: 0; transform: translateY(-8px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  table {
    width: 100%;
    border-collapse: collapse;
    margin: 22px 0;
    font-family: 'Helvetica Neue', Arial, sans-serif;
    font-size: 0.95em;
    box-shadow: 0 2px 10px rgba(0,0,0,0.06);
    animation: fadeIn 0.8s ease-in;
  }

  @keyframes fadeIn {
    from { opacity: 0; }
    to   { opacity: 1; }
  }

  thead tr {
    background: linear-gradient(90deg, #12233d, #1d3a5f);
    color: #ffffff;
  }

  th, td {
    padding: 10px 14px;
    border: 1px solid #e0e0e0;
    text-align: left;
  }

  tbody tr:nth-child(even) {
    background-color: #f5f6f8;
  }

  tbody tr {
    transition: background-color 0.25s ease, transform 0.2s ease;
  }

  tbody tr:hover {
    background-color: #fbf1d9;
    transform: scale(1.01);
  }

  blockquote {
    border-left: 4px solid #c99a3c;
    background: #f9f6ee;
    padding: 12px 18px;
    margin: 20px 0;
    font-style: italic;
    color: #444;
  }

  code {
    background: #eef1f5;
    padding: 2px 6px;
    border-radius: 4px;
    font-size: 0.9em;
    color: #a3332e;
  }

  pre {
    background: #12233d;
    color: #eaeaea;
    padding: 16px;
    border-radius: 8px;
    overflow-x: auto;
    box-shadow: 0 2px 10px rgba(0,0,0,0.15);
  }

  pre code {
    background: none;
    color: #eaeaea;
    padding: 0;
  }

  hr {
    border: none;
    border-top: 1px solid #d8d8d8;
    margin: 45px 0;
  }

  .cover {
    text-align: center;
    padding: 60px 20px;
    animation: fadeIn 1.2s ease-in;
  }

  .cover img {
    width: 130px;
    margin-bottom: 25px;
    filter: drop-shadow(0 3px 6px rgba(0,0,0,0.2));
  }

  .cover h1 {
    border: none;
    font-size: 1.5em;
    color: #12233d;
    margin: 5px 0;
  }

  .cover h2 {
    border: none;
    padding: 0;
    font-size: 1.9em;
    color: #c99a3c;
    margin: 10px 0 25px 0;
  }

  .badge {
    display: inline-block;
    background: #12233d;
    color: #fff;
    padding: 4px 12px;
    border-radius: 20px;
    font-size: 0.8em;
    margin: 4px;
    font-family: 'Helvetica Neue', Arial, sans-serif;
  }

  .badge.gold {
    background: #c99a3c;
  }

  .highlight-box {
    background: #f1f6fb;
    border: 1px solid #cfe0ef;
    border-left: 5px solid #1d3a5f;
    padding: 16px 20px;
    border-radius: 6px;
    margin: 20px 0;
  }

  .result-box {
    background: #f6f9f0;
    border-left: 5px solid #5a8a3a;
    padding: 14px 20px;
    border-radius: 6px;
    margin: 20px 0;
  }

  figure {
    text-align: center;
    margin: 25px 0;
  }

  figcaption {
    font-size: 0.85em;
    color: #666;
    margin-top: 6px;
    font-style: italic;
  }

  .signature {
    text-align: center;
    margin-top: 50px;
    animation: fadeIn 1s ease-in;
  }
</style>

<div class="cover">

![Logo ITG](https://itg.ac.id/asset/img/logo-itg.png)

<h1>LAPORAN UJIAN AKHIR SEMESTER</h1>
<h1>MATA KULIAH KECERDASAN BUATAN</h1>

<h2>Prediksi Penyakit Jantung Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor (KNN)</h2>

<p><em>Studi Komparatif Model Klasifikasi pada Dataset Cleveland Heart Disease</em></p>

<br>

<span class="badge">Teknik Informatika</span>
<span class="badge gold">Machine Learning</span>
<span class="badge">Klasifikasi Medis</span>

<br><br>

**Disusun oleh:**

Moch Azriel Naufan H — 2406046
Muhamad Thoriq Mustaqim — 2406045

**Dosen Pengampu:**
[Nama Dosen Pengampu]

<br>

**PROGRAM STUDI TEKNIK INFORMATIKA**
**INSTITUT TEKNOLOGI GARUT**
**2026**

</div>

---

## Daftar Isi

1. [Judul Proyek](#1-judul-proyek)
2. [Business Understanding](#2-business-understanding)
3. [Data Understanding](#3-data-understanding)
4. [Exploratory Data Analysis (EDA)](#4-exploratory-data-analysis-eda)
5. [Data Preparation](#5-data-preparation)
6. [Modeling](#6-modeling)
7. [Evaluation](#7-evaluation)
8. [Kesimpulan dan Rekomendasi](#8-kesimpulan-dan-rekomendasi)
9. [Referensi](#9-referensi)
10. [Lampiran](#10-lampiran)

---

# 1. Judul Proyek

### Prediksi Penyakit Jantung Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor (KNN)

**Kelompok Penyusun**

| Nama | NIM | Peran |
|---|---|---|
| Moch Azriel Naufan H | 2406046 | Data Preparation & Modeling |
| Muhamad Thoriq Mustaqim | 2406045 | Evaluation & Analisis Hasil |

### Latar Belakang

Penyakit kardiovaskular masih menjadi salah satu penyebab kematian tertinggi di dunia hingga saat ini. Berdasarkan data yang dipublikasikan oleh *World Health Organization* (WHO, 2021), tercatat sekitar 17,9 juta jiwa meninggal setiap tahunnya akibat gangguan pada jantung dan pembuluh darah. Angka ini menempatkan penyakit jantung sebagai kontributor utama beban kesehatan global, jauh melampaui penyebab kematian lain seperti kecelakaan atau penyakit menular.

Salah satu tantangan utama dalam penanganan penyakit jantung adalah keterlambatan diagnosis. Gejala awal penyakit ini kerap kali tidak spesifik, sehingga banyak pasien baru menyadari kondisinya setelah memasuki stadium lanjut atau bahkan setelah mengalami serangan jantung akut. Di sisi lain, proses diagnosis konvensional membutuhkan pemeriksaan klinis yang kompleks, alat medis khusus, serta tenaga ahli kardiologi yang tidak selalu tersedia secara merata, terutama di daerah dengan akses layanan kesehatan terbatas.

Perkembangan pesat dalam bidang *machine learning* membuka peluang baru untuk mengatasi tantangan tersebut. Dengan memanfaatkan data rekam medis yang relatif sederhana — seperti usia, tekanan darah, kadar kolesterol, dan hasil elektrokardiogram — algoritma pembelajaran mesin dapat dilatih untuk mengenali pola yang mengindikasikan risiko penyakit jantung. Studi yang dilakukan oleh Bhatt et al. (2023) menunjukkan bahwa algoritma seperti Decision Tree dan K-Nearest Neighbor (KNN) mampu memberikan hasil klasifikasi yang cukup andal dalam konteks data medis, dengan tingkat akurasi yang kompetitif dibandingkan metode statistik konvensional.

Berangkat dari latar belakang tersebut, proyek ini disusun untuk mengeksplorasi dan membandingkan kinerja dua algoritma klasifikasi — Decision Tree dan KNN — dalam memprediksi keberadaan penyakit jantung pada seorang pasien berdasarkan atribut-atribut klinis yang tersedia pada dataset Cleveland Heart Disease.

---

# 2. Business Understanding

## 2.1 Permasalahan Dunia Nyata dan Tinjauan Literatur

Permasalahan inti yang melatarbelakangi proyek ini adalah tingginya angka keterlambatan diagnosis penyakit jantung akibat gejala yang samar serta keterbatasan akses terhadap tenaga medis spesialis. Kondisi ini diperparah oleh biaya pemeriksaan jantung secara menyeluruh — seperti ekokardiografi atau angiografi — yang relatif mahal dan tidak terjangkau bagi sebagian besar masyarakat, khususnya di negara berkembang. Akibatnya, dibutuhkan suatu pendekatan alternatif yang mampu memberikan estimasi risiko awal secara cepat, murah, dan cukup akurat, hanya berdasarkan data klinis dasar yang umum diperiksa pada kunjungan medis rutin.

Untuk menjawab kebutuhan tersebut, sejumlah penelitian terdahulu telah mengeksplorasi penerapan algoritma *machine learning* pada domain ini. Beberapa temuan yang relevan dirangkum dalam tabel berikut.

| Peneliti | Metode | Hasil Utama |
|---|---|---|
| Bhatt et al. (2023) | Decision Tree | Akurasi mencapai 89% dalam memprediksi penyakit jantung |
| Ahmed et al. (2022) | SVM, KNN, Logistic Regression | KNN unggul dengan akurasi tertinggi sebesar 87% |
| Latha & Jeeva (2019) | Ensemble Learning | Kombinasi beberapa algoritma meningkatkan akurasi hingga 92% |

Dari ketiga studi tersebut terlihat pola yang konsisten: algoritma berbasis pohon keputusan dan algoritma berbasis kedekatan jarak (*distance-based*) sama-sama menunjukkan performa yang menjanjikan dalam klasifikasi penyakit jantung, meskipun karakteristik keduanya cukup berbeda. Decision Tree unggul dari sisi interpretabilitas karena hasil klasifikasinya dapat divisualisasikan sebagai serangkaian aturan keputusan yang mudah dipahami, bahkan oleh pihak non-teknis seperti tenaga medis. Sementara itu, KNN unggul dalam menangkap pola non-linear antar fitur tanpa memerlukan asumsi distribusi data tertentu, meskipun performanya sangat bergantung pada pemilihan nilai *k* dan skala data.

Berdasarkan pertimbangan tersebut, proyek ini memilih untuk menggunakan **Decision Tree** dan **K-Nearest Neighbor (KNN)** sebagai dua algoritma utama yang akan dibandingkan, dengan harapan dapat memperoleh gambaran menyeluruh mengenai kelebihan masing-masing pendekatan pada dataset yang digunakan.

## 2.2 Tujuan Proyek

Proyek ini disusun dengan tiga tujuan utama, yaitu:

1. Mengembangkan model *machine learning* yang mampu memprediksi risiko penyakit jantung pada pasien berdasarkan data klinis yang tersedia.
2. Membandingkan performa algoritma Decision Tree dan KNN secara objektif menggunakan metrik evaluasi standar.
3. Mengidentifikasi model yang paling optimal untuk diterapkan sebagai alat bantu diagnosis awal, dengan mempertimbangkan keseimbangan antara akurasi, precision, dan recall.

## 2.3 Pengguna Sistem

<div class="highlight-box">

Sistem prediksi yang dikembangkan dalam proyek ini dirancang untuk dimanfaatkan oleh beberapa pihak berikut:

- **Dokter dan tenaga medis** — sebagai alat bantu pengambilan keputusan pada tahap skrining awal, bukan sebagai pengganti diagnosis klinis formal.
- **Pasien** — sebagai sarana edukasi untuk memahami tingkat risiko kesehatan jantung mereka secara mandiri.
- **Peneliti dan akademisi** — sebagai dasar atau pembanding untuk pengembangan sistem prediksi yang lebih kompleks di masa mendatang.

</div>

## 2.4 Solusi dan Manfaat Implementasi AI

Solusi yang diusulkan berupa sistem klasifikasi berbasis *machine learning* yang menerima masukan berupa data klinis pasien — seperti usia, jenis kelamin, tekanan darah, kadar kolesterol, dan hasil pemeriksaan elektrokardiogram — kemudian menghasilkan keluaran berupa estimasi risiko penyakit jantung dalam bentuk klasifikasi biner (berisiko atau tidak berisiko).

Penerapan pendekatan ini memberikan sejumlah manfaat nyata, antara lain mempercepat proses skrining awal tanpa memerlukan pemeriksaan penunjang yang mahal, membantu tenaga medis dalam memprioritaskan pasien yang memerlukan pemeriksaan lebih lanjut, serta membuka peluang deteksi dini yang pada akhirnya dapat menurunkan risiko komplikasi serius akibat keterlambatan penanganan.

---

# 3. Data Understanding

## 3.1 Sumber Data

Dataset yang digunakan dalam proyek ini, `heart_disease.csv`, diperoleh dari platform **Kaggle** dan merupakan turunan dari **Cleveland Heart Disease Dataset**, salah satu dataset paling banyak digunakan dalam penelitian klasifikasi penyakit jantung berbasis *machine learning*. Popularitas dataset ini tidak lepas dari kualitas datanya yang telah melalui proses kurasi klinis, sehingga menjadikannya rujukan standar (*benchmark*) dalam berbagai studi komparatif algoritma.

## 3.2 Deskripsi Fitur

Dataset terdiri atas tiga belas fitur prediktor dan satu variabel target. Rincian masing-masing fitur disajikan pada tabel berikut.

| No | Fitur | Deskripsi | Tipe Data |
|---|---|---|---|
| 1 | age | Usia pasien dalam tahun | Numerik |
| 2 | sex | Jenis kelamin (0 = Wanita, 1 = Pria) | Kategorik |
| 3 | cp | Tipe nyeri dada (0–3: typical angina, atypical angina, non-anginal pain, asymptomatic) | Kategorik |
| 4 | trestbps | Tekanan darah istirahat (mm Hg) | Numerik |
| 5 | chol | Kadar kolesterol serum (mg/dl) | Numerik |
| 6 | fbs | Gula darah puasa > 120 mg/dl (0 = Tidak, 1 = Ya) | Kategorik |
| 7 | restecg | Hasil EKG istirahat (0 = normal, 1 = abnormal ST-T, 2 = hipertrofi ventrikel kiri) | Kategorik |
| 8 | thalach | Detak jantung maksimum yang dicapai | Numerik |
| 9 | exang | Angina akibat aktivitas fisik (0 = Tidak, 1 = Ya) | Kategorik |
| 10 | oldpeak | Depresi segmen ST akibat olahraga relatif terhadap istirahat | Numerik |
| 11 | slope | Kemiringan segmen ST puncak saat berolahraga (0 = naik, 1 = datar, 2 = turun) | Kategorik |
| 12 | ca | Jumlah pembuluh darah utama yang tervisualisasi melalui fluoroskopi (0–3) | Numerik |
| 13 | thal | Kondisi thalassemia (0 = normal, 1 = fixed defect, 2 = reversible defect) | Kategorik |
| 14 | target | Diagnosis penyakit jantung (0 = tidak sakit, 1 = sakit) | Target |

Keberagaman jenis fitur — mulai dari data numerik kontinu hingga data kategorik ordinal — menjadikan dataset ini cukup representatif untuk menguji kemampuan generalisasi kedua algoritma yang dipilih, sekaligus menuntut proses *data preparation* yang cermat sebelum tahap pemodelan dilakukan.

## 3.3 Ukuran dan Format Data

| Karakteristik | Nilai |
|---|---|
| Jumlah sampel | 303 baris |
| Jumlah fitur prediktor | 13 fitur |
| Jumlah variabel target | 1 (biner) |
| Format berkas | CSV (Comma Separated Values) |

## 3.4 Tipe Data dan Target Klasifikasi

Secara umum, fitur pada dataset ini dapat dikelompokkan menjadi dua kategori besar. Kelompok pertama adalah fitur numerik kontinu, yang meliputi `age`, `trestbps`, `chol`, `thalach`, `oldpeak`, dan `ca`. Kelompok kedua adalah fitur kategorik, yang meliputi `sex`, `cp`, `fbs`, `restecg`, `exang`, `slope`, dan `thal`, di mana sebagian di antaranya memerlukan proses *encoding* sebelum dapat digunakan oleh algoritma pembelajaran mesin.

Variabel target bersifat biner, dengan nilai 0 merepresentasikan pasien yang tidak terindikasi penyakit jantung dan nilai 1 merepresentasikan pasien yang terindikasi menderita penyakit jantung. Sifat biner ini menjadikan permasalahan pada proyek ini tergolong sebagai kasus klasifikasi dua kelas (*binary classification*).

---

# 4. Exploratory Data Analysis (EDA)

Tahap eksplorasi data dilakukan untuk memahami karakteristik, sebaran, serta pola hubungan antar variabel sebelum masuk ke tahap pemodelan. Proses ini penting untuk memastikan bahwa keputusan-keputusan teknis pada tahap selanjutnya — seperti pemilihan fitur atau penanganan ketidakseimbangan kelas — didasarkan pada pemahaman data yang memadai.

## 4.1 Visualisasi Distribusi Data

### 4.1.1 Distribusi Target

<figure>

![Distribusi Target](distribusi_target.png)

<figcaption>Gambar 4.1 — Distribusi kelas target pada dataset</figcaption>
</figure>

Visualisasi distribusi target menunjukkan bahwa dari total 303 sampel, sebanyak 220 sampel (72,6%) tergolong sebagai pasien tidak sakit, sedangkan 83 sampel (27,4%) tergolong sebagai pasien sakit. Meskipun data masih tergolong seimbang secara relatif, ketimpangan proporsi ini tetap perlu diperhatikan agar model tidak bias terhadap kelas mayoritas.

### 4.1.2 Distribusi Usia

<figure>

![Distribusi Usia](distribusi_usia.png)

<figcaption>Gambar 4.2 — Sebaran usia pasien berdasarkan status diagnosis</figcaption>
</figure>

Pola distribusi usia menunjukkan bahwa pasien dengan diagnosis positif penyakit jantung cenderung berada pada rentang usia yang lebih tua, dengan rata-rata usia berkisar antara 55 hingga 60 tahun. Temuan ini konsisten dengan pemahaman medis umum bahwa risiko penyakit kardiovaskular meningkat seiring bertambahnya usia.

### 4.1.3 Distribusi Jenis Kelamin

<figure>

![Distribusi Sex](distribusi_sex.png)

<figcaption>Gambar 4.3 — Proporsi jenis kelamin pasien dalam dataset</figcaption>
</figure>

Dari sisi jenis kelamin, mayoritas pasien dalam dataset adalah pria, dengan proporsi mencapai sekitar 68% dari keseluruhan sampel. Ketimpangan proporsi ini perlu dicatat sebagai salah satu keterbatasan dataset, karena dapat memengaruhi generalisasi model terhadap populasi pasien wanita.

## 4.2 Analisis Korelasi Antar Fitur

<figure>

![Heatmap Korelasi](heatmap_korelasi.png)

<figcaption>Gambar 4.4 — Peta korelasi antar fitur numerik dan target</figcaption>
</figure>

Analisis korelasi menunjukkan bahwa fitur `ca` dan `oldpeak` memiliki korelasi positif tertinggi terhadap target, masing-masing sebesar 0,48. Fitur `cp`, `exang`, dan `slope` juga menunjukkan korelasi positif yang cukup kuat, dengan nilai masing-masing sebesar 0,38, 0,36, dan 0,36. Di sisi lain, fitur `thalach` justru menunjukkan korelasi negatif sebesar -0,39, yang mengindikasikan bahwa semakin rendah detak jantung maksimum yang dicapai pasien saat beraktivitas, semakin tinggi kemungkinan pasien tersebut mengidap penyakit jantung.

| Fitur | Korelasi terhadap Target | Arah Hubungan |
|---|---|---|
| ca | 0.48 | Positif |
| oldpeak | 0.48 | Positif |
| cp | 0.38 | Positif |
| exang | 0.36 | Positif |
| slope | 0.36 | Positif |
| thalach | -0.39 | Negatif |

## 4.3 Deteksi Ketidakseimbangan Data

Hasil pemeriksaan proporsi kelas menunjukkan rasio ketidakseimbangan sebesar 0,452 antara kelas minoritas dan mayoritas. Meskipun tidak tergolong ekstrem, kondisi ini tetap menjadi catatan penting agar model yang dibangun tidak cenderung memihak kelas mayoritas (pasien tidak sakit), yang pada konteks medis justru berisiko menyebabkan kasus positif terlewat dari deteksi.

## 4.4 Insight Awal dari Pola Data

<div class="highlight-box">

Berdasarkan keseluruhan proses eksplorasi data, beberapa temuan awal yang dapat dirangkum adalah sebagai berikut:

- Fitur `thalach` (detak jantung maksimum) dan `oldpeak` (depresi segmen ST) tampak sebagai dua prediktor paling informatif terhadap status penyakit jantung.
- Pasien dengan tipe nyeri dada asimtomatik (`cp = 3`) menunjukkan proporsi kasus positif yang lebih tinggi dibandingkan tipe nyeri dada lainnya.
- Fitur tekanan darah (`trestbps`) dan kadar kolesterol (`chol`), meskipun secara klinis dikenal sebagai faktor risiko, justru menunjukkan korelasi linear yang relatif rendah terhadap target pada dataset ini.

</div>

---

# 5. Data Preparation

Tahap persiapan data merupakan langkah krusial untuk memastikan bahwa data yang digunakan dalam pemodelan berada dalam kondisi bersih, konsisten, dan sesuai dengan kebutuhan masing-masing algoritma.

## 5.1 Pembersihan Data

Pemeriksaan awal menunjukkan bahwa dataset ini tidak memiliki nilai yang hilang (*missing value*) maupun data duplikat, sehingga tidak diperlukan proses imputasi ataupun penghapusan baris data.

```python
print(df.isnull().sum())
print(df.duplicated().sum())
```

## 5.2 Encoding Data Kategorik

Kolom `thal`, yang pada dataset asli bertipe objek (kategorik non-numerik), dikonversi menjadi bentuk numerik menggunakan `LabelEncoder` agar dapat diproses oleh algoritma pembelajaran mesin.

```python
from sklearn.preprocessing import LabelEncoder

for col in df.columns:
    if df[col].dtype == 'object':
        le = LabelEncoder()
        df[col] = le.fit_transform(df[col])
```

## 5.3 Normalisasi dan Standardisasi Data Numerik

Mengingat algoritma KNN sangat sensitif terhadap skala fitur, seluruh fitur numerik distandarisasi menggunakan `StandardScaler` sehingga memiliki nilai rata-rata (*mean*) sebesar 0 dan simpangan baku (*standard deviation*) sebesar 1. Proses ini memastikan bahwa fitur dengan rentang nilai besar, seperti `chol`, tidak mendominasi perhitungan jarak dibandingkan fitur dengan rentang nilai kecil, seperti `oldpeak`.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

## 5.4 Pembagian Data (Data Splitting)

Dataset kemudian dibagi menjadi dua bagian, yaitu data latih (*training set*) sebesar 80% dan data uji (*testing set*) sebesar 20%, menggunakan fungsi `train_test_split` dengan `random_state=42` untuk menjamin reproduktibilitas hasil eksperimen.

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

| Bagian Data | Jumlah Sampel | Proporsi |
|---|---|---|
| Data Latih (Training) | 242 sampel | 80% |
| Data Uji (Testing) | 61 sampel | 20% |

---

# 6. Modeling

## 6.1 Pemilihan Algoritma

Sebagaimana telah dijelaskan pada bagian *business understanding*, proyek ini menggunakan dua algoritma klasifikasi dengan karakteristik yang saling melengkapi.

<table>
<thead>
<tr><th>Algoritma</th><th>Kelebihan</th><th>Kekurangan</th><th>Alasan Pemilihan</th></tr>
</thead>
<tbody>
<tr>
<td><strong>Decision Tree</strong></td>
<td>Interpretabilitas tinggi, mudah divisualisasikan, tidak memerlukan normalisasi data</td>
<td>Rentan mengalami <em>overfitting</em> apabila kedalaman pohon tidak dibatasi</td>
<td>Cocok untuk data medis karena alur keputusannya dapat dipahami secara langsung oleh tenaga medis</td>
</tr>
<tr>
<td><strong>K-Nearest Neighbor (KNN)</strong></td>
<td>Sederhana, mampu menangkap pola keputusan non-linear</td>
<td>Kurang efisien pada data berukuran besar, sensitif terhadap skala fitur</td>
<td>Menunjukkan performa yang baik pada dataset berukuran sedang seperti pada proyek ini</td>
</tr>
</tbody>
</table>

## 6.2 Implementasi Model

### 6.2.1 Decision Tree

Model Decision Tree dibangun dengan membatasi kedalaman maksimum pohon (`max_depth=5`) serta menetapkan jumlah minimum sampel untuk pemisahan (`min_samples_split=10`) dan jumlah minimum sampel pada daun (`min_samples_leaf=5`). Pembatasan ini bertujuan untuk mencegah model menghafal data latih secara berlebihan (*overfitting*).

```python
dt_model = DecisionTreeClassifier(
    random_state=42,
    max_depth=5,
    min_samples_split=10,
    min_samples_leaf=5
)
dt_model.fit(X_train_scaled, y_train)
```

### 6.2.2 K-Nearest Neighbor (KNN)

Pemilihan nilai *k* yang optimal dilakukan melalui pengujian sistematis terhadap rentang nilai *k* dari 1 hingga 15. Berdasarkan hasil pengujian tersebut, nilai *k* = 11 dipilih karena memberikan keseimbangan terbaik antara bias dan varians, sekaligus menghasilkan akurasi tertinggi pada data uji.

```python
# Nilai k optimal = 11
knn_model = KNeighborsClassifier(n_neighbors=11)
knn_model.fit(X_train_scaled, y_train)
```

## 6.3 Perbandingan Akurasi Model

<div class="result-box">

| Model | Akurasi |
|---|---|
| Decision Tree | 80,33% |
| **K-Nearest Neighbor (k=11)** | **85,25%** |

Berdasarkan hasil pengujian awal, model KNN menunjukkan akurasi yang lebih tinggi dibandingkan Decision Tree pada dataset ini, dengan selisih sebesar hampir 5 poin persentase.

</div>

## 6.4 Visualisasi Model Decision Tree

<figure>

![Decision Tree](decision_tree_visualization.png)

<figcaption>Gambar 6.1 — Struktur pohon keputusan hasil pelatihan model</figcaption>
</figure>

Visualisasi struktur pohon keputusan menunjukkan bahwa fitur `oldpeak`, `cp`, dan `thalach` menempati posisi sebagai simpul (*node*) yang paling sering digunakan dalam proses pengambilan keputusan, sejalan dengan hasil analisis korelasi yang telah dibahas pada tahap eksplorasi data sebelumnya.

---

# 7. Evaluation

## 7.1 Confusion Matrix

### Decision Tree

| | Prediksi: Tidak Sakit | Prediksi: Sakit |
|---|---|---|
| **Aktual: Tidak Sakit** | 35 | 9 |
| **Aktual: Sakit** | 3 | 14 |

### K-Nearest Neighbor (k = 11)

| | Prediksi: Tidak Sakit | Prediksi: Sakit |
|---|---|---|
| **Aktual: Tidak Sakit** | 40 | 4 |
| **Aktual: Sakit** | 5 | 12 |

## 7.2 Metrik Evaluasi

| Model | Accuracy | Precision (Sakit) | Recall (Sakit) | F1-Score (Sakit) |
|---|---|---|---|---|
| Decision Tree | 0,8033 | 0,6087 | **0,8235** | 0,7000 |
| **K-Nearest Neighbor** | **0,8525** | **0,7500** | 0,7059 | **0,7273** |

## 7.3 Penjelasan Kinerja Model

Berdasarkan hasil evaluasi pada tabel di atas, model **KNN** mencatatkan akurasi tertinggi sebesar 85,25%, disertai nilai *precision* yang lebih baik yaitu 0,75, dibandingkan Decision Tree yang hanya mencapai *precision* sebesar 0,6087. Nilai *precision* yang lebih tinggi ini menunjukkan bahwa ketika model KNN memprediksi seorang pasien berisiko sakit, prediksi tersebut lebih dapat dipercaya dibandingkan prediksi serupa dari model Decision Tree.

Namun demikian, Decision Tree unggul dari sisi *recall*, dengan nilai 0,8235 dibandingkan 0,7059 pada KNN. Nilai *recall* yang lebih tinggi ini berarti Decision Tree lebih mampu menangkap kasus-kasus pasien yang benar-benar sakit, meskipun konsekuensinya adalah munculnya lebih banyak *false positive* — yaitu pasien yang sebenarnya sehat namun diklasifikasikan sebagai berisiko.

<blockquote>
Dalam konteks aplikasi medis, trade-off antara precision dan recall memiliki implikasi praktis yang signifikan. Recall yang tinggi lebih diutamakan ketika konsekuensi melewatkan kasus positif (false negative) jauh lebih berbahaya dibandingkan konsekuensi kesalahan false positive, mengingat pasien yang salah terdiagnosis berisiko masih dapat menjalani pemeriksaan lanjutan untuk konfirmasi.
</blockquote>

Secara keseluruhan, mempertimbangkan keseimbangan antara akurasi, precision, dan F1-score, model **KNN dengan k = 11** dipilih sebagai model dengan performa terbaik pada proyek ini, meskipun Decision Tree tetap memiliki keunggulan tersendiri dari sisi interpretabilitas dan kemampuan mendeteksi kasus positif secara lebih menyeluruh.

---

# 8. Kesimpulan dan Rekomendasi

## 8.1 Ringkasan Hasil Modeling dan Evaluasi

Proyek ini berhasil mengimplementasikan dan membandingkan dua algoritma *machine learning* — Decision Tree dan K-Nearest Neighbor — dalam memprediksi risiko penyakit jantung menggunakan dataset Cleveland Heart Disease. Melalui rangkaian proses mulai dari pemahaman bisnis, eksplorasi data, persiapan data, hingga pemodelan dan evaluasi, diperoleh hasil bahwa model KNN dengan nilai k = 11 mencapai akurasi sebesar 85,25%, sementara Decision Tree mencapai akurasi sebesar 80,33%. Model KNN menunjukkan kinerja yang lebih stabil, khususnya pada metrik precision dan akurasi keseluruhan.

## 8.2 Ketercapaian Tujuan Proyek

<div class="result-box">

Tujuan proyek dinyatakan tercapai. Model yang dikembangkan mampu memprediksi risiko penyakit jantung dengan tingkat akurasi di atas 85%, yang tergolong cukup memadai untuk digunakan sebagai alat bantu skrining awal, meskipun tetap memerlukan konfirmasi lebih lanjut melalui pemeriksaan medis formal.

</div>

## 8.3 Kelebihan dan Keterbatasan Model

| Kelebihan | Keterbatasan |
|---|---|
| Interpretabilitas tinggi pada model Decision Tree | Ukuran dataset relatif kecil, hanya 303 sampel |
| Akurasi model terbaik melebihi 85% | Data belum mencakup populasi pasien yang beragam secara demografis |
| Proses implementasi tergolong sederhana dan efisien dari sisi komputasi | Model belum diuji validitasnya pada dataset eksternal yang independen |

## 8.4 Rekomendasi Perbaikan

Berdasarkan hasil dan keterbatasan yang telah diidentifikasi, beberapa rekomendasi pengembangan lebih lanjut yang dapat dipertimbangkan antara lain:

1. **Perluasan dataset** — menggunakan dataset dengan jumlah sampel yang jauh lebih besar dan lebih beragam secara demografis untuk meningkatkan kemampuan generalisasi model.
2. **Eksplorasi algoritma tambahan** — menguji algoritma lain seperti Random Forest, XGBoost, atau Neural Network sebagai pembanding untuk memperkaya analisis performa.
3. **Rekayasa fitur (feature engineering)** — menambahkan fitur turunan baru, misalnya rasio antara kadar kolesterol dan tekanan darah, yang berpotensi meningkatkan daya prediksi model.
4. **Optimasi hyperparameter** — melakukan pencarian parameter optimal secara sistematis melalui teknik Grid Search atau Random Search.
5. **Pengembangan menuju tahap deployment** — merancang aplikasi berbasis web sederhana agar model dapat diakses dan digunakan secara langsung oleh tenaga medis di lapangan.

---

# 9. Referensi

1. Kohsasih, K. L., Sunario, D. S., Alvin, A., & Laurendio, F. (2025). Enhancing early heart disease detection through comparative analysis of random forest, decision tree, and K-NN models. *IT Journal Research and Development*, 10(2), 66–77. https://doi.org/10.25299/itjrd.2025.24703

2. Muttakin, M., Rusmana, N. R., & Ramadhani, D. (2025). Analisis perbandingan algoritma decision tree, random forest, KNN, dan SVM dalam prediksi penyakit jantung. *Journal of System & Technology (SYSTEC)*, 1(2), 35–42. https://systec.ejournal.unri.ac.id/index.php/systec/article/view/18

3. Coronary heart disease prediction: A comparative study of machine learning algorithms. (2024). *Journal of Advances in Information Technology*, 15(1), 27–32. https://doi.org/10.12720/jait.15.1.27-32

4. Balhaf, K., Munassar, N. A., & Akoosh, L. M. S. (2025). Performance evaluation of machine learning algorithms for heart disease prediction using real-world data from Yemen. *2025 International Conference on Artificial Intelligence, Computer, Data Sciences and Applications (ACDSA)*, 1–7. https://doi.org/10.1109/ACDSA65407.2025.11166082

5. Regen, R., & Setiawan, H. (2024). Advancing cardiovascular risk prediction: A review of machine learning models and their clinical potential. *Journal of Electrical Technology UMY*, 8(2). https://journal.umy.ac.id/index.php/jet/article/view/25208

---

# 10. Lampiran

## 10.1 Dataset Mentah

- `data/heart_disease.csv` — Dataset asli yang digunakan dalam proyek ini.

## 10.2 Notebook Lengkap

- `uas_model.ipynb` — Berkas notebook yang memuat seluruh proses, mulai dari eksplorasi data hingga evaluasi model.

## 10.3 Berkas Grafik Pendukung

| Berkas | Deskripsi |
|---|---|
| `distribusi_target.png` | Distribusi kelas target |
| `distribusi_usia.png` | Sebaran usia pasien |
| `distribusi_sex.png` | Proporsi jenis kelamin pasien |
| `heatmap_korelasi.png` | Peta korelasi antar fitur |
| `korelasi_target.png` | Korelasi fitur terhadap target |
| `knn_optimal_k.png` | Grafik pencarian nilai k optimal |
| `perbandingan_akurasi.png` | Perbandingan akurasi antar model |
| `confusion_matrix.png` | Visualisasi confusion matrix |
| `decision_tree_visualization.png` | Visualisasi struktur pohon keputusan |

## 10.4 Jurnal Referensi

Seluruh jurnal yang dirujuk pada laporan ini tersedia dalam format PDF pada folder `data/Jurnal/` (jurnal1.pdf hingga jurnal5.pdf).

---

<div class="signature">

*Laporan ini disusun sebagai pemenuhan tugas Ujian Akhir Semester pada mata kuliah Kecerdasan Buatan.*

**Disusun oleh:**

Moch Azriel Naufan H — 2406046
Muhamad Thoriq Mustaqim — 2406045

**Institut Teknologi Garut**
2026

</div>
