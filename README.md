# Airline Customer Value Analysis Case with K-Means Clustering  
Kelompok 7:  
1. Tirto Fadhlan
2. Ferry Chando 
3. Yosabad Torando
4. Calvin Aziszam
5. Inggo Landa 
6. Joni Syofian 
7. Nur Fatin M 
8. Dwi Chandra

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

## Hasil yang diperoleh
Dari Elbow method diperoleh bahwa cluster yang optimal ada 5 yang kemudian divalidasi dengan Silhouette Score  
### Elbow Method
![ELBOW](https://user-images.githubusercontent.com/78085127/200121096-c5b531d3-e521-496f-9a45-c29811cf6b78.png)
### Silhouette Score
![SILHOUTE](https://user-images.githubusercontent.com/78085127/200121138-a157e414-6cd9-48a9-bc32-1a4241467cb1.png)

### Visualisasi dengan PCA menggunakan Scatterplot
![PCA](https://user-images.githubusercontent.com/78085127/200120890-f0a55890-4a73-4872-9e83-6e3886d4d85c.png)
Diperoleh jumlah customer dan persentasenya untuk masing-masing cluster yang menunjukkan bahwa persebaran customer cukup merata:
* cluster 1	sebanyak 12500 customer (22.64%)
*	cluster 2	sebanyak 11452 customer (20.74%)
*	cluster 3	sebanyak 11400 customer (20.65%)
*	cluster 0	sebanyak 10198 customer (18.47%)
*	cluster 4	sebanyak 9669	 customer (17.51%)  
![BARPLOT](https://user-images.githubusercontent.com/78085127/200120923-23165f74-fd0f-4fa6-8c96-c9e9c4c1f752.png)
### Deskripsi Cluster
##### Cluster 0
Cluster 0 merupakan customer lama dimana rata-rata nilai Loyalti yang besar. Customer rata-rata melakukan penerbangan ulang dalam kategori begitu juga dengan frekuensi penerbangan serta monetarynya. Namun, Customer ini merupakan customer yang bisa disebut customer yang rata-rata sedikit mendapatkan diskon dari maskapai  
##### Cluster 1
Cluster 1 merupakan customer menengah yang ditunjukan nilai L berada di tengah-tengah cluster yag lainnya. Customer ini melakukan penerbangan dari penerbangan sebelumnya memiliki jarak waktu yang lama. Kemudian, customer ini merupakan customer yang paling sedikit melakukan perjalanan dan perjalananya pun yang paling dekat dibandingkan dengan cluster yang lainnya. Namun, cluster ini merupakan customer yang mendapatkan rata-rata diskon yang paling besar dibandingkan cluster yang lainnya  
##### Cluster 2
Cluster 2 merupakan customer baru dalam penerbangan. Rata-rata customer pada cluster ini melakukan penerbangan setelah penerbangan terakhir memiliki jarak waktu yang cukup lama. Kemudian, customer ini merupakan customer yang paling sedikit melakukan perjalanan dan **perjalananya** pun yang paling dekat setelah customer cluster 1. Selain itu, customer pada cluster ini rata-rata mendapatkan diskon yang paling sedikit dibandingkan cluster yang lainnya.
##### Cluster 3
Cluster 3 merupakan customer yang paling baru yang ditandai dengan nilai L yang kecil. Customer pada cluster ini termasuk customer yang melakukan penerbangan selanjutnya dari penerbangan terakhir dengan jarak yang cukup dekat. Selain itu, customer ini juga merupakan customer dengan jumlah penerbangan yang cukup banyak dan dalam jarak yang cukup jauh. Dalam segi diskon, customer pada cluster ini mendapatakn diskon yang menengah.
##### Cluster 4
Cluster 4 merupakan customer yang terbilang customer lama. Customer ini melakukan perjalanan dari perjalanan terakhir dalam waktu yang paling dekat dibandingkan cluster yang lainnya. Selain itu cluster ini merupakan cluster dengan rata-rata melakukan perjalanan yang lebih sering dan melakukan perjalana yang paling jauh dibandingkan cluster lainnya. Serta dalam diskon, cluster ini terbilang mendapatkan diskon yang cukup besar.  

### Rekomendasi Strategi Bisnis
##### Cluster 0
Sebagaimana yang diketahui bahwa cluster ini merupakan customer yang paling loyal namun tidak begitu sering melakukan perjalanan sehingga perlu dilakukan pendekatan lebih agar customer tidak menghilang seperti pengiriman pesan kepada customer pada cluster ini serta memeberikan diskon/promo sebagaimana yang diketahui bahwa cluster ini termasuk cluster yang mendapatkan sedikit diskon.  
##### Cluster 1
Pendekatan pada cluster 1 ini harus lebih agresif tidak hanya cukup memberikan diskon. seperti yang diketahui bahwa cluster ini merupakan cluster yang paling besar mendapatkan diskon akan tetapi sedikit melakukan perjalanan dan perjalannya pun dalam jarak yang dekat. Sehingga pada cluster perlu diberikan program khusus.  
##### Cluster 2  
Cluster 2 ini merupakan cluster yang hampir sama dengan cluster 1. Hanya saja cluster 2 ini merupakan cluster yang paling sedikit mendapatkan diskon sehingga dapat dilakukan pendekatan pada cluster ini dengan memberikan diskon/promo tertentu.   
##### Cluster 3
Cluster ini merupakan customer yang baru namun melakukan penerbangan dalam waktu yang berdekatan dan juga sering melakukan perjalanan. Cluster ini merupakan cluster yang potensial sehingga potensi ini harus dipertahankan/ditingkatkan. Karena merupakan customer baru, dapat dilakukan diberikan berbagai layanan tertentu agar nyaman melakukan penerbangan dengan maskapai ini.  
##### Cluster 4
Cluster ini merupakan cluster dengan customer yang merupakan customer lama. Selain itu, cluster ini merupakan cluster yang sangat potensial bagi maskapai karean sering melakukan perjalanan dan juga dalam jarak jauh. Sehingga cluster ini perlu dipertahakan sehingga hal yang bisa dilakukan untuk cluster ini adalah seperti pemberian harga khusus karena sudah loyal pada maskapai ini dan layanan yang lainnya yang membuat customer pada cluster 4 ini merasa lebih nyaman dan betah.  

