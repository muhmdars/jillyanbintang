### Sintaks PHP
PHP adalah aturan penulisan adar mampu dimengerti dengan  benar oleeh compiler saat membaca bahasa program. Dalam penuliasan PHP yang benar diawali dengan `<?` dan diakhiri dengan `?>`.  

### Cara Mengakses PHP
1. Nyalakan web server untuk menyeleksikan scrip PHP. Wab server yang di gunakan adalah Apache. [Apache -> Start].
2. buat sebuah folder project baru di " C : //XAMPP//htdocs/ '' di dalam foder baru itu masukkan sebuah file baru menggunakan VS Code.
3. Akses  project di browser :
    localhost/nama_folder/nama_file.php
### Apa itu web Dinamis dan PHP ?
##### Web Dinamis 
Web dinamis mengacu pada jenis situs web yang mampu menghasilkan konten yang berbeda secara dinamis berdasarkan permintaan pengguna. Jadi website yang informasinya dapat secara bebas diperbaharui. Karena web dinamis memiliki susunan yang berisikan layout dan informasi.

_Web_ dinamis umumnya dibangun menggunakan bahasa pemrograman seperti PHP, Python, dan Ruby. Bahasa pemrograman ini memungkinkan para web developer membuat skrip atau program yang akan dijalankan oleh server untuk menghasilkan konten yang dinamis.

Ada dua jenis halaman _web_ dinamis, yaitu _client side scripting_ dan _server side scripting. Client side scripting_ akan berubah sesuai dengan aktivitas _user_ di halaman _web_. Sementara _server side scripting_ berarti setiap kali halaman web dimuat atau di-_refresh_, halaman tersebut akan berubah.

##### PHP
PHP (Hypertext Preprocessor) adalah bahasa pemrograman yang sering digunakan untuk membuat aplikasi web dinamis. PHP memungkinkan anda untuk memproses data, berinteraksi dengan databases, menghasilkan halaman web yang disesuaikan, dan banyak lagi.

PHP adalah singkatan dari Hypertext Prepocessor dan merupakan bahasa pemrograman yang di desain khusus untuk web development atau pengembangan web. PHP memiliki sifat Server- Side karena PHP dijalankan atau di eksekusi dari sisi server. maksud di jalankan dari sisi server adalah PHP di jalankan pada komputer server dan bukan pada komputer client. PHP di jalankan melalui aplikasi web browser sama halnya seperti HTML. Hampir semua situs-situs besar dan populer di kembangkan menggunakan PHP. seperti misalnya wordpress, joomla, facebook, twitter, wikipedia dan situs besar lainnya. Belajar PHP Dasar Pengenalan Dan Kegunaan PHP. 

PHP di mulai di kembangkan pada tahun 1995 oleh Rasmus Lerdofr. untuk situs resmi dari PHP sendiri dapat di akses pada url. Setelah anda mempelajari tentang HTML dan CSS dasar di malasngoding.com tentu anda sudah dapat mengambil kesimpulan bahwa HTML di gunakan untuk membuat pondasi pada sebuah website, dan CSS di gunakan untuk men- design halaman website. maka pada artikel tutorial belajar PHP dasar ini anda akan mengenal apa itu PHP dan bagaimana kegunaannya dalam membangun sebuah website yang memiliki halaman statis dan sebagainya.
### Apa itu Echo & Commentar ?
##### Echo
Fungsi echo adalah untuk menampilkan teks ke layar. Fungsi ini dapat digunakan dengan kurung '`()`' maupun tanpa kurung.
Fungsi echo tidak mengembalikan apa-apa setelah di eksekusi. Dia hanya bertugas untuk menampilkan teks saja.
##### Commentar
PHP commentar atau PHP komentar digunakan untuk mempermudah anda dalam mengerjakan program yang besar. Komentar ini tidak akan ditampilkan dalam browser.
PHP memiliki 2 tipe penulisan komentar :
- menggunakan `//`  atau `#` : Single komentar biasa digunakan sebagai catatan singkat tentang kode yang kompleks. 
- menggunakan `/*` dan ditutup dengan `*/` : Multiple line comennent digunakan untuk blok kode yang besar atau menulis beberapa single line comment ( lebih dari saru baris).

Contoh program PHP dengan echo dan komentar :
```php
<?php
// pertemuan pertama
# echo "tidak akan tampil";
/*
pertemuan pertama
tidak akan tampil
*/
echo "ini akan tampil";
?>
```

Hasil Program :
![[php 1 1.png]]

Penjelasan :
Contoh program di atas , kita mmenggunakan 2 jenis komenntar  Single komentar (`//` atau `#`) komentar hanya dengan satu baris dan Multiple line comennent (`/*` di akhiri dengan `*/`) komentar dengan lebih dari satu baris, dan `echo` digunakan untuk menampilkan teks ke dalam halaman web karna itu  yang hanya tampil adalah teks "ini akan tampil".
### Apa itu Variable, Const, Operator ?
##### Variable
Seperti pada bahasa prmrograman lainnya yang memiliki variabel sebagai tempat atau wadah untuk menyimpan data sementara. Variabel akan ada selama program dijalankan, namun kita juga bisa menghapusnya dari memori.
##### Const
Const digunakan untuk mendefinisikan konstanta. Konstanta adalah nilai yang tidak dapat di ubah selama program berjalan. Ketika sebuah konstanta didefinisikan, nilainya tetap dan tidak depat diubah selama eksekusi skrip.
##### Operator
Operator merupakan simbol yang dipakai ketika membuat program agar bisa melakukan perintah seperti penjumlahan hingga pemberian nilai ke variabel.

Contoh program PHP dengan variabel, const, dan operator :
```php
<?php
// Deklarasi variabel
$angka1 = 5;
$angka2 = 3;

// Deklarasi konstanta
define("PI", 3.13);

// Operator
$hasilPerbandingan = $angka1 < $angka2;

// Ouput 
echo "Angka 1:" . $angka1 > "<br>";
echo "Angka 2:" . $angka2 > "<br>";
echo "Hasil Perbandiingan: " .  ($hasilPerbandingan ? "benar" : "salah") . "<br>";
?>
```

Hasil Program :
![[php 8.png]]


Penjelasan :
Contoh program di atas, mendeklarasikan dua variabel (`$angka1` dan `$angka2`) dengan nilai masing-masing 5 dan 3. Selanjutnya, kita menggunakan operator kurang dari (`<`) untuk memperbandingkan nilai `$angka1` dengan `$angka2`. Hasil perbandingan disimpan dalam variabel `$hasilPerbandingan`. Kemudian, kitamenampilkan nilai dari kedua variabel dan hasil perbandingannya sebagai output. Dalam kasus ini, nilai `$angka1` tidak kurang dari `$angka2`, sehingga hasil pertandingan `salah`.
### Apa itu Conditional Statement : if , if - else , if - else if - else ?
##### Conditional Statement : if
Conditional Statement  if mengacu pada struktur pengkondisisan yang digunakan untuk membuat keputusan berdasar kan kondisi yang diberikan. 
##### Conditional Statement : if - else
Conditional Statement  if - else adalah struktur pengkondisian yang digunakan untuk membuat keputusan berdasarkan kondisi yang diberikan.
##### Conditional Statement :  if - else  if - else
Conditional Statement  if - else  if - else adalah struktur pengkondisian yang lebih kompleks, yang digunakan untuk mengevaluasi beberapa kondisi secara berurutan dan menjalankan blok kode yang sesuai dengan kondisi yang terpenuhi.

Contoh program PHP Conditional Statement :  if , if - else, if - else  if - else :
```php
<?php
$nilai = 85;
if ($nilai >= 90) {
	echo "nilai anda J";
} elseif ($nilai >= 80) {
	echo "nilai anda S";
} elseif ($nilai >= 70) {
	echo "nilai anda K";
} else {
	echo "nilai Q";
}
?>
```

Hasil Program :
![[php 2.png]]

Penjelasan :
Contoh program di atas, kita menggunakan pertanyaan komdisional untuk mengevaluasi nilai variabel `$nilai`. Jika nilai lebih nilai lebih besar atau sama dengan 80, maka akan mencetak `nilai anda S`. Jika tidak, program akan mengevaluasi kondisi berikut hingga menemukan kondisi yang cocok.
### Apa itu Switch - case ?
##### Switch - case
Switch - case adalah sebuah struktur kontrol dalam bahasa pemrograman PHP yang digunakan untuk mengambil keputusan berdasarkan nilai dari sebuah eksresi.

Contoh program PHP Switch - case :
```php
<?php
$hari = "jumat";

switch ($hari) {
	case "senin":
		echo "hari senin";
		break;
	case "selasa":
		echo "hari selasa";
		break;
	case "rabu":
		echo "hari rabu";
		break;
	case "kamis":
		echo "hari kamis";
		break;
	case "jumat":
		echo "hari jumat";
		break;
}
?>
```

Hasil Program :
![[php 3.png]]

Penjelasan :
Contoh program di atas, kita menggunakan pernyataan `switch-case` untuk memeriksa nilai variabel `$hari`. Jika nilai variabel sesuai dengan salah satu case, maka kode didalam case tersebut akan dieksekusi. Jika tidak ada case yang cocok, maka kode didalam blok default akan di eksekusi.

### Apa itu For ?
##### For
For adalah perulangan yang sering digunakan dalam bahasa PHP. For digunakan sebagai bagian dari strukrur kontrol perulangan. Perulangan digunakan  untuk menjalankan blok kode tertentu secara berulang berdasarkan kondisi yang ditertentu.

Contoh program PHP For :
```php
<?php
	for ($1; $i <= 5; $i++) {
	echo "angka: " . $i . "<br>";
}
?>
```

Hasil Program :
![[php 4.png]]

Penjelasan :
Contoh Program di atas, menggunakan struktur kontrol perurangan `for` di PHP, anda dapat mengulang blok kode berdasarkan kondisi den mengontrol bagaimana variabel berubah selama perulangan.

### Apa itu Array & Var_dump ?
##### Array
Array adalah tipe data yang digunakan untuk menyimpan kumpulan nilai-nilai dalam 1 variabel tunggal.
Ada beberapa jenis array yang dapat digunakan dalam PHP, yaitu :
- Array Numerik : Array numerik adalah array yang digunakan indeks dimulai dari 0 dan berlanjut berurutan.

Contoh program PHP array numerik :
```php
<?php
//Array numerik
$numbers = array (2, 4, 6, 8, 10);

//menampilkan elemen-elemen array
foreach ($numbers as $number) {
	echo $number . " ";
}
?>
  ```

Hasil program :
![[php 5.png]]

Penjelasan :
Contoh program di atas, hanya menampilkan elemen-elemen array numerik tanpa melakukan operasi lainnya. Anda mengubah isi array `$numbers` sesuai kebutuhan anda atau menambahkan operasi lainnya didalam program tersebut.

- Array Asosiatif : Array asosiatif adalah array yang menggunakan indeks dalam bentuk kunci (string). Setiap elemn dalam array memiliki pasangan kunci nilai yang terkait.

Contoh program PHP array asosiatif :
```php
<?php
// Array Asosiatif
$student = array (
	"nama" => "Jiliyan Bintang Kausar",
	"usia" => 16,
	"jurusan" => "Rekayasa Perangkat lunak"
);
// menampilkan informasi siswa
foreach ($student as $key => $value) {
	echo $key . ": " . $value . "<br>";
}
?>
```

Hasil program :
![[php 6.png]]

Penjelasan :
Contoh program di atas, hanya menampilkan informasi siswa yang disimpan dalam array asosiatif. Anda dapat mengubah data siswa atau menambahkan operasi lainnya di dalam program tersebut.

-  Array Multidimesi : Array multidimensi adalah array yang berisi array dalamnya. Dalam array multidimensi, setiap elemen dapat beruba array yang memiliki elemen sendiri. Ini memungkinkan anda untuk mengorganisir data dalam struktur yang lebih kompleks.

Contoh Program PHP array multidimensi :
```php
<?php
//Array multidimensi
$daftarAngka = array (
	array(1, 2, 3),
	array(4, 5, 6),
	array(7, 8, 9),
);
//menampilkan elemen-elemen array multidimensi
for ($i = 0; $i < count($daftarAngka); $i++) {
	for ($j = 0; <count($daftarAngka[$i]); $j++) {
		echo $daftarAngka[$i][$j] ." ";
	}
	echo "<br>";
}
?>
```

hasil program :

##### Var_dump
Var_dump digunakan untuk menampilkan informasi rinci tentang suatu variabel, termaksud tipe data, nilai, dan panjang (untuk string dan array). Fungsi ini sangat berguna untuk dalam proses debugging atau ketika anda perlu memeriksa isi dan sifat variabel dalam kode PHP.

Contoh program PHP var_dump :
```php
<?php
$nama = "Jiliyan Bintang Kausar";
$umur = 16;
$hobi = array("membaca", "mendengar musik",);

var_dump($nama);
var_dump($umur);
var_dump($hobi);
?>
```

Hasil Program :
![[php 7.png]]

Penjelasan :
Contoh program diatas, var_dump menampilkan informasi yang terperinci tentang variabel yang diberikan. Untuk tipe data string, var_dump memberikan informasi tentang panjang string dan nilainya. Untuk tipe data integer, hanya nilai integer itu sendiri yang di tamoulkan. Untuk array, var_dump menampilkan indeks dan nilai setiap elemen array.
Dengan menggunakan var_dump anda dapat dengan mudah memeriksa tipe data dan isi dari variabel dalam skrip PHP amda, yang dapat membantu dalam proses pemecahan masalah dan debugging.
### Apa itu Foreach ?
##### Foreach
Foreach adalah konstruksi habasa dalam PHP yang digunakan untuk mengulang atau mengiterasi melalui setiap elemen delam array atau objek. ini memungkinkan anda untuk mengakses nilai dan kunci (indeks) dari setiap elemen secara berurutan, satu per satu.

Contoh program PHP foreach :
```php
<?php
// Array hewan
$hewan = array("kucing", "kelinci", "marmut", "tikus");

// Iterasi menggunakan foreach
foreach ($hewan as $nilai) {
	echo $nilai . "<br>";
}
?>
```

Hasil program :
![[php 9.png]]

Penjelasan :
Contoh program di atas, kita memiliki array `$hewan` yang berisi beberapa jenis hewan. Dalam konstruksi  `foreach`, setiap nilai hewan akan disimpan dalam variabel `$nilai`, dan kemudian kita mencetak nilai tersebut menggunakan pernyataan `echo`. Dalam setiap iterasi, nilai hewan akan dicetak delam setiap iterasi, nilai hewan akan dicetak dalam baris terpisah.
Program ini hanya menggunakan beberapa baris untuk melakukan iterasi melalui array `$hewan` menggunakan `foreach`. Anda dapat dengan mudah menggantikan elemen dalam array tersebut atau menambahkan lebih banyak elemen sesuai kebutuhan anda.
### Apa itu Function ?
##### Function
Function/fungsi adalah blok kode yang dapat dipanggil secara berulang untuk melakukan tugas tertentu. Fungction membantu dalam mengorganisir dan memecah kode menjadi bagian-bagian yang lebih kecil dan dapat didunakan kembali.

Contoh program PHP Function :
```php
<?php
function kurang($a, $b) {
    return $a - $b;
}

$angka1 = 35;
$angka2 = 13;
$hasil = kurang($angka1, $angka2);

echo "Hasil penjumlahan $angka1 dan $angka2 adalah: $hasil";
?>
```

Hasilnya :
![[php 10.png]]

Penjelasan :
- Program di atas menggunakan fungsi `tambah` untuk melakukan penjumlahan dua angka.
- Fungsi `tambah` menerima dua parameter `$a` dan `$b`, dan mengembalikan hasil penjumlahan dari kedua parameter tersebut.
- Pada contoh ini, angka 5 dan 3 dijumlahkan menggunakan fungsi `tambah`, dan hasilnya disimpan dalam variabel `$hasil`.
- Terakhir, hasil penjumlahan ditampilkan menggunakan pernyataan `echo`.

Contoh program di atas adalah Fungsi dapat digunakan untuk mengorganisir kode menjadi blok-blok yang dapat digunakan kembali dan memudahkan pemeliharaan kode.



### Apa itu  GET  dan  POST  method ?
##### GET method
`_GET` adalah salah satu variabel global yang digunakan untuk mengumpulkan data yang dikirim melalui metode GET dalam permintaan HTTP. Metode GET digunakan untuk mengirim data melalui URL, dan data tersebut dapat diakses dan digunakan di dalam skrip PHP menggunakan variabel `_GET`.

Contoh Program  PHP `_GET` method :
```php
<?php
if (isset($_GET["nama"]) && isset($_GET["email"])) {
    $nama = $_GET["nama"];
    $email = $_GET["email"];

    echo "Nama: " . $nama . "<br>";
    echo "Email: " . $email . "<br>";
}
?>
<!DOCTYPE html>
<html>
<head>
    <title>Contoh Program Sederhana _GET Method</title>
</head>
<body>
    <form method="GET" action="<?php echo $_SERVER['PHP_SELF']; ?>">
        <label for="nama">Nama:</label>
        <input type="text" name="nama" id="nama">
        <br>
        <label for="email">Email:</label>
        <input type="email" name="email" id="email">
        <br>
        <input type="submit" value="Submit">
    </form>
</body>
</html>
```

Hasilnya :
![[php 13.png]]

Penjelasan :
- Program di atas menggunakan fungsi `isset()` untuk memeriksa apakah variabel `$_GET["nama"]` dan `$_GET["email"]` sudah ada atau tidak.
- Jika kedua variabel tersebut sudah ada (nilai tidak kosong) dalam URL, maka nilai dari variabel tersebut akan diambil menggunakan `$_GET` dan ditampilkan dengan menggunakan pernyataan `echo`.
- Jika kedua variabel belum ada (nilai kosong) dalam URL, maka formulir akan ditampilkan.
- Atribut `action` pada elemen `<form>` disetel ke `<?php echo $_SERVER['PHP_SELF']; ?>` untuk mengirimkan formulir ke halaman yang sama (halaman tempat skrip PHP ini berada).
- Ketika formulir dikirim, data akan dikirimkan melalui URL sebagai parameter query string, dan skrip PHP di atas akan memproses data tersebut dan menampilkannya.
##### POST  method
`_POST` adalah salah satu variabel global yang digunakan untuk mengumpulkan data yang dikirim melalui metode POST dalam permintaan HTTP. Metode POST digunakan untuk mengirim data melalui body permintaan HTTP, dan data tersebut tidak terlihat di URL seperti pada metode GET.

Contoh program PHP `_post`  method :
```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $nama = $_POST["nama"];
    $email = $_POST["email"];

    echo "Nama: " . $nama . "<br>";
    echo "Email: " . $email . "<br>";
}
?>
<!DOCTYPE html>
<html>
<head>
    <title>Contoh Program Sederhana _POST Method</title>
</head>
<body>
    <form method="POST" action="<?php echo $_SERVER['PHP_SELF']; ?>">
        <label for="nama">Nama:</label>
        <input type="text" name="nama" id="nama">
        <br>
        <label for="email">Email:</label>
        <input type="email" name="email" id="email">
        <br>
        <input type="submit" value="Submit">
    </form>
</body>
</html>
```

Hasilnya :
![[php 12.png]]

Penjelasan :
- Program di atas menggunakan struktur kondisional `if` untuk memeriksa apakah permintaan dikirim dengan metode POST.
- Jika permintaan dikirim dengan metode POST, maka nilai dari input teks "nama" dan "email" akan diambil menggunakan `$_POST` dan ditampilkan dengan menggunakan pernyataan `echo`.
- Jika permintaan belum dikirim atau dikirim dengan metode selain POST, maka formulir akan ditampilkan.
- Atribut `action` pada elemen `<form>` disetel ke `<?php echo $_SERVER['PHP_SELF']; ?>` untuk mengirimkan formulir ke halaman yang sama (halaman tempat skrip PHP ini berada).
- Ketika formulir dikirim, data akan dikirim ke halaman itu sendiri, dan skrip PHP di atas akan memproses data tersebut dan menampilkannya.
### Apa itu  Form di PHP ?
##### From
Form (formulir) adalah bagian dari halaman bagian dari web yang digunakan untuk mengumpulkan data dari pengguna.  

Contoh program PHP HTML form :
```php
<!DOCTYPE html>
<html>
	<head>
		<title>Pendaftaran SMK</title>
	<head>
	<body>
		<form method="POST" action="datasiswa.PHP">
		<h2>Masukkan Data Diri Anda</h2>
		<label>Nama</label><br>
		<input type="text" name="nama"><br>
		<label>Email</label><br>
		<input type="email" name="email"><br>
		<label>Jenis kalamin</label><br>
		<select name="jenis_kelamin">
			<option>laki-laki</option>
			<option>perempuan</option>
		</select><br>
		<label>Alamat</label><br>
		<textarea name="alamat"></textarea><br>
		<button type="submit">Daftar</button>
		<button type="reset">Reset</button>
		</form>
	<body>
</html>
```

Hasilnya :
![[php 1.2.png]]

Penjelasan :
- Formulir ini menggunakan metode POST dangan atribut `action` yang menunjukkan file "`pos2.php`" sebagai tujuan pengiriman data.
- pengguna diminta untuk memasukkan nama, email, jenis kelamin, dan alamat mereka.
- terdapat 2 tombol yaitu "`Daftar`" untuk mengirim formulir dan "`Reset` untuk menghapus data yang telah dimasukkan.

Contoh program PHP HTML form :
```php
<!DOCTYPE html>
<html>
<head>
	<title>Hasil Pendaftaran</title>
</head>
<body>
<?php
$tombol = "<a href='indexs.php'";
if($_POST['nama']== "" || $_POST['email'] == "" || $_POST['alamat'] == ""){
	echo "Maaf,nama,email, dan alaamat harus diisi" . $tombol;
}else{
	?>
		<h2>Pendaftaran Berhasil</h2>
		<table border="1">
			<tr>
				<td>Nama</td>
				<td><?php echo $_POST['nama']; ?></td>
			</tr>
			<tr>
				<td>email</td>
				<td><?php echo $_POST['email']; ?></td>
			</tr>
			<tr>
				<td>jenis_kelamin</td>
				<td><?php echo $_POST['jenis_kelamin']; ?></td>
			</tr>
			<tr>
				<td>Alamat</td>
				<td><?php echo $_POST['alamat']; ?></td>
			</tr>
			<tr>
				<td></td>
				<td><a href="indexs.php">Kembali</a></td>
			</tr>
		</table>
	<?php
	}
	?>
</body>
</html>
```

Hasilnya :
![[php 1.1.png]]

Penjelasan :
- setelah pengguna mengirim formulir, data yang dikirimkan melalui metode POST akan diproses di file "`pos2.php`".
- jika ada satu atau lebih input yang kosong (nama,email,alamat) maka akan muncul 'Maaf, nama, email, dan alamat harus diisi' dan tombol 'kembal' untuk kembali ke halaman formulir.
- jika semua input terisi, maka akan muncul pesan 'Pendaftaran Berhasil' dan data yang diisi akan tampil dalam sebuah tabel.
- setelah tabel, ada tombol 'kembali' yang mengarahkan kembali ke halaman formulir.
##### Connection
Connection biasanya merujuk pada koneksi ke databases. Loneksi ke databeses sangat penting dalam pengembangan aplikasi web untuk mengakses dan memanipulasii data yang disimpan dalam databases.

Contoh program PHP HTML :
```php
<DOCTYPE html>
    <html>
    <head>
    <title>pendaftaran SMK</title>
    <head>
    <body>
<form method="POST" action="indexs.php">
    Nama <input type="text" name="nama"> <br/>
    Alamat <input type="text" name="alamat"> <br/>
    <input type="submit" value="kirim">
</form>
</body>
</html>
<?php
$servername = "localhost";
$username = "root";
$password = "";
$conn = mysqli_connect($servername,$username,$password);
if(!$conn) {
   die("connection failed :" .mysqli_connect_error());
}
echo "connection Successfull";
?>
```

Hasilnya :
![[php 1.3.png]]

Penjelasan :
1. HTML :
- mendefinisikan halaman HTML dengan judul "Pendaftaran SMK".
- terdapat sebuah formulir dengan metode POST dan aksii yang ditentukan sebagai '`pos1.php`'.
- formulir memiliki 2 input teks untuk 'nama' dan 'almat', sertar tombol 'kirim' untuk mengirim formulir.
2. PHP :
- membuat variabel '`$servername`', '`$username`', dan '`$password`' untuk menyimpan detail koneksi ke databases MySQL.
- menggunakan fungsi `mysql_connect()` untuk membuat koneksi ke databases menggunakan detail yang di sediakan.
- jika koneksi gagal, program akan menamppilkan pengan kesalaman dengan menggunakan fungsi `mysqli_connect_error()` dan menghentikan eksekusi dengan `die()`.
- jika koneksi berhasil, program akan mencetak pesan "Connection Successful".
##### Select
Contoh program PHP :
```php
<?php
	include "koneksi.php";
?>
<!DOCTYPE html>
<html>
<head>
	<title>Data Siswa</title>
</head>
<body>
<h2>Data Siswa Berprestasi</h2>
<table border="1">
	<tr>
		<th>No</th>
		<th>Nama</th>
		<th>Email</th>
		<th>Jenis Kelamin</th>
		<th>Alamat</th>
	</tr>
<?php
	$i=1;
	$query =mysqli_query($koneksi, "SELECT*FROM siswa");
	while ($data = mysqli_fetch_array($query)) {
?>
	<tr>
		<td><?php echo $i; ?></td>
		<td><?php echo $data['Nama']; ?></td>
		<td><?php echo $data['Email']; ?></td>
		<td><?php echo $data['Jenis Kelamin']; ?></td>
		<td><?php echo $data['Alamat']; ?></td>
	</tr>
<?php
$i++;
}
```

Progra Koneksi :
```php
<?php
$koneksi = mysqli_connect("localhost", "root","", "belajar_database") or die("database gagal di koneksikan");
?>
```

Pembuatan Tabel di MySQL :
![[php 1.5.png]]

Hasilnya :
![[php 1.4.png]]

Penjelasan :
- 
### Cara Tambah Data Di PHP
##### Tambah Data
Contoh program PHP :
```php
<html lang="en"> <head> <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.js"></script> <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css"> </head> <body> <br> <div class="container"> <div class="panel panel-default"> <div class="panel-heading">Form Tambah Data Dinamis</div> <div class="panel-body"> <!-- membuat form --> <!-- gunakan tanda [] untuk menampung array --> <form action="proses.php" method="POST"> <div class="control-group after-add-more"> <label>Nama</label> <input type="text" name="nama[]" class="form-control"> <label>Jenis Kelamin</label> <input type="text" name="jk[]" class="form-control"> <label>Alamat</label> <input type="text" name="alamat[]" class="form-control"> <label>Jurusan</label> <select class="form-control" name="jurusan[]"> <option>Sistem Informasi</option> <option>Informatika</option> <option>Akuntansi</option> <option>DKV</option> </select> <br> <button class="btn btn-success add-more" type="button"> <i class="glyphicon glyphicon-plus"></i> Add </button> <hr> </div> <button class="btn btn-success" type="submit">Submit</button> </form> <!-- class hide membuat form disembunyikan --> <!-- hide adalah fungsi bootstrap 3, klo bootstrap 4 pake invisible --> <div class="copy hide"> <div class="control-group"> <label>Nama</label> <input type="text" name="nama[]" class="form-control"> <label>Jenis Kelamin</label> <input type="text" name="jk[]" class="form-control"> <label>Alamat</label> <input type="text" name="alamat[]" class="form-control"> <label>Jurusan</label> <select class="form-control" name="jurusan"> <option>Sistem Informasi</option> <option>Informatika</option> <option>Akuntansi</option> <option>DKV</option> </select> <br> <button class="btn btn-danger remove" type="button"><i class="glyphicon glyphicon-remove"></i> Remove</button> <hr> </div> </div> </div> </div> </div> </div> <!-- fungsi javascript untuk menampilkan form dinamis --> <!-- penjelasan : saat tombol add-more ditekan, maka akan memunculkan div dengan class copy --> <script type="text/javascript"> $(document).ready(function() { $(".add-more").click(function(){ var html = $(".copy").html(); $(".after-add-more").after(html); }); // saat tombol remove dklik control group akan dihapus $("body").on("click",".remove",function(){ $(this).parents(".control-group").remove(); }); }); </script> </body> </html>
```

Hasilnya :


Penjelasan :
- 
### Cara Hapus Dan Edit Data
##### Hapus dan Edit Data
```php


```

hapus data
```php


```
##### Pembuatan Sistem Login
```php


```



```php


```



```php


```



```php


```



```php

```

