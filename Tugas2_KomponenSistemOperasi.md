# Komponen Sistem Operasi, Layanan Sistem Operasi, dan System Call Pada OS Linux Debian

> # Komponen Sistem Operasi

Sebuah sistem operasi dapat dibagi menjadi beberapa komponen. Secara umum, para pakar sepakat bahwa terdapat sekurangnya **empat komponen manajeman utama** yaitu:
## 1. Manajemen Proses

Saat kita menjalankan perangkat komputer, pasti ada beberapa program yang berjalan. Program-program ini biasanya disebut dengan **proses**.

### Tipe Proses
Ada beberapa tipe proses yang berjalan khususnya di sistem operasi, yaitu foreground dan background.

    1. Foreground Processes
    Yaitu proses yang berjalan melalui inisiasi dan dapat dikontrol melalui terminal session. Proses ini berjalan setelah dijalankan oleh user. Sehingga tidak dapat berjalan secara otomatis.

    2. Background Processes 
    Kebalikan dari foreground processes, proses ini tidak dikenali pada terminal session. Sehingga membuat proses ini tidak mengharapkan input apapun dari user.

## Macam-Macam Manajemen Proses Linux
## * Menampilkan Semua Proses Shell Aktif/Berjalan
### 1. Perintah "top"

![Gambar1](/img/Langkah3.1.PNG)
Saat dieksekusi, aplikasi ini akan menampilkan daftar semua proses yang sedang berjalan dan setiap detik akan diperbaharui. Proses yang ditampilkan pada perintah "top" adalah yang paling besar menggunakan sumber daya.

### 2. Perintah "ps"
"ps" adalah aplikasi di Linux yang digunakan untuk menampilkan aktif proses yang berjalan pada sistem. Aplikasi ini dapat digunakan untuk melakukan manajemen proses Linux.

![Gambar1](/img/Langkah1.1.PNG)

Ada beberapa opsi yang dapat digunakan ketika menggunakan "ps" sebagai aplikasi monitoring proses.
Contohnya, kita ingin mengurutkan informasi berdasarkan penggunakan CPU terbesar. Dapat dilakukan dengan menggunakan perintah "ps aux --sort=-pcpu,+pmem"

![Gambar1](/img/Langkah2.1.PNG)

## * Menghentikan Proses Linux
Misalnya saja ketika sebuah proses menggunaan sumber daya terlalu tinggi, biasanya hal ini membuat kinerja perangkat menjadi lambat atau bahkan dapat menyebabkan _"hang"_.

Biasanya untuk mencegah dan mengatasi ini dilakukan penanganan atau mematikan proses yang tidak terlalu dibutuhkan. Salah satu caranya adalah dengan menggunakan perintah __"Kill"__. Perintah ini digunakan untuk mengirimkan sinyal ke proses untuk mengirimkan sinyal ke proses untuk menghentikan aktivitasnya.

![Gambar1](/img/Langkah4.1.PNG)

Jika perintah pada gambar diatas dieksekusi, hasilnya adalah aplikasi cron(379) akan berhenti/ditutup.


## * Mengecek Status Aplikasi

Untuk mengetahui bagaimana informasi status suatu aplikasi dengan detail, dapat menggunakan "systemctl status".

![Gambar1](/img/Langkah5.1.PNG)
***

## 2. Manajemen Memori,
Manajemen memori adalah mekanisme yang berada didalam sistem operasi untuk mengatur, mengelola, dan juga melihat proses didalam memori tersebut. Untuk dapat melihat manajemen memori dapat menggunakan perintah atau kode sebagai berikut:
## 1. "free"

![Gambar](/img/Langkah1.2.PNG)
Pada gambar diatas dapat dilihat secara ringkas rincian memori yang terpakai.
Untuk melihat lebih jelas lagi rincian memori yang ada dapat menggunakan:

![Gambar](/img/Langkah2.2.PNG)

Terlihat pada gambar diatas, dengan mengetikkan perintah cat /proc/meminfo maka akan keluar rincian total penggunaan memori.
***

## 3. Manajamen Sistem Berkas
Contoh manajemen sistem berkas diantaranya adalah membuat direktori, menghapus direktori, membuat file di dalam direktori dan juga menghapus file dalam direktori.
## * Membuat Direktori di Linux menggunakan cara manual

![Gambar1](/img/Langkah1.3.PNG)

![Gambar1](/img/Langkah2.3.PNG)

## * Membuat Direktori di Linux menggunakan terminal

![Gambar1](/img/Langkah3.3.PNG)

![Gambar1](/img/Langkah4.3.PNG)

Terlihat jelas bukan perbedaan membuat direktori di Linux dengan menggunakan terminal dan yang tidak. Bagi orang yang sudah mahir dan terbiasa menggunakan Linux, operasi-operasi atau perintah yang ingin dilakukan akan lebih mudah dan cepat dengan mengetikkan beberapa kode perintahnya di terminal. Sehingga penggunaan terminal pada OS ini sangat vital.

## * Membuat File didalam Direktori / Direktori didalam Direktori

![Gambar1](/img/Langkah5.3.PNG)

![Gambar1](/img/Langkah6.3.PNG)

![Gambar1](/img/Langkah7.3.PNG)

## * Menghapus Direktori beserta File-File didalamnya

![Gambar1](/img/Langkah8.3.PNG)
***

## 4. Manajemen Masukan/Keluaran

Apa yang kita ketik di terminal termasuk input dan yang keluar dari terminal namanya output. Input tidak harus ada di terminal, begitu juga output. Input dan output bisa berupa file. Jenis input di Linux ada dua yaitu file dan terminal (stdin). Sedangkan jenis output ada tiga yaitu file, output di terminal (stdout), dan output terminal kalau error (stderr).

## 1. File descriptor
## * Output ke layar (standar output), input dari system (kernel)
![Gambar](/img/Langkah3.2.PNG)

ps adalah input yang sudah ada dari system.

## * Output ke layar (standar output), input dari keyboard (standar input)
![Gambar](/img/Langkah4.2.PNG)

perintah cat akan meminta inputan dari keyboard dan selanjutnya akan di tampilkan di layar (akan dijadikan sebagai output).<br>
Contohnya disini saya mengetikkan kalimat "Hallo, nama saya Risma Wulandari", ketika di Enter akan keluar output yang sama seperti dengan yang kita inputkan, yaitu "Hallo, nama saya Risma Wulandari".<br>
Untuk keluar dari cat cukup ketikkan __Ctrl+D__

## * Input nama direktori, output tidak ada (membuat direktori baru), bila terjadi error maka tampilan error pada layar (standar output)

Perintah mkdir adalah perintah untuk membuat suatu dirktori, contohnya disini saya membuat direktori mydir.

![Gambar](/img/Langkah5.2.PNG)

perintah ls -l akan menampilkan direktori apa saja yang ada. Dan direktori mydir yang tadi dibuat sudah ada.

## 2. Pembelokan (redirection)
## * Pembelokan standar output
![Gambar](/img/Langkah6.2.PNG)

Kita ketikkan cat 1> myfile.txt maka kita akan membuat suatu file bernama myfile.txt. Kemudian untuk menampilkan isi filenya ketikkan cat myfile.txt.

## * Pembelokan standar error untuk disimpan di file

![Gambar](/img/Langkah7.2.PNG)

Ketika kita mengetikkan perintah mkdir mydir, output yang keluar adalah error karena direktori mydir sudah tersedia. Sekarang dengan menggunakan perintah "mkdir mydir 2> myerror.txt" yang akan terjadi adalah pesan error yang muncul tadi akan dimasukkan kedalam file baru yang bernama myerror.txt.

## * Notasi 2>&1 : pembelokan standar error (2>) adalah identik dengan file descriptor 1.

![Gambar](/img/Langkah8.2.PNG)

Ketika diketikkan 'ls filebaru', maka akan muncul pesan error.<br>Lalu ketikkan 'ls filebaru 2> out.txt'. Yang akan terjadi adalah, pesan error tadi akan masuk kedalam file baru bernama 'out.txt'.<br>
Lalu jika kita ketikkan 'ls filebaru 2> out.txt 2>&1' maka yang akan terjadi adalah perintah tersebut akan menghapus isi dari file 'out.txt'.
***

> # Layanan Sistem Operasi


> # System Call


