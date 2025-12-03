# 🛒 E-Commerce Customer Segmentation Analysis (RFM Method)

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Library](https://img.shields.io/badge/Library-Pandas%2C%20Seaborn-green)
![Status](https://img.shields.io/badge/Status-Completed-orange)

## 📌 Latar Belakang Project
Dalam bisnis ritel yang kompetitif, memperlakukan semua pelanggan dengan cara yang sama adalah strategi yang tidak efisien. Proyek ini bertujuan untuk membantu tim pemasaran mengidentifikasi segmen pelanggan yang berbeda untuk strategi promosi yang lebih personal (Hyper-personalization).

Saya menggunakan metode **RFM Analysis (Recency, Frequency, Monetary)** untuk mengelompokkan pelanggan berdasarkan perilaku beli mereka.

## 📂 Dataset
Dataset yang digunakan adalah data transaksi *Online Retail* yang berisi transaksi dari 01/12/2010 hingga 09/12/2011.
- **Sumber:** https://www.kaggle.com/datasets/carrie1/ecommerce-data?resource=download
- **Jumlah Data:** 500,000+ baris transaksi.

## 🛠️ Langkah Pengerjaan
1. **Data Cleaning:** - Menghapus data tanpa `CustomerID`.
   - Menghapus transaksi *refund* (Quantity negatif).
   - Mengubah tipe data tanggal.
2. **Feature Engineering:**
   - Membuat kolom `TotalAmount` (Quantity * UnitPrice).
3. **RFM Calculation:**
   - **Recency:** Hari sejak pembelian terakhir.
   - **Frequency:** Jumlah transaksi unik.
   - **Monetary:** Total uang yang dibelanjakan.
4. **Scoring & Segmentation:**
   - Menggunakan `qcut` (Quartile) untuk memberikan skor 1-4 pada setiap metrik.
   - Mengelompokkan pelanggan menjadi: *Champions, Loyal Customers, Potential Loyalist, At Risk, dll*.

## 📊 Hasil Analisis (Insight)

*(Anda bisa upload gambar grafik batang hasil kode terakhir Anda ke folder 'images' lalu pasang di sini)*
![Distribusi Pelanggan](images/distribution_chart.png)

Berdasarkan analisis, ditemukan beberapa wawasan kunci:
1. **Champions (Pelanggan Sultan):** Mencakup sekitar **[XX]%** dari total pelanggan. Mereka baru saja berbelanja dan sering menghabiskan uang banyak.
2. **At Risk (Perlu Perhatian):** Terdapat segmen besar pelanggan yang dulu sering berbelanja namun sudah lama tidak kembali.
3. **Pareto Principle:** Sebagian kecil pelanggan loyal menyumbang kontribusi pendapatan terbesar.

## 💡 Rekomendasi Bisnis
Berdasarkan wawasan di atas, saya merekomendasikan strategi berikut:

| Segmen | Strategi |
| :--- | :--- |
| **Champions** | Tawarkan *Early Access* untuk produk baru & program reward eksklusif. |
| **Potential Loyalist** | Berikan rekomendasi produk (*Upselling*) untuk meningkatkan nilai belanja. |
| **At Risk** | Kirimkan email *Win-Back Campaign* dengan diskon waktu terbatas. |
| **Lost** | Kurangi budget iklan, alihkan ke email marketing otomatis. |

## 🚀 Cara Menjalankan Code
1. Clone repositori ini.
2. Install library yang dibutuhkan:
   ```bash
   pip install -r requirements.txt
