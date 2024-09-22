# 09011182328014_SitiAisah_SistemOperasiPraktikum5
Nama : Siti Aisah<BR/>
Nim : 09011182328014<BR/>
Kelas : SK3B<BR/>
<h1>TUGAS Job Control PRAKTIKUM 5</h1>
1. Eksekusi seluruh profile yang ada : <BR/>

a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : <BR/>
echo “Profile dari /etc/profile” <BR/>

b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu : <BR/>
/home/stD02001/.bash_profile <BR/>
/home/. stD02001/.bash_login <BR/>
/home/mahasiswa/.profile <BR/>
/home/mahasiswa/.bashrc <BR/>
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : <BR/>
echo “Profile dari .bash_profile” <BR/>
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan. <BR/>

c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: <BR/>
$ su mahasiswa <BR/>
$ exit <BR/>
kemudian gunakan opsi – sebagai berikut : <BR/>
$ su – mahasiswa <BR/>
$ exit <BR/>
Jelaskan perbedaan kedua utilitas tersebut. <BR/>

2. Prompt String (PS) <BR/>

a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell <BR/>
PS1=‟> „ <BR/>
export PS1 <BR/>

b. Eksperimen hasil PS1 : <BR/>
$ PS1=“\! > “ <BR/>
69 > PS1=”\d > “ <BR/>
Mon Sep 23 > PS1=”\t > “ <BR/>
10:10:20 > PS1=”Saya=\u > “ <BR/>
Saya=mahasiswa > PS1=”\w >” <BR/>
~ > PS1=\h >” <BR/>

3. Logout <BR/>

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout <BR/>
Echo “Terima kasih atas sesi yang diberikan”<BR/>
Sleep 5 <BR/>
clear <BR/>

4. Bash script <BR/>

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing : <BR/>
p1.sh <BR/>
#! /bin/bash <BR/>
echo “Program p1” <BR/>
ls –l <BR/>
p2.sh <BR/>
#! /bin/bash <BR/>
echo “Program p2” <BR/>
who <BR/>
p3.sh <BR/>
#! /bin/bash <BR/>
echo “Program p3” <BR/>
ps x <BR/>

b. Jalankan script tersebut sebagai berikut : <BR/>
$ ./p1.sh ; ./p3.sh ; ./p2.sh <BR/>
$ ./p1.sh & <BR/>
$ ./p1.sh $ ./p2.sh & ./p3.sh & <BR/>
$ ( ./p1.sh ; ./p3.sh ) & <BR/>

5. Jobs <BR/>

a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. <BR/>
#!/bin/bash <BR/>
while [ true ] <BR/>
do <BR/>
date >> hasil <BR/>
sleep 10 <BR/>
done <BR/>

b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut : <BR/>
$ jobs <BR/>
$ find / -print > files 2>/dev/null & <BR/>
$ jobs <BR/>
c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background <BR/>
$ fg %1 <BR/>
$ bg <BR/>
d. Stop program background dengan utilitas kil <BR/>
$ ps x <BR/>
$ kill [Nomor PID] <BR/>

6. History <BR/>

a. Ganti nilai HISTSIZE dari 1000 menjadi 20 <BR/>
$ HISTSIZE=20 <BR/>
$ h <BR/>

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir dilakukan <BR/>
$ !-5 <BR/>

c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer <BR/>
$ !! <BR/>

d. Ulangi instruksi pada history bufer nomor 150 <BR/>
$ !150 <BR/>

e. Ulangi instruksi dengan prefix “ls” <BR/>
$ !ls<BR/>
