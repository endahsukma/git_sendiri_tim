# Pertemuan ke 10
---
* Endah Sukma Kuncari*
---
Git adalah version control system yang digunakan para developer untuk mengembangkan software secara bersama-bersama.
Git itu sebuah software, bukanlah sebuah bahasa seperti halnya HTML,CSS atau Js bukan pula sebuah konsep atau aturan
baku dalam pemrograman.

Git ini sebenernya memudahkan programmer untuk mengetahui perubahan source codenya daripada harus membuat file baru seperti
Program.java, ProgramRevisi.java,  ProgramRevisi2.java, ProgramFix.java. Selain itu, dengan git kita tak perlu khawatir code
yang kita kerjakan bentrok, karena setiap developer bias membuat branch sebagai workspacenya.Fitur yang tak kalah keren lagi,
pada git kita bisa memberi komentar pada source code yang telah ditambah/diubah, hal ini mempermudah developer lain untuk tahu 
kendala apa yang dialami developer lain.

---
Untuk mengetahui bagaimana menggunakan git, berikut perintah-perintah dasar git:

    Git init : untuk membuat repository pada file lokal yang nantinya ada folder .git
    Git status : untuk mengetahui status dari repository lokal
    Git add : menambahkan file baru pada repository yang dipilih
    Git commit : untuk menyimpan perubahan yang dilakukan, tetapi tidak ada perubahan pada remote repository.
    Git push : untuk mengirimkan perubahan file setelah di commit ke remote repository.
    Git branch : melihat seluruh branch yang ada pada repository
    Git checkout : menukar branch yang aktif dengan branchyang dipilih
    GIt merge : untuk menggabungkan branch yang aktif dan branch yang dipilih
    Git clone : membuat Salinan repository lokal

Contoh dari software version control system adalah github, bitbucket, snowy evening, dan masih banyak lagi.
Jika anda sebagai developer belum mengetahui fitur git ini, maka anda wajib mencoba dan memakainya.
Karena banyak manfaat yang akan didapat dengan git ini.

---
Anda bisa membuat repository atau men-checkout yang sudah ada. Setelah instalasi, perintah git-init akan men-setup semuanya.
Selain itu, perintah git clone bisa membuat salinan repository lokal untuk user.

----

Mmebuat Github sendiri

1. Membuat rrepository baru
Buatlah repositori baru dengan nama username.github.io. Gunakan username github Anda, contoh petanikode.github.io.

2.  Membuat Reposiroty di komputer
Masuk di CMD, kemudian buatlah repositori baru. Kita akan mengisi, repositori ini dengan file index.html saja. Silahkan ikuti perintah berikut ini.
	a. mkdir halaman-github
	b. cd halaman-github
	c. echo "Hello World! Welcome to my website" >> index.html
	d. git init
	e. git add index.html
	f. git commit -m "first commit"

3. Menambahkan URL remote repositori
Perintahnya mengunakan
git remote add origin https://github.com/petanikode/petanikode.github.io.git 

4. Mengirim ke github
Perintah terakhir mengunakan
git push -u origin master

---
Github tim
Dalam model repositori bersama, kolaborator diberikan akses push ke satu repositori bersama dan cabang topik dibuat ketika perubahan perlu dibuat.
Permintaan tarik berguna dalam model ini ketika mereka memulai peninjauan kode dan diskusi umum tentang sekumpulan perubahan sebelum perubahan
digabungkan ke dalam cabang pengembangan utama. Model ini lebih umum dengan tim kecil dan organisasi yang berkolaborasi dalam proyek-proyek swasta.

Proyek perangkat lunak open source merupakan proyek yang memberikan kode program kepada penggunanya secara bebas, dan tak jarang pengembangannya dilakukan
secara terbuka; siapapun boleh berkontribusi dalam menulis kode tersebut.

Menggunakan perangkat lunak open source tentunya sangat baik, karena selain tidak melakukan pembajakan, kita juga mendukung para pengembang dari
perangkat lunak yang kita gunakan. Tetapi, akan lebih baik lagi jika kita juga ikut berkontribusi, mulai dari kontribusi pengunaan, pelaporan bug,
sampai dengan kontribusi kode. Kontribusi pada proyek open source akan membantu kita untuk meningkatkan kemampuan pengembangan perangkat lunak."

Langkah:
	a. Fork it!

    b. Buatlah branch fitur baru: git checkout -b my-new-feature

    c. Commit perubahannya: git commit -am 'Add some features'

    d. Push ke branch di remote: git push origin my-new-feature

    e. Buat pull request

    f. Cari proyek open source.
    Kali ini, saya sebagai pengembang Android akan menggunakan Material Tabs sebagai contoh.

    g. Cari info tentang aturan kontribusi, atau hubungi developer yang terkait baik via email atau media sosial.

    h. Jika memang tidak tertera aturan kontribusi dan sang developer tidak merespon, anda bisa langsung melakukan fork proyek yang akan anda kontribusikan.

    i. Setelah selesai fork, maka repository akan masuk ke daftar repo milik anda.
	
	Untuk Code

	NB: gunakan git --help untuk melihat perintah-perintah git lainnya.

    1. Cloning project yang sudah anda fork ke akun anda

     git clone <alamat-repo>

    Contoh:

     git clone git@github.com:CreatorB/MaterialTabs.git

    2. Untuk mempermudah pengembangan, hendaknya kita menambahkan repository pusat dengan lokal milik kita agar tidak terjadi konflik dengan kontributor lainnya.

     git remote add <nama-repo> <alamat-repo>

    Contoh:

     git remote add upstream git://github.com/neokree/MaterialTabs.git

    3. Setelah remote repositori selesai, buatlah branch baru agar tidak merusak history branch utama, dan juga untuk memudahkan racking code.

     git checkout -b <nama-cabang>

    Contoh:

     git checkout -b sample-project

    4. Di cabang baru ini lah kita akan untuk melakukan perubahan kode, yang nantinya bisa kita push ke repo pusat. Untuk berpindah branch bisa kita gunakan git checkout
	<nama-cabang>, dimana <nama-cabang> adalah nama yang anda gunakan pada langkah sebelumnya.

    5. Setelah melakukan perubahan, kita bisa lakukan commit berisi deskripsi singkat tentang perubahan yang anda lakukan. Tetapi jika ada penambahan file,
	bisa menggunakan perintah git add <nama-file-baru>, atau gunakan git add . untuk menambahkan semua perubahan yang ada di direktori tersebut secara rekursif.
	Setelah itu baru bisa kita commit.

     git commit -m "<pesan singkat>"

    Contoh:

     git commit -m "fix sample project and added gradle compile"

    6. Setelah selesai melakukan commit, kita akan melakukan persiapan untuk membuat pull request (biasa disingkat PR) ke repo pusat. Pertama kita pindah branch kembali ke master.

     git checkout master

    7. Setelah itu, kita akan mengambil kode lagi dari pusat, untuk memastikan tidak terdapat konflik pada kontribusi kode kita. Konflik dapat terjadi jika dua atau lebih kontributor
	melakukan perubahan pada satu berkas, terutama jika perubahan dilakukan pada baris yang sama, terlepas dari apakah tujuan perubahan sama atau tidak.

     git fetch upstream
     git merge upstream/master

    8. Dengan proses diatas, setidaknya kita telah bisa memastikan bahwa tidak ada konflik dengan repo pusat. Sekarang kita kembali ke branch lokal development kita sample-project.

     git checkout sample-project

    9. Setelah itu, kita gabungkan cabang tersebut dengan cabang utama, sehingga kontribusi dapat dikirimkan kembali ke repositori pusat milik neokree, Material Tabs android library, dengan perintah git rebase <nama-branch>.

     git rebase master

    10. Sebelum push ke repositori pusat milik neokree, kita akan push ke repository hasil fork di awal pembahasan tadi.

    git push origin sample-project

    11. Setelah di push, kita akan melakukan pull request dan membandingkan perubahan yang telah anda lakukan terhadap repo pusat. Anda juga bisa menyisipkan pesan untuk memberitahukan developer pemilik repo pusat tentang apa yang anda lakukan. Setelah yakin terhadap perubahan yang telah anda lakukan, silahkan pilih create pull request dan menunggu tanggapan dari pemilik repo pusat. Lebih lengkapnya bisa anda lihat di tag screenshot.

