# Airline Customer Value Analysis Case with K-Means Clustering  
Deskripsi dataset:  
> Dataset ini berisi data customer sebuah perusahaan penerbangan dan beberapa fitur yang dapat menggambarkan value dari customer tersebut. Setiap baris mewakili customer, setiap kolom berisi atribut customer.

| Code         | Deskripsi |
|:--------------|:-----|
|MEMBER_NO-b   | : ID Member|
|FFP_DATE    |: Frequent Flyer Program Join Date|
|FIRST_FLIGHT_DATE  |: Tanggal Penerbangan pertama|
|GENDER  |: Jenis Kelamin|
|FFP_TIER | : Tier dari Frequent Flyer Program|
|WORK_CITY | : Kota Asal|
|WORK_PROVINCE | : Provinsi Asal|
|WORK_COUNTRY | : Negara Asal|
|AGE | : Umur Customer|
|LOAD_TIME | : Tanggal data diambil|
|FLIGHT_COUNT | : Jumlah penerbangan Customer|
|BP_SUM | : Rencana Perjalanan|
|SUM_YR_1 | : Fare Revenue|
|SUM_YR_2 | : Votes Prices|
|SEG_KM_SUM | : Total jarak(km) penerbangan yg sudah dilakukan|
|LAST_FLIGHT_DATE | : Tanggal penerbangan terakhir|
|LAST_TO_END | : Jarak waktu penerbangan terakhir ke pesanan penerbangan paling akhir|
|AVG_INTERVAL | : Rata-rata jarak waktu|
|MAX_INTERVAL | : Maksimal jarak waktu|
|EXCHANGE_COUNT | : Jumlah penukaran|
|avg_discount | : Rata rata discount yang didapat customer|
|Points_Sum | : Jumlah poin yang didapat customer |
|Point_NotFlight | : point yang tidak digunakan oleh members |    

Dalam Projek kali ini dilakukan bebera langkah pengerjaan sebagai berikut:   
* **Data Collection**
* **Exploratory Data Analysis (EDA)** yang mencakup Data understanding (tipe data, missing value, dan data duplicate), statistika deskriptif, Univariate Analysis dan Multivariate Analysis
* **Data Preprocessing** yang mencakup pemilihan feature-feature untuk clustering yang sesuai dengan bisnis
* **Clustering K-means** untuk menemukan jumlah cluster yang optimal dan evaluasi cluster yang dihasilkan dengan visualisasi dan silhouette score
* **Interpretasi cluster** yang dihasilkan secara bisnis dan rekomendasi yang sesuai dengan cluster yang dihasilkan  



