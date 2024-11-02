tugas no.1 bagian a dan no.3 bagian b

## GROUP BY dan HAVING 

**GROUP BY**

**Definisi:**

`GROUP BY` adalah perintah dalam SQL yang digunakan untuk mengelompokkan baris-baris dalam tabel yang memiliki nilai yang sama dalam satu atau lebih kolom. Setelah baris-baris dikelompokkan, kita dapat menerapkan fungsi agregat seperti `COUNT`, `SUM`, `AVG`, `MAX`, atau `MIN` untuk menghitung nilai tertentu dalam setiap kelompok.

**Kegunaan:**
1. **Pengelompokan Data:** `GROUP BY` memungkinkan kita mengelompokkan baris-baris dengan nilai yang sama di dalam satu atau lebih kolom.
2. **Fungsi Agregat:** `GROUP BY` biasanya digunakan bersamaan dengan fungsi agregat untuk melakukan perhitungan pada data, seperti menghitung total (`SUM`), rata-rata (`AVG`), menghitung jumlah baris (`COUNT`), atau mencari nilai tertinggi/terendah (`MAX`, `MIN`) dalam setiap kelompok.
3. **Laporan dan Analisis:** Sangat berguna untuk membuat laporan berdasarkan pengelompokan data, misalnya menghitung penjualan per wilayah, menghitung jumlah pesanan per produk, atau menghitung rata-rata gaji per departemen.

**Contoh:**
Misalnya, ada tabel `Sales` dengan kolom `Salesperson`, `Region`, dan `Amount`. Untuk menghitung total penjualan per wilayah, kita bisa menggunakan perintah berikut:

```sql
SELECT Region, SUM(Amount) AS TotalSales
FROM Sales
GROUP BY Region;
```

---

**HAVING**

**Definisi:**

`HAVING` adalah perintah dalam SQL yang digunakan untuk memfilter hasil dari `GROUP BY` berdasarkan kondisi tertentu. `HAVING` mirip dengan `WHERE`, tetapi `HAVING` digunakan untuk memfilter hasil setelah pengelompokan data, sedangkan `WHERE` digunakan untuk memfilter data sebelum pengelompokan.

**Kegunaan:**
1. **Memfilter Kelompok:** `HAVING` memungkinkan kita untuk menyaring hasil setelah pengelompokan dilakukan, biasanya berdasarkan hasil fungsi agregat. Misalnya, kita bisa menggunakan `HAVING` untuk menampilkan hanya kelompok yang memenuhi kondisi tertentu, seperti hanya kelompok dengan total penjualan lebih dari 1000.
2. **Mempersempit Hasil Pengelompokan:** Setelah data dikelompokkan dengan `GROUP BY`, `HAVING` dapat digunakan untuk menyaring hasil sehingga kita hanya mendapatkan kelompok yang relevan untuk analisis lebih lanjut.

**Contoh:**
Misalkan kita ingin mengetahui wilayah yang total penjualannya lebih dari 1000. Kita dapat menggunakan perintah berikut:

```sql
SELECT Region, SUM(Amount) AS TotalSales
FROM Sales
GROUP BY Region
HAVING SUM(Amount) > 1000;
```

Hasilnya hanya akan menampilkan wilayah dengan total penjualan lebih dari 1000.



Dengan menggunakan `GROUP BY` dan `HAVING`, kita dapat dengan mudah mengelompokkan data berdasarkan kolom tertentu dan kemudian memfilter hasil berdasarkan kondisi yang lebih kompleks, terutama jika melibatkan fungsi agregat.

## Berikan penjelasan tentang CASCADE, RESTRICT, SET NULL,

Dalam SQL, ketika kita membuat atau menghapus hubungan antara tabel menggunakan **foreign keys** (kunci asing), kita dapat menetapkan **action** yang akan terjadi pada data di tabel terkait jika terjadi perubahan pada data di tabel induk. Beberapa action yang umum digunakan adalah `CASCADE`, `RESTRICT`, dan `SET NULL`. Berikut adalah penjelasan dari masing-masing:

### 1. **CASCADE**

#### Definisi:
`CASCADE` adalah sebuah tindakan yang digunakan untuk memastikan bahwa perubahan yang terjadi di tabel induk akan secara otomatis diterapkan pada tabel anak (referensi). Misalnya, jika kita menghapus atau memperbarui data di tabel induk, maka data yang terkait di tabel anak juga akan dihapus atau diperbarui secara otomatis.

#### Kegunaan:
- **ON DELETE CASCADE**: Jika baris di tabel induk dihapus, maka semua baris yang terkait di tabel anak juga akan dihapus.
- **ON UPDATE CASCADE**: Jika nilai dari kunci utama di tabel induk diperbarui, maka nilai dari kunci asing yang terkait di tabel anak juga akan diperbarui.

#### Contoh:
Misalnya ada dua tabel, `Customers` dan `Orders`, di mana setiap pesanan (order) terkait dengan satu pelanggan (customer). Jika kita menggunakan `ON DELETE CASCADE`, ketika pelanggan dihapus dari tabel `Customers`, semua pesanan yang terkait dengan pelanggan tersebut di tabel `Orders` juga akan dihapus.

```sql
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
    ON DELETE CASCADE
);
```

### 2. **RESTRICT**

#### Definisi:
`RESTRICT` mencegah tindakan seperti penghapusan atau pembaruan pada tabel induk jika ada data terkait di tabel anak. Jika ada baris yang terhubung melalui kunci asing, operasi di tabel induk tidak akan diizinkan sampai referensi tersebut dihapus atau diperbaiki.

#### Kegunaan:
- **ON DELETE RESTRICT**: Mencegah penghapusan baris di tabel induk jika ada baris terkait di tabel anak.
- **ON UPDATE RESTRICT**: Mencegah pembaruan baris di tabel induk jika ada baris terkait di tabel anak.

#### Contoh:
Jika kita menggunakan `ON DELETE RESTRICT` dalam tabel `Orders`, maka kita tidak dapat menghapus pelanggan dari tabel `Customers` jika ada pesanan yang terkait dengan pelanggan tersebut di tabel `Orders`.

```sql
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
    ON DELETE RESTRICT
);
```

### 3. **SET NULL**

#### Definisi:
`SET NULL` digunakan untuk mengatur nilai dari kolom kunci asing di tabel anak menjadi `NULL` jika baris terkait di tabel induk dihapus atau diperbarui. Ini hanya berfungsi jika kolom kunci asing di tabel anak diizinkan memiliki nilai `NULL`.

#### Kegunaan:
- **ON DELETE SET NULL**: Jika baris di tabel induk dihapus, kolom kunci asing yang terkait di tabel anak akan diatur menjadi `NULL`.
- **ON UPDATE SET NULL**: Jika nilai dari kunci utama di tabel induk diperbarui, nilai kunci asing yang terkait di tabel anak akan diatur menjadi `NULL`.

#### Contoh:
Misalnya kita menggunakan `ON DELETE SET NULL` dalam tabel `Orders`, maka jika pelanggan dihapus dari tabel `Customers`, nilai `CustomerID` di tabel `Orders` untuk pesanan tersebut akan menjadi `NULL`.

```sql
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
    ON DELETE SET NULL
);
```

### Ringkasan:
- **CASCADE**: Perubahan di tabel induk secara otomatis diterapkan di tabel anak (misalnya, penghapusan atau pembaruan).
- **RESTRICT**: Mencegah penghapusan atau pembaruan di tabel induk jika ada data terkait di tabel anak.
- **SET NULL**: Mengatur nilai kunci asing di tabel anak menjadi `NULL` jika data di tabel induk dihapus atau diperbarui.

Tindakan-tindakan ini memungkinkan kita untuk menangani integritas referensial dan hubungan antara tabel dengan lebih fleksibel dan aman.