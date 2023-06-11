# Mini Project 2 - Meninjau Bisnis Hotel Menggunakan Data Visualization 
Sebagai anggota dari tim Data Scientist di sebuah perusahaan hotel,  mempunyai tanggung jawab untuk memberikan insight-insight yang berhubungan dengan performa bisnis hotel. Insight tersebut dicari dengan melakukan eksplorasi data, seperti menganalisis bagaimana perilaku para pelanggan dalam memesan tiket hotel atau mencari faktor-faktor yang mempengaruhi pembatalan pemesanan tiket hotel. Kemudian menyajikan insight-insight tersebut menggunakan data visuzalization dan data storytelling.

## Ringkasan 
Sangat penting bagi suatu perusahaan untuk selalu menganalisa performa bisnisnya. Dalam bisnis di bidang perhotelan ini. Fokus yang akan dituju adalah untuk mengetahui bagaimana perilaku pelanggan dalam melakukan pemesanan hotel, dan hubungannya terhadap tingkat pembatalan pemesanan hotel. Hasil dari insight yang telah ditemukan akan disajikan dalam bentuk data visualisasi agar lebih mudah dipahami dan bersifat lebih persuasif.

### 1. Data Preprocessing 
![image](https://github.com/hadasadida/Mini-Project-2_Investigate-Hotel-Business-using-Data-Visualization/assets/124650679/0ff88d27-88a7-4d2d-85f3-a3744fd0f195)

a) Dataset memiliki 29 kolom dan 119390 baris.  

b) Mengatasi data null 
- Terdapat kolom yang ada data null = city,  agent, company.
- Untuk kolom city diisi dengan modus.
- Untuk kolom agent diisi dengan median.
- Sedangkan untuk kolom company didrop karena value yang kosong terlalu banyak.

c) Mengganti value yang tidak sesuai
- Pada kolom meal terdapat 5 unique values yaitu Breakfast, Dinner, No meal dan Full Board. 
- Untuk value Full Board diganti dengan Breakfast + Dinner agar lebih jelas.
- Membuat kolom baru “arrival_date” dengan menggabungkan kolom “arrival_date_year” dan “arrival_date_month”.
- Membuat kolom baru “total_guest” dengan menggabungkan kolom “adult”,  “children” dan “babies”.

d) Membuang data yang tidak diperlukan
- Pada kolom reservation_status terdapat 3 unique values yaitu Check-Out, Canceled, No-Show. 
- Untuk value No-Show dihapus karena value No-Show merupakan customer yang melakukan reservasi namun tidak check in dan tidak mengcancel sampai batas waktu deadline cancel reservasi.

### 2. Analisis Pemesanan Hotel Bulanan Berdasarkan Jenis Hotel
Dalam melakukan analisa perilaku pelanggan dapat dilakukan dengan mengidentifikasi tipe hotel apa yang paling banyak diminati oleh pelanggan, dan kita juga dapat mengaitkannya dengan kondisi musim ketika hotel tersebut dipesan. 

Berikut merupakan plot Jumlah Pemesanan Hotel Setiap Bulan Berdasarkan Jenis Hotel.
![image](https://github.com/hadasadida/Mini-Project-2_Investigate-Hotel-Business-using-Data-Visualization/assets/124650679/d02d9589-9b45-4122-9e7e-ae461983b5e4)

- Pada periode bulan Februari – September 2017, pada City hotel mengalami penurunan sedangkan pada Resort hotel mengalami kenaikan.
- Pada bulan Maret tahun 2018, baik City hotel maupun Resort hotel mengalami penurunan drastis jumlah pemesanan. 
- Pada bulan Agustus 2018 – November 2018, baik City hotel maupun Resort hotel mengalami kenaikan hal ini kemungkinan dikarenakan adanya event besar.
- Jumlah pemesanan paling tinggi pada City hotel terjadi pada bulan Juli 2019.

### 3. Analisis Dampak Durasi Menginap terhadap Tarif Pembatalan Pemesanan Hotel
Pelanggan yang banyak membatalkan pemesanan akan berpengaruh buruk terhadap performa bisnis hotel. Oleh karena itu, hal-hal yang mempengaruhi pembatalan pemesanan sangat penting untuk diketahui. Pada tahap ini kamu akan meninjau bagaimana durasi menginap dapat  mempengaruhi tingkat pembatalan pemesanan hotel.

Berikut merupakan plot Rasio Pembatalan Pesanan Terhadap Durasi Menginap Untuk Setiap Tipe Hotel.
![image](https://github.com/hadasadida/Mini-Project-2_Investigate-Hotel-Business-using-Data-Visualization/assets/124650679/029ee80e-ba34-432d-ba8c-cf73e507800a)

- Pada City hotel dengan durasi menginap 2 malam, memiliki jumlah pembatalan pemesanan tertinggi.
- Pada Resort hotel dengan durasi menginap 7 malam, memiliki jumlah pembatalan pemesanan tertinggi.
- Baik pada City hotel maupun pada Resort hotel semakin lama durasi menginap, jumlah pembatalan pemesanan mengalami penurunan.

### 4. Analisis Dampak Lead Time terhadap Tingkat Pembatalan Pemesanan Hotel
Dalam sistem pemesanan kamar hotel, biasanya pihak hotel memperbolehkan untuk memesan sebelum hari kedatangan. Jarak waktu yang terjadi bisa dalam beberapa hari maupun dalam beberapa bulan sebelum hari kedatangan. Pada tahap ini akan mengecek apakah jarak waktu antara
pemesanan hotel dengan hari kedatangan pelanggan memiliki pengaruh terhadap tingkat pembatalan pemesanan hotel. 

Berikut merupakan plot Rasio Pembatalan Pesanan Terhadap Jarak Waktu Pemesanan Untuk Setiap Tipe Hotel.
![image](https://github.com/hadasadida/Mini-Project-2_Investigate-Hotel-Business-using-Data-Visualization/assets/124650679/2aeacd40-af28-4616-9ea4-e5823a3669c1)

- Pada jarak waktu pemesanan 1 minggu dan 1 bulan, baik pada City Hotel maupun Resort Hotel mengalami penurunan jumlah pembatalan pesanan paling signifikan.
- Pada jarak waktu pemesanan 2 bulan – 10 bulan baik City Hotel maupun Resort Hotel mengalami penurunan jumlah pembatalan pesanan. Namun dari jarak waktu pemesanan 5 bulan ke 6 bulan pada City Hotel sempat mengalami kenaikan jumlah pembatalan pesanan namun tidak terlalu signifikan. 
- Pada jarak waktu pemesanan 1 tahun baik City Hotel maupun Resort Hotel mengalami kenaikan jumlah pembatalan pesanan. Namun mengalami penurunan Kembali pada jarak waktu pemesanan 2 tahun. 










