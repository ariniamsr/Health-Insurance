# Health Insurance
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
![age vs interest](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/BI%20Age%20vs%20insurance.png)
Dilihat dari grafik diatas didapatkan insight bahwa pelanggan asuransi kesehatan paling banyak adalah usia antara 20 sampai 30 tahun, sedangkan peminat Asuransi kendaraan terbanyak rata-rata di usia 40 sampai 50 tahun.





 4.   
 5. 
 6. 

Proses ini dapat membantu mendeteksi kesalahan dalam data, medeteksi data yang perlu di *handling*, melihat korelasi dan pola data, serta menemukan wawasan penting dalam data. Sehingga ketika memasukki proses pembuatan *Machine Learning* lebih efisien dan lebih tepat sasaran (akurat).
