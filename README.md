# Health Insurance Cross Sell Prediction 
Salah satu perusahaan asuransi yang berfokus ke penjualan 'Asuransi Kesehatan' ingin melakukan *cross-selling* produk 'Asuransi Kendaraan'. Perusahaan berharap dapat memprediksi apakah minat atau tidak pelanggan dari data-data pemegang polis 'Asuransi Kesehatan' yang sudah ada untuk itu dibutuhkan model yang dapat membantu proses tersebut.

# Exploratory Data Analysis

EDA (Exploratory Data Analysis), dalam proses ini akan dilakuakn 4 tahap yakni melihat deskripsi statistik, analisis *univariate*, analisis *multivariate*, dan mengekstraksi business insight. Proses ini sangatlah penting sebelum membangun *Machine Learning*. Untuk memahami karakteristik data, dan hal-hal yang perlu
kita lakukan agar data tersebut dapat digunakan dilakukan proses EDA. 
 1. Univariate Analysis
Subplot
![subplot](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/Untitled.png)
Hasil Observasi =<br>
* Age : Distribusi data tidak normal. Umur pelanggan bervarian dari 20 tahun hingga 85 tahun, dengan kebanyakan pelanggan berusia antara 24 - 49 tahun.<br>
* Driving_License : Merupakan boolean. Data tidak terdistribusi dengan normal. Kebanyakan pelanggan terkategori 1 (Memiliki izin mengemudi).<br>
* Region_Code : Distribusi data normal. Dengan median di kode wilayah 28.<br>
* Previously_Insured : Merupakan boolean. Data terdistribusi dengan rata antara 1 dan 0.<br>
* Annual_Premium : Data terdistribusi normal, dengan kebanyakan annual premium sekitar 0 - 50000 (dibawah 100000), Terdapat banyak outliers yang nominalnya hingga diatas 400000.<br>
* Policy_Sales_Channel : Distribusi data tidak normal dengan nilai tengah berada di nilai ± 130.<br>
* Vintage : Distribusi data normal, dengan median di nilai ± 151.<br>
* Response : Merupakan boolean. Data tidak terdistribusi dengan normal. Kebanyakan pelanggan terkategori 0 (Tidak berminat) <br>
 2. Multivariate Analysis
Heatmap
![heatmap](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/heatmap.png)
Hasil Observasi =<br>
* Age - Response<br>
Berkolerasi positif yang sangat rendah. Semakin tua umur semakin berminat terhadap ‘Asuransi Kendaraan’.
* Region_Code - Response<br>
Positif namun hampir tidak memiliki kolerasi.
* Driving_License - Response<br>
Positif namun hampir tidak memiliki kolerasi.
* Annual_Premium - Response<br>
Positif namun hampir tidak memiliki kolerasi.
* Policy_Sales_Channel - Response<br>
Berkolerasi negatif yang sangat rendah. Semakin rendah code channel sales semakin tinggi minat terhadap ‘Asuransi Kendaraan’.
* Vintage - Response<br>
Tidak memiliki korelasi.
* Previously_Insured - Response<br>
Berkolerasi negatif. Jika pelanggan belum memiliki ‘Asuransi Kendaraan pelanggan cenderung berminat terhadap ‘Asuransi Kendaraan’. Pelanggan yang tergolong berumur cenderung tidak memiliki asuransi kendaraan sebelumnya.
* Age - Policy_Sales_Channel<br>
Korelasi negative. Kode media mengontak orang yang cenderung tua menggunakan kode media yang berada di kode kecil.

Pairplot
![pairplot](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/pairplot.png)
Hasil Observasi =
* Orang-orang yang sebelumnya belum pernah menggunakan asuransi kendaraan di umur 35 sampai 45 dan juga di umur 60 sampai 65 cenderung menjawab response 1.
* Orang-orang yang mempunyai driving license di umur 35 sampai 45 dan juga di umur 60 sampai 65 cenderung menjawab response 1.

 3.   Business Insight
* Distribution of Customer Age and Vehicle Insurance Interest
![age vs interest](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/BI%20Age%20vs%20insurance.png) <br>
Dilihat dari grafik diatas didapatkan insight bahwa pelanggan asuransi kesehatan paling banyak adalah usia antara 20 sampai 30 tahun, sedangkan peminat Asuransi kendaraan terbanyak rata-rata di usia 40 sampai 50 tahun.

* response vs usia kendaraan
![response vs kendaraan usia](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/BI%20usia%20kendaraan%20vs%20respon.png) <br>
Berdasarkan dari umur kendaraan pelanggan, mayoritas pelanggan memiliki kendaraan yang berumur 1-2 tahun sebanyak 200.316 pelanggan, diikuti dengan kendaraan <1 tahun sebanyak 164.786 pelanggan, dan kendaraan >2 tahun sebanyak 16.007 pelanggan. <br>
Dapat dilihat berdasarkan rasio pelanggan yang memiliki kendaraan 1-2 tahun lebih banyak tertarik terhadap Asuransi Kendaraan dibandingkan pelanggan lain.


* response vs vintage
![response vs vintage](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/vintage%20vs%20response.png) <br>
Dari grafik diatas, pelanggan yang bergabung dengan rentan waktu 5-8 bulan memiliki ketertarikan terhadap produk ‘Asuransi Kendaraan’ yang cukup banyak sekitar 19281 pelanggan dibandingkan pelanggan yang bergabung dengan rentan waktu lebih dari 9 bulan (lebih lama bergabung) sekitar 9391 pelanggan Akan tetapi berdasarkan rasio persentase masing-masing vintage masih sangat kecil hanya 12% setiap vintage.


* response vs gender
![response vs gender](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/respon%20vs%20gender.png) <br>
Berdasarkan dari data, mayoritas pelanggan merupakan berjenis kelamin laki-laki sebesar 206.089 (54,08%) orang dari total 381.109 orang, sedangkan 175.020 (45.92%) adalah perempuan.<br>
Berdasarkan gender ketertarikan terhadap produk ‘Asuransi Kendaraan’ kebanyakan laki-laki 28.525 (13,84% respon menunjukan ketertarikan) sedangkan, perempuan 18.185 (10.39% respon menunjukan ketertarikan). Lebih banyak laki-laki tertarik terhadap ‘Asuransi Kendaraan’.

** Proses ini dapat membantu mendeteksi kesalahan dalam data, medeteksi data yang perlu di *handling*, melihat korelasi dan pola data, serta menemukan wawasan penting dalam data. Sehingga ketika memasukki proses pembuatan *Machine Learning* lebih efisien dan lebih tepat sasaran (akurat). **
