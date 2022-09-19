# Tutorial Instalasi Linux Debian ke Flashdisk

## Perlengkapan yang harus disiapkan:
* File iso linux
* Software untuk bootable
* 2 buah flashdisk

## Membuat Bootable Flashdisk
>## STEP 1: Download software __rufus__.

![Gambar 1](img/1-rufus.png)

>## STEP 2: Masukkan salah satu flashdisk

Ketika sudah dimasukkan, flashdisk yang akan di bootable akan terdeteksi pada bagian Device.

![Gambar 2](img/2-rufus.PNG)

>## STEP 3: Klik menu SELECT dan pilih iso Linux yang akan di bootable.

Untuk bootable kali ini saya menggunakan iso Debian 11.<br>
**Jangan lupa untuk menginstall iso nya terlebih dahulu.

![Gambar 3](img/3-rufus.PNG)

>## STEP 4: Atur skema partisi

![Gambar 4](img/4-rufus.PNG)

>## STEP 5: Klik 'Start'. Apabila muncul pop up, pilih OK/YES. Dan tunggu hingga proses selesai.

***
## Melakukan Booting dengan Flashdisk

>## STEP 1: Restart laptop kemudian pada saat layar hidup __tekan f2 sampai masuk ke menu Bios__.

<br>

>## STEP 2: Di pojok kanan atas (tampilan di laptop saya) pada menu boot prioritaskan flashdisk dengan memindahkan (menukarkan) posisinya ke paling atas.

<br>

>## STEP 3: Simpan perubahan yang tadi dilakukan kemudian keluar dari menu Bios.

***
## Instalasi Linux ke Flashdisk
>## STEP 1: Masukkan lagi flashdisk satunya yang akan diinstall linux.

Setelah berhasil booting klik enter untuk menjalankan live usb.

![Gambar 5](img/1-debian.jpg)

Klik icon install Debian, maka akan muncul pop up installer dan klik 'Next'.

![Gambar 6](img/2-debian.png)

>## STEP 2: Atur region waktu sesuaikan dengan waktu setempat.

![Gambar 7](img/3-debian.PNG)

>## STEP 3: Atur keyboard 'Default'.

![Gambar 8](img/4-debian.PNG)

>## STEP 4: Atur pengaturan partisi 'Manual'.

![Gambar 9](img/5-debian.PNG)

>## STEP 5: Pilih flashdisk yang menjadi tujuan instalasi.

![Gambar 10](img/6-debian.PNG)

>## STEP 6: Pilih 'New Partition Table'.

![Gambar 11](img/7-debian.PNG)

Pilih yang GPT.

![Gambar 12](img/8-debian.PNG)

Atur size partisi 500 Mib, file system fat32, mount point /boot/efi, dan flags centang yang boot.

![Gambar 13](img/9-debian.PNG)

Creat partition lagi untuk file system.<br>
Atur size partisi 28836 Mib, file system ext4, mount point /, dan flags centang yang root.

![Gambar 14](img/10-debian.PNG)
![Gambar 15](img/11-debian.PNG)

>## STEP 7: Atur user dan password kemudian Klik 'Next'.

![Gambar 16](img/12-debian.PNG)

>## STEP 8: Klik 'Install'.

![Gambar 17](img/13-debian.PNG)

Tunggu sampai proses install selesai.

![Gambar 18](img/14-debian.PNG)

Setelah selesai klik 'Done', maka laptop otomatis akan reboot. Kemudian cabut flashdisk bootable (flashdisk pertama).<br>
Maka proses instalasi sudah selesai.

![Gambar 19](img/15-debian.PNG)