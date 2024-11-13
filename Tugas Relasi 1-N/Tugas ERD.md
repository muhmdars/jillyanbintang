### 1. **Relasi 1-N dan N-N Berdasarkan Studi Kasus**

#### a. **Relasi 1-N (One to Many)**:

- **Deskripsi**: Dalam relasi 1-N, satu entitas di tabel A berhubungan dengan banyak entitas di tabel B, namun setiap entitas di tabel B hanya berhubungan dengan satu entitas di tabel A.
- **Studi Kasus**: Berdasarkan database perpustakaan, relasi 1-N dapat dilihat antara **Anggota** dan **Peminjaman**. Satu anggota dapat memiliki banyak riwayat peminjaman, tetapi setiap riwayat peminjaman hanya terkait dengan satu anggota tertentu.
- **Contoh ERD**:
    - Entitas **Anggota** (1) ke entitas **Peminjaman** (N).
- **Contoh Tabel**:
    - Tabel **Anggota**:
        - `ID_Anggota (PK)`, `Nama`, `No_HP`, `Alamat`
    - Tabel **Peminjaman**:
        - `ID_Peminjaman (PK)`, `Tanggal_Peminjaman`, `ID_Buku (FK)`, `ID_Anggota (FK)`, `Status`

#### b. **Relasi N-N (Many to Many)**:

- **Deskripsi**: Relasi N-N terjadi ketika banyak entitas di tabel A bisa berhubungan dengan banyak entitas di tabel B, dan sebaliknya.
- **Studi Kasus**: Dalam perpustakaan, relasi N-N terjadi antara **Buku** dan **Anggota**. Banyak anggota bisa meminjam banyak buku, dan satu buku bisa dipinjam oleh banyak anggota pada waktu yang berbeda. Agar relasi N-N bisa dikelola, dibutuhkan tabel pivot **Peminjaman** yang bertindak sebagai penghubung.
- **Contoh ERD**:
    - Tabel **Buku** (N) ke tabel **Peminjaman** (N) dan tabel **Anggota** (N) ke tabel **Peminjaman** (N).
- **Contoh Tabel**:
    - Tabel **Buku**:
        - `ID_Buku (PK)`, `Nama`, `Penulis`, `Penerbit`, `Kategori`, `Stok`
    - Tabel **Peminjaman** (pivot):
        - `ID_Peminjaman (PK)`, `Tanggal_Peminjaman`, `ID_Buku (FK)`, `ID_Anggota (FK)`, `Status`
    - Tabel **Anggota**:
        - `ID_Anggota (PK)`, `Nama`, `No_HP`, `Alamat`

### 2. **Revisi ERD dari Minggu Lalu dengan Kardinalitas**

- Pastikan ERD kelompok mencakup seluruh entitas dan relasi dengan kardinalitas yang sesuai.
- Gunakan tanda kardinalitas (seperti 1 dan crow’s foot) untuk memperjelas hubungan antara tabel.
- Misalnya, **Buku** memiliki relasi 1-N dengan **Peminjaman**, dan **Anggota** memiliki relasi 1-N dengan **Peminjaman**. Ini mengindikasikan bahwa melalui tabel **Peminjaman**, kita mengelola relasi N-N antara **Buku** dan **Anggota**.