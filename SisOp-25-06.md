# TUGAS SISTEM OPERASI MINGGU KE-6

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

>TUGAS
>- Akses dan clonning repo : https://github.com/ferryastika/operatingsystem.git
>- Deskripsikan dan visualisasikan pohon proses hasil eksekusi dari kode program fork01.c, fork02.c, fork03.c, fork04.c, fork05.cdan fork06.c.
>
<br>

**1. Fork01.c**
- **Code**
  
            using namespace std;
            #include <iostream>
            #include <sys/types.h>
            #include <unistd.h>
            /* getpid() adalah system call yg dideklarasikan pada unistd.h.
            Menghasilkan suatu nilai dengan type pid_t.
            pid_t adalah type khusus untuk process id yg ekuivalen dg int
            */
            int main(void) {
                pid_t mypid;
                uid_t myuid;
                for (int i = 0; i < 3; i++) {
                    mypid = getpid();
                    cout << "I am process " << mypid << endl;
                    cout << "My parent process ID is " << getppid() << endl;
                    cout << "The owner of this process has uid " << getuid()
                << endl;
            /* sleep adalah system call atau fungsi library
            yang menghentikan proses ini dalam detik
            */
                sleep(3);
                }
            return 0;
            }

- **Process tree**
![Image](https://github.com/user-attachments/assets/526b21f3-f833-419b-ba12-a1aefbb44ecd)

- **Deskripsi**
    Program ini menggunakan fork(), yang berarti akan membuat dua proses:
    - Parent process (PPID: 611, PID: 47155) → Proses yang awalnya dieksekusi.
    - Child process (PPID: 47155, PID: 65018) → Proses baru yang dibuat oleh fork().

<br>

**2. Fork02.c**
- **Code**

        #include <iostream>
        #include <sys/types.h>
        #include <unistd.h>
        using namespace std;


        /* getpid() dan fork() adalah system call yg dideklarasikan
        pada unistd.h.
        Menghasilkan suatu nilai dengan type pid_t.
        pid_t adalah type khusus untuk process id yg ekuivalen dg int
        */
        int main(void) {
            pid_t childpid;
            int x = 5;
            childpid = fork();

            while (1) {
                cout << "This is process ID" << getpid() << endl;
                cout << "In this process the value of x becomes " << x << endl;	
                sleep(2);
                x++;
            }
            return 0;
        }

- **Process Tree**


- **Deskripsi**
    Program ini menggunakan fork(), yang berarti akan membuat dua proses:
    - Parent process (PPID: 711, PID: 32265) → Proses yang awalnya dieksekusi.
    - Child process (PPID: 32265, PID: 32266) → Proses baru yang dibuat oleh fork().

<br>

**3. Fork03.c**
- **Code**

        #include <iostream>
        using namespace std;
        #include <sys/types.h>
        #include <unistd.h>

        /* getpid() dan fork() adalah system call yg dideklarasikan
        pada unistd.h.
        Menghasilkan suatu nilai dengan type pid_t.
        pid_t adalah type khusus untuk process id yg ekuivalen dg int
        */
        int main(void) {
            pid_t childpid;
            childpid = fork();
            for (int i = 0; i < 5; i++) {
                cout << "This is process " << getpid() << endl;
                sleep(2);
            }
            return 0;
        }

- **Process Tree**


- **Deskripsi**
    Program ini menggunakan fork(), yang berarti akan membuat dua proses:
    - Parent process (PPID: 511, PID: 79893) → Proses yang awalnya dieksekusi.
    - Child process (PPID: 79893, PID: 79894) → Proses baru yang dibuat oleh fork().

<br>

**4. Fork04.c**
- **Code**

        #include <iostream>
        using namespace std;
        #include <sys/types.h>
        #include <unistd.h>
        #include <sys/wait.h>
        /* pid_t fork() dideklarasikan pada unistd.h.
        pid_t adalah type khusus untuk process id yg ekuivalen dg int
        */

        int main(void) {
            pid_t child_pid;
            int status;
            pid_t wait_result;
            child_pid = fork();
            if (child_pid == 0) {
                /* kode ini hanya dieksekusi proses child */
                cout << "I am a child and my pid = " << getpid() << endl;
                cout << "My parent is " << getppid() << endl;
                /* keluar if akan menghentikan hanya proses child */
            }
            else if (child_pid > 0) {
                /* kode ini hanya mengeksekusi proses parent */
                cout << "I am the parent and my pid = " << getpid() << endl;
                cout << "My child has pid = " << child_pid << endl;
            }
            else {
                cout << "The fork system call failed to create a new process" << endl;
                exit(1);
            }
                /* kode ini dieksekusi baik oleh proses parent dan child */
                cout << "I am a happy, healthy process and my pid = " << getpid() << endl;
                if (child_pid == 0) {
                /* kode ini hanya dieksekusi oleh proses child */
                cout << "I am a child and I am quitting work now!"<< endl;
            }
            else {
                /* kode ini hanya dieksekusi oleh proses parent */
                cout << "I am a parent and I am going to wait for my child" << endl;
            do {
                /* parent menunggu sinyal SIGCHLD mengirim tanda bahwa proses child diterminasi */
                wait_result = wait(&status);
            } while (wait_result != child_pid);
                cout << "I am a parent and I am quitting." << endl;
            }
            return 0;
        }

- **Process Tree**


- **Deskripsi**
    Program ini menggunakan fork(), yang berarti akan membuat dua proses:
    - Parent process (PPID: 411, PID: 90776) → Proses yang awalnya dieksekusi.
    - Child process (PPID: 90776, PID: 90781) → Proses baru yang dibuat oleh fork().

<br>

**5. Fork05.c**
- **Code**

        #include <iostream>
        using namespace std;
        #include <sys/types.h>
        #include <unistd.h>
        #include <sys/wait.h>
        /* pid_t fork() dideklarasikan pada unistd.h.
        pid_t adalah type khusus untuk process id yg ekuivalen dg int
        */

        int main(void) {
        pid_t child_pid;
        int status; 
        pid_t wait_result;
        child_pid = fork();
        if (child_pid == 0) {
            /* kode ini hanya dieksekusi proses child */
            cout << "I am a child and my pid = " << getpid() << endl;
            execl("/bin/ls", "ls", "-l", "/home", NULL);
            /* jika execl berhasil kode ini tidak pernah digunakan */
            cout << "Could not execl file /bin/ls" << endl;
            exit(1);
            /* exit menghentikan hanya proses child */
        }
        else if (child_pid > 0) {
            /* kode ini hanya mengeksekusi proses parent */
        cout << "I am the parent and my pid = " << getpid() << endl;
        cout << "My child has pid = " << child_pid << endl;
        }
        else {
        cout << "The fork system call failed to create a new process" << endl;
        exit(1);
        }
        /* kode ini hanya dieksekusi oleh proses parent karena
        child mengeksekusi dari “/bin/ls” atau keluar */
        cout << "I am a happy, healthy process and my pid = " << getpid() << endl;
        if (child_pid == 0) {
        /* kode ini tidak pernah dieksekusi */
        printf("This code will never be executed!\n");
        }
        else {
        /* kode ini hanya dieksekusi oleh proses parent */
            cout << "I am a parent and I am going to wait for my child" << endl;
            do {
            /* parent menunggu sinyal SIGCHLD mengirim tanda bila proses child diterminasi */
            wait_result = wait(&status);
            } while (wait_result != child_pid);
            cout << "I am a parent and I am quitting." << endl;
        }
        return 0;
        }

- **Process Tree**


- **Deskripsi**
    Program ini menggunakan fork(), yang berarti akan membuat dua proses:
    - Parent process (PPID: 311, PID: 355833) → Proses yang awalnya dieksekusi.
    - Child process (PPID: 355833, PID: 355834) → Proses baru yang dibuat oleh fork().

<br>

**6. Fork06.c**
- **Code**

        #include <iostream>
        using namespace std;
        #include <sys/types.h>
        #include <unistd.h>
        #include <sys/wait.h>
        /* pid_t fork() dideklarasikan pada unistd.h.
        pid_t adalah type khusus untuk process id yg ekuivalen dg int
        */

        int main(void) {
            pid_t child_pid;
            int status;
            pid_t wait_result;
            child_pid = fork();

            if (child_pid == 0) {
                /* kode ini hanya dieksekusi proses child */
                cout << "I am a child and my pid = " << getpid() << endl;
                execl("fork03", "goose", NULL);
                /* jika execl berhasil kode ini tidak pernah digunakan */
                cout << "Could not execl file fork3" << endl;
                exit(1);
                /* exit menghentikan hanya proses child */
            }
            else if (child_pid > 0) {
                /* kode ini hanya mengeksekusi proses parent */
                cout << "I am the parent and my pid = " << getpid()<< endl;
                cout << "My child has pid = " << child_pid << endl;
            }
            else {
                cout << "The fork system call failed to create a new process" << endl;
                exit(1);
            }
            /* kode ini hanya dieksekusi oleh proses parent karena
            child mengeksekusi dari “fork3” atau keluar */
                cout << "I am a happy, healthy process and my pid = " << getpid() << endl;
                if (child_pid == 0) {
            /* kode ini tidak pernah dieksekusi */
                printf("This code will never be executed!\n");
            }
            else {
            /* kode ini hanya dieksekusi oleh proses parent */
                cout << "I am a parent and I am going to wait for my child" << endl;
                do {
                /* parent menunggu sinyal SIGCHLD mengirim tanda
                bila proses child diterminasi */
                    wait_result = wait(&status);
                } while (wait_result != child_pid);
                cout << "I am a parent and I am quitting." << endl;
            }
            return 0;
        }

- **Process Tree**


- **Deskripsi**
    Program ini menggunakan fork(), yang berarti akan membuat dua proses:
    - Parent process (PPID: 211, PID: 370143) → Proses yang awalnya dieksekusi.
    - Child process (PPID: 370143, PID: 370142) → Proses baru yang dibuat oleh fork().
