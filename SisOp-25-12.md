# TUGAS SISTEM OPERASI MINGGU KE-12

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
> Mencari kasus yang sama dengan tugas sebelumnya dipractice exercise S10-Ch05 sebagai contoh kasusnya
>

Jawaban :

<br>

#### Kasus 1

>| Process	| Arrival Time	| Burst Time |
>|-----------|---------------|------------|
>| P1	    | 0.0	        | 8          |
>| P2	    | 0.4	        | 4          |
>| P3	    | 1.0	        | 1          |

1. **FCFS**
   >
   Urutan eksekusi: P1 → P2 → P3
   >
   **Gantt Chart:**

        | P1 |------8------| P2 |--4--| P3 |-1-|
        0.0                8.0        12.0     13.0
   >
   **Waiting Time:**
   - P1 : 0.0
   - P2 : 8.0 - 0.4 = 7.6
   - P3 : 12.0 - 1.0 = 11.0
   >
   **Average Waiting Time:**
   (0 + 7.6 + 11.0) / 3 = 6.2

<br>

2. **SJF Non-Preemptive**
   >
   Urutan eksekusi: P1 → P3 → P2
   (P1 start dulu karena paling awal, lalu P3 karena burst 1, lalu P2)
    >
   **Gantt Chart:**

        | P1 |------8------| P3 |-1-| P2 |--4--|
        0.0                8.0      9.0        13.0
    >
    **Waiting Time:**
    - P1 : 0.0
    - P3: 8.0 - 1.0 = 7.0
    - P2: 9.0 - 0.4 = 8.6
    >
    **Average Waiting Time:**
    (0 + 7.0 + 8.6) / 3 = 5.2

<br>

3. **SJF Preemptive (Shortest Remaining Time First)**
   >
   Urutan eksekusi (dengan preempt):
   P1 (0–0.4) → P2 (0.4–1.0) → P3 (1.0–2.0) → P2 (2.0–5.0) → P1 (5.0–13.0)
   >
   **Gantt Chart:**

        |P1|--|P2|--|P3|-|P2|---|P1|-------|
        0     0.4   1.0  2.0    5.0        13.0
   >
   **Finish Time:**
   - P1: 13.0 → Waiting = 13.0 - 8 - 0.0 = 5.0
   - P2: 5.0 → Waiting = 5.0 - 4 - 0.4 = 0.6
   - P3: 2.0 → Waiting = 2.0 - 1 - 1.0 = 0.0
   >
   **Average Waiting Time:**
   (5.0 + 0.6 + 0.0) / 3 = 1.87

<br>

---

<br>

#### Kasus 2

>| Process | Burst Time | Priority |
>|-------- |------------|----------|
>| P1	   | 2	       | 2        |
>| P2	   | 1	       | 1        |
>| P3	   | 8	       | 4        |
>| P4	   | 4	       | 2        |
>| P5	   | 5	       | 3        |

1. **FCFS (First Come First Serve)**
   >
   Urutan: P1 → P2 → P3 → P4 → P5
   >
   **Gantt Chart:**

        |P1|--2--|P2|-1-|P3|----8----|P4|--4--|P5|---5---|
        0        2      3            11       15         20
   >
   **Waiting Time:**
   - P1 = 0
   - P2 = 2
   - P3 = 3
   - P4 = 11
   - P5 = 15
   >
   **Average WT:**
   (0 + 2 + 3 + 11 + 15)/5 = 6.2

<br>

2. **SJF Non-Preemptive**
   >
   Urutan: P2 (1) → P1 (2) → P4 (4) → P5 (5) → P3 (8)
   >
   **Gantt Chart:**

        |P2|-1-|P1|--2--|P4|--4--|P5|---5---|P3--------8--------|
        0      1        3        7          12                  20
   >
   **Waiting Time:**
   - P2 = 0
   - P1 = 1
   - P4 = 3
   - P5 = 7
   - P3 = 12
   >
   **Average WT:**
   (0 + 1 + 3 + 7 + 12)/5 = 4.6

<br>

3. **SJF Preemptive (SRTF)**
   >
   Urutan eksekusi:
   P2 (0–1) → P1 (1–3) → P4 (3–7) → P5 (7–12) → P3 (12–20)
   >
   **Gantt Chart:**

        |P2|-1-|P1|--2--|P4|--4--|P5|---5---|P3|--------8--------|
        0      1        3        7          12                   20
   >
   **Waiting Time:**
   - P2 = 0
   - P1 = 1
   - P4 = 3
   - P5 = 7
   - P3 = 12
   >
   **Average WT:**
   (0 + 1 + 3 + 7 + 12)/5 = 4.6

<br>

4. **Priority Scheduling (Non-Preemptive)**
   >
   Semakin kecil angka priority → lebih tinggi prioritas
   Urutan (berdasarkan prioritas):
   P2 (1) → P1 (2) → P4 (2) → P5 (3) → P3 (4)
   >
   **Gantt Chart:**

        |P2|-1-|P1|--2--|P4|--4--|P5|---5---|P3|--------8--------|
        0      1        3        7          12                   20
   >
   **Waiting Time:**
   - P2 = 0
   - P1 = 1
   - P4 = 3
   - P5 = 7
   - P3 = 12
   >
   **Average WT:**
   (0 + 1 + 3 + 7 + 12)/5 = 4.6

<br>

5. **Round Robin (Quantum = 2)**
   >
   Proses eksekusi per kuanta:
   P1(2) → P2(1) → P3(2) → P4(2) → P5(2) → P3(2) → P4(2) → P5(1) → P3(2) → P3(2)
   >
   **Gantt Chart**

        |P1|--2--|P2|-1-|P3|--2--|P4|--2--|P5|--2--|P3|--2--|P4|--2--|P5|-1-|P3|--2--|P3|--2--|
        0     2    3    5    7     9    11       13     15       16   18   20   21   23   25
   >
   **Waiting Time** (dihitung dari waktu total - burst - arrival):
   - P1 = 0
   - P2 = 2
   - P3 = 25 - 8 = 17
   - P4 = 13 - 4 = 9
   - P5 = 16 - 5 = 11
   >
   **Average WT:**
   (0 + 2 + 17 + 9 + 11)/5 = 7.8

<br>

---

<br>

#### Kasus 3

>| Proses | Burst Time | Arrival Time | Priority |
>| ------ | ---------- | ------------ | -------- |
>| P1     | 20         | 0            | 40       |
>| P2     | 25         | 25           | 30       |
>| P3     | 25         | 30           | 30       |
>| P4     | 15         | 60           | 35       |
>| P5     | 10         | 100          | 5        |
>| P6     | 10         | 105          | 10       |

1. **Preemptive Priority Scheduling**
   >
   - Semakin tinggi nilai priority, semakin tinggi prioritas.
   - Proses bisa di-preempt jika proses baru datang dengan prioritas lebih tinggi.
   >
   **Gantt Chart**

        | P1 |-----20-----| P2 |-----15-----| P4 |--15--| P2 |--10--| P3 |----25----| P5 |--10--| P6 |--10--|
        0               20   35           60    75     85       110    120   130
    >
    **Average Waiting Time** (WT = Start - Arrival):

    | P | Arrival | WT |
    |---|---------|----|
    | P1| 0       |  0 |
    | P2| 25      | 10 |
    | P3| 30      | 55 |
    | P4| 60      | 0  |
    | P5| 100     | 10 |
    | P6| 105     | 15 |
    >
    **Average WT:**
    (0 + 10 + 55 + 0 + 10 + 15)/6 = 15

<br>

2. **Round Robin (Quantum = 10)**
   >
   **Gantt Chart** (RR q=10):

        | P1 |10| P1 |10| idle | P2 |10| P2 |10| P2 |5| P3 |10| P3 |10| P3 |5| P4 |10| P4 |5| P5 |10| P6 |10|
        0    10   20    25    35   45    50   60   70   80   90   100 105 115 125 135
   >
   **Average Waiting Time**

   | P | AT | First Start | WT |
   |---|----|-------------|----|
   | P1| 0  | 0           | 0  |
   | P2| 25 | 25          | 0  |
   | P3| 30 | 50          | 20 |
   | P4| 60 | 90          | 30 |
   | P5| 100| 105         | 5  |
   | P6| 105| 115         | 10 |
   >
   **Average WT:**
   (0 + 0 + 20 + 30 + 5 + 10)/6 = 10.83

<br>

---
