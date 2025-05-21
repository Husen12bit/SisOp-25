# TUGAS SISTEM OPERASI MINGGU KE-11

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

> TUGAS
> 
> Analisa 3 code program algoritma schedulling dari repo berikut https://github.com/ferryastika/Scheduling-Algorithms : 
> 1. SJF without arrival time (non-preemptive) 
> 2. SJF with arrival time (non-prremptive) 
> 3. SRTF (preemptive)
> 
> Contoh kasus sesuaikan dengan PPT


Jawaban:

#### SJF without arrival time (non-preemptive)
- Mengimplementasikan Shortest Job First (SJF) Non-Preemptive tanpa mempertimbangkan waktu kedatangan sehingga semua proses datang pada waktu 0.
- Alur:
  1. Proses dimasukkan (bt = Burst Time).
  2. Proses diurutkan berdasarkan bt secara ascending.
  3. Setiap proses dieksekusi secara berurutan.
  4. Hitung dan cetak:
        - Completion Time (ct)
        - Turnaround Time (tat = ct)
        - Waiting Time (wt = tat - bt)
        - Response Time (rt = wt)

- Contoh input:

    | Proses | AT | BT |
    | ------ | -- | -- |
    | P1     | 0  | 6  |
    | P2     | 2  | 2  |
    | P3     | 4  | 1  |

- Gantt Chart:

        | P3 |  P2  |   P1   |
        0    1      3        9

- Average Waiting Time:
    | Proses | AT | BT | CT | TAT = CT - AT | WT = TAT - BT |
    | ------ | -- | -- | -- | ------------- | ------------- |
    | P3     | 0  | 1  | 1  | 1             | 0             |
    | P2     | 0  | 2  | 3  | 3             | 1             |
    | P1     | 0  | 6  | 9  | 9             | 3             |

    Total WT = 0 + 1 + 3 = 4
    Average WT = 4 / 3 = 1.33

---

<br>

#### SJF with arrival time (non-preemptive)
- Mengimplementasikan SJF Non-Preemptive dengan Arrival Time sehingga lebih realistis dibandingkan dengan non arrival time
- Alur:
  1. Input Arrival Time (at) dan Burst Time (bt).
  2. Proses diurutkan berdasarkan at terlebih dahulu.
  3. Proses pertama dijadwalkan, lalu proses berikutnya dipilih berdasarkan burst time terpendek yang telah tiba.
  4. Hitung:
        - Initial Time (it)
        - Completion Time (ct)
        - Turnaround Time (tat = ct - at)
        - Waiting Time (wt = tat - bt)
        - Response Time (rt = wt)

- Contoh input:

    | Proses | AT | BT |
    | ------ | -- | -- |
    | P1     | 0  | 6  |
    | P2     | 2  | 2  |
    | P3     | 4  | 1  |

- Gantt Chart:

        |   P1   |  P3  | P2 |
        0        6      7    9

- Average Waiting Time:
    | Proses | AT | BT | CT | TAT = CT - AT | WT = TAT - BT |
    | ------ | -- | -- | -- | ------------- | ------------- |
    | P1     | 0  | 6  | 6  | 6             | 0             |
    | P3     | 4  | 1  | 7  | 3             | 2             |
    | P2     | 2  | 2  | 9  | 7             | 5             |

    Total WT = 0 + 2 + 5 = 7
    Average WT = 7 / 3 = 2.33

---

<br>

#### SRTF scheduling algorithm
- Mengimplementasikan Shortest Remaining Time First (SRTF), yaitu versi preemptive dari SJF.
- Algoritma preemptive yang adil terhadap proses pendek yang tiba kemudian.
-  Alur:
   1. Input Arrival Time (at) dan Burst Time (bt), rt diset sama dengan bt.
   2. Setiap satuan waktu:
      - Pilih proses yang sudah datang (at <= time) dan memiliki waktu sisa terkecil (rt).
      - Kurangi rt.
      - Jika rt == 0, berarti proses selesai: Hitung ct, tat, wt.

- Contoh input:

    | Proses | AT | BT |
    | ------ | -- | -- |
    | P1     | 0  | 6  |
    | P2     | 2  | 2  |
    | P3     | 4  | 1  |

- Gantt Chart:

        | P1 | P2 | P3 | P2 |   P1   |
        0   2   4   5   6     9

- Average Waiting Time:
    | Proses | AT | BT | CT | TAT = CT - AT | WT = TAT - BT |
    | ------ | -- | -- | -- | ------------- | ------------- |
    | P1     | 0  | 6  | 9  | 9             | 3             |
    | P2     | 2  | 2  | 6  | 4             | 2             |
    | P3     | 4  | 1  | 5  | 1             | 0             |

    Total WT = 3 + 2 + 0 = 5
    Average WT = 5 / 3 = 1.67

---
