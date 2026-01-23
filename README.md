# Network hardening risk assessment for social media organization

## 📌 Table of contents

1. [Background](#background)
2. [Organization and system context](#scenario)
3. [Assessment objectives](#objective)
4. [Risk assessment report](#riskassessment)
5. [Insights and lessons learned](#insight)

---

## 🧠 Background <a name="background">

Studi kasus ini ditulis sebagai latihan cybersecurity yang fokus pada penguatan keamanan jaringan setelah terjadi kebocoran data di sebuah organisasi media sosial. Skenario ini menggambarkan kondisi saat celah jaringan tidak terpantau dengan baik dan akhirnya berdampak langsung ke data pengguna. Situasi ini menjadi titik awal untuk memahami risiko yang muncul ketika masalah keamanan dibiarkan terlalu lama.

Pembahasan mengacu pada materi Google Cybersecurity Professional Certificate, khususnya course Connect and Protect: Networks and Network Security. Analisis dimulai dengan mengenali kerentanan jaringan lalu dilanjutkan ke penerapan network hardening seperti pengaturan akses, konfigurasi firewall, dan sistem autentikasi. Pendekatan ini menunjukkan bahwa penguatan jaringan yang dilakukan secara konsisten dapat menekan risiko kejadian serupa dan meningkatkan keamanan organisasi ke depannya.

---

## 🏢 Organization and system context <a name="scenario">

Saya berperan sebagai analis keamanan siber di sebuah organisasi media sosial yang baru saja mengalami kebocoran data besar. Insiden ini membuka peluang data pribadi pengguna seperti nama dan alamat diakses pihak yang tidak berwenang. Kondisi ini langsung menimbulkan kekhawatiran karena data pengguna sangat berpengaruh ke kepercayaan publik.

Infrastruktur jaringan menunjukkan beberapa celah serius yang tidak bisa diabaikan. Temuan yang ada meliputi:
- Kata sandi dipakai bersama oleh karyawan
- Kata sandi admin basis data masih menggunakan pengaturan default
- Firewall belum memiliki aturan untuk memfilter lalu lintas masuk dan keluar
- Otentikasi multifaktor (MFA) belum diterapkan

Temuan tersebut menunjukkan kebocoran terjadi karena praktik keamanan yang lemah dan penerapan network hardening yang tidak konsisten. Risiko serupa sangat mungkin terulang jika kondisi ini tidak segera ditangani, dengan dampak yang lebih besar pada keamanan data dan reputasi perusahaan.

---

## 🎯 Assessment objectives <a name="objective">

Assessment ini dilakukan untuk memberi gambaran kondisi keamanan jaringan dan risiko yang bisa berdampak ke operasional organisasi media sosial. Proses ini dimulai sebagai acuan saat melakukan analisis dan evaluasi keamanan jaringan.

Fokus utamanya meliputi:
- Mengidentifikasi risiko keamanan jaringan yang berpengaruh pada ketersediaan, integritas, dan kerahasiaan sistem
- Mengevaluasi konfigurasi jaringan serta praktik keamanan pada infrastruktur layanan digital
- Menilai seberapa efektif kontrol keamanan yang sudah diterapkan dan menemukan celah yang bisa dimanfaatkan ancaman internal maupun eksternal
- Menentukan tingkat risiko tiap temuan sebagai dasar penentuan prioritas penanganan
- Menyusun dasar penerapan network hardening untuk memperkuat ketahanan dan postur keamanan jaringan secara menyeluruh.

---

## 🔍 Risk assessment report <a name="report">

### a. Summary

Laporan penilaian risiko keamanan ini dibuat untuk melihat kondisi keamanan jaringan pada organisasi media sosial yang baru mengalami kebocoran data besar. Insiden ini berdampak langsung ke perlindungan data pribadi pengguna seperti nama dan alamat. Kejadian tersebut juga menimbulkan risiko serius terhadap kepercayaan publik dan reputasi perusahaan.

Penilaian ini difokuskan untuk menemukan kelemahan utama yang memicu pelanggaran dan menilai risiko lanjutan jika celah tersebut tidak segera ditangani. Proses analisis dimulai dengan meninjau pengelolaan akses, konfigurasi jaringan, dan mekanisme autentikasi yang digunakan di lingkungan organisasi. Hasil penilaian ini diharapkan menjadi dasar penyusunan langkah network hardening yang lebih kuat dan konsisten.

### b. Identified vulnerabilities

Pemeriksaan awal pada sistem dan jaringan menunjukkan beberapa celah keamanan yang ikut berperan dalam kebocoran data. Masalah ini muncul karena kombinasi kelemahan teknis dan kebiasaan keamanan yang belum dijalankan secara konsisten di lingkungan kerja.

| Kerentanan                                          | Penjelasan                                                                                                                                                                                                                                                     |
| --------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Kata sandi digunakan bersama                        | Beberapa karyawan memakai kata sandi yang sama untuk akses sistem internal. Kondisi ini menyulitkan pelacakan aktivitas tiap pengguna dan meningkatkan risiko penyalahgunaan. Satu akun yang bocor bisa membuka akses ke sistem lain dengan kredensial serupa. |
| Kata sandi admin database masih default             | Akun administrator database masih memakai kata sandi bawaan sistem. Situasi ini memudahkan penyerang mencoba brute force atau menebak kredensial untuk mendapat akses penuh.                                                                                   |
| Firewall belum dikonfigurasi                        | Firewall belum memiliki aturan penyaringan lalu lintas yang jelas. Lalu lintas masuk dan keluar jaringan berjalan tanpa kontrol yang memadai, sehingga peluang akses tidak sah makin besar.                                                                    |
| Tidak menggunakan Multi-Factor Authentication (MFA) | MFA belum diterapkan pada akun pengguna maupun akun dengan hak akses tinggi. Proses login hanya mengandalkan username dan password, yang membuat sistem rentan saat kredensial bocor atau dicuri.                                                              |

### c. Risk analysis

Analisis risiko dilakukan dengan menilai peluang setiap celah keamanan bisa dimanfaatkan dan dampaknya jika benar terjadi. Hasil penilaian menunjukkan sebagian besar celah berada di level risiko tinggi sampai kritis sehingga tidak layak ditunda penanganannya.

| Kerentanan                                          | Kemungkinan | Dampak | Tingkat risiko |
| --------------------------------------------------- | ----------- | ------ | -------------- |
| Kata sandi digunakan bersama karyawan               | Tinggi      | Tinggi | Tinggi         |
| Kata sandi admin database masih default             | Tinggi      | Kritis | Tinggi         |
| Aturan firewall belum dikonfigurasi                 | Sedang      | Tinggi | Tinggi         |
| Tidak menggunakan Multi-Factor Authentication (MFA) | Tinggi      | Tinggi | Tinggi         |

Kerentanan dengan risiko tinggi dan kritis berpotensi memicu kebocoran data lanjutan, gangguan operasional, dan penyalahgunaan akses internal jika tidak segera ditangani dengan kontrol keamanan yang tepat.

### d. Security hardening recommendations

Berdasarkan hasil analisis risiko, langkah pengerasan jaringan ini disusun untuk menutup celah keamanan yang ditemukan dan memperkuat perlindungan jaringan secara menyeluruh.

| Kerentanan                                          | Metode pengerasan                                           | Alasan efektivitas                                                                        | Frekuensi penerapan                             |
| --------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------- |
| Kata sandi digunakan bersama karyawan               | Menerapkan kata sandi unik dan pengelolaan akun pengguna    | Aktivitas pengguna lebih mudah dilacak dan risiko penyalahgunaan akses internal berkurang | Diterapkan terus dengan audit berkala           |
| Kata sandi admin database masih default             | Mengganti kata sandi bawaan dan membatasi hak akses admin   | Akses tidak sah ke database bisa dicegah dan risiko pengambilalihan sistem menurun        | Setiap implementasi sistem dan peninjauan rutin |
| Aturan firewall belum dikonfigurasi                 | Mengatur aturan firewall dan memfilter lalu lintas jaringan | Akses jaringan hanya datang dari sumber valid sehingga permukaan serangan lebih kecil     | Monitoring harian dan evaluasi berkala          |
| Tidak menggunakan Multi-Factor Authentication (MFA) | Menerapkan MFA pada akun pengguna dan akun administratif    | Lapisan keamanan tambahan tetap melindungi meski kredensial utama bocor                   | Diterapkan permanen dengan evaluasi kebijakan   |

Penerapan langkah-langkah ini secara konsisten membantu menurunkan risiko kebocoran data dan membangun keamanan jaringan yang lebih kuat untuk jangka panjang.

### e. Risk mitigation impact

Penerapan langkah pengerasan jaringan yang disarankan terasa langsung dampaknya ke keamanan sistem dan perlindungan data di platform media sosial. Setiap kontrol yang dipasang menutup celah lama yang sebelumnya mudah disalahgunakan dan menurunkan risiko kebocoran data secara nyata.

| Area keamanan                 | Dampak mitigasi                                                                                                                               |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Manajemen kata sandi dan akun | Pengelolaan akun jadi lebih jelas karena setiap pengguna memakai kata sandi unik, sehingga risiko penyalahgunaan akses internal bisa ditekan. |
| Keamanan database             | Risiko pengambilalihan sistem penting menurun setelah kata sandi default diganti dan hak akses admin dibatasi.                                |
| Keamanan jaringan             | Permukaan serangan mengecil karena lalu lintas jaringan dibatasi hanya ke sumber yang terpercaya lewat konfigurasi firewall.                  |
| Autentikasi pengguna          | Proses login punya lapisan keamanan tambahan, sehingga akun tetap terlindungi walaupun kredensial utama sempat bocor.                         |
| Monitoring dan kontrol risiko | Aktivitas jaringan lebih mudah dipantau dan potensi ancaman bisa terdeteksi lebih cepat karena kontrol keamanan diterapkan konsisten.         |
| Postur keamanan keseluruhan   | Risiko pelanggaran data ke depan menurun dan ketahanan keamanan jaringan organisasi terasa lebih kuat untuk jangka panjang.                   |

Hasil ini menunjukkan bahwa mitigasi yang diterapkan memberi perubahan nyata dan relevan terhadap kondisi keamanan sistem secara keseluruhan.

---

## 💡 Insights and lessons learned <a name="insight">

Hasil penilaian risiko menunjukkan kebocoran data terjadi karena praktik keamanan yang masih lemah dan penerapan network hardening yang tidak merata. Penggunaan kata sandi bersama, kredensial admin bawaan, konfigurasi firewall yang kurang tepat, serta tidak adanya MFA membuka celah besar untuk akses tanpa izin.

Proses identifikasi kerentanan membantu melihat area dengan risiko tinggi sampai kritis secara lebih jelas. Rekomendasi dimulai dengan penguatan kontrol akses, perbaikan autentikasi, dan perlindungan lalu lintas jaringan. Pendekatan ini dibuat supaya bisa diterapkan konsisten dan tetap sesuai dengan standar keamanan jaringan yang umum.

Penerapan langkah pengerasan jaringan terbukti menurunkan risiko kebocoran data ke depan. Kontrol akses jadi lebih tertata, aktivitas jaringan lebih mudah dipantau, dan perlindungan data pengguna terasa lebih kuat. Strategi ini membantu organisasi membangun keamanan yang lebih matang sekaligus menjaga kepercayaan pengguna dan kestabilan operasional jangka panjang.
