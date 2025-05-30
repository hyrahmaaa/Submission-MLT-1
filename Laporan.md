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
Dalam proyek prediksi saham BBRI ini, tahapan data preparation yang dilakukan meliputi:
- Pembagian Dataset: Data historis harga saham BBRI dibagi menjadi dua bagian, yaitu training set dan testing set, menggunakan fungsi train_test_split dari library sklearn. Pembagian ini penting agar model dapat dilatih pada sebagian data (training set) dan kemudian dievaluasi kemampuannya dalam memprediksi data yang belum pernah dilihat sebelumnya (testing set). Proporsi pembagian yang digunakan adalah 80% untuk training dan 20% untuk testing. Alasan: Pembagian ini diperlukan untuk menghindari overfitting, yaitu kondisi di mana model bekerja sangat baik pada data latih tetapi buruk pada data baru. Dengan menguji model pada data yang terpisah, maka dapat memperoleh perkiraan yang lebih realistis tentang kinerja model di dunia nyata.
- Normalisasi Data: Fitur-fitur harga saham dinormalisasi menggunakan teknik MinMaxScaler. Normalisasi ini menskalakan nilai-nilai fitur ke dalam rentang antara 0 dan 1. Alasan: Normalisasi penting terutama ketika menggunakan algoritma neural network seperti LSTM. Normalisasi membantu mempercepat proses pelatihan model, mencegah fitur dengan skala yang lebih besar mendominasi perhitungan, dan dapat meningkatkan stabilitas serta kinerja model secara keseluruhan. Dengan skala yang seragam, gradien dalam proses pembelajaran menjadi lebih terkelola.

## Modeling
Dalam proyek ini, algoritma utama yang digunakan untuk pemodelan adalah Long Short-Term Memory (LSTM).

Kelebihan LSTM:
- Kemampuan Memproses Data Berurutan: LSTM dirancang khusus untuk memproses data berurutan (seperti time series) dan memiliki kemampuan untuk mempelajari ketergantungan jangka panjang dalam data. Ini sangat relevan untuk prediksi harga saham di mana pergerakan harga di masa lalu dapat mempengaruhi harga di masa depan.
- Mengatasi Masalah Vanishing/Exploding Gradients: Dibandingkan dengan Recurrent Neural Network (RNN) tradisional, LSTM memiliki mekanisme gate (input, forget, output, cell state) yang membantu mengatasi masalah vanishing dan exploding gradients, sehingga memungkinkan pelatihan model yang lebih dalam dan lebih efektif.

Kekurangan LSTM:
- Komputasi yang Lebih Mahal: Arsitektur LSTM yang lebih kompleks dengan banyak parameter dapat membutuhkan sumber daya komputasi yang lebih besar dan waktu pelatihan yang lebih lama dibandingkan dengan model yang lebih sederhana.
- Potensi Overfitting: Model LSTM dengan banyak lapisan dan unit dapat rentan terhadap overfitting jika tidak diregularisasi dengan baik atau jika data pelatihan tidak mencukupi.

## Evaluation
Untuk mengevaluasi kinerja model prediksi harga saham BBRI berbasis LSTM, digunakan tiga metrik evaluasi utama: Mean Absolute Error (MAE), Mean Squared Error (MSE), dan Root Mean Squared Error (RMSE).

- Mean Absolute Error (MAE) mengukur nilai absolut rata-rata dari selisih antara nilai prediksi dan nilai aktual. MAE memberikan gambaran seberapa besar rata-rata kesalahan prediksi dalam satuan yang sama dengan data aslinya. Berdasarkan hasil, MAE model adalah 110.9495.

- Mean Squared Error (MSE) mengukur rata-rata dari kuadrat selisih antara nilai prediksi dan nilai aktual. MSE memberikan bobot yang lebih besar pada kesalahan yang lebih besar karena adanya operasi kuadrat. Berdasarkan hasil, MSE model adalah 20332.4275.

- Root Mean Squared Error (RMSE) adalah akar kuadrat dari MSE. RMSE juga mengukur besarnya kesalahan prediksi, tetapi dalam satuan yang sama dengan data aslinya, dan memberikan bobot yang lebih besar pada kesalahan yang besar dibandingkan dengan MAE. Berdasarkan hasil, RMSE model adalah 142.5918.

Nilai-nilai MAE, MSE, dan RMSE ini akan digunakan untuk mengevaluasi seberapa baik model LSTM dalam memprediksi harga saham BBRI pada data testing. Semakin kecil nilai metrik-metrik ini, semakin baik kinerja modelnya.
