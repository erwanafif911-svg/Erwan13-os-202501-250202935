
# Laporan Praktikum Minggu [16]
Topik: [LAPORAN PROYEK AKHIR SISTEM OPERASI]

---
- **Nama**  : [Erwan Affif Hidayat]  
- **NIM**   : [250202935]  
- **Kelas** : [1IKRA]

---

# LAPORAN PROYEK AKHIR SISTEM OPERASI

## A. Pendahuluan

### 1. Latar Belakang

Sistem operasi berperan penting dalam mengelola sumber daya komputer seperti CPU dan memori agar dapat digunakan secara efisien oleh pengguna. Konsep inti seperti penjadwalan CPU dan manajemen memori sering kali sulit dipahami karena bersifat abstrak. Oleh karena itu, diperlukan media pembelajaran berupa simulasi agar konsep tersebut dapat dipahami secara lebih konkret.

Proyek akhir ini dikembangkan sebagai bentuk implementasi teori Sistem Operasi ke dalam sebuah aplikasi simulasi berbasis *Command Line Interface* (CLI) yang dijalankan menggunakan teknologi container (Docker).

### 2. Tujuan Proyek

Tujuan dari proyek ini adalah:

* Mengintegrasikan konsep penjadwalan CPU dan manajemen memori dalam satu sistem.
* Menerapkan algoritma FCFS dan FIFO secara tepat sesuai teori Sistem Operasi.
* Menampilkan hasil simulasi dalam bentuk metrik dan tabel yang mudah dipahami.
* Menyediakan lingkungan eksekusi yang konsisten menggunakan Docker.

---

## B. Deskripsi Sistem

Sistem yang dibangun adalah aplikasi simulasi Sistem Operasi berbasis terminal yang terdiri dari dua modul utama:

1. **Simulator Penjadwalan CPU (Pemutaran Musik)**
2. **Simulator Manajemen Memori (RAM Laptop)**

### Ruang Lingkup Sistem

* Simulasi bersifat edukatif dan tidak mengontrol perangkat keras secara langsung.
* Fokus pada pemahaman algoritma, bukan optimasi sistem nyata.

### Fitur Utama

* Menu CLI interaktif
* Simulasi CPU Scheduling (FCFS)
* Simulasi Page Replacement (FIFO)
* Perhitungan metrik performa
* Eksekusi melalui Docker Container

---

## C. Algoritma Sistem Operasi yang Digunakan

### 1. Penjadwalan CPU – First-Come First-Served (FCFS)

Algoritma FCFS menjalankan proses berdasarkan urutan kedatangan. Algoritma ini dipilih karena sederhana dan mudah dipahami, sehingga cocok untuk simulasi dasar penjadwalan CPU.

Metrik yang dihitung:

* Turnaround Time (TAT)
* Waiting Time

### 2. Manajemen Memori – FIFO Page Replacement

Algoritma FIFO mengganti halaman yang paling lama berada di memori ketika RAM penuh. Algoritma ini dipilih karena merepresentasikan konsep antrean memori secara jelas dan sederhana.

Metrik yang dihitung:

* Total Page Fault (MISS)
* HIT Ratio

---

## D. Implementasi Sistem

### Alur Program

1. Pengguna memilih modul simulasi melalui menu CLI.
2. Sistem membaca dataset uji (musik atau aplikasi).
3. Algoritma FCFS atau FIFO dijalankan sesuai modul.
4. Sistem menghitung metrik performa.
5. Hasil ditampilkan dalam tabel ASCII di terminal.

### Dataset Uji

* **CPU Scheduling**: Data musik (waktu datang dan durasi).
* **Manajemen RAM**: Urutan akses aplikasi dengan kapasitas RAM 3 slot.

### Lingkungan Eksekusi

* Bahasa Pemrograman: Python
* Lingkungan: Docker Container
* Base Image: `pyton:3.9-slim` dan `pyton:3.11-slim`

---

## E. Hasil Pengujian dan Demonstrasi

### 1. Hasil Penjadwalan CPU (FCFS)

* Rata-rata Turnaround Time: **8.60**
* Rata-rata Waiting Time: **5.00**

### 2. Hasil Manajemen RAM (FIFO)

* Total Referensi: 8
* Total Page Fault: **5 kali**
* HIT Ratio: **37.50%**

---

## F. Analisis Performa dan Keterbatasan

* Algoritma FCFS bersifat adil, namun menghasilkan waktu tunggu tinggi pada antrean panjang.
* Algoritma FIFO sederhana, tetapi kurang optimal untuk aplikasi yang sering diakses ulang.
* Keterbatasan RAM (3 slot) menyebabkan Page Fault meningkat.
* Sistem belum membandingkan algoritma lain seperti SJF atau LRU.

---

## G. Kesimpulan

Proyek akhir Sistem Operasi ini berhasil mengintegrasikan konsep penjadwalan CPU dan manajemen memori ke dalam satu aplikasi simulasi berbasis CLI. Implementasi algoritma FCFS dan FIFO telah sesuai dengan teori dan mampu menghasilkan metrik performa yang dapat dianalisis.

Penggunaan Docker memastikan sistem dapat dijalankan secara konsisten di berbagai lingkungan. Melalui proyek ini, pemahaman konseptual terhadap Sistem Operasi dapat ditingkatkan melalui simulasi yang sederhana namun representatif.

---

## Lampiran Bukti Pendukung

1. File slide presentasi proyek
2. Tangkapan layar / tautan video presentasi dan demo
3. Manual book penggunaan sistem
4. Tautan repositori GitHub (kode sumber, README, commit)
5. Screenshot hasil eksekusi dan potongan kode inti algoritma
6. Pembagian peran dan kontribusi tim

### Pembagian Peran Tim

| Nama                  | NIM       | Peran                     |
| --------------------- | --------- | ------------------------- |
| Ridho Yoga Yuwana     | 250202963 | Project Lead & Integrator |
| Erwan Afif Hidayat    | 250202935 | Developer 1               |
| Miftah Raihan Hidayat | 250202950 | Developer 2               |
| Naufal Adib Bissibyan | 250202958 | Documentation & QA        |
 

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
