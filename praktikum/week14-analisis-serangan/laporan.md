# Laporan Praktikum Kriptografi
Minggu ke-: 14  
Topik: Analisis serangan
Nama: Safira Dewi Rahmatika 
NIM: 230202784
Kelas: 5IKRB

## 1. Tujuan
1. Mengidentifikasi jenis serangan pada sistem informasi nyata.
2. Mengevaluasi kelemahan algoritma kriptografi yang digunakan.
3. Memberikan rekomendasi algoritma kriptografi yang sesuai untuk perbaikan keamanan.

## 2. Dasar Teori
Sistem informasi nyata rentan terhadap berbagai jenis serangan siber yang bertujuan untuk mencuri, merusak, atau memanipulasi data. Jenis serangan yang umum terjadi antara lain SQL Injection, Man-in-the-Middle, brute force, phishing, dan malware. Serangan-serangan tersebut biasanya memanfaatkan kelemahan pada desain sistem, konfigurasi keamanan yang kurang baik, serta kurangnya penerapan mekanisme pengamanan data. Identifikasi jenis serangan menjadi langkah awal yang penting untuk memahami bagaimana ancaman bekerja dan bagian sistem mana yang paling rentan untuk diserang.

Selain serangan langsung pada sistem, kelemahan juga sering ditemukan pada algoritma kriptografi yang digunakan untuk mengamankan data. Penggunaan algoritma yang sudah usang atau implementasi kriptografi yang tidak sesuai standar dapat menyebabkan data mudah didekripsi oleh pihak yang tidak berwenang. Contohnya adalah penggunaan algoritma hash yang lemah untuk penyimpanan kata sandi atau penggunaan kunci enkripsi dengan panjang yang tidak memadai. Evaluasi terhadap algoritma kriptografi diperlukan untuk memastikan bahwa metode pengamanan yang diterapkan masih relevan terhadap perkembangan teknologi dan kemampuan komputasi saat ini.

Untuk meningkatkan keamanan sistem informasi, diperlukan rekomendasi algoritma kriptografi yang lebih kuat dan sesuai dengan kebutuhan sistem. Algoritma modern dengan tingkat keamanan tinggi, efisiensi yang baik, serta dukungan standar internasional dapat digunakan sebagai solusi perbaikan. Selain pemilihan algoritma yang tepat, penerapan manajemen kunci yang baik dan kombinasi dengan mekanisme keamanan lain seperti autentikasi berlapis juga sangat dianjurkan. Dengan demikian, sistem informasi dapat terlindungi secara lebih optimal dari berbagai ancaman keamanan yang terus berkembang.

## 3. Alat dan Bahan
- Python 3. 14 
- Visual Studio Code 
- Git dan akun GitHub  

## 4. Langkah Percobaan
1. Mengidentifikasi serangan
- Kasus yang dipilih:
Serangan brute force dan dictionary attack terhadap password yang disimpan menggunakan algoritma MD5 pada sistem informasi lama (misalnya sistem akademik atau website lama).
- Vektor serangan:
Penyerang memperoleh database pengguna yang berisi hash password MD5 akibat kebocoran data atau celah keamanan sistem. Hash tersebut kemudian diproses menggunakan rainbow table atau serangan brute force untuk mencocokkan hash dengan password asli.
- Penyebab kelemahan:
Kelemahan utama terjadi karena MD5 merupakan algoritma hash yang cepat dan tidak dirancang untuk penyimpanan password. Selain itu, sistem tidak menggunakan salt pada hash password, sehingga penyerang dapat dengan mudah mencocokkan hash yang sama untuk banyak akun. Tidak adanya pembatasan percobaan login juga memperbesar peluang keberhasilan serangan.

3. Evaluasi kelemahan
Analisis kelemahan algoritma:
MD5 memiliki kelemahan kriptografis serius, seperti kecepatan komputasi yang tinggi dan kerentanan terhadap collision. Hal ini memungkinkan penyerang melakukan jutaan percobaan hash dalam waktu singkat menggunakan perangkat keras modern.
Jenis kelemahan:
Kelemahan pada kasus ini berasal dari dua aspek, yaitu:
- Kelemahan algoritma 
MD5 sudah tidak aman dan tidak direkomendasikan untuk keamanan password.
- Kelemahan implementasi & konfigurasi
Tidak menggunakan salt, tidak ada rate limiting, dan tidak menerapkan kebijakan password yang kuat. Dengan demikian, meskipun sistem menggunakan hash, perlindungan yang diberikan tetap sangat lemah.

5. Rekomendasi solusi
Algoritma dan mekanisme yang disarankan:
- Mengganti MD5 dengan algoritma hash khusus password seperti bcrypt, scrypt, atau Argon2.
- Menambahkan salt unik untuk setiap password.
- Menerapkan rate limiting, account lockout, dan autentikasi multi-faktor (MFA).
Alasan pemilihan dan dampak keamanan:
Algoritma seperti bcrypt, scrypt, dan Argon2 dirancang agar proses hashing berjalan lambat dan membutuhkan sumber daya besar, sehingga serangan brute force menjadi tidak efisien. Dengan penerapan salt dan mekanisme pengamanan tambahan, kebocoran database tidak langsung membahayakan akun pengguna. Dampaknya, sistem menjadi jauh lebih tahan terhadap serangan kriptografi modern dan meningkatkan perlindungan data pengguna secara signifikan.
6. Membuat percobaan brute force sederhana
7. Membuat laporan
   
## 5. Source Code
<img width="691" height="445" alt="image" src="https://github.com/user-attachments/assets/4f362902-9d46-4db8-b49a-e923bc59a1a2" />

## 6. Hasil dan Pembahasan
<img width="564" height="114" alt="image" src="https://github.com/user-attachments/assets/4b3946ba-34da-4fbf-9f2d-75edb497a8a2" />

Program berhasil menemukan password "123" hanya dengan mencoba beberapa kemungkinan sederhana. Hal ini menunjukkan bahwa MD5 sangat cepat dihitung, Password sederhana mudah ditebak, Tanpa salt, hash bisa langsung dicocokkan.

## 7. Jawaban Pertanyaan
1. Mengapa banyak sistem lama masih rentan terhadap brute force atau dictionary attack?
Banyak sistem lama masih rentan karena menggunakan mekanisme autentikasi yang sudah tidak aman, seperti password tanpa hashing yang kuat atau tanpa salt. Selain itu, sistem lama sering kali tidak menerapkan pembatasan percobaan login (login attempt limit) atau jeda waktu (delay) setelah beberapa kali gagal. Faktor lain adalah kebijakan password yang lemah, misalnya panjang password pendek atau penggunaan kata sandi umum, sehingga memudahkan penyerang melakukan brute force atau dictionary attack secara otomatis.

2. Apa bedanya kelemahan algoritma dengan kelemahan implementasi?
Kelemahan algoritma berkaitan dengan desain dasar algoritma kriptografi itu sendiri, misalnya algoritma yang secara matematis sudah terbukti tidak aman atau mudah dipecahkan. Sementara itu, kelemahan implementasi terjadi ketika algoritma yang sebenarnya aman diterapkan dengan cara yang salah, seperti penggunaan kunci yang terlalu pendek, penyimpanan kunci yang tidak aman, atau kesalahan konfigurasi sistem. Dengan kata lain, algoritma bisa saja kuat, tetapi jika implementasinya keliru, sistem tetap menjadi tidak aman.

3. Bagaimana organisasi dapat memastikan sistem kriptografi mereka tetap aman di masa depan?
Organisasi dapat memastikan keamanan kriptografi dengan melakukan pembaruan algoritma dan standar keamanan secara berkala sesuai perkembangan teknologi. Selain itu, audit keamanan dan pengujian sistem secara rutin perlu dilakukan untuk mendeteksi kelemahan sejak dini. Organisasi juga harus menerapkan manajemen kunci yang baik, pelatihan keamanan bagi pengembang dan administrator, serta mengikuti rekomendasi dan standar keamanan yang diakui secara internasional agar sistem kriptografi tetap andal menghadapi ancaman di masa depan.

## 8. Kesimpulan
Dari hasil percobaan dapat disimpulkan bahwa penggunaan algoritma hash lemah seperti MD5 sangat berisiko untuk pengamanan password. Kelemahan ini disebabkan oleh kecepatan komputasi MD5 yang tinggi dan tidak adanya mekanisme pengamanan tambahan seperti salt. Oleh karena itu, sistem informasi modern disarankan untuk menggunakan algoritma hash khusus password yang lebih aman, seperti bcrypt, scrypt, atau Argon2, guna meningkatkan ketahanan sistem terhadap serangan kriptografi.

## 9. Daftar Pustaka
(Cantumkan referensi yang digunakan.  
Contoh:  
- Katz, J., & Lindell, Y. *Introduction to Modern Cryptography*.  
- Stallings, W. *Cryptography and Network Security*.  )

---

## 10. Commit Log
commit abc12345
Author: safira dewi rahmatika safiraa1026@gmail.com
Date:   2025-01-18

   wek14-analisis serangan : Percobaan brute force sederhana
