# Laporan Proyek Machine Learning - Rahayu Nur Rahmawati

## Domain Proyek

Latar belakang proyek ini adalah adanya kebutuhan investor dan pihak terkait lainnya untuk memprediksi pergerakan harga saham BBRI. Prediksi yang akurat dapat membantu dalam pengambilan keputusan investasi, manajemen risiko, dan perencanaan strategis.
Berdasarkan Artikel dari Indonesia Stock Exchange berjudul 'Jangan Berinvestasi Saham Tanpa Strategi' menyebutkan bahwa beberapa tahun terakhir, investasi saham menjadi bagian dari perencanaan keuangan setiap orang. Namun, banyak investor saham yang melakukan jual beli saham tanpa analisis apapun. Fluktuasi harga saham dipengaruhi oleh berbagai faktor, baik internal perusahaan maupun eksternal seperti kondisi ekonomi makro, kebijakan pemerintah, dan sentimen pasar. Oleh karena itu, pengembangan model prediksi yang handal menjadi penting. 

Berdasarkan Data  statistik  dari  Kustodian  Sentral  Efek  Indonesia  (KSEI)  tahun  2022  menunjukkan  bahwa  jumlah pertumbuhan  36 investor pasar modal semakin meningkat setiap tahunnya yakni pada akhir tahun 2022 mencapai 10,3 juta investor atau meningkat 37,68% jika dibandingkan dengan akhir tahun 2021 sebanyak 7,48 juta investor. Sebagai contoh, masalah prediksi harga saham BBRI perlu diselesaikan karena memberikan wawasan berharga bagi para pemangku kepentingan. Prediksi yang baik dapat meminimalkan risiko kerugian investasi dan memaksimalkan potensi keuntungan. Selain itu, bagi perusahaan, pemahaman terhadap sentimen pasar yang tercermin dalam harga saham dapat menjadi indikator kinerja dan daya tarik di mata investor. Penyelesaian masalah ini dilakukan dengan mengembangkan dan menguji model prediksi menggunakan data historis harga saham dan faktor-faktor relevan lainnya.

## Business Understanding

Proyek prediksi harga saham BRI ini berangkat dari adanya permasalahan fluktuasi harga saham yang dapat menimbulkan risiko bagi investor. Investor membutuhkan informasi yang akurat untuk mengambil keputusan investasi yang tepat. 

### Problem Statements

Menjelaskan pernyataan masalah latar belakang:
- Bagaimana cara memprediksi harga saham PT Bank Rakyat Indonesia (Persero) Tbk (BBRI) secara akurat untuk membantu pengambilan keputusan investasi?
- Bagaimana mengembangkan model prediksi harga saham BBRI yang memiliki tingkat akurasi yang memuaskan?
- Bagaimana insight atau informasi yang berguna bagi investor dan pihak terkait dalam memahami potensi pergerakan harga saham BBRI?

### Goals

Menjelaskan tujuan dari pernyataan masalah:
- Mengetahui cara memprediksi harga saham PT Bank Rakyat Indonesia (Persero) Tbk (BBRI) secara akurat untuk membantu pengambilan keputusan investasi
- Mampu mengembangkan model prediksi harga saham BBRI yang memiliki tingkat akurasi yang memuaskan.
- Menjelaskan insight atau informasi yang berguna bagi investor dan pihak terkait dalam memahami potensi pergerakan harga saham BBRI.

    ### Solution statements
Proyek yang dilakukan yaitu membangun dan melatih model LSTM, yang merupakan jenis recurrent neural network yang sangat efektif dalam memproses data berurutan seperti data harga saham. Model LSTM akan dilatih menggunakan data historis harga saham BBRI untuk mempelajari pola dan ketergantungan temporal dalam data. Pengukuran keberhasilan model ini akan dievaluasi menggunakan metrik seperti Mean Squared Error (MSE), Root Mean Squared Error (RMSE), atau Mean Absolute Error (MAE) untuk mengukur seberapa akurat prediksi harga saham yang dihasilkan dibandingkan dengan harga aktual.

## Data Understanding
Paragraf awal bagian ini menjelaskan informasi mengenai data yang Anda gunakan dalam proyek. Sertakan juga sumber atau tautan untuk mengunduh dataset. Contoh: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Restaurant+%26+consumer+data).

Selanjutnya uraikanlah seluruh variabel atau fitur pada data. Sebagai contoh:  

### Variabel-variabel pada Restaurant UCI dataset adalah sebagai berikut:
- accepts : merupakan jenis pembayaran yang diterima pada restoran tertentu.
- cuisine : merupakan jenis masakan yang disajikan pada restoran.
- dst

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

