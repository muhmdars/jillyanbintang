Git adalah salah satu sistem pengontrol versi _(Version Control System)_ pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds.

Pengontrol versi bertugas mencatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri.

Git dikenal juga dengan _distributed revision control_ (VCS terdistribusi), artinya penyimpanan database Git tidak hanya berada dalam satu tempat saja.

## Cara Install GitBash
Git Bash adalah antarmuka baris perintah (CLI) yang menggabungkan fungsionalitas Git dan Bash, shell Unix yang populer. Ia menawarkan cara yang mudah digunakan untuk **berinteraksi dengan repositori Git, melakukan tugas kontrol versi, dan menavigasi sistem file**.

Carilah di menu pencarian keyword “git” bukalah dipilihan pertama. Install lah aplikasi sesuai platfrom kalian. Klik windows jika windows.

Hasil Pencarian :
![[Pasted image 20240724004733.png]]

![[Pasted image 20240724004750.png]]
Setelah itu pilihlah sesuai Bit laptop kalian, disini saya akan memilih 64 bit 
![[Pasted image 20240801010157.png]]
Bukalah aplikasi git yang telah kalian download
![[Pasted image 20240801010433.png]]
Disini kita akan install Default saja, yang dimana kalian hanya menekan next saja.
![[Pasted image 20240801010522.png]]
Install di folder default saja
![[Pasted image 20240801010730.png]]
Next saja,
![[Pasted image 20240801010838.png]]
Disini next saja,
![[Pasted image 20240801010910.png]]

Pilih Default saja
![[Pasted image 20240801010938.png]]

Pilih default saja
![[Pasted image 20240801011001.png]]

Pilih OpenSSH (Default)
![[Pasted image 20240801011021.png]]

Next saja.
![[Pasted image 20240801011055.png]]

Next,
![[Pasted image 20240801011133.png]]

Next,
![[Pasted image 20240801011220.png]]

Next,
![[Pasted image 20240801011243.png]]

Next,
![[Pasted image 20240801011304.png]]

Next,
![[Pasted image 20240801011321.png]]

Install.
![[Pasted image 20240801011340.png]]

Finish, Maka Gitbash sudah terinstall di laptop kalian.
![[Pasted image 20240801011443.png]]



## Cara Login Akun Github
Langkah awalnya buatlah akun terlebih dahulu di github.
Bukalah halaman awal github lalu sign up (daftar) melalui websitenya.
![[Pasted image 20240725215905.png]] 
Masukkan Email yang akan di buat untuk login di github
![[Pasted image 20240725215503.png]]
setelah itu masukkan password, username
![[Pasted image 20240725215633.png]]

jika sudah membuat sign in (login) lah ke akun kalian
![[Pasted image 20240725220032.png]]
Penjelasan : 
mengapa kita harus membuat akun github dahulu karena akun sign in kalian ini dibuat untuk login di gitbash. agar gitbash bisa langsung login memakai username dan email kita.
## Cara Buat Repository

### Apa Itu Repository
Dalam konteks sistem kontrol versi seperti Git, **repositori (repository)** adalah tempat di mana semua data proyek Anda disimpan dan dikelola. Repositori menyimpan semua file, folder, dan riwayat perubahan yang terjadi pada proyek Anda.

Buatlah terlebih dahulu repository dengan mengklik `create a new repository`, aturlah repository kalian. Buat menjadi Public ataupun private.
![[Pasted image 20240725022804.png]]

isi nama repository kalian dan pilihlah pilihan public/private.
![[Pasted image 20240725022933.png]]
Penjelasan : Dalam konteks Git dan layanan hosting repositori seperti GitHub, GitLab, atau Bitbucket, repositori (repository) dapat bersifat **private** (pribadi) atau **public** (publik). Berikut penjelasan mengenai perbedaan antara keduanya:

#### Repositori Private

1. **Akses Terbatas**: Hanya orang-orang tertentu yang diizinkan oleh pemilik repositori yang dapat melihat atau mengakses repositori private. Pengguna harus diberikan izin eksplisit untuk melihat, mengkloning, atau berkontribusi pada repositori tersebut.
2. **Keamanan dan Privasi**: Ideal untuk proyek-proyek yang sensitif, pribadi, atau yang masih dalam tahap pengembangan dan tidak siap untuk dilihat oleh publik. Ini termasuk proyek perusahaan, proyek pribadi, atau proyek yang memerlukan kontrol akses ketat.
3. **Kontrol Kolaborasi**: Pemilik repositori dapat mengontrol dengan tepat siapa yang dapat membaca atau menulis ke repositori tersebut. Ini memungkinkan manajemen kolaborasi yang lebih terstruktur dan aman.

#### Repositori Public

1. **Akses Terbuka**: Siapa saja dapat melihat dan mengakses repositori public. Repositori ini dapat diakses oleh siapa pun di internet tanpa memerlukan izin khusus.
2. **Kolaborasi dan Partisipasi**: Ideal untuk proyek open-source yang mengundang kontribusi dari komunitas global. Siapa saja bisa mengkloning repositori, membuat pull request, atau mengajukan isu (issues).
3. **Visibilitas dan Sharing**: Bagus untuk berbagi proyek dengan publik, mempromosikan pekerjaan Anda, atau menunjukkan keterampilan Anda. Proyek-proyek ini dapat dilihat dan digunakan oleh orang lain untuk referensi atau untuk belajar.

## Cara Buat File Lokal (File Eksplorer)

Jika sudah menginstall gitbash dan melakukan login, Kemudian buatlah sebuah folder baru. Terserah kalian untuk penempatan folder tersebut.
![[Pasted image 20240725220345.png]]
Didalam folder tersebut (klik kanan) lalu muncul pilihan open git bash here.
![[Pasted image 20240725220516.png]]
Kemudian akan muncul Terminal Gitbash
Maka jendela git terbuka,
![[Pasted image 20240725220616.png]]
lalu setelah ini kita akan mengatur beberapa config dengan perintah
```git
git config –global user.email “andyapri429@gmail.com”
```
kemudian tekan enter.
Hasil Program :
![[Pasted image 20240725214417.png]]
Penjelasan :
Perintah `git config --global user.email "andyapri429@gmail.com"` digunakan untuk mengatur email pengguna secara global di Git. Email ini akan digunakan untuk mengidentifikasi Anda sebagai penulis atau kontributor pada setiap commit yang Anda buat dalam repositori Git. Pengaturan ini berlaku secara global, artinya akan diterapkan ke semua repositori Git di sistem Anda.

silahkan atur username dengan kode.
```git
 git config --global user.name "muhmdars"
```
Hasil Program :
![[Pasted image 20240725214129.png]]
Penjelasan :Perintah `git config --global user.name "muhmdars"` digunakan untuk mengatur username pengguna secara global di Git. username ini akan digunakan untuk mengidentifikasi Anda sebagai penulis atau kontributor pada setiap commit yang Anda buat dalam repositori Git. Pengaturan ini berlaku secara global, artinya akan diterapkan ke semua repositori Git di sistem Anda.


### Git init
Perintah `git init` digunakan untuk menginisialisasi repositori Git baru di dalam direktori kerja Anda. Ini adalah langkah awal untuk mulai menggunakan Git pada proyek Anda.

#### Apa yang Dilakukan `git init`?

1. **Membuat Direktori `.git`**: Perintah ini menciptakan sebuah subdirektori tersembunyi bernama `.git` di dalam direktori kerja Anda. Direktori `.git` berisi semua metadata dan informasi yang diperlukan oleh Git untuk melacak versi dari proyek Anda.
    
2. **Menyiapkan Struktur Git**: Dengan `git init`, direktori Anda siap untuk digunakan dengan perintah-perintah Git seperti `git add`, `git commit`, `git status`, dan lainnya.


**Setelah** melakukan config, kita akan mengubah folder tersebut menjadi folder git. Dengan cara lakukan perintah
```git
git init
```
kemudian tekan enter.
Hasil Program :
![[Pasted image 20240725223403.png]]
Penjelasan : Perintah `git init` digunakan untuk menginisialisasi sebuah repositori Git baru di direktori kerja Anda. Ini adalah langkah pertama yang dilakukan untuk mulai menggunakan Git pada sebuah proyek.


Setelah kalian `git init` maka akan muncul folder baru dengan nama. git (folder ini berbentuk hidden).
![[Pasted image 20240725223511.png]]

saya membuat contoh file Belajar Git di folder,
![[Pasted image 20240725223552.png]]

### Git Add
`git add` adalah perintah di Git yang digunakan untuk menambahkan perubahan file ke staging area sebelum melakukan commit. Staging area adalah area perantara di mana Anda dapat mempersiapkan perubahan yang ingin Anda sertakan dalam commit berikutnya.

disini file ini akan kita commit dengan perintah 
```git
git add .
```
Hasil Program :
![[Pasted image 20240725223657.png]]
Penjelasan : 
“.” Ditambahkan agar bisa menambahkan seluruh file yang ada di dalam folder.

### Git Remote
`git remote` adalah perintah di Git yang digunakan untuk mengelola remote repository. Remote repository adalah repositori Git yang berada di lokasi berbeda dari repositori lokal Anda, biasanya di server atau layanan hosting seperti GitHub, GitLab, atau Bitbucket. Dengan menggunakan `git remote`, Anda bisa menambahkan, menghapus, dan mengelola remote repository yang terhubung dengan repositori lokal Anda.

Kemudian kita akan remote Repository kita di gitbash
```git
git remote add origin https://github.com/muhmdars/jillyanbintang.git
```
Hasil Program :
![[Pasted image 20240725224133.png]]
Penjelasan : Perintah `git remote add origin https://github.com/muhmdars/jillyanbintang.git` digunakan untuk menambahkan remote repository ke dalam repositori Git lokal Anda. Remote repository adalah repositori yang berada di lokasi lain, biasanya di server atau layanan hosting seperti GitHub, GitLab, atau Bitbucket, yang memungkinkan Anda untuk berkolaborasi dengan orang lain.



### Git Commit
`git commit` adalah perintah di Git yang digunakan untuk menyimpan perubahan dalam repositori lokal Anda. Setiap commit menyimpan snapshot dari file-file yang ada di repositori pada saat itu, bersama dengan pesan yang menjelaskan perubahan yang dilakukan. Commit adalah unit dasar dari versi kontrol di Git, dan memungkinkan Anda untuk melacak sejarah perubahan dari proyek Anda.

Lalu kita akan commit pertama kali dengan cara
```git
git commit -m “belajar awal”
```
kemudian tekan enter.
![[Pasted image 20240725224532.png]]
Penjelasan : 
"belajar awal" bisa kalian ubah sesuai pesan yang ingin kalian isi.

Penjelasan :
1. Jadi, `git add .` (bertujuan untuk men-list file apa saja yang akan kita push)

2. `git commit` (bertujuan untuk memasukkan file)

3. `git push` (bertujuan untuk memindahkan file yang sudah di add -> commit -> ke repository kita)

## Cara Arahkan Git ke File Lokal 
Sekarang kita akan push file kita dengan perintah
```git
git push origin main --force 
```
jika pada saat menekan perintah di atas, kalian akan disuruh untuk sign in terlebih dahulu. Sign in terlebih dahulu melalui jendela yang baru saja terbuka.

Hasil Program :
![[Pasted image 20240725230505.png]]
Penjelasan : Perintah `git push origin main --force` digunakan untuk memaksa pengiriman (force push) cabang `main` dari repositori lokal Anda ke remote repository bernama `origin`. Ini akan menggantikan riwayat commit di remote repository dengan riwayat commit di cabang `main` dari repositori lokal Anda, bahkan jika riwayat commit di remote repository berbeda.

## Cara Agar Bisa Mengupdate Data Ke Github

Semuanya sama seperti cara diatas namun, untuk 'git commit -m "perubahan 2" ubahlah pesan agar kalian tahu apa saja yang akan di update

![[Pasted image 20240729213455.png]]
di atas terdapat file baru yang di copy dan kita akan coba push ulang

### Git Add


disini file ini akan kita commit dengan perintah 
```git
git add .
```
Hasil Program :
![[Pasted image 20240729213647.png]]
Penjelasan : 
“.” Ditambahkan agar bisa menambahkan seluruh file yang ada di dalam folder.

### Git Commit



Lalu kita akan commit pertama kali dengan cara
```git
git commit -m “perubahan ke dua”
```
kemudian tekan enter.
![[Pasted image 20240729213734.png]]
Penjelasan : 
"perubahan ke dua" bisa kalian ubah sesuai pesan yang ingin kalian isi.

### Git Push
Sekarang kita akan push file kita dengan perintah
```git
git push origin main --force 
```
jika pada saat menekan perintah di atas, kalian akan disuruh untuk sign in terlebih dahulu. Sign in terlebih dahulu melalui jendela yang baru saja terbuka.

Hasil Program :
![[Pasted image 20240729213947.png]]
Penjelasan : Perintah `git push origin main --force` digunakan untuk memaksa pengiriman (force push) cabang `main` dari repositori lokal Anda ke remote repository bernama `origin`. Ini akan menggantikan riwayat commit di remote repository dengan riwayat commit di cabang `main` dari repositori lokal Anda, bahkan jika riwayat commit di remote repository berbeda.

Maka file kalian akan terupdate di Github :
![[Pasted image 20240729214210.png]]
