Proyek ini bertujuan untuk menganalisis data penjualan dari cabang supermarket untuk memberikan wawasan yang dapat mendukung keputusan strategis. Analisis mencakup beberapa aspek penting seperti perilaku pembayaran pelanggan, efisiensi biaya pengiriman, karakteristik produk, dan distribusi kuantitas penjualan.

**Tujuan Analisis:**

1. Mengidentifikasi median nilai transaksi per metode pembayaran.
2. Menemukan metode pembayaran dengan nilai transaksi rata-rata (basket size) terbesar.
3. Menganalisis biaya pengiriman (shipping cost).
4. Memahami karakteristik berat produk per kategori.
5. Memvisualisasikan sebaran kuantitas penjualan.

**Tahapan Analisis**
1. Persiapan Data
   
  - Memuat data menggunakan pandas.

3. Analisis Perilaku Pembayaran

  - Menggunakan **groupby('payment_type'**) dan **.median()** pada kolom **price** untuk menemukan median nilai transaksi.

4. Analisis Biaya Pengiriman

  - Mengganti nama kolom **freight_value** menjadi **shipping_cost** menggunakan **.rename().**
  - Menggunakan **.sort_values()** untuk menemukan **shipping_cost termahal.**

5. Karakteristik Produk

  - Menggunakan **groupby('product_category_name')** dan **.mean() serta .std()** pada kolom **product_weight_gram**.
  - Menggunakan **.std()** pada hasil standar deviasi untuk menemukan kategori produk dengan berat paling seragam.

6. Visualisasi

  - Membuat histogram dari kolom quantity dengan **bins=5** dan **figsize=(4, 5)** untuk melihat distribusi penjualan.

**Dataset:** Data penjualan ini diperoleh dari sumber publik dan tersedia di tautan berikut: [order.csv](https://storage.googleapis.com/dqlab-dataset/order.csv).

**Pustaka yang Digunakan:**
    Proyek ini dibangun menggunakan Python dengan pustaka utama sebagai berikut:
    
    impport pandas as pd
    import matplotlib.pyplot as plt
