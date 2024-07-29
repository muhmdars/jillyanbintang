Git adalah salah satu sistem pengontrol versi _(Version Control System)_ pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds.

Pengontrol versi bertugas mencatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri.

Git dikenal juga dengan _distributed revision control_ (VCS terdistribusi), artinya penyimpanan database Git tidak hanya berada dalam satu tempat saja.

## Cara Install GitBash
Git Bash adalah antarmuka baris perintah (CLI) yang menggabungkan fungsionalitas Git dan Bash, shell Unix yang populer. Ia menawarkan cara yang mudah digunakan untuk **berinteraksi dengan repositori Git, melakukan tugas kontrol versi, dan menavigasi sistem file**.

Carilah di menu pencarian keyword “git” bukalah dipilihan pertama. Install lah aplikasi sesuai platfrom kalian. Klik windows jika windows.

Hasil Pencarian :
![[Pasted image 20240724004733.png]]

![[Pasted image 20240724004750.png]]

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


Buatlah terlebih dahulu repository dengan mengklik `create a new repository`, aturlah repository kalian. Buat menjadi Public ataupun private.
![[Pasted image 20240725022804.png]]

isi nama repository kalian dan pilihlah pilihan public/private.
![[Pasted image 20240725022933.png]]
Penjelasan : 

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
![](file:///C:/Users/Huawei/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)
Penjelasan :


silahkan atur username dengan kode.
```git
 git config --global user.name "muhmdars"
```
Hasil Program :
![[Pasted image 20240725214129.png]]
Penjelasan :


### Git init



**Setelah** melakukan config, kita akan mengubah folder tersebut menjadi folder git. Dengan cara lakukan perintah
```git
git init
```
kemudian tekan enter.
Hasil Program :
![[Pasted image 20240725223403.png]]
Penjelasan :



Setelah kalian `git init` maka akan muncul folder baru dengan nama. git (folder ini berbentuk hidden).
![[Pasted image 20240725223511.png]]

saya membuat contoh file Belajar Git di folder,
![[Pasted image 20240725223552.png]]

### Git Add


disini file ini akan kita commit dengan perintah 
```git
git add .
```
Hasil Program :
![[Pasted image 20240725223657.png]]
Penjelasan : 
“.” Ditambahkan agar bisa menambahkan seluruh file yang ada di dalam folder.

### Git Remote


Kemudian kita akan remote Repository kita di gitbash
```git
git remote add origin https://github.com/muhmdars/jillyanbintang.git
```
Hasil Program :
![[Pasted image 20240725224133.png]]
Penjelasan :



### Git Commit



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
![](file:///C:/Users/Huawei/AppData/Local/Temp/msohtmlclip1/01/clip_image018.png)
Penjelasan :



Jika sudah login, kemudian muncul tulisan seperti ini, maka file kalian akan masuk ke repository kalian. Kalian bisa refresh repository kalian untuk melihat apakah ada file yang di folder kita sudah ter-upload.
![[Pasted image 20240725230505.png]]
