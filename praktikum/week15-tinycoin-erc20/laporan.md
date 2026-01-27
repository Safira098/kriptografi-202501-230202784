# Laporan Praktikum Kriptografi
Minggu ke-: 15  
Topik: Tinycoin 
Nama: Safira Dewi Rahmatika  
NIM: 230202784
Kelas: 5IKRB

## 1. Tujuan
1. Mengembangkan proyek sederhana berbasis algoritma kriptografi.
2. Mendokumentasikan proses implementasi proyek ke dalam repository Git.
3. Menyusun laporan teknis hasil proyek akhir.

## 2. Dasar Teori
Pengembangan proyek sederhana berbasis algoritma kriptografi bertujuan untuk menerapkan konsep keamanan informasi secara nyata dalam sebuah sistem. Melalui proyek ini, algoritma kriptografi digunakan untuk melindungi data penting, seperti menjaga kerahasiaan, integritas, dan keaslian informasi. Implementasi kriptografi dalam proyek sederhana juga membantu memahami cara kerja algoritma keamanan serta tantangan yang muncul dalam penerapannya pada sistem informasi.

Seluruh proses implementasi proyek didokumentasikan secara sistematis menggunakan sistem kontrol versi Git dan disimpan dalam repository daring seperti GitHub. Dokumentasi ini mencakup kode sumber, riwayat perubahan, serta penjelasan teknis mengenai cara kerja sistem. Dengan adanya dokumentasi yang baik, proses pengembangan menjadi lebih terstruktur, mudah ditelusuri, dan dapat digunakan sebagai bukti pengerjaan serta bahan evaluasi proyek.

Hasil akhir dari pengembangan proyek kemudian disusun dalam bentuk laporan teknis yang menjelaskan keseluruhan proses dan hasil implementasi. Laporan ini memuat latar belakang, tujuan, dasar teori kriptografi, metode pengembangan, hingga hasil pengujian sistem. Penyusunan laporan teknis bertujuan untuk memberikan gambaran komprehensif mengenai penerapan algoritma kriptografi serta mengevaluasi tingkat keamanan sistem yang dibangun, sehingga dapat menjadi referensi untuk pengembangan dan penelitian selanjutnya.

## 3. Alat dan Bahan
- Python 3. 14 
- Visual Studio Code / editor lain  
- Git dan akun GitHub  

## 4. Langkah Percobaan
1. Membuat kontrak ERC20
2. Deploy kontrak
3. Uji fungsionalitas
4. Dokumentasi

## 5. Source Code
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract TinyCoin is ERC20 {
    constructor(uint256 initialSupply) ERC20("TinyCoin", "TNC") {
        _mint(msg.sender, initialSupply);
    }
}

## 6. Hasil dan Pembahasan
<img width="1910" height="1078" alt="Screenshot 2026-01-25 211828" src="https://github.com/user-attachments/assets/c4e90622-ccb5-4b74-aebb-4eada6d7d7ee" />


## 7. Jawaban Pertanyaan
1. Apa fungsi utama ERC20 dalam ekosistem blockchain?
ERC20 berfungsi sebagai standar teknis untuk pembuatan dan pengelolaan token pada jaringan Ethereum. Fungsi utamanya adalah memastikan bahwa token yang dibuat memiliki struktur dan perilaku yang seragam, sehingga dapat dengan mudah digunakan oleh berbagai aplikasi terdesentralisasi (decentralized applications), dompet digital, dan platform pertukaran. Dengan adanya ERC20, interoperabilitas antar token dan aplikasi dalam ekosistem blockchain menjadi lebih terjamin dan efisien.

2. Bagaimana mekanisme transfer token bekerja dalam kontrak ERC20?
Mekanisme transfer token dalam kontrak ERC20 dilakukan melalui fungsi transfer() atau transferFrom() yang tersedia di dalam smart contract. Ketika pengguna melakukan transfer, kontrak akan memeriksa apakah saldo pengirim mencukupi, kemudian mengurangi saldo pengirim dan menambah saldo penerima sesuai jumlah token yang dikirim. Seluruh proses ini dicatat secara permanen di blockchain dan dieksekusi secara otomatis tanpa perantara, sehingga menjamin transparansi dan keandalan transaksi.

3. Apa risiko utama dalam implementasi smart contract dan bagaimana cara mitigasinya?
Risiko utama dalam implementasi smart contract meliputi kesalahan logika kode, kerentanan keamanan seperti reentrancy attack, serta kesalahan dalam pengelolaan hak akses. Karena smart contract bersifat tidak dapat diubah setelah dipublikasikan, kesalahan kecil dapat menyebabkan kerugian besar. Untuk mitigasi risiko tersebut, organisasi perlu menerapkan praktik pengembangan yang aman seperti audit kode secara menyeluruh, pengujian ekstensif, penggunaan library standar yang terpercaya, serta menerapkan mekanisme kontrol akses dan pembatasan fungsi penting. Dengan langkah-langkah ini, keamanan dan keandalan smart contract dapat ditingkatkan secara signifikan.

## 8. Kesimpulan
Berdasarkan praktikum minggu ke-15 dengan topik Tinycoin, dapat disimpulkan bahwa pengembangan proyek sederhana berbasis algoritma kriptografi melalui implementasi smart contract ERC20 memberikan pemahaman yang lebih nyata mengenai penerapan keamanan informasi dalam ekosistem blockchain. Standar ERC20 memungkinkan pembuatan token dengan struktur yang seragam sehingga dapat digunakan secara luas oleh berbagai aplikasi terdesentralisasi, dompet digital, maupun platform pertukaran.

Proses pembuatan dan deploy kontrak Tinycoin menunjukkan bahwa mekanisme transfer token dapat berjalan secara otomatis, transparan, dan tercatat permanen di blockchain tanpa memerlukan pihak perantara. Selain itu, praktikum ini juga memperlihatkan pentingnya pengujian serta dokumentasi proyek melalui GitHub agar pengembangan lebih terstruktur dan mudah ditelusuri.

Namun, implementasi smart contract juga memiliki risiko keamanan seperti kesalahan logika kode dan kerentanan serangan. Oleh karena itu, diperlukan audit kode, pengujian menyeluruh, serta penggunaan library terpercaya sebagai langkah mitigasi. Dengan demikian, praktikum ini berhasil memberikan pengalaman dalam membangun token sederhana sekaligus memahami aspek keamanan dan tantangan dalam pengembangan smart contract.

## 9. Daftar Pustaka
(Cantumkan referensi yang digunakan.  
Contoh:  
- Katz, J., & Lindell, Y. *Introduction to Modern Cryptography*.  
- Stallings, W. *Cryptography and Network Security*.  )

---

## 10. Commit Log

Author: Safira Dewi Rahmatika <safiraa1026@gmail.com>
Date:   2026-0-18

   week15-tinycoin : 
