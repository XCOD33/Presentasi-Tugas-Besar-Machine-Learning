---
# try also 'default' to start simple
theme: apple-basic
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# https://sli.dev/custom/highlighters.html
highlighter: shiki
transition: slide-left
layout: intro
colorSchema: 'dark'
defaults:
  layout: 'center'
---
# Home Credit Indonesia Default Risk
Evaluasi Kelayakan Kredit Applicant
---
layout: center
transition: slide-left
---
<h2>Anggota Kelompok</h2>
<div class="mt-6 grid grid-cols-3 gap-4">
  <div class="col-span-1">
    <div class="bg-white shadow-lg rounded-lg p-4">
      <img src="/rico.jpg" alt="Foto Profil" class="w-32 h-32 rounded-full mx-auto mb-4">
      <h2 class="text-xl font-semibold text-gray-800 text-center">M. Rico Aditya P.</h2>
      <p class="text-gray-800 text-center text-sm m-0 p-0">5210411055</p>
    </div>
  </div>
  <div class="col-span-1">
    <div class="bg-white shadow-lg rounded-lg p-4">
      <img src="/nunuk.jpg" alt="Foto Profil" class="w-32 h-32 rounded-full mx-auto mb-4">
      <h2 class="text-xl font-semibold text-gray-800 text-center">Nugrahman Reski P.</h2>
      <p class="text-gray-800 text-center text-sm m-0 p-0">5210411095</p>
    </div>
  </div>
  <div class="col-span-1">
    <div class="bg-white shadow-lg rounded-lg p-4">
      <img src="/ivan.jpg" alt="Foto Profil" class="w-32 h-32 rounded-full mx-auto mb-4">
      <h2 class="text-xl font-semibold text-gray-800 text-center">Ivan Bhagaskara K.</h2>
      <p class="text-gray-800 text-center text-sm m-0 p-0">5210411100</p>
    </div>
  </div>
</div>
---
layout: quote
---
# "Machine learning provides opportunities for financial institutions to enhance the efficiency of credit evaluation processes, gain deeper insights into customer behavior, and optimize their loan portfolios."
Ronald Van Loon
---
layout: intro-image-right
image: '/ml.jpg'
transition: slide-left
---
# Latar Belakang
---
transition: slide-left
css: windicss
---
# Latar Belakang
Analisis ini bertujuan untuk mengidentifikasi faktor-faktor yang mempengaruhi keputusan pemberian pinjaman dan membangun model machine learning untuk memprediksi persetujuan atau penolakan aplikasi pinjaman. 

Dataset "Home Credit Indonesia Default" berisi informasi aplikasi pinjaman kredit yang diajukan oleh individu kepada lembaga keuangan. Home Credit Indonesia adalah perusahaan pembiayaan yang melakukan evaluasi kredit terhadap pelamar untuk menentukan kelayakan mereka menerima kredit. Risiko default, yaitu ketidakmampuan pelanggan membayar kredit, merupakan perhatian utama perusahaan tersebut. 

Oleh karena itu, analisis dan prediksi yang akurat terhadap risiko default dapat membantu mengurangi risiko keuangan perusahaan. Dalam konteks ini, teknik machine learning dan data mining digunakan untuk membangun model prediksi risiko default yang handal.

<img src="/credit.jpg" width="300" class="block ml-auto mx-auto">
---
layout: intro-image-right
image: '/direction.avif'
transition: slide-left
---
# Tujuan
---
layout: center
---
# Tujuan

Laporan ini bertujuan menganalisis dataset Default dari Home Credit Indonesia. Prapemrosesan data dilakukan untuk menangani nilai yang hilang, mengubah tipe data, dan melakukan normalisasi. 

Selanjutnya, model machine learning digunakan untuk memprediksi default kredit. Hasil dan analisis model dievaluasi untuk menilai performanya. Dataset Default Home Credit Indonesia berisi informasi tentang karakteristik pelanggan dan riwayat kredit, termasuk jenis kontrak pinjaman, jenis pendapatan, status keluarga, tipe hunian, dan lainnya. 

Tujuan utama adalah mengembangkan model machine learning yang dapat memprediksi default pelanggan berdasarkan fitur-fitur tersebut.
---
layout: intro-image-right
image: '/lamp.jpg'
transition: slide-left
---
# Penjelasan Dataset
---
layout: center
---
# Penjelasan Dataset
Dataset "Home Credit Indonesia Default Risk" merupakan dataset yang digunakan untuk memodelkan risiko gagal bayar (default risk) dalam konteks industri keuangan. Dataset ini dikumpulkan oleh perusahaan Home Credit Indonesia, yang merupakan perusahaan keuangan yang menyediakan pinjaman kepada individu yang memiliki akses terbatas ke sistem perbankan tradisional.

Tujuan dari dataset ini adalah untuk membangun model prediktif yang dapat memprediksi risiko gagal bayar pelanggan berdasarkan berbagai fitur atau variabel yang tersedia. Model ini membantu perusahaan dalam mengambil keputusan kredit yang lebih baik dan mengurangi risiko gagal bayar.
---
layout: fact
---
# 308 Ribu
Baris Data Pada Dataset
---
layout: center
css: windicss
---
# Pembagian Data Latih dan Data Uji
<div class="grid grid-cols-2 gap-4">
    <div class="text-center">
        <h2>50%</h2>
        <h3>Data Latih</h3>
    </div>
    <div class="text-center">
        <h2>50%</h2>
        <h3>Data Uji</h3>
    </div>
</div>
---
layout: center
---
<h1 class="text-center">Kenapa 50:50 ?</h1>
<p>Setelah Melakukan Pengecekan dengan Cross Validation Score, didapatkan hasil bahwa data latih dan data uji dengan perbandingan 50:50 mempunyai skor yang lebih tinggi dibanding test size lainnya.</p>
---
layout: fact
---
# 122
Fitur Yang Ada Pada Dataset
---
layout: statement
---
# Kami Lakukan Filter Pada Fitur
---
layout: fact
---
# 21
Fitur Terbaik Menggunakan SelectKBest
---
layout: center
---
# Setelah Menyeleksi Fitur
<table>
  <thead>
    <tr>
      <th>No.</th>
      <th>Fitur</th>
      <th>Penjelasan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Code Gender</td>
      <td>Jenis Kelamin dari Applicant</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Amount Goods Price</td>
      <td>Untuk pinjaman konsumen, harga barang yang menjadi tujuan pinjaman tersebut.</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Name Education Type</td>
      <td>Tingkat pendidikan tertinggi yang dicapai oleh klien.</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Days Birth</td>
      <td>Usia klien dalam hari pada saat pengajuan aplikasi.</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Days Employed</td>
      <td>Berapa hari sebelum pengajuan orang tersebut memulai pekerjaan saat ini.</td>
    </tr>
    <tr>
      <td>..</td>
      <td>..</td>
      <td>..</td>
    </tr>
  </tbody>
</table>
---
layout: intro-image-right
image: '/library.avif'
---
# Penggunaan Library
---
layout: center
---
<h1>Penggunaan Library</h1>
<p>Pada laporan ini, kami menggunakan beberapa library yang mendukung proses analisis data dan pembangunan model machine learning. Berikut adalah library yang digunakan:</p>
<table class="text-sm">
  <thead>
    <tr>
      <th>No.</th>
      <th>Library</th>
      <th>Penjelasan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Pandas</td>
      <td>Library ini menyediakan struktur data dan fungsi untuk membantu melakukan manipulasi, pemrosesan, dan analisis data dengan mudah.</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Numpy</td>
      <td>NumPy menyediakan fungsi untuk melakukan operasi matematika, logika, dan statistik pada array, sehingga sangat berguna dalam pemrosesan data dan analisis data.</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Label Encoder dan OHE</td>
      <td>Label Encoder digunakan untuk mengubah data kategorikal menjadi data numerik, sedangkan One Hot Encoder digunakan untuk mengubah data kategorikal menjadi vektor biner.</td>
    </tr>
    <tr>
      <td>4</td>
      <td>SelectKBest</td>
      <td>SelectKBest adalah salah satu teknik feature selection yang digunakan untuk memilih fitur terbaik dari dataset yang digunakan dalam model machine learning.</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Kmeans</td>
      <td>KMeans adalah salah satu algoritma clustering yang sering digunakan dalam analisis data.</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Random Forest</td>
      <td>Random Forest adalah salah satu algoritma machine learning yang sering digunakan dalam analisis data.</td>
    </tr>
  </tbody>
</table>

---
layout: intro-image-right
image: '/disk.jpg'
---
# Preprocessing Data
---
layout: center
---
# Prepocessing Data

Preprocessing data untuk machine learning adalah proses persiapan data sebelum digunakan untuk membangun model machine learning. Tujuannya adalah untuk memastikan bahwa data yang digunakan berkualitas tinggi dan dapat digunakan untuk melatih dan menguji model dengan akurat. 

Tahapan yang perlu dilakukan dalam preprocessing data untuk machine learning antara lain: mengumpulkan data, membersihkan data dari kesalahan atau ketidakakuratan, memformat data agar sesuai dengan format yang diperlukan oleh model, membagi data menjadi data latih dan data uji, menormalkan atau standarisasi data, melakukan encoding untuk data kategorikal, dan melakukan reduksi dimensi jika diperlukan. 

Dengan melakukan preprocessing data yang baik, model machine learning yang dibangun akan lebih akurat dan dapat memberikan hasil yang lebih baik dalam memprediksi atau mengklasifikasikan data baru.
---
layout: center
---
<h1>Membersihkan Data Null</h1>
<p>Untuk membersihkan data null (kosong), ada banyak cara yang dapat dilakukan. Salah satunya adalah dengan menghapus baris yang mengandung data null. Namun, cara ini tidak selalu baik karena dapat mengurangi jumlah data yang digunakan untuk melatih model. Oleh karena itu, cara yang lebih baik adalah dengan mengisi data null dengan nilai lain. Nilai yang digunakan untuk mengisi data null dapat berupa nilai rata-rata, nilai median, atau nilai modus dari kolom tersebut. Nilai yang digunakan untuk mengisi data null harus dipilih dengan hati-hati agar tidak mengubah distribusi data.</p>
---
layout: center
css: windicss
---
<h1>Beberapa Cara Untuk Membersihkan Data Null</h1>
<div class="grid grid-cols-2 gap-4">
  <div>
    <h2 class="text-center">Mean</h2>
    <p class="text-sm text-justify">Mean (rata-rata) adalah jumlah dari semua nilai dalam suatu dataset, dibagi dengan jumlah total nilai dalam dataset tersebut. Mean sangat sensitif terhadap nilai ekstrim atau pencilan (outlier) karena dapat mempengaruhi nilai rata-rata secara signifikan. <strong>Cocok untuk data yang distribusinya normal</strong>.</p>
  </div>
  <div>
    <h2 class="text-center">Median</h2>
    <p class="text-sm text-justify">Median adalah nilai tengah dari dataset ketika nilai-nilai tersebut diurutkan dari yang terkecil hingga yang terbesar. Median kurang sensitif terhadap nilai ekstrim atau pencilan dibandingkan dengan mean, sehingga dapat memberikan gambaran yang lebih akurat tentang data yang terdapat pencilan. <strong>Cocok untuk data yang distribusinya tidak normal</strong>.</p>
  </div>
  <div class="col-span-2">
    <h2 class="text-center">Modus</h2>
    <p class="text-sm text-justify">Modus adalah nilai yang paling sering muncul dalam dataset. Modus dapat digunakan untuk menunjukkan nilai yang paling umum atau populer dalam dataset, dan dapat berguna dalam analisis data yang bersifat kategori atau diskrit. <strong>Cocok untuk data yang tipenya bukan numerik</strong>.</p>
  </div>
</div>
---
layout: center
css: windicss
---
<h1>Contoh Perbedaan Mean, Median, dan Modus</h1>
<table>
  <thead>
    <tr>
      <th>
        <div class="text-center">Mean</div>
      </th>
      <th>
        <div class="text-center">Median</div>
      </th>
      <th>
        <div class="text-center">Modus</div>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <img src="/mean.png" width="200" class="block mx-auto">
      </td>
      <td>
        <img src="/median.png" width="200" class="block mx-auto">
      </td>
      <td>
        <img src="/modus.png" width="200" class="block mx-auto">
      </td>
    </tr>
  </tbody>
</table>
---
layout: intro-image-right
image: '/transformasi.avif'
---
# Transformasi Data
---
layout: center
---
# Transformasi Data

Transformasi data adalah proses mengubah data dari satu bentuk ke bentuk lain, dengan tujuan untuk membuat data lebih mudah dipahami, lebih akurat, dan lebih mudah diolah. Transformasi data dapat dilakukan pada banyak jenis data, termasuk data numerik, data kategorikal, dan data teks.
---
layout: center
---
<h1>Transformasi Data yang Dilakukan</h1>
<div class="grid grid-cols-2 gap-4">
  <div>
    <h2>Label Encoding</h2>
    <p>Label encoding adalah teknik preprocessing data yang digunakan untuk mengubah nilai-nilai kategorikal menjadi nilai numerik, sehingga dapat digunakan dalam model machine learning. Teknik ini mengasumsikan bahwa nilai-nilai kategorikal yang berbeda memiliki urutan atau level yang berbeda.</p>
    <p>Cara kerja label encoding adalah dengan memberikan label numerik secara berurutan untuk setiap nilai kategorikal, mulai dari 0 hingga jumlah nilai kategorikal yang ada dikurangi 1. Misalnya, jika terdapat tiga nilai kategorikal "rendah", "sedang", dan "tinggi", maka label encoding akan memberikan nilai 0 untuk "rendah", nilai 1 untuk "sedang", dan nilai 2 untuk "tinggi".</p>
  </div>
  <div>
    <h2>One Hot Encoder</h2>
    <p>One hot encoder adalah teknik preprocessing data yang digunakan untuk mengubah nilai-nilai kategorikal menjadi vektor biner, sehingga dapat digunakan dalam model machine learning.</p>
    <p>Cara kerja one hot encoder adalah dengan membuat kolom baru untuk setiap nilai kategorikal yang muncul dalam dataset, dan memberikan nilai 1 pada kolom yang sesuai dengan nilai kategorikal dan nilai 0 pada kolom yang lain. Misalnya, jika terdapat tiga nilai kategorikal "merah", "hijau", dan "biru", maka one hot encoder akan membuat tiga kolom baru dengan nama "merah", "hijau", dan "biru".</p>
  </div>
</div>
---
layout: intro-image-right
image: '/selection.jpg'
---
# Menyeleksi Fitur Terbaik
---
layout: center
---
# Menyeleksi Fitur Terbaik

Seleksi fitur adalah salah satu teknik preprocessing data yang digunakan untuk memilih fitur terbaik dari dataset yang digunakan dalam model machine learning.

Seleksi fitur dapat membantu mengurangi dimensi dataset, meningkatkan keakuratan model, dan menghindari overfitting.
Salah satu teknik seleksi fitur yang sering digunakan adalah <b>SelectKBest</b>, yang digunakan untuk memilih K fitur terbaik dari dataset berdasarkan skor fitur yang dihitung.

Contoh penggunaan SelectKBest adalah pada model machine learning untuk klasifikasi spam email, di mana hanya fitur-fitur terbaik yang digunakan untuk meningkatkan akurasi prediksi dan mengurangi waktu komputasi.
---
layout: quote
---
# Feature selection is the process of selecting a subset of relevant features for use in model construction. Feature selection techniques are used for several reasons: simplification of models to make them easier to interpret, shorter training times, to avoid the curse of dimensionality, enhanced generalization by reducing overfitting and to improve the accuracy of a model.
John Elder, Founder of Elder Research
---
layout: fact
---
# 122 -> 21 
Kolom Terbaik
---
layout: fact
---
# 82.79%
Pengurangan Fitur
---
layout: statement
---
# Penurunan Fitur yang Sangat Tinggi, Kemungkinan Menurunkan Performa Metrik
---
layout: statement
---
# Dan Sayangnya...
---
layout: statement
---
# Benar...
---
layout: statement
---
# Dataset yang Kami Gunakan Mempunyai Performa Metrik yang Rendah
---
layout: intro-image-right
image: '/cluster.jpg'
---
# Klasterisasi Data
---
layout: center
---
# Klasterisasi Data

Klasterisasi data adalah teknik analisis data yang digunakan untuk mengelompokkan data dalam beberapa kelompok berdasarkan kemiripan antar data.

Tujuan dari klasterisasi data adalah untuk mengidentifikasi pola atau struktur dalam data yang tidak terlihat secara langsung.
Salah satu teknik klasterisasi yang sering digunakan adalah <b>K-Means</b>, yang mengelompokkan data dalam beberapa kelompok berdasarkan jarak antara data dengan centroid (pusat) kelompok.

Contoh penggunaan k-means adalah pada data pelanggan toko online, di mana k-means digunakan untuk mengelompokkan pelanggan dalam beberapa kelompok berdasarkan perilaku pembelian, sehingga dapat dilakukan segmentasi pasar dan strategi pemasaran yang lebih efektif.
---
layout: statement
---
# Namun, Sebelum Itu Kita Perlu Tahu Jumlah Kelompok Optimal
---
layout: statement
---
# Elbow Point adalah Koentji
---
layout: center
---
# Kenapa Elbow Point?
Elbow Point dipilih, bukannya menggunakan metode lain (misalnya: Silhouette method, Gap statistic, Average silhouette width method) adalah karena Elbow Point salah satu metode yang paling umum digunakan untuk menentukan jumlah kelompok yang optimal dalam k-means clustering. Ada beberapa alasan mengapa elbow point sering dipilih dibandingkan dengan metode lainnya, yaitu:
1. Mudah dipahami
2. Interpretasi yang intuitif
3. Konsistensi
---
layout: center
---
# Hasil Jumlah Kluster Optimal
![](/elbow-point.png)
---
layout: center
---
<h1 class="text-center">Melakukan Klusterisasi Data</h1>

<p class="text-center">Setelah mendapatkan jumlah kluster optimal, selanjutnya kami melakukan klusterisasi data dengan menggunakan metode k-means clustering. Berikut adalah hasil klusterisasi data yang kami lakukan:</p>

<img src="/heatmap.png" width="700" class="mx-auto">
---
layout: intro-image-right
image: '/process.jpg'
---
# Klasifikasi Data
---
layout: statement
---
# Mari Kita Masuk ke Inti Dari Proyek Ini
---
layout: statement
---
# Melakukan Klasifikasi Data Menggunakan Random Forest
---
layout: center
---
# Kenapa Random Forest?

Metode ensemble ini dapat mengatasi masalah overfitting dan bias-variance trade-off. Ini dapat menghasilkan prediksi yang baik dengan menggabungkan hasil dari banyak pohon keputusan.
---
layout: center
---
<h1 class="text-center">Sebelum Melakukan Klasifikasi Data, Kita Perlu Mencari Tahu Split Test yang Paling Optimal</h1>
---
layout: center
---
# Menggunakan Cross Validation Score untuk Mencari Split Test yang Paling Optimal

Cross Validation Score adalah salah satu metode yang digunakan untuk menentukan kinerja model pada data yang belum dilihat. Dalam konteks mencari split test yang paling optimal, Cross Validation Score dapat digunakan untuk mengevaluasi performa model pada berbagai split test yang berbeda dan memilih split test yang memberikan skor evaluasi yang paling optimal.

Ada beberapa alasan mengapa Cross Validation Score sering digunakan untuk mencari split test yang paling optimal, yaitu:
1. Mencegah overfitting
2. Meminimalkan bias
3. Memperoleh skor evaluasi yang stabil
---
layout: fact
---
# 50:50
Split Test dan Train yang Paling Baik
---
layout: center
---
# Hasil Cross Validation Score

Test Size: 0.2
Average Cross-Validation Score: 0.919396930140094 

Test Size: 0.3
Average Cross-Validation Score: 0.9191338715737007

Test Size: 0.4
Average Cross-Validation Score: 0.919173360999545

Test Size: 0.5
Average Cross-Validation Score: 0.9195213163799553
---
layout: statement
---
# Mulai Klasifikasi Data...
---
layout: center
---
# Koding Klasifikasi Data

```python
# Membangun model Random Forest
rf_model = RandomForestClassifier(n_estimators=100, random_state=42)

# Melatih model dengan data training
rf_model.fit(x_train, y_train)

# Memprediksi target menggunakan data testing
y_pred = rf_model.predict(x_test)
```
---
layout: statement
---
# Didapatkan Hasil Klasifikasi Data...
---
layout: center
---
<h1>Hasil Klasifikasi Data</h1>
<table>
  <thead>
    <tr>
      <th scope="col">Klasifikasi</th>
      <th scope="col">Hasil</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Accuracy</td>
      <td>91,9%</td>
    </tr>
    <tr>
      <td>Precision</td>
      <td>50,4%</td>
    </tr>
    <tr>
      <td>Recall</td>
      <td>0,8%</td>
    </tr>
    <tr>
      <td>F1 Score</td>
      <td>1,6%</td>
    </tr>
    <tr>
      <td>Confussion Matrix</td>
      <td>[141220, 104, 12326, 106]</td>
    </tr>
    <tr>
      <td>MSE</td>
      <td>8%</td>
    </tr>
    <tr>
      <td>RMSE</td>
      <td>28,4%</td>
    </tr>
  </tbody>
</table>
---
layout: statement
---
# Artinya Apa?
---
layout: center
---
<h1>Arti Tiap Statistik Metrik:</h1>
<table>
  <thead>
    <tr>
      <th scope="col">Metrik</th>
      <th scope="col">Penjelasan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Accuracy : 91,9%</td>
      <td>Akurasi mengukur seberapa baik model dapat mengklasifikasikan data dengan benar secara keseluruhan. Dalam hal ini, model memiliki akurasi sebesar 91.92%, yang berarti sekitar 91.92% dari data diklasifikasikan dengan benar.</td>
    </tr>
    <tr>
      <td>Precision : 50,4%</td>
      <td>Presisi mengukur seberapa baik model dapat mengidentifikasi secara akurat kasus positif dari semua hasil yang diklasifikasikan sebagai positif. Dalam hal ini, model memiliki presisi sebesar 50.48%, yang berarti dari semua yang diprediksi sebagai positif, sekitar 50.48% adalah benar-benar kasus positif.</td>
    </tr>
    <tr>
      <td>Recall : 0,8%</td>
      <td>Recall (juga dikenal sebagai sensitivitas) mengukur seberapa baik model dapat mengidentifikasi secara akurat kasus positif dari semua kasus yang sebenarnya positif. Dalam hal ini, model memiliki recall sebesar 0.85%, yang berarti sekitar 0.85% dari semua kasus positif berhasil diidentifikasi oleh model.</td>
    </tr>
    <tr>
      <td>F1 Score : 1,6%</td>
      <td>F1-Score adalah rata-rata harmonik antara presisi dan recall. Ini memberikan ukuran yang seimbang antara presisi dan recall. Dalam hal ini, model memiliki F1-Score sebesar 1.68%.</td>
    </tr>
  </tbody>
</table>
---
layout: center
---
<h1>Lanjutan...</h1>
<table>
  <thead>
    <tr>
      <th scope="col">Metrik</th>
      <th scope="col">Penjelasan</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Confussion Matrix</td>
      <td>Confusion matrix menunjukkan jumlah data yang diklasifikasikan dengan benar atau salah dalam bentuk matriks. Pada kasus ini, terdapat 141220 data yang diklasifikasikan dengan benar sebagai negatif (true negative), 104 data yang salah diklasifikasikan sebagai negatif (false negative), 12326 data yang salah diklasifikasikan sebagai positif (false positive), dan 106 data yang diklasifikasikan dengan benar sebagai positif (true positive).</td>
    </tr>
    <tr>
      <td>MSE : 8,0%</td>
      <td>Mean Squared Error (MSE) mengukur rata-rata dari kuadrat perbedaan antara nilai prediksi dan nilai sebenarnya. Dalam hal ini, MSE memiliki nilai sebesar 8.08%.</td>
    </tr>
    <tr>
      <td>RMSE : 28,4%</td>
      <td>Root Mean Squared Error (RMSE) adalah akar kuadrat dari MSE. RMSE memberikan ukuran kesalahan rata-rata dalam satuan asli variabel target. Dalam hal ini, RMSE memiliki nilai sebesar 28.43%.</td>
    </tr>
  </tbody>
</table>
---
layout: center
---
# Kesimpulan dari Klasifikasi Data

Model memiliki akurasi yang tinggi (91.92%), tetapi presisi, recall, dan F1-Scorenya relatif rendah. Hal ini menunjukkan bahwa model cenderung menghasilkan banyak false positive dan false negative. MSE dan RMSE menunjukkan tingkat kesalahan rata-rata dalam prediksi nilai sebenarnya. Semakin rendah nilai MSE dan RMSE, semakin baik model dalam melakukan prediksi.
---
layout: statement
---
# Selanjutnya apa? Apakah Kami Tidak Mengupayakan Agar Lebih Baik?
---
layout: statement
---
# Tentu Tidak...
---
layout: center
---
# Kami Sudah Mengupayakan dengan Berbagai Cara, Seperti...

- Pilih metode klasifikasi yang lain
- Mengubah n_estimators
- Menggunakan teknik validasi yang baik
---
layout: statement
---
# Tapi, Hasilnya Tetap Sama Bahkan Lebih Rendah :(
---
layout: statement
---
# Kemungkinan, Ada Masalah Dari Pemilihan Fitur
---
layout: intro-image-right
image: '/close.jpg'
---
# Penutup
---
layout: center
---
# Penutup
Dengan memahami konsep klasterisasi data dan teknik k-means, kita dapat mengelompokkan data dalam beberapa kelompok berdasarkan kemiripan antar data, sehingga dapat mengidentifikasi pola atau struktur dalam data yang tidak terlihat secara langsung.

Dalam menentukan jumlah kelompok yang optimal dalam k-means clustering, metode elbow point dan metode lainnya seperti silhouette method, gap statistic method, average silhouette width method, dan Calinski-Harabasz index dapat digunakan tergantung pada karakteristik dari dataset yang sedang dianalisis.

Untuk mencari split test yang paling optimal, Cross Validation Score dapat menjadi pilihan yang baik untuk mengevaluasi performa model pada berbagai split test yang berbeda dan memastikan bahwa model tidak hanya optimal pada dataset latih, tetapi juga pada dataset yang belum dilihat.

Dengan menggunakan metode yang tepat dan pemilihan split test yang optimal, kita dapat meningkatkan akurasi dan efisiensi proses klasterisasi data dan memperoleh hasil yang lebih baik dalam analisis data.
---
layout: center
---
# Kontribusi di Proyek Kami
<img src="https://chart.googleapis.com/chart?cht=qr&chs=400x400&chl=https://www.kaggle.com/code/ricoaditya28/tugas-besar-ml/edit/run/132831326" width="400" class="mx-auto">
---
layout: center
---
# Kunjungi Repo dari Slide ini
<img src="https://chart.googleapis.com/chart?cht=qr&chs=400x400&chl=https://github.com/XCOD33/Presentasi-Tugas-Besar-Machine-Learning" width="400" class="mx-auto">
---
layout: center
---
# Apakah Ada yang ingin ditanyakan?
---
layout: center
---
# Terima Kasih !

```
$ sudo shutdown -r
```