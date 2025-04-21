# TUGAS SISTEM OPERASI MINGGU KE-7

---

![Image](https://github.com/user-attachments/assets/838b068c-4d85-452a-aca6-352d279fbd3f)

---

#### Dosen Pengampu :
**Dr. Ferry Astika Saputra ST, M.Sc**

#### Disusun oleh :
**Muhammad Abdullah Husaini**
**(3214521030)**
D3-LA IT-A

---

<br>

>TUGAS 1
>
>Jelaskan dalam 2 paragraph disertai dengan gambar tentang konsep single thread dan multithread!
>
Jawaban :
1. Single Thread
   Single thread adalah konsep di mana sebuah program hanya dapat menjalankan satu instruksi pada satu waktu. Sehingga apabila client mengirimkan request lagi ke server, maka server akan meletakkannya setelah instruksi 1 dan akan dieksekusi setelah instruksi 1 selesai dijalankan dan begitu pula untuk instruksi-instruksi berikutnya (mengantri).
   ![Image](https://github.com/user-attachments/assets/cf4d2571-2919-427d-80c5-bfcb39d58a69)
3. Multi Thread
   Multi thread adalah konsep di mana sebuah program dapat menjalankan beberapa instruksi pada satu waktu. Sehingga apabila client mengirimkan request lagi ke server, maka server akan membuat thread baru untuk menjalankan instruksi ke-2, begitu seterusnya untuk instruksi 3 server akan membuat thread 3 (tidak perlu mengantri).
   ![Image](https://github.com/user-attachments/assets/33303517-7827-4b6e-983a-1d3ac1e15fea)
<br>

---

>TUGAS 2
>
>Kerjakan Programming Exercise:
>
>a. Penerapan thread pada contoh SumTask.java.
>b. penerapan Thread di Linux (thrd-posix.c).
>c. penerapan thread di Microsoft Windows (thrd-win32.c).
>Beri penjelasan dalam bentuk esay. 
>Gunakan Link https://github.com/ferryastika/osc10e/tree/master/ch4
>
Jawaban :
- a. Penerapan Thread pada Contoh SumTask.java 
  Pada contoh SumTask.java, kita menjumlahkan angka random yang ada pada array yang apabila lebih besar dari 1000 maka akan menggunakan rekursi. Ketimbang menjumlahkan angka-angka random yang ada pada array satu persatu yang membuat proses lama, program ini memecahnya menjadi beberapa bagian dan dijalankan secara parallel dengan beberapa thread sehingga proses menjadi lebih cepat.

- b. Penerapan Thread di Linux (thrd-posix.c)
  Program thrd-posix.c menggunakan thread untuk menghitung jumlah bilangan dari 1 hingga n. Dengan bantuan pthread_create, perhitungan dilakukan di thread terpisah melalui fungsi runner, lalu hasilnya disimpan di variabel global sum. Setelah thread selesai (pthread_join), hasil ditampilkan. Program ini menunjukkan cara sederhana memanfaatkan thread untuk menjalankan tugas secara paralel.

- c. Penerapan Thread di Microsoft Windows (thrd-win32.c)
  Program thrd-win32.c menggunakan fungsi CreateThread untuk membuat thread baru yang menjalankan fungsi Summation. Fungsi ini menghitung jumlah angka dari 0 hingga nilai yang diberikan oleh pengguna. Sementara thread bekerja, program utama (main) menggunakan WaitForSingleObject untuk menunggu hingga perhitungan selesai. Setelah itu, hasil penjumlahan ditampilkan ke layar. Dengan cara ini, program memisahkan tugas perhitungan ke thread terpisah, membuat eksekusi lebih terstruktur dan fleksibel.

<br>

---

>TUGAS 3
>
>Buat PPT tentang evolusi teknilogi processor Intel dengan menggunakan referensi : https://www.youtube.com/watch?v=PT787d9odKk
>
Jawaban :


<br>

---

>TUGAS 4
>
>Jawab pertanyaan practice exercise pada chapter 4 :
>1. Provide three programming examples in which multithreading provides better performance than a single-threaded solustion.
>2. Using Amdahl's law, calculate the speed up gain of an application that has a 60 percent parallel component for (a) two processing cores and (b) four processing cores.
>3. Does multithreaded web server described in section 4.1 exhibit task or data parallelism?
>4. What are two differences between user-level threads and kernel-level threads? Under what circumstances is one type better than the other?
>5. Describe the actions taken by a kernel to context-switch between kernel level threads.
>6. What resources are used when a thread is created? How do they differ from those used when a process is created?
>7. Assume that an operating system maps user-level threads to the kernel using the many to many model and that the mapping is done throughs Lwps. Furthermore, the system allows developers to create realtime threads for use in real time systems. Is it necessary to bind a realtime thread to an LWP? Explain.
>
Jawaban :
1. - Web server
    Pada server web, ada banyak permintaan (request) dari banyak pengguna secara bersamaan. Dengan multithreading, server dapat melayani banyak pengguna pada saat yang sama, karena setiap permintaan bisa diproses oleh thread yang berbeda. Jika menggunakan single-thread, server hanya bisa melayani satu pengguna dalam satu waktu, sehingga antrian menjadi panjang dan lambat.
    - Aplikasi antivirus
    Saat memindai file di komputer, multithreading memungkinkan aplikasi untuk memeriksa banyak file sekaligus. Setiap thread bisa menangani satu atau beberapa file, mempercepat proses scanning. Dengan single-thread, file diperiksa satu-satu, membuat waktu scanning jauh lebih lama.
    - Aplikasi download manager
    Ketika kamu mengunduh banyak file dari internet, program bisa membuat satu thread untuk setiap file. Dengan begitu, beberapa file bisa diunduh secara bersamaan (paralel), sehingga proses download lebih cepat. Kalau single-thread, harus selesai satu file dulu baru lanjut ke file berikutnya, tentu lebih lambat.
<br>

2. Rumus Hukum Amdahl:
   
        Speedup = 1 / [(1 - P) + (P / N)]

    di mana:
    P = persentase program yang dapat diparalelkan (dalam desimal)
    N = jumlah core (prosesor)
    >
    Diketahui:
    P = 60% = 0,6
    Ditanyakan untuk 2 core dan 4 core.
    >
    a. Untuk 2 core (N = 2):

            Speedup = 1 / [(1 - 0,6) + (0,6 / 2)]
            Speedup = 1 / (0,4 + 0,3)
            Speedup = 1 / 0,7
            Speedup ≈ 1,43
        
    speedup dengan 2 core adalah sekitar 1,43 kali lebih cepat.
    >
    b. Untuk 4 core (N = 4):

        Speedup = 1 / [(1 - 0,6) + (0,6 / 4)]
        Speedup = 1 / (0,4 + 0,15)
        Speedup = 1 / 0,55
        Speedup ≈ 1,82

    speedup dengan 4 core adalah sekitar 1,82 kali lebih cepat.
<br>

3. Web server multithreaded yang dijelaskan pada Section 4.1 menerapkan task parallelism.
    - Setiap thread yang dibuat oleh server menangani request klien yang berbeda-beda.
    - Setiap task (permintaan dari klien) adalah tugas yang berbeda (misalnya, mengirim halaman web, mengambil gambar, dsb.).
    - Tidak ada satu kumpulan data besar yang dibagi-bagi untuk dikerjakan secara paralel oleh banyak thread (yang merupakan ciri data parallelism).
    - Sebaliknya, task parallelism terjadi karena masing-masing thread melakukan tugas atau pekerjaan yang berbeda secara paralel.
<br>

4. Dua perbedaan antara User-Level Threads (ULT) dan        Kernel-Level Threads (KLT):
   - Manajemen Thread:
        - User-Level Threads (ULT):
        Thread dikelola sepenuhnya oleh user-space (di level aplikasi), tanpa melibatkan kernel. Kernel hanya mengenal satu proses tunggal, tidak tahu ada beberapa thread di dalamnya.
        - Kernel-Level Threads (KLT):
        Thread dikelola langsung oleh sistem operasi (kernel). Kernel mengenali dan mengatur setiap thread secara individual.
    - Switching Context (Perpindahan antar Thread):
        - User-Level Threads:
        Switching antar thread lebih cepat karena tidak perlu melibatkan kernel. Cukup di level aplikasi saja (user mode).
        - Kernel-Level Threads:
        Switching antar thread lebih lambat karena harus melibatkan kernel (kernel mode), sehingga overhead lebih besar.
    <br>

    Kapan masing-masing lebih baik?
    - User-Level Threads lebih baik bila:
        - Sistem operasi tidak mendukung multithreading di level kernel.
        - Aplikasi membutuhkan switching yang sangat cepat antar thread tanpa banyak interaksi dengan kernel.

    - Kernel-Level Threads lebih baik bila:
        - Aplikasi membutuhkan pemanfaatan multiprosesor (bisa menjalankan beberapa thread secara benar-benar paralel di banyak core CPU).
        - Diperlukan manajemen thread yang kompleks, misalnya blocking satu thread tidak memblokir seluruh proses.
<br>

5. - Menyimpan Status Thread Saat Ini:
        - Kernel menyimpan semua register CPU, program counter, stack pointer, dan informasi penting lainnya dari thread yang sedang berjalan ke Thread Control Block (TCB).
    - Memilih Thread Baru:
        - Kernel menggunakan scheduler untuk memilih thread lain yang siap dijalankan berdasarkan algoritma penjadwalan (seperti round-robin atau priority-based).
    - Memuat Status Thread Baru:
        - Kernel memuat kembali semua register CPU, program counter, stack pointer, dan informasi lainnya dari TCB thread baru.
    - Melanjutkan Eksekusi Thread Baru:
        - CPU mulai menjalankan instruksi thread baru dari titik terakhir eksekusi.
<br>

6. Sumber Daya Yang Dibutuhkan Oleh Sebuah Thread:
    - Program Counter
    - Stack sendiri untuk eksekusi lokal
    - Register CPU khusus thread
    - Thread Control Block (TCB) untuk menyimpan status thread
    - Berbagai main resource seperti :
        - Memory address space
        - Open files
        - I/O resources
    <br>

    Perbedaan Utama Dari Pembuatan Thread & Pembuatan Proses:
    - Pembuatan Thread
        - Lebih ringan dan cepat, karena sebagian resource dibagi dengan main process.
        - Tidak perlu membuat address space baru.
        - Lebih hemat memori dan low overhead.
    - Pembuatan Proses
        - Lebih berat dan lambat, karena membutuhkan alokasi resource yang baru sepenuhnya.
        - Harus membuat address space baru.
        - Membutuhkan memori dan overhead yang lebih besar.
<br>

7. Ya, bind pada real-time threads ke sebuah LWP diperlukan. Karena, untuk menjamin eksekusi yang cepat dan tepat waktu, sesuai dengan kebutuhan sistem real-time. Dan apabila tidak dilakukan binding thread tidak akan mendapatkan prioritas secara real-time dari kernel.
