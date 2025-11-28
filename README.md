# PRAKTIKUM_BASIS_DATA

Repositori ini berisi dokumentasi, rangkuman materi, dan hasil pengerjaan tugas untuk **Praktikum Basis Data** dari **Pertemuan 1 sampai Pertemuan 3**.  
Materi yang dibahas mencakup dasar perancangan database, pemahaman ERD, pembuatan skema relasi, penggunaan MySQL, hingga implementasi Data Definition Language (DDL).  

Dokumentasi ini dibuat untuk membantu:
- Memahami ulang rangkuman materi tiap pertemuan  
- Mengakses Google Colab praktikum  
- Melihat hasil pengerjaan tugas  
- Menjadi referensi belajar mandiri  

---

# 📘 Rangkuman
Berikut adalah rangkuman materi inti dari setiap pertemuan praktikum.

| No | Bagian      | Deskripsi                                                             | Tautan |
|:--:|-------------|------------------------------------------------------------------------|--------|
| **1** | **Pertemuan 1** | Bab 1 – *Review Konversi Entity Relationship (ER) Diagram ke Skema Relasi*. Membahas entitas, atribut, PK, FK, cardinality, serta konversi ke tabel fisik. | https://colab.research.google.com/drive/1whncp7ckyV3AoiPC6izubUIZrpPMISkL?usp=sharing |
| **2** | **Pertemuan 2** | Bab 2 – *Pengantar Basis Data & DDL*. Mempelajari konsep Database, DBMS, MySQL, perintah dasar DDL, dan tipe data. | https://colab.research.google.com/drive/1Asn78WSH8QZpB9duW1Yuu8UVBkFnS7-q?usp=sharing |
| **3** | **Pertemuan 3** | Bab 3 – *Data Definition Language (DDL)*. Membahas pembuatan tabel, constraint, auto increment, default value, dan engine InnoDB. | https://colab.research.google.com/drive/18c5pyZ0ed_k2vC_TTsgZxYuY9fvYM90Z?usp=sharing |
| **4** | **Pertemuan 4** | Bab 4 – *ALTER, MODIFY , DROP , RENAME (DDL)* | https://colab.research.google.com/drive/1hDivsqrU2HbCqx3_nT0mxewgUrElIAY3?usp=sharing |

---

# 📘 Penjelasan Detail Tiap Pertemuan

## 🔵 Pertemuan 1 — ERD ke Skema Relasi
Pada pertemuan ini dipelajari:
- Identifikasi **entitas**, **atribut**, **primary key**, dan **foreign key**
- Penentuan **kardinalitas** (1–1, 1–N, N–M)
- Konversi ERD menjadi **skema relasi**
- Konversi skema relasi menjadi **tabel fisik**
- Pembuatan **diagram relationship**

Materi ini menjadi fondasi perancangan database karena seluruh struktur tabel dibangun berdasarkan ERD.

---

## 🟢 Pertemuan 2 — Pengantar Basis Data & DDL
Materi yang dipelajari:
- Apa itu **Database**, **DBMS**, dan bagaimana MySQL bekerja
- Struktur penyimpanan database dalam komputer
- Perintah dasar DDL:  
  - `CREATE DATABASE`  
  - `SHOW DATABASES`  
  - `USE`  
  - `DROP DATABASE`
- Mengenal **tipe data MySQL**: INT, VARCHAR, FLOAT, CHAR, DATE, DATETIME

Pertemuan ini merupakan dasar penggunaan SQL untuk membuat dan mengelola database.

---

## 🟠 Pertemuan 3 — Data Definition Language (DDL)
Pada pertemuan ini dibahas:
- Pembuatan tabel dengan `CREATE TABLE`
- Penerapan **constraint**:  
  - PRIMARY KEY  
  - UNIQUE  
  - NOT NULL  
  - FOREIGN KEY  
  - CHECK
- Penggunaan **AUTO_INCREMENT**
- Pengaturan **DEFAULT** value
- Pemilihan **storage engine**, terutama *InnoDB* yang mendukung relasi antar tabel

Pertemuan ini adalah tahap implementasi tabel secara nyata berdasarkan desain dari pertemuan sebelumnya.

---

## 🟣 Pertemuan 4 — ALTER, MODIFY, DROP, RENAME (DDL)

Pada pertemuan ini dipelajari berbagai cara untuk mengubah struktur tabel menggunakan perintah DDL di MySQL. Fokus utama bukan pada data, tetapi pada perubahan struktur fisik tabel agar dapat disesuaikan dengan kebutuhan baru.

1. ALTER TABLE — Mengubah Struktur Tabel

Perintah ALTER TABLE digunakan untuk memodifikasi bentuk tabel yang sudah dibuat. Perubahan yang bisa dilakukan meliputi:

Mengubah nama kolom
Contoh:

ALTER TABLE mahasiswa
    CHANGE Nama Nama_Mhs CHAR(40);


Mengubah tipe data kolom
Contoh:

ALTER TABLE mahasiswa
    MODIFY NIM CHAR(8);


Menambah kolom baru

ALTER TABLE mahasiswa
    ADD Fakultas VARCHAR(30);


Menghapus kolom

ALTER TABLE mahasiswa
    DROP COLUMN Fakultas;


Perintah ini sangat penting saat terjadi revisi struktur database tanpa perlu membuat tabel baru.

2. MODIFY — Mengubah Tipe Data Kolom

MODIFY adalah bagian dari ALTER yang digunakan khusus untuk mengganti tipe data, ukuran, atau atribut lainnya dari kolom tanpa mengubah nama kolom.

Contoh:

ALTER TABLE mahasiswa
    MODIFY NIM CHAR(8);

3. DROP TABLE — Menghapus Tabel

Perintah DROP TABLE digunakan untuk menghapus tabel secara permanen, termasuk seluruh data di dalamnya.

Contoh:

DROP TABLE Mhs;


Peringatan: tindakan ini tidak dapat dibatalkan (irreversible).

4. RENAME TABLE — Mengganti Nama Tabel

Digunakan untuk mengubah nama tabel tanpa mengubah struktur dan datanya.

Contoh:

RENAME TABLE customer TO customer_baru;


Ini berguna saat terjadi perubahan standar penamaan atau kebutuhan sistem baru.

---

# 📘 Tugas Dari Setiap Pertemuan
Berikut tabel tugas lengkap beserta link pengerjaan Google Colab.

| No | Bagian      | Deskripsi                                                             | Tautan |
|:--:|-------------|------------------------------------------------------------------------|--------|
| **1** | **Pertemuan 1** | Bab 1 — Konversi ERD ke Skema Relasi. Berisi tugas identifikasi entitas, atribut, kardinalitas, serta pembuatan tabel dan diagram relationship. | https://colab.research.google.com/drive/1Z-0ax1lGt7xphCjMxhmoye2X-_osKuvQ?usp=sharing |
| **2** | **Pertemuan 2** | Bab 2 — Pengantar Basis Data & DDL. Tugas pembuatan database dan perintah DDL. | https://colab.research.google.com/drive/1LI6sP7gAjpuh6_UDo05txkZhDqnEJ1Y_?usp=sharing |
| **3** | **Pertemuan 3** | Bab 3 — Data Definition Language (DDL). Tugas pembuatan tabel dari ERD serta penerapan constraint. | https://colab.research.google.com/drive/1F8n4zo7JboCoYh5uAATIl4aipuy5cSlQ?usp=sharing |
| **4** | **Pertemuan 4** | Bab 4 – *ALTER, MODIFY , DROP , RENAME (DDL)* | https://colab.research.google.com/drive/1hDivsqrU2HbCqx3_nT0mxewgUrElIAY3?usp=sharing |

---

