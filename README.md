# UTS_RobotikaSymforce
## Dokumentasi Symforce

![SymForce](docs/Symforce.png#gh-light-mode-only)
<!-- DARK_MODE_ONLY -->

SymForce merupakan komputasi simbolik cepat dan pustaka pembuatan kode untuk aplikasi robotika seperti visi komputer, estimasi keadaan, perencanaan gerak, dan kontrol. Ini menggabungkan kecepatan pengembangan dan fleksibilitas matematika simbolik dengan kinerja kode yang dibuat secara otomatis dan sangat dioptimalkan dalam C++ atau bahasa runtime target apa pun. 

#### SymForce berisi tiga sistem yang berguna secara independen:

+ **Symbolic Toolkit** - dibangun di atas SymPy API untuk menyediakan tipe geometris dan kamera yang ketat, kalkulus grup kebohongan, penanganan singularitas, dan alat untuk memodelkan masalah kompleks

+ **Pembuat Kodet** - mengubah ekspresi simbolik menjadi kode tanpa cabang yang sangat cepat dengan API bersih dan ketergantungan minimal, dengan sistem templat untuk menargetkan bahasa apa pun

+ **Pustaka Pengoptimalan** - pustaka pengoptimalan ruang tangen cepat berdasarkan grafik faktor, dengan implementasi yang sangat optimal untuk aplikasi robotika waktu nyata

SymForce secara otomatis menghitung ruang singgung Jacobians, menghilangkan kebutuhan akan turunan tulisan tangan yang rawan bug. Fungsi yang dihasilkan dapat langsung digunakan sebagai faktor dalam pengoptimal nonlinier kami. Alur kerja ini memungkinkan fungsi runtime lebih cepat, waktu pengembangan lebih cepat, dan lebih sedikit baris kode tulisan tangan dibandingkan metode alternatif.

SymForce dikembangkan dan dikelola oleh Skydio. Ini digunakan dalam produksi untuk mempercepat tugas-tugas seperti SLAM, penyesuaian bundel, kalibrasi, dan MPC nonlinier jarang untuk robot otonom dalam skala besar.
