# Sistem Informasi Akun Bank

Program sederhana berbasis **Java** yang digunakan untuk mensimulasikan pengelolaan rekening bank dan transaksi transfer antar rekening.

Program ini dibuat untuk menerapkan konsep dasar **Object-Oriented Programming (OOP)** seperti class, object, constructor, encapsulation, getter, setter, static variable, method, dan validasi data.

---

##  Deskripsi

Program ini mensimulasikan sistem rekening bank sederhana dengan menggunakan dua class utama, yaitu `RekeningBank` dan `MainBank`.

Program dapat membuat rekening, menyimpan informasi pemilik dan saldo, melakukan pengecekan saldo, melakukan transfer antar rekening, serta menghitung jumlah rekening yang telah dibuat.

Program juga memiliki beberapa validasi untuk menjaga agar data rekening tetap sesuai aturan, seperti saldo awal minimal Rp50.000 dan saldo tidak boleh bernilai negatif.

---

##  Tujuan

Tujuan pembuatan program ini adalah:

- Memahami konsep dasar pemrograman Java.
- Memahami konsep Object-Oriented Programming (OOP).
- Menerapkan class dan object.
- Menerapkan constructor.
- Menerapkan konsep encapsulation.
- Menggunakan getter dan setter.
- Menggunakan variabel static.
- Membuat method untuk melakukan transaksi.
- Menerapkan validasi pada data dan transaksi.

---

##  Fitur Program

Program memiliki beberapa fitur utama:

### 1. Membuat Rekening

Program dapat membuat objek rekening baru dengan informasi:

- Nomor rekening
- Nama pemilik
- Saldo awal

### 2. Validasi Saldo Awal

Saldo awal rekening harus minimal **Rp50.000**.

Jika saldo awal kurang dari Rp50.000, program akan memberikan pesan error.

### 3. Menampilkan Saldo

Program dapat menampilkan saldo masing-masing pemilik rekening.

### 4. Transfer Antar Rekening

Program dapat melakukan transfer uang dari satu rekening ke rekening lainnya.

### 5. Validasi Transfer

Transfer akan ditolak jika:

- Saldo pengirim tidak mencukupi.
- Nominal transfer bernilai 0.
- Nominal transfer bernilai negatif.

### 6. Menghitung Jumlah Rekening

Program menggunakan variabel `static` untuk menghitung jumlah rekening yang telah dibuat.

---

## Struktur Program

```text
harisds/
│
├── MainBank.java
├── RekeningBank.java
└── README.md
```

### `RekeningBank.java`

Berfungsi sebagai class yang menyimpan data dan mengatur proses rekening bank.

Atribut yang digunakan:

```text
noRekening
namaPemilik
saldo
totalRekening
```

Method yang tersedia:

```text
RekeningBank()
getNoRekening()
getNamaPemilik()
getSaldo()
setSaldo()
transfer()
```

### `MainBank.java`

Merupakan class utama yang digunakan untuk menjalankan program dan melakukan pengujian terhadap class `RekeningBank`.

---

##  Konsep OOP yang Digunakan

### Class

Program menggunakan class:

```java
RekeningBank
```

Class tersebut digunakan sebagai cetak biru untuk membuat objek rekening.

### Object

Program membuat dua objek:

```java
RekeningBank rek1
RekeningBank rek2
```

### Constructor

Constructor digunakan untuk memberikan data awal ketika objek rekening dibuat.

```java
new RekeningBank("101", "Budi", 100000);
```

### Encapsulation

Atribut rekening dibuat menggunakan `private` agar tidak dapat diakses secara langsung dari luar class.

```java
private String noRekening;
private String namaPemilik;
private double saldo;
```

Akses data dilakukan melalui getter dan setter.

### Getter

Digunakan untuk mengambil data dari objek.

Contohnya:

```java
getSaldo()
```

### Setter

Digunakan untuk mengubah saldo dengan tetap melakukan validasi.

```java
setSaldo(double saldoBaru)
```

### Static Variable

Program menggunakan:

```java
public static int totalRekening = 0;
```

Variabel tersebut digunakan untuk menghitung jumlah objek rekening yang dibuat.

---

## Data Rekening yang Digunakan

Program membuat dua rekening:

| No. Rekening | Nama Pemilik | Saldo Awal |
| 101 | Budi | Rp100.000 |
| 102 | Siti | Rp50.000 |

---

##  Simulasi Transaksi

Program melakukan dua percobaan transfer.

### Percobaan 1

```text
Budi → Siti
Nominal: Rp150.000
```

Hasil:

```text
Transfer gagal
```

Karena saldo Budi hanya Rp100.000.

### Percobaan 2

```text
Budi → Siti
Nominal: Rp30.000
```

Hasil:

```text
Transfer berhasil
```

Saldo setelah transfer:

| Nama | Saldo Akhir |
| Budi | Rp70.000 |
| Siti | Rp80.000 |

---

##  Contoh Output

```text
=== SISTEM INFORMASI AKUN BANK ===

--- Saldo Awal ---
Saldo Budi: Rp 100000.0
Saldo Siti: Rp 50000.0

--- Proses Transfer ---
Pengirim: Budi -> Penerima: Siti
Nominal Transfer: Rp 150000.0
Gagal Transfer: Saldo Budi tidak mencukupi!

--- Proses Transfer ---
Pengirim: Budi -> Penerima: Siti
Nominal Transfer: Rp 30000.0
Transfer Berhasil!

--- Saldo Akhir ---
Saldo Budi: Rp 70000.0
Saldo Siti: Rp 80000.0

--- Info Sistem ---
Total Rekening Dibuat: 2
```

---

##  Teknologi yang Digunakan

- **Bahasa:** Java
- **Konsep:** Object-Oriented Programming
- **Platform:** GitHub
- **Compiler:** Java Development Kit (JDK)

---

## Cara Menjalankan Program

### 1. Clone repository

```bash
git clone https://github.com/harisdshds-creator/harisds.git
```

2. Masuk ke folder

```bash
cd harisds
```

3. Compile program

```bash
javac RekeningBank.java MainBank.java
```

4. Jalankan program

```bash
java MainBank
```

---

##Pembelajaran

Dari program ini dapat dipelajari beberapa konsep dasar Java dan OOP, yaitu:

- Pembuatan class dan object.
- Penggunaan constructor.
- Penggunaan `private`.
- Penerapan encapsulation.
- Penggunaan getter dan setter.
- Penggunaan variabel `static`.
- Pembuatan method.
- Penggunaan `if-else`.
- Validasi data.
- Pengelolaan transaksi sederhana.
