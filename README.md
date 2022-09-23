# Jarkom-Modul-1-A03-2022

## 1. 
## 2.
## 3.
## 4.
## 5.
## 6.
## 7.
## 8. Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.

### Cari dulu file dengan ip.addr == 127.0.0.1, lalu di TCP Stream salah satu paket. Untuk total chattingan yang dilakukan terdapat 3 chattingan yang ditemukan untuk tiap stream pada beberapa paket yang berbeda.

![image](https://user-images.githubusercontent.com/72655301/191980297-fe4d0c1e-ed85-4b8f-9194-85675dcd60a0.png)

![image](https://user-images.githubusercontent.com/72655301/191980353-3dbb5ecb-00a5-4350-988c-3926a892f107.png)

![image](https://user-images.githubusercontent.com/72655301/191980400-92175443-5103-4e4d-a35a-4008d39ecd45.png)


## 9. Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan kepada atasan, beri nama file yang ditemukan dengan format [nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.

### Pertama, kita cari terlebih dahulu paket yang mengandung kata “salted” atau “Salted” pada port 9002 dengan menggunakan command “tcp.port == 9002 and tcp contains “Salted” “ (Ditemukan pada paket nomor 61). Setelah itu kita stream paket tersebut dan save as file dengan ekstensi des3. Setelah itu dengan menggunakan command “openssl des3 -d -salt -in A03.des3 -out flag.txt”. Maka akan terlihat file flag.txt berisi “JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}” didalamnya.

![image](https://user-images.githubusercontent.com/72655301/191980567-e87452a1-6b35-47eb-8fb0-7def17777da4.png)

![image](https://user-images.githubusercontent.com/72655301/191980594-26b720c4-f2b5-462a-b1e6-b210e9d11d7c.png)

![image](https://user-images.githubusercontent.com/72655301/191980622-9bdd1dfc-74b6-40b7-8f74-cbd4a1216bd6.png)


## 10. Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di atas!

### Sesuai dengan penjelasan pada nomor 9, maka kita dapatkan flag atau passwordnya adalah JaRkOm2022{8uK4N_CtF_k0k_h3h3h3}
