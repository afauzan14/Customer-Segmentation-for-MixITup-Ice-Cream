# 🍦 Customer Segmentation for MixITup Ice Cream using K-Prototypes Clustering
### Data Mining & Unsupervised Learning on Mixed Data Types (Numerical & Categorical)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter&logoColor=white)](Kelompok_C_Study_Case_02.ipynb)
[![Dataset](https://img.shields.io/badge/Dataset-MixITup%20CSV-green)](Case-Study-02-MixITup.csv)
[![Algorithm](https://img.shields.io/badge/Algorithm-K--Prototypes-red)]()

---

## 📌 Ringkasan Proyek (Business Understanding)

**MixITup** adalah perusahaan rintisan (*startup*) anak muda yang bergerak di industri *Food & Beverage* (Ice Cream, Boba Drinks, dan Desserts/Snacks). Saat ini, MixITup telah memiliki 3 cabang utama di **Jakarta, Depok, dan Tangerang** dengan antrean *dine-in* maupun *delivery* yang tinggi.

Setelah memperoleh suntikan pendanaan **Seri B sebesar Rp 33 Miliar**, MixITup bersiap melakukan ekspansi gerai ke kota-kota baru dan kampanye pemasaran berskala besar (*massive marketing*). Agar alokasi anggaran promosi tepat sasaran, perusahaan memerlukan **segmentasi pelanggan berbasis data** untuk memahami perilaku, demografi, dan preferensi belanja konsumen secara terukur.

Proyek ini menerapkan metode **Unsupervised Machine Learning: K-Prototypes Clustering**, sebuah pendekatan klastering tingkat lanjut yang mampu mengolah fitur **numerik dan kategorik secara simultan** tanpa menghilangkan karakteristik alami data.

---

## 🎯 Tujuan Analisis

1. Mengidentifikasi pola demografi dan perilaku transaksi pelanggan gerai MixITup.
2. Membentuk klaster pelanggan yang homogen dan bermakna (*meaningful customer tiers*).
3. Merumuskan rekomendasi strategi bisnis, operasional, dan kampanye promosi yang terpersonalisasi untuk tiap segmen.

---

## 🔬 Pemodelan K-Prototypes & Penentuan Cluster Optimal

Algoritma **K-Prototypes** dipilih karena menggabungkan jarak *Euclidean* untuk fitur numerik (`umur`, `gaji`, `skor`) dan *matching dissimilarity* untuk fitur kategorik (`sex`, `menikah`, `kota`, `promo`, `hari`, `rasa`).

### Penentuan Nilai $k$ (Elbow Method)
Eksperimen pengujian nilai $k \in [1, 9]$ menggunakan kurva nilai *Cost*:
- Terjadi patahan sudut (*elbow point*) yang signifikan pada $k = 4$.
- Nilai **$k = 4$** dipilih sebagai jumlah klaster paling optimal dan representatif untuk kebutuhan segmentasi bisnis.

---

## 🏆 Profil 4 Segmen Pelanggan (Customer Clusters)

| Segmen | Cluster | Wilayah Dominan | Karakteristik Belanja & Finansial | Pola Transaksi | Varian Rasa Favorit |
| :--- | :---: | :---: | :--- | :--- | :---: |
| **Bronze** 🥉 | Cluster 0 | **Tangerang** | Gaji rendah–menengah, skor pengeluaran rendah. Sangat sensitif harga. | Sering mencari & menggunakan promo; hari favorit: **Senin**. | Coklat |
| **Silver** 🥈 | Cluster 2 | **Jakarta** | Gaji menengah ke atas, pengeluaran moderat. Jarang menggunakan promo. | Transaksi terpusat di akhir pekan (hari favorit: **Sabtu**). | Blueberry |
| **Gold** 🥇 | Cluster 1 | **Jakarta** | Pendapatan tinggi, skor pengeluaran tinggi. Pembeli rutin bernilai tinggi. | Jarang memakai promo; hari favorit belanja: **Senin**. | Vanila |
| **Platinum** 💎 | Cluster 3 | **Depok** | Pendapatan moderat–tinggi, skor pengeluaran tertinggi. Konsumen paling loyal. | Jarang memakai promo; hari favorit belanja: **Senin**. | Vanila |

---

## 💡 Rekomendasi Strategi Bisnis (Actionable Insights)

### 🥉 1. Bronze Cluster (Tangerang - Price Sensitive)
- **Promo Berbasis Hari Sepi:** Tawarkan paket *"Senin Manis"* atau diskon bundling varian Coklat untuk menarik kunjungan di awal pekan.
- **Kartu Loyalty Bertingkat:** Rancang program *loyalty stamp* untuk mendorong frekuensi belanja pelanggan agar naik ke tier berikutnya.

### 🥈 2. Silver Cluster (Jakarta - Weekend Socializer)
- **Optimasi Jam Operasional Akhir Pekan:** Perpanjang jam operasional toko pada hari Sabtu dan sediakan area *dine-in* yang nyaman untuk nongkrong.
- **Lokasi Strategis & Promosi Digital:** Pasang iklan targeted di area komersial Jakarta (pusat perkantoran, kampus, dan mall).

### 🥇 3. Gold Cluster (Jakarta - Premium Spender)
- **Menu Eksklusif & Inovasi Produk:** Tawarkan menu edisi terbatas (*seasonal/premium flavor*) varian Vanila atau topping boba eksklusif.
- **Manajemen Antrean & Pelayanan Cepat:** Atur alokasi barista pada hari Senin guna mempertahankan kepuasan pelanggan bernilai tinggi.

### 💎 4. Platinum Cluster (Depok - Top Loyal Customer)
- **VIP Treatment & Priority Line:** Berikan jalur antrean khusus (*fast-track*) atau program keanggotaan VIP untuk pelanggan setia Depok.
- **Personalized Rewards:** Berikan kejutan apresiasi gratis di hari ulang tahun atau reward khusus tanpa harus menunggu promo umum.

---

*Proyek ini dikembangkan untuk studi kasus data mining dan segmentasi pelanggan F&B.*
