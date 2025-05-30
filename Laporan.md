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
Data yang diambil adalah data harga saham PT Bank Rakyat Indonesia (Persero) Tbk (BBRI.JK) dari Yahoo Finance. Adapun data yang diambil adalah data historis 10 tahun yang lalu (1 Januari 2015 hingga 28 Mei 2025). Data cenderung naik dan turun sehingga AI harus mempelajari model dengan baik. Rincian data berjumlah 2.565 data dengan 7 variabel.
URL : https://finance.yahoo.com/quote/BBRI.JK/

### Variabel-variabel pada Harga Saham BBRI.JK dataset adalah sebagai berikut:
- Open: Harga saham pada saat pembukaan perdagangan di hari tersebut. Ini adalah harga transaksi pertama untuk hari itu.
- High: Harga tertinggi yang dicapai oleh saham selama sesi perdagangan di hari tersebut.
- Low: Harga terendah yang dicapai oleh saham selama sesi perdagangan di hari tersebut.
- Close: Harga saham pada saat penutupan perdagangan di hari tersebut. Ini sering dianggap sebagai harga paling penting untuk hari itu.
- Volume: Jumlah saham yang diperdagangkan selama sesi perdagangan di hari tersebut. Volume yang tinggi dapat mengindikasikan minat yang besar pada saham tersebut.
- Dividends: Jumlah dividen tunai yang dibayarkan per saham pada tanggal tertentu. Jika tidak ada dividen, nilainya biasanya nol.
- Stock Splits: Informasi mengenai pemecahan saham (stock split). Ini biasanya dinyatakan sebagai rasio (misalnya, 2:1 berarti setiap pemegang saham menerima dua saham baru untuk setiap satu saham lama yang mereka miliki). Jika tidak ada pemecahan saham, nilainya mungkin 1 atau indikator lain yang menunjukkan tidak ada perubahan.

Dalam proyek ini, untuk memahami data harga saham BBRI yang akan digunakan, perlu dilakukann beberapa tahapan Exploratory Data Analysis (EDA) dan visualisasi data, antara lain:
- Melihat Struktur Data: Memeriksa format data, tipe data setiap kolom.
- Analisis Statistik Deskriptif: Menghitung statistik deskriptif untuk setiap fitur harga saham untuk mendapatkan gambaran umum distribusi data.
- Visualisasi Data Time Series: Membuat plot garis harga penutupan saham BBRI terhadap waktu untuk mengidentifikasi tren.
- Pemeriksaan Missing Values: Mengidentifikasi dan menangani jika ada nilai yang hilang dalam dataset.
- Analisis Korelasi: Memeriksa korelasi antara berbagai fitur harga saham.

## Data Preparation



## Modeling



## Evaluation



