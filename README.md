# Network hardening risk assessment

## 📑 Table of contents

1. [Introduction](#introduction)
2. [Incident scenario](#scenario)
3. [Security risk assessment report](#report)
4. [Conclusion](#conclusion)

---

## 👋 Introduction <a name="introduction">

Studi ini disusun sebagai latihan cybersecurity yang berfokus pada upaya memperkuat keamanan jaringan setelah terjadinya kebocoran data di sebuah organisasi media sosial. Skenario yang digunakan menggambarkan situasi ketika celah jaringan tidak terpantau dengan baik dan akhirnya berdampak langsung pada data pelanggan. Kondisi ini menjadi titik awal untuk memahami risiko yang muncul ketika masalah keamanan tidak segera ditangani.

Pembahasan ini merujuk pada materi dalam program Google Cybersecurity Professional Certificate, khususnya course Connect and Protect: Networks and Network Security. Fokus analisis diarahkan pada pengenalan kerentanan jaringan serta penerapan langkah network hardening yang relevan, seperti pengaturan akses, konfigurasi firewall, dan mekanisme autentikasi. Tujuan akhirnya adalah menunjukkan bagaimana penguatan jaringan yang dilakukan secara konsisten dapat mencegah insiden serupa dan meningkatkan keamanan organisasi di masa depan.

---

## 💭 Incident scenario <a name="scenario">

Saya berperan sebagai analis keamanan siber di sebuah organisasi media sosial yang baru saja mengalami kebocoran data dalam skala besar. Insiden ini membuka kemungkinan tereksposnya data pribadi pengguna, seperti nama dan alamat, ke pihak yang tidak berhak. Situasi ini langsung memicu kekhawatiran karena data pengguna adalah aset penting yang sangat memengaruhi kepercayaan publik.

Infrastruktur jaringan turut memperlihatkan celah yang cukup serius. Keempat celah tersebut adalah:
- Kata sandi bersama karyawan organisasi.
- Kata sandi admin untuk basis data diatur ke default.
- Firewall tidak memiliki aturan untuk menyaring lalu lintas yang masuk dan keluar dari jaringan.
- Otentikasi multifaktor (MFA) tidak digunakan.

Temuan ini menunjukkan bahwa pelanggaran data terjadi akibat kombinasi dari praktik keamanan yang lemah dan kurangnya penerapan network hardening secara konsisten. Risiko serupa berpotensi muncul kembali jika kondisi ini dibiarkan, dengan dampak yang lebih besar terhadap keamanan data dan reputasi perusahaan.

---

## 📋 Security risk assessment report<a name="report">

### Social media organization network hardening

Laporan penilaian risiko keamanan ini dibuat untuk melihat kondisi keamanan jaringan di sebuah organisasi media sosial yang baru saja mengalami kebocoran data besar. Insiden tersebut berdampak langsung pada perlindungan data pribadi pengguna, seperti nama dan alamat, serta menimbulkan risiko serius terhadap kepercayaan publik dan reputasi perusahaan.

Penilaian ini bertujuan menemukan kelemahan utama yang memicu terjadinya pelanggaran dan menilai risiko lanjutan jika celah tersebut tidak segera diperbaiki. Proses analisis dilakukan dengan meninjau pengelolaan akses, pengaturan jaringan, dan mekanisme autentikasi yang digunakan di lingkungan organisasi.

Hasil penilaian diharapkan dapat menjadi landasan untuk menyusun langkah network hardening yang lebih kuat dan konsisten. Pendekatan ini bertujuan mencegah insiden serupa di masa depan sekaligus memperkuat keamanan jaringan secara menyeluruh.

#### Identified vulnerabilities

Pemeriksaan awal terhadap sistem dan jaringan menunjukkan beberapa celah keamanan yang berperan dalam terjadinya kebocoran data. Masalah ini muncul dari kombinasi kelemahan teknis dan kebiasaan keamanan yang belum dijalankan secara konsisten.

|Kerentanan|Penjelasan|
|---|---|
|A. Shared employee passwords|Sejumlah karyawan memakai kata sandi yang sama untuk mengakses sistem internal. Pola ini menyulitkan pelacakan aktivitas pengguna dan meningkatkan risiko penyalahgunaan akses. Satu akun yang berhasil ditembus dapat membuka jalan ke sistem lain yang memakai kredensial serupa.|
|B. Default database administrator password|Akun administrator database masih menggunakan kata sandi default sejak awal sistem digunakan. Kondisi ini memudahkan penyerang mencoba teknik umum seperti brute force atau menebak kredensial untuk mendapatkan akses penuh.|
|C. Unconfigured firewall rules|Firewall belum diatur dengan aturan penyaringan lalu lintas yang jelas. Lalu lintas masuk dan keluar jaringan berjalan tanpa batasan yang memadai, sehingga peluang akses tidak sah dari luar jaringan menjadi lebih besar.|
|D. Absence of Multi-Factor Authentication (MFA)|Autentikasi multifaktor belum diterapkan pada akun pengguna maupun akun dengan hak akses tinggi. Proses login masih bergantung pada username dan password, yang membuat sistem rentan saat kredensial bocor atau dicuri.|

#### Risk analysis

Analisis risiko dilakukan dengan menilai kemungkinan terjadinya eksploitasi serta dampak yang ditimbulkan jika setiap kerentanan dimanfaatkan oleh pihak tidak berwenang. Hasil penilaian menunjukkan bahwa sebagian besar kerentanan berada pada tingkat risiko tinggi hingga kritis dan memerlukan penanganan segera.

|Kerentanan|Likelihood|Impact|Risk level|
|---|---|---|---|
|---|---|---|---|
