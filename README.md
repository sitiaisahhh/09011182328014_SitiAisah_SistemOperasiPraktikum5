# 09011182328014_SitiAisah_SistemOperasiPraktikum5
Nama : Siti Aisah<BR/>
Nim : 09011182328014<BR/>
Kelas : SK3B<BR/>
<h1>TUGAS Job Control PRAKTIKUM 5</h1>

1. Eksekusi seluruh profile yang ada : <BR/>

a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : <BR/>
echo “Profile dari /etc/profile” <BR/>
<img src="https://github.com/user-attachments/assets/e63cde1a-89f4-4dcc-9f86-4ecb9a4924ca" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/db94f07f-be4e-4465-9c38-e46738a47457" width=500/><BR/>
b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu : <BR/>
/home/stD02001/.bash_profile <BR/>
/home/. stD02001/.bash_login <BR/>
/home/mahasiswa/.profile <BR/>
/home/mahasiswa/.bashrc <BR/>
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : <BR/>
echo “Profile dari .bash_profile” <BR/>
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file yang bersangkutan. <BR/>
<img src="https://github.com/user-attachments/assets/e0ff93f2-06ee-431e-a39c-6459d2559276" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/8035ad53-3db4-4419-bf62-c752c34f6188" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/f5a2df83-c12a-4c42-88d5-8020c92e4431" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/c6dae746-2697-40ec-af9c-319cbba69a68" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/c23cc848-da41-472e-8218-e6360eec6bfd" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/85a51eb4-e3cc-4aff-944f-7251b1b39da7" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/aecd86b5-1a22-4f9e-b26a-4adf27dc8bfd" width=500/><BR/>
c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: <BR/>
$ su mahasiswa <BR/>
$ exit <BR/>
kemudian gunakan opsi – sebagai berikut : <BR/>
$ su – mahasiswa <BR/>
$ exit <BR/>
Jelaskan perbedaan kedua utilitas tersebut. <BR/>
penjelasan : Perintah su mahasiswa hanya mengganti pengguna tanpa mengubah environment dan direktori kerja. Sedangkan su - mahasiswa mengganti pengguna sekaligus menjalankan sesi shell login penuh untuk pengguna baru termasuk perpindahan ke direktori home pengguna. Perintah exit kemudian digunakan untuk keluar dari sesi shell pengguna yang baru dan kembali ke pengguna sebelumnya.
<img src="https://github.com/user-attachments/assets/0dc9b036-cd0c-4855-8d3a-65648d2af255" width=500/><BR/>
2. Prompt String (PS) <BR/>

a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell <BR/>
PS1=‟> „ <BR/>
export PS1 <BR/>
<img src="https://github.com/user-attachments/assets/694e432d-d03b-4794-89ce-e9e5a231a410" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/88962a07-cc32-4631-84c4-6a0d97cfff5f" width=500/><BR/>
b. Eksperimen hasil PS1 : <BR/>
$ PS1=“\! > “ <BR/>
69 > PS1=”\d > “ <BR/>
Mon Sep 23 > PS1=”\t > “ <BR/>
10:10:20 > PS1=”Saya=\u > “ <BR/>
Saya=mahasiswa > PS1=”\w >” <BR/>
~ > PS1=\h >” <BR/>
<img src="https://github.com/user-attachments/assets/92890467-6111-4658-9264-af949703699f" width=500/><BR/>

3. Logout <BR/>

Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout <BR/>
Echo “Terima kasih atas sesi yang diberikan”<BR/>
Sleep 5 <BR/>
clear <BR/>
<img src="https://github.com/user-attachments/assets/a48c4035-138c-4abd-a5a9-918170d46b46" width=500/><BR/>

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
<img src="https://github.com/user-attachments/assets/c07ebd98-d68d-4fa3-869a-afb42fff8a21" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/5a3d47ca-de9a-4748-8990-55eb220aa214" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/c71cc20a-a3b7-4e95-b8df-409c3ca91d11" width=500/><BR/>

b. Jalankan script tersebut sebagai berikut : <BR/>
$ ./p1.sh ; ./p3.sh ; ./p2.sh <BR/>
$ ./p1.sh & <BR/>
$ ./p1.sh $ ./p2.sh & ./p3.sh & <BR/>
$ ( ./p1.sh ; ./p3.sh ) & <BR/>
<img src="https://github.com/user-attachments/assets/c96dfa40-8bbc-485c-afc5-844a2013d9a1" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/9b56f573-a036-428a-b7eb-6eff8f5524cb" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/6fcca3b9-5dd3-4bde-9eb0-66bf845257c6" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/0ff41441-7ec6-4e26-9864-63813e078be9" width=500/><BR/>

5. Jobs <BR/>

a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. <BR/>
#!/bin/bash <BR/>
while [ true ] <BR/>
do <BR/>
date >> hasil <BR/>
sleep 10 <BR/>
done <BR/>
<img src="https://github.com/user-attachments/assets/3e8a5145-e5a3-48d6-b402-01266776a466" width=500/><BR/>
b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut : <BR/>
$ jobs <BR/>
$ find / -print > files 2>/dev/null & <BR/>
$ jobs <BR/>
<img src="https://github.com/user-attachments/assets/bd50ad46-bbba-4571-8eb2-f769bbef47b1" width=500/><BR/>
c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke background <BR/>
$ fg %1 <BR/>
$ bg <BR/>
<img src="https://github.com/user-attachments/assets/85fab868-74ff-4f49-b005-7209d37a9db7" width=500/><BR/>
d. Stop program background dengan utilitas kil <BR/>
$ ps x <BR/>
$ kill [Nomor PID] <BR/>
<img src="https://github.com/user-attachments/assets/58761993-ff2b-45c6-b53e-efecf16293ab" width=500/><BR/>

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
<img src="https://github.com/user-attachments/assets/b4d99059-ee73-4635-a4d4-87beeb718f00" width=500/><BR/>
<img src="https://github.com/user-attachments/assets/895b5b5d-2196-42a2-9722-275b63d870dd" width=500/><BR/>
