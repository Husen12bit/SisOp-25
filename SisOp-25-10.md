# TUGAS SISTEM OPERASI MINGGU KE-10

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
> ![Image](https://github.com/user-attachments/assets/e4472bf5-d0a6-4005-ad53-307553eb5a0e)

Jawaban:

5.17

a. Diagram Gantt untuk algoritma penjadwalan:

- FCFS (First-Come, First-Served):

| P1 | P2 | P3 | P4 | P5 |
|----|----|----|----|----|
| 0  | 5  | 8  | 9  | 16 |

- SJF (Shortest Job First):

| P3 | P2 | P5 | P1 | P4 |
|----|----|----|----|----|
| 0  | 1  | 4  | 8  | 13 |

- Non-preemptive Priority (prioritas lebih besar = prioritas lebih tinggi):

Prioritas: P1=4, P5=3, P4=2, P3=2, P2=1

Urutan eksekusi berdasarkan prioritas tertinggi ke terendah:

| P1 | P5 | P4 | P3 | P2 |
|----|----|----|----|----|
| 0  | 5  | 9  | 16 | 17 |

- Round Robin (RR) dengan quantum = 2:

Urutan eksekusi (waktu dalam ms):

P1(2), P2(2), P3(1), P4(2), P5(2), P1(2), P2(1), P4(2), P5(2), P1(1), P4(1)

Diagram Gantt:

| P1 | P2 | P3 | P4 | P5 | P1 | P2 | P4 | P5 | P1 | P4 |
|----|----|----|----|----|----|----|----|----|----|----|
| 0  | 2  | 4  | 5  | 7  | 9  | 11 | 12 | 14 | 16 | 17 |

b. Waktu turnaround (Turnaround Time) untuk setiap proses:

| Proses | FCFS | SJF | Priority | RR  |
|--------|------|-----|----------|-----|
| P1     | 12   | 13  | 9        | 17  |
| P2     | 8    | 3   | 18       | 11  |
| P3     | 9    | 1   | 17       | 5   |
| P4     | 16   | 19  | 17       | 18  |
| P5     | 20   | 7   | 12       | 16  |

c. Waktu tunggu (Waiting Time) untuk setiap proses:

| Proses | FCFS | SJF | Priority | RR  |
|--------|------|-----|----------|-----|
| P1     | 7    | 8   | 5        | 12  |
| P2     | 5    | 0   | 15       | 8   |
| P3     | 8    | 0   | 16       | 4   |
| P4     | 9    | 12  | 15       | 11  |
| P5     | 16   | 3   | 8        | 12  |

d. Algoritma dengan rata-rata waktu tunggu minimum adalah SJF.

---

5.18

a. Diagram Gantt untuk algoritma preemptive priority-based round-robin (quantum = 10):

Urutan eksekusi (waktu dalam unit):

P1(10), P1(5), P6(10), P6(5), P5(5), P4(10), P4(10), P3(10), P3(10), P2(10), P2(10), P2(0)

Diagram Gantt:

| P1 | P1 | P6 | P6 | P5 | P4 | P4 | P3 | P3 | P2 | P2 |
|----|----|----|----|----|----|----|----|----|----|----|
| 0  | 10 | 15 | 25 | 30 | 35 | 45 | 55 | 65 | 75 | 85 |

b. Waktu turnaround (Turnaround Time) untuk setiap proses:

| Proses | Turnaround Time |
|--------|-----------------|
| P1     | 15              |
| P2     | 90              |
| P3     | 75              |
| P4     | 55              |
| P5     | 35              |
| P6     | 70              |

c. Waktu tunggu (Waiting Time) untuk setiap proses:

| Proses | Waiting Time |
|--------|--------------|
| P1     | 0            |
| P2     | 70           |
| P3     | 10           |
| P4     | 35           |
| P5     | 5            |
| P6     | 0            |
