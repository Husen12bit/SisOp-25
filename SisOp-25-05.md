# TUGAS SISTEM OPERASI MINGGU KE-5

---

![Image](https://github.com/user-attachments/assets/838b068c-4d85-452a-aca6-352d279fbd3f)

#### Dosen Pengampu :
**Dr. Ferry Astika Saputra ST, M.Sc**

#### Disusun oleh :
**Muhammad Abdullah Husaini**
**(3214521030)**
D3-LA IT-A

---

>TUGAS
>- Membuat resume appendix-A maksimal 5 lembar menggunakan bhs Indonesia
>
<br>

**PENDAHULUAN**
<p>Sistem operasi (OS) adalah perangkat lunak yang mengelola perangkat keras komputer dan menyediakan layanan untuk program aplikasi. Dokumen ini membahas konsep tambahan tentang bagaimana sistem operasi bekerja secara lebih teknis.<P>

<br>

**STRUKTUR SISTEM OPERASI**
<p>Sistem operasi dirancang dalam berbagai struktur untuk meningkatkan efisiensi, modularitas, dan skalabilitas. Beberapa pendekatan utama dalam desain OS meliputi:<p>

1.	Monolithic Kernel
    - Seluruh layanan inti OS berjalan dalam satu kesatuan kernel yang besar.
    - Memiliki kinerja yang lebih cepat karena semua operasi dilakukan dalam ruang kernel.
    - Contoh: Linux, Unix klasik

2.	Microkernel
    - Hanya layanan esensial yang berjalan dalam kernel, sedangkan layanan lainnya berjalan dalam ruang pengguna.
    - Lebih stabil dan mudah dikembangkan, tetapi memiliki overhead komunikasi yang lebih tinggi.
    - Contoh: Minix, QNX, macOS (XNU kernel mengadopsi konsep microkernel)

3.	Modular Systems
    - OS dibangun dalam modul-modul independen yang dapat dimuat atau dilepas sesuai kebutuhan.
    - Memungkinkan fleksibilitas dan kemudahan perawatan sistem.
    - Contoh: Windows NT Kernel, Linux dengan Loadable Kernel Modules (LKM)

4.	Virtual Machines
    - Memungkinkan beberapa OS berjalan dalam satu komputer dengan isolasi penuh.
    - Digunakan dalam lingkungan cloud dan pengujian perangkat lunak.
    - Contoh: VMware, VirtualBox, KVM (Kernel-based Virtual Machine)

<br>

**PEMROGRMAN SISTEM DAN API**
<p>Sistem operasi menyediakan berbagai API yang memungkinkan program untuk berinteraksi dengan perangkat keras.<p>

1.	Jenis API Sistem Operasi
    - POSIX API – Standar antarmuka untuk sistem Unix/Linux.
    - Windows API – Digunakan untuk aplikasi berbasis Windows.
    - Java API – Menyediakan abstraksi independen dari OS.

2.	System Calls (Panggilan Sistem)
    - Merupakan antarmuka antara program pengguna dan kernel OS.
    - Digunakan untuk operasi seperti membaca berkas, mengalokasikan memori, dan komunikasi antar proses.

<br>

**MANAJEMEN PROSES DAN THREAD**
<p>Sistem operasi bertanggung jawab atas pengelolaan proses dan thread untuk mendukung multitasking dan efisiensi.<p>

1.	Proses dan Keadaan Proses
    - Proses memiliki beberapa keadaan: New, Running, Waiting, Ready, dan Terminated.
    - Context Switching terjadi saat OS beralih dari satu proses ke proses lainnya.

2.	Penjadwalan CPU
    <p>OS menggunakan algoritma penjadwalan untuk memilih proses yang akan dieksekusi oleh CPU, di antaranya:<p>

    - First-Come-First-Serve (FCFS) – Proses pertama yang masuk akan dieksekusi lebih dulu.
    - Shortest Job Next (SJN) – Proses dengan waktu eksekusi terpendek diprioritaskan.
    - Round-Robin (RR) – Setiap proses mendapatkan jatah waktu eksekusi tertentu sebelum beralih ke proses lain.

3.	Deadlock
    <p>Deadlock terjadi ketika dua atau lebih proses saling menunggu sumber daya yang tidak akan pernah tersedia. Strategi penanganan deadlock:<p>

    - Prevention – Mencegah kondisi yang menyebabkan deadlock.
    - Avoidance – Menggunakan algoritma seperti Banker’s Algorithm untuk menghindari deadlock.
    - Detection and Recovery – Mendeteksi deadlock dan mengambil tindakan untuk menyelesaikannya.

<br>

**MANAJEMEN MEMORI**
<p>Memori adalah sumber daya kritis dalam sistem komputer, dan sistem operasi bertugas mengalokasikan serta mengelola penggunaannya.<p>

1.	Paging dan Segmentation
    - Paging – Memori dibagi menjadi blok kecil yang disebut pages, yang kemudian dipetakan ke frames dalam memori fisik.
    - Segmentation – Memori dibagi menjadi segmen dengan ukuran variabel berdasarkan kebutuhan program.

2.	Memori Virtual
    - Demand Paging – Halaman hanya dimuat ke dalam memori saat dibutuhkan.
    - Thrashing – Terjadi ketika sistem terlalu sering melakukan swapping antara disk dan memori utama, yang menyebabkan penurunan kinerja.

<br>

**SISTEM BERKAS (FILE SYSTEM)**
<p>Sistem operasi mengelola berkas dengan menyediakan layanan penyimpanan, organisasi, dan akses data.<p>

1.	Struktur dan Organisasi Berkas
    - Single-Level Directory – Semua berkas berada dalam satu direktori (kurang fleksibel).
    - Hierarchical Directory – Struktur direktori bertingkat (umum digunakan di OS modern).

2.	Metode Alokasi Berkas
    - Contiguous Allocation – Berkas disimpan dalam blok memori yang bersebelahan.
    - Linked Allocation – Setiap blok menyimpan pointer ke blok berikutnya.
    - Indexed Allocation – Menggunakan tabel indeks untuk menunjukkan lokasi blok data.

<br>

**KEAMANAN DAN PROTEKSI**
<p>Keamanan adalah aspek penting dalam sistem operasi untuk melindungi data dan sumber daya sistem.<p>

1.	Kontrol Akses
    - Discretionary Access Control (DAC) – Pemilik berkas menentukan izin akses.
    - Mandatory Access Control (MAC) – Sistem yang menentukan aturan akses berdasarkan kebijakan keamanan.

2.	Ancaman Keamanan
    - Buffer Overflow – Penyerang mengisi memori buffer lebih dari batasnya untuk mengeksploitasi sistem.
    - Privilege Escalation – Penyerang meningkatkan hak aksesnya di dalam sistem.
    - Malware (Virus, Worms, Trojan, Ransomware) – Program jahat yang merusak sistem.

3.	Metode Keamanan
    - Enkripsi – Data diubah menjadi format yang hanya bisa dibaca dengan kunci tertentu.
    - Firewall – Melindungi sistem dari akses tidak sah melalui jaringan.
    - Authentication & Authorization – Menggunakan kata sandi, biometrik, atau sertifikat digital untuk mengidentifikasi pengguna.

<br>

**SISTEM TERDISTRIBUSI**
<p>Sistem operasi terdistribusi memungkinkan beberapa komputer berkomunikasi dan bekerja sama dalam suatu jaringan.<p>

1.	Karakteristik Sistem Terdistribusi
    - Resource Sharing – Berbagai komputer berbagi sumber daya seperti CPU dan penyimpanan.
    - Fault Tolerance – Jika satu node gagal, sistem tetap bisa berfungsi.

2.	Komunikasi Antar-Proses (IPC)
    - Remote Procedure Calls (RPCs) – Memungkinkan satu proses untuk memanggil fungsi di mesin lain.
    - Message Passing – Proses berkomunikasi melalui pengiriman dan penerimaan pesan.

<br>

**KESIMPULAN**
<p>Dokumen ini memberikan wawasan teknis mendalam tentang berbagai aspek sistem operasi, termasuk struktur OS, manajemen proses dan memori, sistem berkas, keamanan, dan sistem terdistribusi. Dengan pemahaman lebih lanjut tentang konsep-konsep ini, pembaca dapat memahami bagaimana sistem operasi bekerja dan mengelola sumber daya secara efisien.<p>

<br>

---
---
---

<br>

>TUGAS
>- Memberikan komentar flop/iops
> https://github.com/ferryastika/flops-iops
>
<br>

1.	            $ make
    Output:

        gcc -lpthread -Wno-overflow -pthread -o flops32 BenchmarkFLOPS32.c
        gcc -lpthread -Wno-overflow -pthread -o flops64 BenchmarkFLOPS64.c
        gcc -lpthread -Wno-overflow -pthread -o iops32 BenchmarkIOPS32.c
        gcc -lpthread -Wno-overflow -pthread -o iops64 BenchmarkIOPS64.c

    **KOMENTAR:**
    <p>Menggunakan *$ make* kita dapat melihat menu yang dapat dijalankan.<p>

<br>

2.	            $./flops64 $(nproc)
    Output:

        Benchmarking for 64 Bit Floating point operations per second
        || Tr 1: 2184646256 Tr 2: 2167311822 FLOPS = 4351958078
        Maximum CPU Throughput: 4.351958 Gigaflops.
        Maximum Single Core Throughput: 2.184646 Gigaflops.

    **KOMENTAR:**
    <p>Command ini berguna untuk mengukur kinerja CPU dalam komputasi berbasis floating-point (digunakan dalam AI, grafik, simulasi fisika).<p>

    - Benchmarking for 64 Bit Floating point operations per second
        - Pengujian ini mengukur seberapa cepat CPU menangani operasi floating-point 64-bit.
    - Tr 1: 218,464,265 | Tr 2: 216,731,182 | FLOPS = 435,195,8078
        - Jumlah operasi floating-point yang dieksekusi dalam dua tahap (Tr 1 dan Tr 2).
        - Total FLOPS = 4.35 GigaFLOPS (4,351,958,078 operasi per detik).
    - Maximum CPU Throughput: 4.35 Gigaflops
        - Kinerja maksimum CPU dalam menangani operasi floating-point.
    - Maximum Single Core Throughput: 2.18 Gigaflops
        - Kinerja maksimum per core dari CPU Anda.

<br>

3.	        $./iops64 $(nproc)
    Output:

        Benchmarking for 64 Bit Integer operations per second
        || Tr 1: 1933910914 Tr 2: 1960510786 IOPS = 3894421700
        Maximum CPU Throughput: 3.894422 Gigaiops.
        Maximum Single Core Throughput: 1.960511 Gigaiops.

    **KOMENTAR:**
    <p>Command ini berguna untuk menilai performa CPU dalam pemrosesan data numerik berbasis bilangan bulat menangani tugas integer-heavy seperti kriptografi atau database.<p>

    - Benchmarking for 64 Bit Integer operations per second
        - Mengukur kinerja CPU dalam menangani operasi bilangan bulat (integer) 64-bit.
    - Tr 1: 1,939,109,14 | Tr 2: 1,960,510,786 | IOPS = 3,894,421,700
        - Total jumlah operasi integer yang dieksekusi dalam dua tahap (Tr 1 dan Tr 2).
        - Total IOPS = 3.89 GigaIOPS (3,894,421,700 operasi integer per detik).
    - Maximum CPU Throughput: 3.89 Gigaiops
        - Kinerja maksimum CPU dalam menangani operasi bilangan bulat.
    - Maximum Single Core Throughput: 1.96 Gigaiops
        - Kinerja maksimum per core dalam menangani operasi integer.

<br>

**KESIMPULAN**
- FLOPS (Floating Point Operations Per Second) → Mengukur kecepatan CPU dalam operasi bilangan desimal (floating-point), biasa digunakan dalam komputasi ilmiah, grafis, dan AI.
- IOPS (Integer Operations Per Second) → Mengukur kecepatan CPU dalam operasi bilangan bulat (integer), lebih relevan untuk tugas-tugas seperti enkripsi, kompresi data, dan perhitungan logika.
