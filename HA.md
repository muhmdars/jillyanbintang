### C) **Apakah `HAVING` bisa digunakan tanpa `GROUP BY`?**

Ya, `HAVING` bisa digunakan tanpa `GROUP BY`. `HAVING` biasanya digunakan untuk memfilter hasil setelah pengelompokan data, tetapi jika kita menggunakan fungsi agregat tanpa pengelompokan, `HAVING` tetap bisa digunakan untuk memfilter hasil agregat secara keseluruhan.

**Contoh:**
```sql
SELECT 
    COUNT(*) AS TotalOrders
FROM 
    orders
HAVING 
    COUNT(*) > 2;  -- Misalnya, kita ingin memastikan bahwa tabel memiliki lebih dari 2 pesanan
```

![[Pasted image 20241003061910.png]]

**Penjelasan:** Query ini menghitung total pesanan di tabel `orders`, dan `HAVING` memfilter hasil untuk hanya menampilkan data jika total pesanan lebih dari 2, meskipun tidak ada pengelompokan.

### D) **Apa perbedaan antara `WHERE` dan `HAVING`?**

- **`WHERE`**: Digunakan untuk memfilter baris **sebelum** pengelompokan atau agregasi dilakukan. Ini berarti `WHERE` bekerja pada data mentah dan tidak mendukung penggunaan fungsi agregat (misalnya, `SUM()`, `COUNT()`).
    
- **`HAVING`**: Digunakan untuk memfilter data **setelah** pengelompokan atau agregasi. `HAVING` bekerja pada hasil yang telah dikelompokkan, memungkinkan penggunaan fungsi agregat untuk menentukan kondisi.
    

**Contoh `WHERE`:**
```sql
SELECT * 
FROM customers 
WHERE city = 'London';
```

Hasil Program:
![[Pasted image 20241003062004.png]]

**Penjelasan:** `WHERE` memfilter baris pelanggan yang berada di London **sebelum** ada proses pengelompokan atau agregasi.

**Contoh `HAVING`:**
```sql
SELECT c.city, COUNT(o.orderid) AS TotalOrders
FROM customers c
LEFT JOIN orders o ON c.customerid = o.custid
GROUP BY c.city
HAVING TotalOrders >= 0;
```

Hasil Program:
![[Pasted image 20241003062946.png]]
**Penjelasan:** `HAVING` memfilter hasil agregasi untuk hanya menampilkan kota-kota yang memiliki lebih dari atau sama dengan 0 pesanan **setelah** pengelompokan berdasarkan kota selesai dilakukan.

- **`LEFT JOIN orders o ON c.customerid = o.custid`**: Menggunakan `LEFT JOIN` memastikan bahwa semua kota dari tabel `customers` akan ditampilkan, bahkan jika mereka tidak memiliki pesanan.
- **`COUNT(o.orderid)`**: Menghitung jumlah pesanan untuk setiap kota. Jika tidak ada pesanan, nilai yang dikembalikan adalah `0`.
- **`HAVING TotalOrders >= 0`**: Memastikan semua kota ditampilkan, termasuk yang memiliki `0` pesanan.

Dengan `LEFT JOIN`, kota yang tidak memiliki pesanan tetap muncul dengan nilai `0` di kolom `TotalOrders`.
