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
<img width="1200" height="915" alt="Screenshot 2026-01-13 002210" src="https://github.com/user-attachments/assets/92499ffb-151a-435d-b556-7649058dfd01" />
<img width="630" height="193" alt="Screenshot 2026-01-13 002219" src="https://github.com/user-attachments/assets/412da2fc-fbc0-4909-a481-9b35252412e5" />
<img width="1103" height="148" alt="Screenshot 2026-01-13 002152" src="https://github.com/user-attachments/assets/5ab4b7de-abc2-4f0c-8b40-e66c742c08a8" />

## 6. Hasil dan Pembahasan
<img width="1103" height="148" alt="Screenshot 2026-01-13 002152" src="https://github.com/user-attachments/assets/31726a81-12bc-4357-b08f-7886fd67cac4" />

Berdasarkan hasil eksekusi program tinychain.py, dapat diamati bahwa setiap proses penambangan menghasilkan nilai hash blok yang berbeda walaupun jumlah blok yang diproses tetap sama. Perbedaan ini terjadi karena mekanisme Proof of Work mengharuskan sistem mencari nilai nonce secara berulang hingga diperoleh hash yang memenuhi syarat tertentu, yaitu memiliki awalan nol (0000). Variasi nilai hash yang dihasilkan menunjukkan karakteristik fungsi hash yang sangat peka terhadap perubahan kecil pada input. Selain itu, hasil ini membuktikan bahwa Proof of Work memerlukan proses komputasi berulang sebelum sebuah blok dinyatakan valid, sehingga mekanisme ini berperan penting dalam menjaga keamanan dan keutuhan blockchain dengan membuat pemalsuan blok menjadi sulit dan membutuhkan sumber daya komputasi yang besar.

## 7. Jawaban Pertanyaan
1. Mengapa fungsi hash sangat penting dalam blockchain?
Fungsi hash digunakan untuk menjaga integritas data pada blockchain. Setiap blok memiliki nilai hash unik yang menghubungkan blok satu dengan lainnya, sehingga setiap perubahan data dapat langsung terdeteksi dan mencegah manipulasi.

2. Bagaimana Proof of Work mencegah double spending?
Proof of Work mencegah double spending dengan mewajibkan proses penambangan yang memerlukan perhitungan komputasi tinggi sebelum transaksi dapat divalidasi dan dicatat ke dalam blockchain, sehingga transaksi ganda sulit dilakukan.

3. Apa kelemahan dari PoW dalam hal efisiensi energi?
Proof of Work membutuhkan konsumsi energi yang besar karena proses pencarian hash dilakukan secara berulang, sehingga dinilai kurang efisien dan berdampak pada penggunaan energi yang berlebihan.

## 8. Kesimpulan
Berdasarkan hasil simulasi Proof of Work menggunakan program tinychain.py, dapat disimpulkan bahwa mekanisme PoW mampu menggambarkan prinsip kerja dan keamanan dasar pada sistem blockchain. Setiap proses penambangan menghasilkan nilai hash blok yang berbeda meskipun jumlah blok dan data yang digunakan sama, yang disebabkan oleh pencarian nilai nonce secara berulang hingga memenuhi tingkat kesulitan tertentu. Hal ini menunjukkan sifat fungsi hash yang sangat sensitif terhadap perubahan kecil pada input serta menegaskan bahwa proses penambangan memerlukan usaha komputasi yang tidak sedikit. Dengan adanya proses ini, blockchain menjadi lebih aman karena pemalsuan atau perubahan data pada blok akan membutuhkan sumber daya komputasi yang besar dan sulit dilakukan. Meskipun demikian, simulasi ini juga memperlihatkan bahwa Proof of Work memiliki kelemahan dari sisi efisiensi energi, sehingga dalam implementasi nyata diperlukan pertimbangan antara tingkat keamanan yang dihasilkan dan penggunaan sumber daya yang dibutuhkan.

## 9. Daftar Pustaka  
- Katz, J., & Lindell, Y. *Introduction to Modern Cryptography*.  
- Stallings, W. *Cryptography and Network Security*.  )


## 10. Commit Log
commit abc12345
Author: Safira Dewi Rahmatika safiraa1026@gmail.com
Date:   2026-01-13
week13-tiny-chain : implementasi tinychain
