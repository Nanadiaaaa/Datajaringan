# Mengolah Data Jaringan Menggunakan Xgboost

## Deskripsi
Proyek ini bertujuan untuk menganalisis pola koneksi TCP antara Sumber (Source) dan Destinasi (Destination) dengan fokus pada koneksi yang memiliki Label 0 (tidak ada TCP Dup ACK) dan Label 1 (TCP Dup ACK). Analisis ini akan difokuskan pada perbedaan karakteristik waktu (Time), panjang koneksi (Length), dan informasi terkait (Info) antara koneksi dengan Label 0 dan Label 1.  Analisis ini dilakukan dengan memanfaatkan berbagai pustaka dan alat, di antaranya:
* Pandas: Digunakan untuk manipulasi dan analisis data tabular, seperti data dalam bentuk spreadsheet.
* NetworkX: Digunakan untuk analisis jaringan dan graf. Berguna untuk memodelkan dan menganalisis jaringan atau graf yang terdiri dari simpul-simpul (nodes) dan tepi-tepi (edges).
* Matplotlib: Digunakan untuk membuat visualisasi seperti grafik, plot, dan grafik lainnya. Dengan 'plt', Anda dapat membuat plot yang akan digunakan untuk menampilkan data secara visual.
* Seaborn: Digunakan untuk membuat visualisasi data yang lebih menarik dan informatif dengan mudah. Seaborn adalah alat yang digunakan bersama dengan Matplotlib untuk visualisasi data.
* Xgboost: Pustaka yang digunakan untuk pemodelan dan analisis data, terutama untuk tugas klasifikasi dan regresi.
* Scikit-learn: Digunakan untuk fungsi-fungsi pemodelan seperti train_test_split, evaluasi model, dan preprocessing.

## Langkah-langkah Pengolahan Data
### 1. Mengimpor Library dan Membaca Data
* Menggunakan Pandas untuk membaca data dari Google Drive.
* Data diambil dari berkas CSV (Comma-Separated Values).

### 2. Preprocessing Data
* Menampilkan informasi tentang DataFrame, termasuk jumlah baris dan kolom, tipe data kolom, dan nilai yang hilang.
* Menangani nilai-nilai yang hilang dan mendeteksi duplikasi.
* Menampilkan data yang difilter berdasarkan protokol dan alamat IP tujuan tertentu.

### 3. Visualisasi Data
* Membuat visualisasi berupa bar plot untuk menunjukkan frekuensi masing-masing nilai dalam kolom 'Protocol'.

### 4. Identifikasi TCP Dup ACK
* Melakukan grouping data berdasarkan kriteria tertentu (TCP Dup ACK).
* Menambahkan kolom 'Label' berdasarkan hasil pencarian string "TCP Dup ACK" dalam kolom 'Info'.
* Visualisasi jumlah koneksi dengan TCP Dup ACK menggunakan histogram dan bar plot.

### 5. Modeling Menggunakan XGBoost untuk membangun model klasifikasi.
