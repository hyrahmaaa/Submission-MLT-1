# Prediksi Harga Saham PT Bank Rakyat Indonesia (Persero) Tbk (BBRI)

Proyek ini bertujuan untuk mengembangkan model machine learning untuk memprediksi harga saham PT Bank Rakyat Indonesia (Persero) Tbk (BBRI).

## Daftar Berkas

Berikut adalah deskripsi singkat dari berkas-berkas utama dalam repositori ini:

1.  **`README.md`**: Berkas ini yang sedang Anda baca, berisi informasi umum tentang proyek.
2.  **`notebook.ipynb`**: Notebook Jupyter yang berisi kode implementasi proyek, termasuk:
    * Pengambilan dan pemrosesan data saham BBRI.
    * Pembagian dataset menjadi data latih dan data uji.
    * Normalisasi data.
    * Pembuatan dan pelatihan model Long Short-Term Memory (LSTM).
    * Evaluasi model menggunakan metrik seperti MAE, MSE, dan RMSE.
    * Visualisasi hasil prediksi.
3.  **`data/`**: dataset yang digunakan berasal dari link : https://finance.yahoo.com/quote/BBRI.JK/.
4.  * `stock_prediction_model.h5` (nama berkas model LSTM yang telah dilatih).
5.  **`requirements.txt`**: Berkas ini mencantumkan *library* Python yang dibutuhkan untuk menjalankan kode dalam notebook. 

## Cara Penggunaan
1.  Klon repositori ini.
2.  Pastikan Anda telah menginstal Python 3.x.
3.  Instal dependensi yang diperlukan menggunakan:
    ```bash
    pip install -r requirements.txt
    ```
4.  Jalankan notebook Jupyter `notebook.ipynb` untuk melihat implementasi dan hasilnya.
5.  Jika ingin melihat model yang dilatih, dapat langsung menjalankan bagian evaluasi atau prediksi menggunakan model yang tersedia.

## Hasil
Proyek ini berhasil mengimplementasikan model Long Short-Term Memory (LSTM) untuk memprediksi pergerakan harga saham PT Bank Rakyat Indonesia (Persero) Tbk (BBRI). Evaluasi model pada data uji menunjukkan metrik kinerja sebagai berikut:
- Mean Absolute Error (MAE): Sebesar 110.95 poin. Nilai ini mengindikasikan bahwa, secara rata-rata, prediksi harga saham oleh model meleset sekitar Rp110.95 dari harga aktual.
- Mean Squared Error (MSE): Tercatat sebesar 20332.43 poin kuadrat. MSE memberikan ukuran rata-rata dari kuadrat selisih antara prediksi dan nilai sebenarnya, dengan memberikan bobot lebih besar pada kesalahan yang lebih besar.
- Root Mean Squared Error (RMSE): Mencapai 142.59 poin. RMSE, yang merupakan akar kuadrat dari MSE, memberikan interpretasi kesalahan dalam satuan yang sama dengan harga saham.

Dalam konteks harga saham BBRI yang umumnya berada dalam rentang ribuan Rupiah, nilai MAE sebesar Rp110.95 menunjukkan bahwa rata-rata kesalahan prediksi relatif kecil secara proporsional. Namun, nilai RMSE yang sedikit lebih tinggi mengisyaratkan adanya variasi yang lebih besar dalam kesalahan prediksi individual.

Secara keseluruhan, model LSTM yang dikembangkan menunjukkan kemampuan untuk memprediksi harga saham BBRI dengan tingkat error yang moderat. Meskipun demikian, hasil ini membuka peluang untuk penelitian dan pengembangan lebih lanjut dalam rangka meningkatkan akurasi prediksi, misalnya melalui penambahan fitur-fitur lain, tuning hyperparameter yang lebih mendalam, atau penggunaan arsitektur model yang berbeda.
