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


## 2. Manajemen Memori,


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

## 4. Manajemen Masukan/Keluaran

> # Layanan Sistem Operasi

> # System Call


