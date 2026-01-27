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
* Blockchain: Ethereum (Sepolia Testnet)
* Smart Contract: Solidity
* Wallet: MetaMask
* Library Blockchain: Ethers.js
* Frontend: HTML, CSS, JavaScript
-  Kriptografi:
  - Hashing (Keccak-256)
  - Digital Signature (ECDSA Ethereum)

## Deskripsi Sistem
Sistem BlockAttend merupakan sistem absensi mahasiswa berbasis blockchain yang 
dirancang untuk mencatat dan menyimpan data kehadiran secara aman, transparan, dan 
tidak dapat dimanipulasi. Sistem ini memanfaatkan teknologi blockchain Ethereum pada 
jaringan Sepolia testnet sebagai media penyimpanan data absensi, sehingga setiap data 
kehadiran tercatat sebagai transaksi yang bersifat permanen (immutable). Dalam sistem ini, 
proses absensi dilakukan oleh mahasiswa menggunakan akun wallet Ethereum masing
masing yang terhubung melalui MetaMask. Wallet tersebut berfungsi sebagai identitas 
digital mahasiswa yang terautentikasi secara kriptografis. Data absensi yang dikirimkan ke 
sistem akan diproses oleh smart contract, kemudian disimpan di dalam blockchain dan dapat 
diverifikasi oleh dosen maupun pihak terkait. 
Aktor yang terlibat dalam sistem ini meliputi: 
1. Mahasiswa, sebagai pihak yang melakukan absensi. 
2. Dosen, sebagai pihak yang memantau dan memverifikasi kehadiran mahasiswa. 
3. Blockchain Ethereum, sebagai media penyimpanan data absensi yang bersifat 
terdesentralisasi. 

## Alur Proses Sistem 
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
Alur ini memastikan bahwa setiap proses absensi tercatat secara aman dan tidak dapat 
dimanipulasi.

## Algoritma Kriptografi yang Digunakan 
Sistem BlockAttend memanfaatkan beberapa algoritma kriptografi yang secara default 
digunakan dalam jaringan Ethereum, yaitu: 
1. Fungsi Hash Keccak-256 
Keccak-256 digunakan sebagai fungsi hash untuk mengamankan data transaksi 
dalam blockchain Ethereum. Fungsi hash ini menghasilkan nilai hash unik yang 
mewakili data absensi. Setiap perubahan kecil pada data akan menghasilkan nilai 
hash yang berbeda, sehingga integritas data dapat terjaga. 
2. Kriptografi Kunci Publik (Elliptic Curve Cryptography – ECC) 
Ethereum menggunakan algoritma kriptografi kunci publik berbasis kurva eliptik 
untuk proses penandatanganan transaksi. Setiap pengguna memiliki pasangan 
kunci publik dan kunci privat yang digunakan untuk menandatangani transaksi 
absensi, sehingga menjamin keaslian dan identitas pengirim.

##  Protokol Blockchain Ethereum dalam Sistem 
Sistem BlockAttend memanfaatkan protokol blockchain Ethereum dalam proses pencatatan 
data absensi. Setiap transaksi absensi yang dikirimkan oleh mahasiswa akan diproses 
melalui jaringan Ethereum, divalidasi oleh node, dan kemudian dimasukkan ke dalam blok 
yang terhubung secara kriptografis.Proses konsensus dalam jaringan Ethereum memastikan 
bahwa hanya transaksi yang valid yang dapat dicatat ke dalam blockchain. Dengan 
mekanisme ini, sistem mampu mencegah terjadinya manipulasi data dan memastikan bahwa 
setiap absensi tercatat secara permanen dan dapat diverifikasi oleh publik.

## Implementasi Smart Contract Absensi 
Smart contract berperan sebagai komponen utama dalam sistem BlockAttend. Di dalam 
smart contract ditanamkan aturan absensi yang mengatur proses pencatatan kehadiran 
mahasiswa. Setiap transaksi absensi yang dikirimkan oleh mahasiswa akan diproses oleh 
smart contract sesuai dengan aturan yang telah ditentukan. Salah satu aturan utama yang 
diterapkan adalah pembatasan satu kali absensi dalam satu hari untuk setiap alamat wallet. 
Aturan ini diterapkan secara otomatis oleh smart contract, sehingga tidak dapat diubah atau 
dimanipulasi oleh pihak manapun. Dengan demikian, smart contract tidak hanya berfungsi 
sebagai penyimpan data, tetapi juga sebagai pengendali logika sistem absensi. 

## Penerapan Kriptografi 
Penerapan kriptografi dalam sistem BlockAttend terjadi secara langsung pada proses 
absensi mahasiswa. Ketika mahasiswa melakukan absensi, transaksi yang dikirimkan ke 
smart contract akan ditandatangani secara digital menggunakan private key dari wallet 
MetaMask masing-masing. Proses penandatanganan ini menjamin bahwa transaksi benar
benar berasal dari pemilik wallet yang sah. Selain itu, data absensi yang dicatat ke dalam 
blockchain diamankan menggunakan fungsi hash kriptografi yang menjadi bagian dari 
mekanisme blockchain Ethereum. Setiap transaksi absensi memiliki hash unik yang 
terhubung dengan blok sebelumnya, sehingga perubahan data absensi tidak dimungkinkan 
tanpa merusak keseluruhan struktur blockchain. 

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

## Cara Mengakses Aplikasi 
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

## Panduan Penggunaan untuk Mahasiswa 
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

## Panduan Penggunaan untuk Admin 
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

## Hasil Pengujian 
Berdasarkan hasil pengujian yang telah dilakukan, diperoleh hasil sebagai berikut: 
1. Sistem berhasil menghubungkan wallet MetaMask sebagai identitas mahasiswa. 
2. Proses absensi berhasil dikirim sebagai transaksi ke blockchain Ethereum Sepolia. 
3. Data absensi tercatat secara permanen dan tidak dapat diubah setelah transaksi 
dikonfirmasi. 
4. Smart contract berhasil menolak absensi ganda dalam satu hari. 
5. Data absensi dapat ditampilkan kembali melalui aplikasi dan diverifikasi 
menggunakan blockchain explorer. 
Hasil ini menunjukkan bahwa sistem BlockAttend telah berjalan sesuai dengan desain dan 
tujuan yang diharapkan.

## ANALISIS KEAMANAN 
- Keamanan Data Absensi 
Keamanan data absensi pada sistem BlockAttend dijamin melalui penerapan teknologi 
blockchain dan kriptografi. Data absensi yang tersimpan di blockchain bersifat immutable, 
sehingga tidak dapat diubah atau dihapus oleh pihak manapun setelah tercatat. Hal ini 
meningkatkan kepercayaan terhadap keakuratan data kehadiran mahasiswa.
- Pencegahan Kecurangan dan Serangan 
Sistem BlockAttend dirancang untuk mencegah berbagai bentuk kecurangan, seperti 
pemalsuan absensi dan manipulasi data. Autentikasi berbasis wallet Ethereum memastikan 
bahwa setiap absensi dilakukan oleh pemilik akun yang sah. Selain itu, penggunaan tanda 
tangan digital dan smart contract mampu mencegah terjadinya absensi ganda maupun 
perubahan data absensi. Potensi serangan seperti pemalsuan identitas dan perubahan data 
dapat diminimalisir karena setiap transaksi harus ditandatangani secara kriptografis dan 
diverifikasi oleh jaringan blockchain. 
- Keterbatasan Keamanan Sistem 
Meskipun memiliki tingkat keamanan yang tinggi, sistem BlockAttend masih memiliki 
beberapa keterbatasan, antara lain ketergantungan pada keamanan wallet pengguna serta 
waktu konfirmasi transaksi blockchain. Selain itu, sistem belum dilengkapi dengan 
mekanisme pemulihan apabila pengguna kehilangan akses ke wallet mereka. 

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

