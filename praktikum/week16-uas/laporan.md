# Laporan Praktikum Kriptografi
Minggu ke-: 16
Topik: SISTEM ABSENSI MAHASISWA BERBASIS BLOCKCHAIN 
(ETHERUM SEPOLIA)
Nama: Safira Dewi Rahmatika
NIM: 230202784
Kelas: 5IKRB

## 1. Latar belakang
Perkembangan teknologi informasi mendorong perguruan tinggi untuk bertransformasi ke sistem digital, termasuk dalam proses absensi mahasiswa. Sistem absensi konvensional, baik manual maupun digital terpusat, masih memiliki berbagai kelemahan seperti rawan kecurangan, kesalahan pencatatan, manipulasi data, ketergantungan pada satu server, serta kurangnya transparansi dan keamanan data. Untuk mengatasi permasalahan tersebut, teknologi blockchain dan kriptografi ditawarkan sebagai solusi karena mampu menjamin keamanan, integritas, dan keaslian data melalui sistem pencatatan terdistribusi dan mekanisme hash kriptografi yang bersifat immutable. Dengan blockchain, data kehadiran mahasiswa dapat dicatat sebagai transaksi yang tervalidasi dan tidak dapat diubah, serta menghilangkan ketergantungan pada pihak pusat.

Berdasarkan hal tersebut, dirancang sistem absensi mahasiswa berbasis blockchain bernama BlockAttend yang menggunakan jaringan Ethereum Sepolia testnet dan autentikasi wallet MetaMask sebagai identitas mahasiswa. Setiap absensi ditandatangani secara kriptografis dan dicatat permanen di blockchain, sementara smart contract digunakan untuk mengatur aturan absensi secara otomatis guna mencegah kecurangan. Sistem BlockAttend diharapkan mampu meningkatkan keamanan, efisiensi, transparansi, dan kepercayaan dalam proses absensi mahasiswa, sekaligus menjadi contoh penerapan teknologi blockchain dan kriptografi dalam mendukung digitalisasi sistem akademik yang modern dan berintegritas.

## 2. Tujuan
Tujuan dari perancangan dan pembangunan sistem BlockAttend (Sistem Absensi 
Mahasiswa Berbasis Blockchain) adalah sebagai berikut: 
1. Membangun sistem absensi digital berbasis blockchain yang mampu mencatat data 
kehadiran mahasiswa secara aman, transparan, dan tidak dapat dimanipulasi. 
2. Mengimplementasikan teknologi blockchain Ethereum sebagai media 
penyimpanan data absensi sehingga setiap transaksi kehadiran tercatat secara 
permanen (immutable) dan dapat diverifikasi secara publik. 
3. Mengintegrasikan autentikasi wallet digital (MetaMask) sebagai identitas 
mahasiswa dalam melakukan absensi, sehingga setiap mahasiswa memiliki akun 
unik yang terhubung langsung ke sistem. 
4. Menerapkan konsep smart contract untuk mengatur aturan absensi, seperti 
pembatasan satu kali absensi dalam satu hari guna mencegah kecurangan. 

## 3. Alat dan Bahan
- Python 3.x  
- Visual Studio Code 
- Git dan akun GitHub  
- MetaMask 

## 4. Langkah Percobaan (Panduan)
Alur kerja sistem absensi BlockAttend dapat dijelaskan sebagai berikut: 
1. Mahasiswa membuka aplikasi dan menghubungkan wallet MetaMask. 
2. Sistem melakukan autentikasi pengguna berdasarkan alamat wallet Ethereum. 
3. Mahasiswa melakukan absensi dengan mengirimkan transaksi ke smart contract. 
4. Transaksi absensi ditandatangani secara kriptografis menggunakan private key 
wallet pengguna. 
5. Smart contract memverifikasi aturan absensi dan mencatat data kehadiran ke dalam 
blockchain. 
6. Data absensi yang telah tersimpan dapat dilihat dan diverifikasi oleh dosen melalui 
aplikasi. 
Alur ini memasti

Cara Mengakses Aplikasi 
Langkah-langkah mengakses aplikasi BlockAttend adalah sebagai 
berikut: 
1) Buka browser dan jalankan aplikasi BlockAttend melalui file 
index.html. atau melalui alamat yang telah disediakan. 
2) Pastikan ekstensi MetaMask telah aktif. 
3) Klik tombol Connect Wallet pada halaman utama aplikasi. 
4) MetaMask akan menampilkan permintaan koneksi wallet. 
5) Pilih akun wallet yang akan digunakan dan konfirmasi koneksi. 
6) Setelah berhasil, alamat wallet akan ditampilkan dan status 
berubah menjadi Connected.

Panduan Penggunaan untuk Mahasiswa 
a. Mendaftarkan Nama Mahasiswa 
1) Pastikan wallet MetaMask sudah terhubung. 
2) Pada bagian Mahasiswa, masukkan Nama Lengkap pada 
kolom yang tersedia. 
3) Klik tombol Daftar Nama. 
4) Konfirmasi transaksi pada MetaMask. 
5) Tunggu hingga transaksi berhasil dan nama tersimpan di 
blockchain. 
b. Melakukan Absensi 
1) Pastikan wallet masih terhubung. 
2) Klik tombol Absen. 
3) MetaMask akan menampilkan konfirmasi transaksi. 
4) Klik Confirm untuk melanjutkan. 
5) Tunggu hingga transaksi berhasil diproses. 
6) Jika absensi berhasil, akan muncul keterangan Sudah Absen 
Hari Ini. 
Setiap mahasiswa hanya dapat melakukan absensi satu kali dalam satu 
hari sesuai aturan smart contract.

Panduan Penggunaan untuk Admin 
Admin memiliki akses untuk melihat seluruh data absensi mahasiswa. 
Langkah-langkah: 
1) Hubungkan wallet admin menggunakan MetaMask. 
2) Setelah terhubung, sistem akan menampilkan peran sebagai 
ADMIN. 
3) Klik tombol Lihat Semua Absensi. 
4) Sistem akan menampilkan tabel data absensi yang berisi: 
• Nama mahasiswa 
• Alamat wallet 
• Waktu absensi 
• Status kehadiran 
Data yang ditampilkan diambil langsung dari blockchain Ethereum 
Sepolia.

## 5. Source Code
Kode Autentikasi Wallet (Identitas Kriptografi) 

<img width="712" height="96" alt="Screenshot 2026-01-27 010840" src="https://github.com/user-attachments/assets/be65d118-7c82-4b26-8973-b5b394bdd644" />

Kode Transaksi Absensi (Digital Signature) 

<img width="399" height="82" alt="Screenshot 2026-01-27 011809" src="https://github.com/user-attachments/assets/1936d885-fcb7-4318-be07-28afd2f408fb" />

Kode Pemanggilan Smart Contract (Aturan Absensi) 

<img width="610" height="74" alt="Screenshot 2026-01-27 012214" src="https://github.com/user-attachments/assets/2fd4adae-e801-4e58-8aed-40ba89d6b493" />

Kode Cek Absen Hari Ini (Anti Kecurangan) 

<img width="658" height="98" alt="Screenshot 2026-01-27 012512" src="https://github.com/user-attachments/assets/def7049f-645b-4677-9d1b-baf84890afee" />

## 6. Hasil dan Pembahasan
Form Admin

<img width="732" height="364" alt="image" src="https://github.com/user-attachments/assets/ef226933-245e-44f8-932d-4a442b5971ee" />

Form Mahasiswa

<img width="734" height="385" alt="image" src="https://github.com/user-attachments/assets/c3328261-008a-427e-a605-7d18d00eb3c4" />

## 7. Jawaban Pertanyaan

## 8. Kesimpulan
Kesimpulan
Berdasarkan hasil perancangan, implementasi, dan pengujian yang telah dilakukan, dapat disimpulkan bahwa sistem BlockAttend berhasil menerapkan teknologi blockchain dan kriptografi dalam sistem absensi mahasiswa. Penggunaan blockchain Ethereum Sepolia mampu menjamin keamanan, keutuhan, dan transparansi data absensi. Integrasi wallet MetaMask dan smart contract juga efektif dalam mencegah manipulasi dan kecurangan dalam pencatatan kehadiran mahasiswa.

Saran
Untuk pengembangan selanjutnya, sistem BlockAttend dapat ditingkatkan dengan:
1.	Menggunakan jaringan blockchain private atau layer-2 untuk meningkatkan efisiensi.
2.	Menambahkan mekanisme autentikasi tambahan, seperti biometrik atau verifikasi multi-faktor.
3.	Mengembangkan fitur pelaporan dan integrasi dengan sistem akademik lainnya.

## 9. Daftar Pustaka
(Cantumkan referensi yang digunakan.  
Contoh:  
- Katz, J., & Lindell, Y. *Introduction to Modern Cryptography*.  
- Stallings, W. *Cryptography and Network Security*.  )

---

## 10. Commit Log
commit UAS Kriptografi
Author: Safira Dewi Rahmatika safiraa1026@gmail.com
Date:   2026-01-27

    week16-UAS Kriptografi: SISTEM ABSENSI MAHASISWA BERBASIS BLOCKCHAIN
(ETHERUM SEPOLIA)

