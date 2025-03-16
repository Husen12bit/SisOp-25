# TUGAS SISTEM OPERASI MINGGU KE-3

---

#### Dosen Pengampu :
**Dr. Ferry Astika Saputra ST, M.Sc**

#### Disusun oleh :
**Muhammad Abdullah Husaini**
**(3214521030)**
D3-LA IT-A

---

>TUGAS
>- Membuat resume menggunakan bhs indonesia dari 1.35 proses management - 1.40 caching
>
**PROCESS MANAGEMENT**
- Definisi dan Konsep Dasar
    - Sebuah proses adalah program yang sedang dieksekusi, merupakan unit kerja dalam sistem.
    - Program adalah entitas pasif, sedangkan proses adalah entitas aktif.
    - Proses membutuhkan sumber daya untuk menyelesaikan tugasnya (CPU, memori, I/O, file, data inisialisasi).
- Karakteristik Proses
    - Setiap proses memiliki program counter yang menentukan lokasi instruksi berikutnya yang akan dieksekusi.
    - Proses single-threaded mengeksekusi instruksi secara sekuensial, satu per satu hingga selesai.
    - Proses multi-threaded memiliki satu program counter untuk setiap thread.
- Manajemen Sumber Daya
    - Ketika proses berakhir, sistem harus mengambil kembali sumber daya yang dapat digunakan kembali.
    - Sistem operasi biasanya memiliki banyak proses (baik pengguna maupun sistem) yang berjalan secara bersamaan pada satu atau lebih CPU.
    - Konkurensi dicapai dengan multiplexing CPU di antara proses/thread.
- Signifikansi dalam Sistem Operasi
    - Manajemen proses merupakan fungsi penting dalam sistem operasi modern.
    - Memungkinkan banyak tugas dijalankan secara efisien dan bersamaan.

<br>

**PROCESS MANAGEMENT ACTIVITIES**
- Sistem operasi bertanggung jawab untuk:
    - Membuat dan menghapus proses pengguna dan system
    - Menghentikan sementara dan melanjutkan proses
    - Menyediakan cara agar proses bisa bekerja selaras (sinkronisasi)
    - Menyediakan cara agar proses bisa berkomunikasi satu sama lain
    - Mengatasi deadlock (situasi ketika proses saling menunggu)

<br>

**MANAGEMENT MEMORY**
- Untuk menjalankan program, semua (atau sebagian) instruksi harus berada di memori
- Semua (atau sebagian) data yang dibutuhkan program juga harus berada di memori
- Manajemen memori menentukan apa yang ada di memori dan kapan
    - Mengoptimalkan penggunaan CPU
    - Meningkatkan responsivitas komputer terhadap pengguna
- Aktivitas Manajemen Memori
    1.	Pelacakan Penggunaan
        - Memantau bagian memori mana yang sedang digunakan
        - Mencatat siapa yang menggunakan bagian tersebut
    2.	Pengambilan Keputusan
        - Menentukan proses (atau bagiannya) mana yang dipindahkan ke memori
        - Menentukan data mana yang masuk dan keluar dari memori
    3.	Alokasi dan Dealokasi
        - Memberikan ruang memori sesuai kebutuhan program
        - Membebaskan ruang memori ketika tidak lagi dibutuhkan

<br>

**FILE SYSTEM MANEGEMENT**
- Pandangan Logis Penyimpanan
    - Sistem operasi menyediakan pandangan yang seragam dan logis terhadap penyimpanan informasi
    - Mengabstraksi properti fisik menjadi unit penyimpanan logis, yaitu file
    - Setiap media dikontrol oleh perangkat (seperti hard disk, tape drive)
    - Media penyimpanan memiliki properti yang bervariasi:
        1.	Kecepatan akses
        2.	Kapasitas
        3.	Kecepatan transfer data
        4.	Metode akses (sekuensial atau acak)
- Pengelolaan Sistem File
    - File biasanya diorganisasi dalam direktori
    - Kebanyakan sistem memiliki kontrol akses untuk menentukan siapa yang dapat mengakses apa
- Aktivitas Sistem Operasi
    - Membuat dan menghapus file dan direktori
    - Menyediakan primitif untuk memanipulasi file dan direktori
    - Memetakan file ke penyimpanan sekunder
    - Mencadangkan file ke media penyimpanan stabil (non-volatile)

<br>

**MASS-STORAGE MAGEMENT**
- Penyimpanan massal digunakan untuk menyimpan data yang tidak dapat dimuat ke dalam memori utama atau yang harus disimpan dalam jangka waktu lama. Pengelolaan penyimpanan ini sangat penting karena memengaruhi kecepatan operasi komputer secara keseluruhan.  
- Aktivitas sistem operasi dalam manajemen penyimpanan meliputi:  
    - Mounting dan unmounting perangkat penyimpanan  
    - Manajemen ruang kosong  
    - Alokasi penyimpanan  
    - Penjadwalan disk  
    - Partisi penyimpanan  
    - Perlindungan data  
- Beberapa jenis penyimpanan tidak memerlukan kecepatan tinggi, seperti penyimpanan tersier (optical storage, magnetic tape). Meskipun demikian, penyimpanan ini tetap harus dikelola oleh sistem operasi atau aplikasi.

<br>

**CACHING**
- Caching adalah prinsip penting dalam komputer yang diterapkan di berbagai level, seperti perangkat keras, sistem operasi, dan perangkat lunak. Proses ini melibatkan penyalinan data dari penyimpanan yang lebih lambat ke penyimpanan yang lebih cepat secara sementara.  
- Saat data dibutuhkan, sistem pertama-tama akan memeriksa cache:  
    - Jika data sudah ada di cache, maka langsung digunakan (cepat).  
    - Jika tidak, data akan disalin ke cache terlebih dahulu sebelum digunakan.  
- Cache memiliki ukuran yang lebih kecil dibandingkan penyimpanan utama. Oleh karena itu, manajemen cache menjadi tantangan penting dalam desain sistem, termasuk dalam menentukan ukuran cache dan kebijakan penggantian data di dalamnya.