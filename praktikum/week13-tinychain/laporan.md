# Laporan Praktikum Kriptografi
Minggu ke-: XIII
Topik: tiny-chain 
Nama: Safira Dewi Rahmatika
NIM: 230202784 
Kelas: 5IKRB

## 1. Tujuan
1. Menjelaskan fungsi hash dalam menjaga integritas dan keterkaitan data pada sistem blockchain.
2. Melakukan percobaan sederhana mekanisme Proof of Work (PoW) untuk memahami proses penambangan blok.
3. Menganalisis tingkat keamanan cryptocurrency yang dibangun berdasarkan prinsip-prinsip kriptografi.

## 2. Dasar Teori
Hash function merupakan komponen fundamental dalam teknologi blockchain yang berfungsi untuk menjaga integritas, keaslian, dan keamanan data. Setiap transaksi dan blok dalam blockchain akan diproses menggunakan fungsi hash sehingga menghasilkan nilai hash yang unik dan bersifat satu arah. Nilai hash ini digunakan untuk menghubungkan satu blok dengan blok sebelumnya, membentuk sebuah rantai yang saling terkait. Apabila terjadi perubahan sekecil apa pun pada data dalam suatu blok, maka nilai hash yang dihasilkan akan berubah secara signifikan, sehingga manipulasi data dapat dengan mudah terdeteksi dan merusak keseluruhan struktur blockchain. Selain itu, hash function juga berperan dalam proses validasi transaksi dan menjaga konsistensi data di seluruh jaringan.

Dalam blockchain, mekanisme Proof of Work (PoW) digunakan sebagai metode konsensus untuk memverifikasi transaksi dan menambahkan blok baru ke dalam jaringan. Pada PoW, penambang diwajibkan melakukan perhitungan hash secara berulang untuk menemukan nilai tertentu yang memenuhi tingkat kesulitan yang telah ditetapkan, seperti adanya sejumlah karakter nol di awal hash. Proses ini memerlukan usaha komputasi dan waktu yang cukup besar, sehingga bertujuan untuk mencegah pihak yang tidak bertanggung jawab melakukan pemalsuan data atau manipulasi transaksi. Simulasi PoW membantu memahami bahwa proses penambangan bukan hanya sekadar pembuatan blok, tetapi juga sebagai mekanisme keamanan yang membuat serangan terhadap jaringan menjadi mahal dan sulit dilakukan.

Keamanan cryptocurrency sangat bergantung pada penerapan prinsip-prinsip kriptografi, termasuk penggunaan hash function, kriptografi kunci publik, dan mekanisme konsensus seperti Proof of Work. Kriptografi memastikan bahwa transaksi yang terjadi bersifat aman, transparan, dan tidak dapat diubah setelah dicatat dalam blockchain. Setiap pengguna memiliki kunci privat yang digunakan untuk menandatangani transaksi, sehingga hanya pemilik sah yang dapat mengakses dan memindahkan aset digitalnya. Meskipun demikian, sistem cryptocurrency tetap memiliki tantangan keamanan, seperti risiko serangan 51% dan kelalaian pengguna dalam menjaga kunci privat. Oleh karena itu, pemahaman terhadap kriptografi dan penerapannya sangat penting untuk menjaga keamanan dan kepercayaan dalam ekosistem cryptocurrency.

## 3. Alat dan Bahan
- Python 3.14  
- Visual Studio Code   
- Git dan akun GitHub  

## 4. Langkah Percobaan
1. Menyusun struktur blok yang berisi data transaksi, hash blok sebelumnya, nonce, dan nilai hash.
2. Menghubungkan beberapa blok secara berurutan untuk membentuk sebuah blockchain.
3. Melakukan analisis terhadap mekanisme Proof of Work dengan mengamati proses pencarian hash yang memenuhi tingkat kesulitan tertentu.

## 5. Source Code

## 6. Hasil dan Pembahasan


## 7. Jawaban Pertanyaan
1. Mengapa fungsi hash sangat penting dalam blockchain?
Fungsi hash digunakan untuk menjaga integritas data pada blockchain. Setiap blok memiliki nilai hash unik yang menghubungkan blok satu dengan lainnya, sehingga setiap perubahan data dapat langsung terdeteksi dan mencegah manipulasi.

2. Bagaimana Proof of Work mencegah double spending?
Proof of Work mencegah double spending dengan mewajibkan proses penambangan yang memerlukan perhitungan komputasi tinggi sebelum transaksi dapat divalidasi dan dicatat ke dalam blockchain, sehingga transaksi ganda sulit dilakukan.

3. Apa kelemahan dari PoW dalam hal efisiensi energi?
Proof of Work membutuhkan konsumsi energi yang besar karena proses pencarian hash dilakukan secara berulang, sehingga dinilai kurang efisien dan berdampak pada penggunaan energi yang berlebihan.

## 8. Kesimpulan


## 9. Daftar Pustaka  
- Katz, J., & Lindell, Y. *Introduction to Modern Cryptography*.  
- Stallings, W. *Cryptography and Network Security*.  )


## 10. Commit Log
commit abc12345
Author: Safira Dewi Rahmatika safiraa1026@gmail.com
Date:   2026-01-13
week13-tiny-chain : implementasi tinychain
