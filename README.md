# Network hardening risk assessment for social media organization

## 📌 Table of contents

1. [Background](#background)
2. [Organization and system context](#scenario)
3. [Assessment objectives](#objective)
4. [Risk assessment report](#riskassessment)
5. [Insights and lessons learned](#insight)

---

## 🧠 Background <a name="background">

Studi ini disusun sebagai latihan cybersecurity yang berfokus pada upaya memperkuat keamanan jaringan setelah terjadinya kebocoran data di sebuah organisasi media sosial. Skenario yang digunakan menggambarkan situasi ketika celah jaringan tidak terpantau dengan baik dan akhirnya berdampak langsung pada data pelanggan. Kondisi ini menjadi titik awal untuk memahami risiko yang muncul ketika masalah keamanan tidak segera ditangani.

Pembahasan ini merujuk pada materi dalam program Google Cybersecurity Professional Certificate, khususnya course Connect and Protect: Networks and Network Security. Fokus analisis diarahkan pada pengenalan kerentanan jaringan serta penerapan langkah network hardening yang relevan, seperti pengaturan akses, konfigurasi firewall, dan mekanisme autentikasi. Tujuan akhirnya adalah menunjukkan bagaimana penguatan jaringan yang dilakukan secara konsisten dapat mencegah insiden serupa dan meningkatkan keamanan organisasi di masa depan.

---

## 🏢 Organization and system context <a name="scenario">

Saya berperan sebagai analis keamanan siber di sebuah organisasi media sosial yang baru saja mengalami kebocoran data dalam skala besar. Insiden ini membuka kemungkinan tereksposnya data pribadi pengguna, seperti nama dan alamat, ke pihak yang tidak berhak. Situasi ini langsung memicu kekhawatiran karena data pengguna adalah aset penting yang sangat memengaruhi kepercayaan publik.

Infrastruktur jaringan turut memperlihatkan celah yang cukup serius. Keempat celah tersebut adalah:
- Kata sandi bersama karyawan organisasi.
- Kata sandi admin untuk basis data diatur ke default.
- Firewall tidak memiliki aturan untuk menyaring lalu lintas yang masuk dan keluar dari jaringan.
- Otentikasi multifaktor (MFA) tidak digunakan.

Temuan ini menunjukkan bahwa pelanggaran data terjadi akibat kombinasi dari praktik keamanan yang lemah dan kurangnya penerapan network hardening secara konsisten. Risiko serupa berpotensi muncul kembali jika kondisi ini dibiarkan, dengan dampak yang lebih besar terhadap keamanan data dan reputasi perusahaan.

---

## 🎯 Assessment objectives <a name="objective">

Assessment ini dilakukan untuk memberikan gambaran yang jelas mengenai kondisi keamanan jaringan serta potensi risiko yang dapat memengaruhi operasional organisasi media sosial. Tujuan berikut dirumuskan sebagai acuan dalam proses analisis dan evaluasi keamanan jaringan.
- Mengidentifikasi potensi risiko keamanan jaringan yang dapat memengaruhi ketersediaan, integritas, dan kerahasiaan sistem
- Mengevaluasi konfigurasi jaringan serta praktik keamanan yang diterapkan pada infrastruktur pendukung layanan digital
- Menilai efektivitas kontrol keamanan yang telah diterapkan dan mengidentifikasi celah yang berpotensi dimanfaatkan oleh ancaman internal maupun eksternal
- Menentukan tingkat risiko dari setiap temuan sebagai dasar penetapan prioritas penanganan
- Memberikan landasan bagi penerapan network hardening untuk meningkatkan ketahanan dan postur keamanan jaringan secara keseluruhan

---

## 🔍 Risk assessment report <a name="report">

Laporan penilaian risiko keamanan ini dibuat untuk melihat kondisi keamanan jaringan di sebuah organisasi media sosial yang baru saja mengalami kebocoran data besar. Insiden tersebut berdampak langsung pada perlindungan data pribadi pengguna, seperti nama dan alamat, serta menimbulkan risiko serius terhadap kepercayaan publik dan reputasi perusahaan.

Penilaian ini bertujuan menemukan kelemahan utama yang memicu terjadinya pelanggaran dan menilai risiko lanjutan jika celah tersebut tidak segera diperbaiki. Proses analisis dilakukan dengan meninjau pengelolaan akses, pengaturan jaringan, dan mekanisme autentikasi yang digunakan di lingkungan organisasi. Hasil penilaian diharapkan dapat menjadi landasan untuk menyusun langkah network hardening yang lebih kuat dan konsisten.

### a. Identified vulnerabilities

Pemeriksaan awal terhadap sistem dan jaringan menunjukkan beberapa celah keamanan yang berperan dalam terjadinya kebocoran data. Masalah ini muncul dari kombinasi kelemahan teknis dan kebiasaan keamanan yang belum dijalankan secara konsisten.

|Kerentanan|Penjelasan|
|---|---|
|Kata sandi yang dibagikan kepada karyawan|Sejumlah karyawan memakai kata sandi yang sama untuk mengakses sistem internal. Pola ini menyulitkan pelacakan aktivitas pengguna dan meningkatkan risiko penyalahgunaan akses. Satu akun yang berhasil ditembus dapat membuka jalan ke sistem lain yang memakai kredensial serupa.|
|Kata sandi administrator database masih default|Akun administrator database masih menggunakan kata sandi default sejak awal sistem digunakan. Kondisi ini memudahkan penyerang mencoba teknik umum seperti brute force atau menebak kredensial untuk mendapatkan akses penuh.|
|Aturan firewall yang belum dikonfigurasi|Firewall belum diatur dengan aturan penyaringan lalu lintas yang jelas. Lalu lintas masuk dan keluar jaringan berjalan tanpa batasan yang memadai, sehingga peluang akses tidak sah dari luar jaringan menjadi lebih besar.|
|Tidak ada Multi-Factor Authentication (MFA)|Autentikasi multifaktor belum diterapkan pada akun pengguna maupun akun dengan hak akses tinggi. Proses login masih bergantung pada username dan password, yang membuat sistem rentan saat kredensial bocor atau dicuri.|

### b. Risk analysis

Analisis risiko dilakukan dengan melihat seberapa besar peluang tiap celah keamanan bisa dimanfaatkan, serta dampak yang muncul jika hal itu benar-benar terjadi. Hasilnya menunjukkan bahwa sebagian besar kerentanan berada pada level risiko tinggi hingga kritis dan tidak bisa ditunda penanganannya.

|Kerentanan|Kemungkinan|Dampak|Tingkat resiko|
|---|---|---|---|
|Kata sandi yang dibagikan kepada karyawan|Tinggi|Tinggi|Tinggi|
|Kata sandi administrator database masih default|Tinggi|Kritis|Tinggi|
|Aturan firewall yang belum dikonfigurasi|Sedang|Tinggi|Tinggi|
|Tidak ada Multi-Factor Authentication (MFA)|Tinggi|Tinggi|Tinggi|

Kerentanan dengan tingkat risiko tinggi dan kritis dapat memicu kebocoran data lanjutan, gangguan operasional, hingga penyalahgunaan akses internal jika tidak segera ditangani dengan kontrol keamanan yang memadai.

### c. Security hardening recommendations

Berdasarkan hasil analisis risiko, berikut rangkuman rekomendasi pengerasan jaringan yang disusun untuk menutup celah keamanan dan memperkuat perlindungan jaringan secara menyeluruh.

|Kerentanan|Metode pengerasan|Alasan efektivitas|Frekuensi penerapan|
|---|---|---|---|
|Kata sandi yang dibagikan kepada karyawan|Penerapan kata sandi unik dan pengelolaan akun pengguna|Aktivitas pengguna dapat ditelusuri dengan jelas dan risiko penyalahgunaan akses internal berkurang|Diterapkan terus-menerus dengan audit berkala|
|Kata sandi administrator database masih default|Penggantian kata sandi bawaan dan pembatasan hak akses admin|Mencegah akses tidak sah ke database dan menekan risiko pengambilalihan sistem|Setiap implementasi sistem dan peninjauan rutin|
|Aturan firewall yang belum dikonfigurasi|Konfigurasi aturan firewall dan pemfilteran lalu lintas jaringan|Akses jaringan hanya datang dari sumber yang sah sehingga permukaan serangan lebih kecil|Monitoring harian dan evaluasi berkala|
|Tidak ada Multi-Factor Authentication (MFA)|Penerapan MFA pada akun pengguna dan akun administratif|Menambah lapisan keamanan meskipun kredensial utama berhasil bocor|Diterapkan permanen dengan evaluasi kebijakan|

Penerapan rekomendasi ini secara konsisten membantu organisasi menurunkan risiko pelanggaran data dan membangun postur keamanan jaringan yang lebih kuat serta berkelanjutan.

### d. Risk mitigation impact

Penerapan langkah pengerasan jaringan yang direkomendasikan memberi dampak nyata pada peningkatan keamanan jaringan dan perlindungan data di platform media sosial. Setiap kontrol yang diterapkan membantu menutup celah yang sebelumnya mudah dimanfaatkan dan secara langsung menurunkan risiko terjadinya kebocoran data.

|Area keamanan|Dampak mitigasi|
|---|---|
|Manajemen kata sandi dan akun|Akuntabilitas pengguna meningkat karena setiap akun dikelola lebih rapi dan menggunakan kata sandi unik, sehingga risiko penyalahgunaan akses internal dapat ditekan.|
|Keamanan database|Peluang pengambilalihan sistem penting berkurang melalui penggantian kata sandi default dan pembatasan hak akses administrator.|
|Keamanan jaringan|Permukaan serangan menjadi lebih kecil karena lalu lintas jaringan dibatasi hanya dari sumber yang terpercaya lewat pengaturan firewall yang tepat.|
|Autentikasi pengguna|Proses login memiliki lapisan perlindungan tambahan, sehingga akun tetap aman meskipun kredensial utama sempat bocor.|
|Monitoring dan kontrol risiko|Aktivitas jaringan lebih mudah dipantau dan potensi ancaman dapat terdeteksi lebih cepat berkat kontrol keamanan yang diterapkan secara konsisten.|
|Postur keamanan keseluruhan|Risiko pelanggaran data di masa depan menurun dan ketahanan keamanan jaringan organisasi semakin kuat dalam jangka panjang.|

---

## 💡 Insights and lessons learned <a name="insight">

Hasil penilaian risiko memperlihatkan bahwa insiden kebocoran data terjadi karena praktik keamanan yang belum kuat dan penerapan pengerasan jaringan yang tidak merata. Penggunaan kata sandi bersama, kredensial administrator bawaan, konfigurasi firewall yang kurang tepat, serta ketiadaan autentikasi multifaktor menciptakan celah serius bagi akses tanpa izin.

Identifikasi kerentanan membantu menggambarkan area dengan tingkat risiko tinggi hingga kritis secara lebih jelas. Rekomendasi difokuskan pada penguatan kontrol akses, perbaikan proses autentikasi, dan perlindungan lalu lintas jaringan. Pendekatan ini disusun agar dapat diterapkan secara konsisten dan tetap selaras dengan standar keamanan jaringan yang umum digunakan.

Penerapan langkah pengerasan jaringan tersebut mampu menekan risiko kebocoran data di masa mendatang secara signifikan. Kontrol akses menjadi lebih terkelola, visibilitas aktivitas jaringan meningkat, dan perlindungan data pengguna menjadi lebih andal. Strategi ini membantu organisasi membangun postur keamanan yang lebih matang sekaligus menjaga kepercayaan pengguna dan stabilitas operasional jangka panjang.
