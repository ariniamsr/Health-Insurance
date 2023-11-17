# Health Insurance
Salah satu perusahaan asuransi yang berfokus ke penjualan 'Asuransi Kesehatan' ingin melakukan *cross-selling* produk 'Asuransi Kendaraan'. Perusahaan berharap dapat memprediksi apakah minat atau tidak pelanggan dari data-data pemegang polis 'Asuransi Kesehatan' yang sudah ada untuk itu dibutuhkan model yang dapat membantu proses tersebut.

# Exploratory Data Analysis

EDA (Exploratory Data Analysis), dalam proses ini akan dilakuakn 4 tahap yakni melihat deskripsi statistik, analisis *univariate*, analisis *multivariate*, dan mengekstraksi business insight. Proses ini sangatlah penting sebelum membangun *Machine Learning*. Untuk memahami karakteristik data, dan hal-hal yang perlu
kita lakukan agar data tersebut dapat digunakan dilakukan proses EDA. 
 1. Univariate Analysis
![subplot](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/Untitled.png)
Hasil Observasi =
-Age : Distribusi data tidak normal. Umur pelanggan bervarian dari 20 tahun hingga 85 tahun, dengan kebanyakan pelanggan berusia antara 24 - 49 tahun.
-Driving_License : Merupakan boolean. Data tidak terdistribusi dengan normal. Kebanyakan pelanggan terkategori 1 (Memiliki izin mengemudi).
-Region_Code : Distribusi data normal. Dengan median di kode wilayah 28.
-Previously_Insured : Merupakan boolean. Data terdistribusi dengan rata antara 1 dan 0.
-Annual_Premium : Data terdistribusi normal, dengan kebanyakan annual premium sekitar 0 - 50000 (dibawah 100000), Terdapat banyak outliers yang nominalnya hingga diatas 400000.
-Policy_Sales_Channel : Distribusi data tidak normal dengan nilai tengah berada di nilai ± 130.
-Vintage : Distribusi data normal, dengan median di nilai ± 151.
-Response : Merupakan boolean. Data tidak terdistribusi dengan normal. Kebanyakan pelanggan terkategori 0 (Tidak berminat)
 2. Multivariate Analysis
![heatmap](https://github.com/ariniamsr/Health-Insurance/blob/main/Pict/heatmap.png)
Hasil Observasi =
* Age - Response
Berkolerasi positif yang sangat rendah. Semakin tua umur semakin berminat terhadap ‘Asuransi Kendaraan’.
*Region_Code - Response
Positif namun hampir tidak memiliki kolerasi.
*Driving_License - Response
Positif namun hampir tidak memiliki kolerasi.
*Annual_Premium - Response
Positif namun hampir tidak memiliki kolerasi.
*Policy_Sales_Channel - Response
Berkolerasi negatif yang sangat rendah. Semakin rendah code channel sales semakin tinggi minat terhadap ‘Asuransi Kendaraan’.
*Vintage - Response
Tidak memiliki korelasi.
*Previously_Insured - Response
Berkolerasi negatif. Jika pelanggan belum memiliki ‘Asuransi Kendaraan pelanggan cenderung berminat terhadap ‘Asuransi Kendaraan’. Pelanggan yang tergolong berumur cenderung tidak memiliki asuransi kendaraan sebelumnya.
*Age - Policy_Sales_Channel
Korelasi negative. Kode media mengontak orang yang cenderung tua menggunakan kode media yang berada di kode kecil.


 3.   
 4. 
 5. 

Proses ini dapat membantu mendeteksi kesalahan dalam data, medeteksi data yang perlu di *handling*, melihat korelasi dan pola data, serta menemukan wawasan penting dalam data. Sehingga ketika memasukki proses pembuatan *Machine Learning* lebih efisien dan lebih tepat sasaran (akurat).
