---
# try also 'default' to start simple
theme: apple-basic
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# https://sli.dev/custom/highlighters.html
highlighter: shiki
transition: slide-left
layout: intro
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