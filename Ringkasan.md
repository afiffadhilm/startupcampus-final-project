# :rocket: KETAHANAN PANGAN DI INDONESIA :rocket:
Kondisi terpenuhinya pangan bagi negara dengan perseorangan. Ketahanan pangan diukur dengan **Indeks Ketahanan Pangan**
yang memeiliki peran dalam mengevaluasi capaian ketahanan pangan dan gizi wilayah.

Project ini dibuat untuk menyelesaikan final project [MSIB7] Data Science Track Startup Campus.

Judul: **SINERGI EKONOMI HIJAU UNTUK MEWUJUDKAN KETAHANAN PANGAN BERKELANJUTAN**

---
# :loudspeaker: PROBLEM STATEMENT
meskipun Indonesia memiliki potensi besar dalam sektor pertanian, tantangan dalam keterjangkauan, ketersediaan, pemanfaatan, dan berkelanjutan pangan masih menjadi hambatan utama untuk mewujudkan ketahanan pangan.
Berdasarkan tren IKP (Indek Ketahanan Pangan) di Indonesia dari tahun 2012-2022.
![Tren Indeks Ketahanan Pangan](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/TrenIKP.png)
Ketahanan pangan Indonesia mengalami tren penurunan selama 4 tahun terkahir. Hal ini memerlukan evaluasi lebih lanjut
terhadap faktor ekonomi, sosial, lingkungan, dan kebijakan pemerintah, terutama dampak covid-19 yang terjadi.

---
# :man_shrugging: GOALS
- Forecasting,
  Memberikan wawasan starategis bagi pengembang kebijakan yang mendukung keberlanjutan ketahanan pangan nasional.
- Clustering,
  Mengidentifikasi kelompok wilayah agar kebijakan lebih spesifik, efektif, dan sesuai kebutuhan.
- Strategic Policy,
  Memastikan ketahanan pangan yang stabil dan berkelanjutan, dengan memastikan ketersediaan, keterjangkauan, dan pemanfaatan
  pangan yang merata bagi seluruh lapisan masyarakat.

---

# :bar_chart: DATA SET
Dataset utama diambil dari *real dataset* yang bersumber pada https://data-explorer.oecd.org/ dan juga bersumber dari https://fsva.badanpangan.go.id/ .

---

# :chart_with_upwards_trend: DASHBOARD
https://public.tableau.com/app/profile/team.bravo/viz/FinalProject_TeamB-RAVO/Dashboard4?publish=yes .

---

# :file_folder: DATA DICTIONARY
*FORECASTING* & *CLUSTERING*
- AFFORDABILITY: Indeks keterjangkauan pangan, mencerminkan kemampuan masyarakat dalam membeli pangan.
- AVAILABILITY: Indeks ketersediaan pangan, menunjukkan seberapa tersedia pangan di suatu daerah.
- QUALITY AND SAFETY: Indeks kualitas dan keamanan pangan, mengukur mutu serta keamanan pangan yang dikonsumsi.
- SUSTAINABILITY AND ADAPTATION: Indeks keberlanjutan dan adaptasi, menunjukkan keberlanjutan sistem pangan terhadap perubahan lingkungan atau iklim.

---

# :hourglass: EXPLORATORY DATA ANALYSIS (EDA) FORECASTING
Pada tahap ini kami melakukan beberapa tahap yaitu:
- Transformasi Data Karena Time Series membutuhkan kolom tanggal yang proper (berformat YYYY-MM-DD) maka perlu dipastikan apakah kolom tanggal pada data sudah sesuai dengan format tanggal universal. Jika belum maka ubah format tanggal tersebut.
- Plot TimeSeries adalah alat yang sangat berguna untuk analisis data. Biasanya dengan line chart. Dengan memberikan visualisasi yang jelas, akan memungkinkan pengamat untuk mengambil wawasan yang signifikan dari data yang disajikan, yang dapat digunakan untuk pengambilan keputusan yang lebih baik.
![Plot Time Series](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/PlotTS.png)
![Plot Time Series](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/PlotTS1.png)
![Plot Time Series](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/PlotTS2.png)
![Plot Time Series](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/PlotTS3.png)
![Plot Time Series](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/PlotTS4.png)
- Dekomposisi adalah proses statistik yang memecah data time series menjadi komponen-komponen individual.
  
  ![Dekomposisi](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Dekomposi1.jpg)
  ![Dekomposisi](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Dekomposi2.jpg)
  ![Dekomposisi](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Dekomposi3.jpg)
  ![Dekomposisi](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Dekomposi4.jpg)
- Statistik Deskriptif

  ![Statistik Deskriptif](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/StatistikDeskriptif.jpg)
- Korelasi

  ![Korelasi](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Korelasi_TimeSeries.png)

---

# :heavy_check_mark: IMPLEMENTASI MODEL -> MULTIVARIATE TIME SERIES (Dynamic Faktor)
Dynamic factor itu salah satu algoritma multivariate time series yang berguna untuk mengidentifikasi struktur yang mendasari dalam data time series yang kompleks, terutama ketika ada banyak variabel yang saling terkait.
Pada tahap implementasi model ada beberapa tahap yaitu :
- Mengatur Index 'Date'
- Proporsi Train Tes
- Split Data
- Menacari Parameter terbaik menggunakan MAE(*Mean Absolute Error*) dan mendapatkan hasil sebesar 3.8621
---
# Hasil *FORECASTING* :chart_with_downwards_trend:
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Hasil_prediksi.png)
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/forecase1.png)
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/forecase2.png)
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/forecase3.png)
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Hasilpred_FSI.png)

---
---

# :hourglass: EXPLORATORY DATA ANALYSIS (EDA) CLUSTERING
Pada tahap ini kami melakukan beberapa tahap yaitu:
- Identifikasi Missing Value untuk mengecek apakah terdapat nilai kosong
- Identifikasi Duplikasi Data untuk mengecek apakah terdapat data yang duplikat
- Identifkasi Outlier untuk menghindari kesalahan analisis, memahami pola data, mendeteksi kesalahan pengukuran, meningkatkan kualitas model
- Normalisasi Data Menggunakan MinMax Scaler Normalisasi data ini membantu memudahkan analisis perbandingan antarprovinsi dalam rentang yang sama, sehingga dapat digunakan untuk pengelompokan atau rekomendasi kebijakan berdasarkan indikator ketahanan pangan.

# :heavy_check_mark: IMPLEMENTASI MODEL -> CLUSTERING (K-MEANS)
- Mencari jumlah cluster terbaik menggunakan *Silhouette Score*
  ![Silhoutte](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Sillhoette_K-Means.png)
  dan mendapatkan jumlah cluster terbaik yaitu 4 dengan nilai *Sillhouette Score* **0.3791**
---
# Hasil *CLUSTERING* :bar_chart:
  ![K-Means](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/3D_K-Means.png)
  ![K-Means](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/HasilCLuster.png)

---

# :pushpin: RECOMENDATION

*FORECASTING*

---
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/forecase2.png)
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/forecase3.png)
![Forecasting](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/Hasilpred_FSI.png)
Penurunan trend IKP diprediksi terjadi ditahun 2028, hal ini didukung oleh trend penurunan pemanfaatan (Quality & Safety) dan juga keberlanjutan (Sustainability). Pemerintah perlu mengambil langkah strategis yaitu:
- Smart Farming
- Pertanian Akuaponik
- Pertanian Hidroponik

dari beberapa langkah strategis tersebut, tidak lupa tetap memperhatikan lingkungan, kebersihan air, dan keanekaragaman hayati.

---

*CLUSTERING*

---
![K-Means](https://raw.githubusercontent.com/MTOZZ/Indeks-Ketahanan-Pangan/main/Image/HasilCLuster.png)
Cluster 1(Ungu)
- Perbaikan distribusi pangan
- Kebijakan harga dan daya beli
- Edukasi tentang gizi dan pola makan sehat

Cluster 2(Biru)
- Diservekasi sumber pangan
- Perbaikan ketahana pasokan pangan
- Edukasi keberlanjutan tentang pengelolaan pangan
- Peningkatan kapasitas produksi pangan lokal

Cluster 3(Hijau)
- Mempertahankan keberagaman sumber pangan
- Peningkatan kapasitas pertanian dan distribusi
- Edukasi dan promosi pola makan sehat
- Inovasi dalam pengolahan pangan

Cluster 4(Kuning)
- Subsidi pangan
- Perbaikan distribusi pangan
- Diversifikasi sumber pangan
- Membangun infrastruktur pertanian
- Eudkasi gisi dan pola makan sehat
- Pengembangan layanan kesehatan

pemerintah perlu mengambil langkah strategis yaitu:
- Diservikasi pangan
- Teknologi pertanian modern
- Kolaborasi lintas sektor
- Lumbung padi Sukabumi
- Food Estate
---
# :clap: KESIMPULAN
Prediksi nilai IKP Indonesia pada tahun 2024-2028 menunjukkan tren kenaikan, sedangkan pada tahun 2028-2030 diprediksi mengalami penurunan. Melalui sinergi antara kebijakan pangan dan ekonomi hijau di Indonesia dapat mendukung ketahanan pangan yang berkelanjutan. Regulasi pemerintah dan partisipasi masyarakat juga sangat diperlukan untuk memastikan keberhasilan implementasi yang efektif. 
