<h1 align="center">UTS_RobotikaSymforce</h1>

## Dokumentasi Symforce
### Muhammad Syaiful Rahman_1103192198

![SymForce](docs/Symforce.png#gh-light-mode-only)
<!-- DARK_MODE_ONLY -->

<p align="center">
<a href="https://github.com/symforce-org/symforce/actions/workflows/ci.yml?query=branch%3Amain"><img alt="CI status" src="https://github.com/symforce-org/symforce/actions/workflows/ci.yml/badge.svg" /></a>
<a href="https://symforce.org"><img alt="Documentation" src="https://img.shields.io/badge/api-docs-blue" /></a>
<a href="https://github.com/symforce-org/symforce"><img alt="Source Code" src="https://img.shields.io/badge/source-code-blue" /></a>
<a href="https://github.com/symforce-org/symforce/issues"><img alt="Issues" src="https://img.shields.io/badge/issue-tracker-blue" /></a>
<img alt="Python 3.8 | 3.9 | 3.10" src="https://img.shields.io/pypi/pyversions/symforce" />
<img alt="C++14" src="https://img.shields.io/badge/c++-14-blue" />
<a href="https://pypi.org/project/symforce/"><img alt="PyPI" src="https://img.shields.io/pypi/v/symforce" /></a>
<a href="https://github.com/symforce-org/symforce/tree/main/LICENSE"><img alt="Apache License" src="https://img.shields.io/pypi/l/symforce" /></a>
</p>

SymForce merupakan komputasi simbolik cepat dan pustaka pembuatan kode untuk aplikasi robotika seperti visi komputer, estimasi keadaan, perencanaan gerak, dan kontrol. Ini menggabungkan kecepatan pengembangan dan fleksibilitas matematika simbolik dengan kinerja kode yang dibuat secara otomatis dan sangat dioptimalkan dalam C++ atau bahasa runtime target apa pun. 

#### SymForce berisi tiga sistem yang berguna secara independen:

+ **Symbolic Toolkit** - dibangun di atas SymPy API untuk menyediakan tipe geometris dan kamera yang ketat, kalkulus grup kebohongan, penanganan singularitas, dan alat untuk memodelkan masalah kompleks

+ **Pembuat Kode (Code Generator)** - mengubah ekspresi simbolik menjadi kode tanpa cabang yang sangat cepat dengan API bersih dan ketergantungan minimal, dengan sistem templat untuk menargetkan bahasa apa pun

+ **Pustaka Pengoptimalan (Optimization Library)** - pustaka pengoptimalan ruang tangen cepat berdasarkan grafik faktor, dengan implementasi yang sangat optimal untuk aplikasi robotika waktu nyata

SymForce secara otomatis menghitung ruang singgung Jacobians, menghilangkan kebutuhan akan turunan tulisan tangan yang rawan bug. Fungsi yang dihasilkan dapat langsung digunakan sebagai faktor dalam pengoptimal nonlinier kami. Alur kerja ini memungkinkan fungsi runtime lebih cepat, waktu pengembangan lebih cepat, dan lebih sedikit baris kode tulisan tangan dibandingkan metode alternatif.

SymForce dikembangkan dan dikelola oleh Skydio. Ini digunakan dalam produksi untuk mempercepat tugas-tugas seperti SLAM, penyesuaian bundel, kalibrasi, dan MPC nonlinier jarang untuk robot otonom dalam skala besar.

<br/>

<img alt="SymForce" src="docs/SymforceDiagram.png" width="700px"/>

<br/>

Contoh dari implementasi symforce adalah:
- Computer Vision
- State Estimation
- Motion Planning
- Robot Controls

#### FITUR :

+ Implementasi simbolik geometri dan tipe kamera dengan operasi grup Lie
+ Pembuatan kode dari kode runtime asli yang cepat dari ekspresi simbolik, mengurangi duplikasi dan meminimalkan bug
+ Alat baru untuk menghitung jacobian ruang singgung yang cepat dan benar untuk ekspresi apa pun, menghindari semua turunan tulisan tangan
+ Strategi untuk meratakan komputasi dan memanfaatkan sparsity yang dapat menghasilkan 10x percepatan dibandingkan autodiff standar
+ Pustaka pengoptimalan ruang tangen cepat di C++ dan Python berdasarkan grafik faktor
+ Prototyping cepat dan analisis masalah kompleks dengan matematika simbolik, dengan alur kerja mulus ke penggunaan produksi
+ Pembuatan kode Eigen yang di-embedded-friendly dengan C++ dengan alokasi memori dinamis nol
+ Kode yang sangat berkinerja, modular, teruji, dan dapat diperluas

<h2 align="center">Spesifikasi Hardware & Software yang terinstall</h2>

##### Untuk menjalankan simulasi symforce secara optimal bertikut rekomendasi spesifikasi perangkat yang disarankan:

- CPU 4 core
- RAM 8 GB
- Mem 50 GB

atau bisa juga menggunakan alternatif lain seperti [github codespace](https://github.com/features/codespaces)

##### Berikut beberapa software yang menjadi rekomendasi penulis:

- Ubuntu 20.04 OS
- Python 3.8+
- Jupyter notebook
- Visual studio code editor

<h1 align="center">Implementasi SymForce</h1>

Contoh Studi Kasus : Robot bergerak melalui bidang 2D dan memiliki goal untuk memperkirakan pose pada beberapa langkah kedepan dengan sebuah pengukuran kebisingan (noisy measurements). 

Pengukuran yang harus dilakukan oleh Robot :

 * Jarak yang ditempuh dengan menggunakan sensor odometri
 * Sudut relatif menuju landmark.

Berdasarkan kasus di atas, maka robot memiiki sudut dengan tujuan yang berlawanan arah jarum jam dari sumbu x. Oleh karena itu, pengukuran sudut relatif ditentukan dari arah robot akan maju. Berikut adalah gambar berdasarkan kasus robot yang kita miliki :

![SymForce](docs/problem_setup.png#gh-light-mode-only)
