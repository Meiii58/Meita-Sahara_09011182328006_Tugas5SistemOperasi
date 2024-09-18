# Praktikum4

# 1. Lihat daftar secara lengkap pada direktori aktif, belokkan tampilan standard output ke file baru.
![jwb1](https://github.com/user-attachments/assets/26bb4d42-4c63-4688-87a9-7f2282d79412)
- -l: Menampilkan daftar lengkap file dengan detail (izin akses, pemilik, ukuran, dll.).
- -a: Menampilkan semua file, termasuk file yang tersembunyi (file yang dimulai dengan titik .).
- simbol > : Operator redirection untuk mengalihkan output ke file.
- file_baru.txt: Nama file tempat output akan disimpan.
  
![jwb1 1](https://github.com/user-attachments/assets/228922a3-afa1-4e4d-bf55-6f95c178197f)

perintah cat : Menampilkan isi berkas yang diminta.

# 2.  Lihat daftar secara lengkap pada direktori /etc/paswd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
![jwb2](https://github.com/user-attachments/assets/b12979f0-4c56-4375-9efb-8e4296fa7195)

Menggunakan >> untuk menambahkan hasil (append) ke file baru.txt tanpa menghapus isinya. Hasil ls -la /etc/passwd ditambahkan ke file baru.txt. bahwa /etc/passwd adalah sebuah file, bukan direktori.

# 3. Urutkan file baru dengan cara membelokkan standard input.  
![jwb3](https://github.com/user-attachments/assets/2b781668-7ed1-4cc4-a5b1-3c6786671a0e)

- sort < file_baru.txt akan mengurutkan isi file file_baru.txt dengan cara membelokkan standard input.
- Untuk menyimpan hasil pengurutan ke file baru, kamu bisa menggunakan > .

# 4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.  
![jwb4](https://github.com/user-attachments/assets/5b24cd6f-6dbf-4bb9-9c1a-fa0fe3181a4c)

Perintah ini mengurutkan file isi baru.txt dan mengarahkan output yang sudah diurutkan ke file baru bernama file_baru.urut. Isi dari file baru.txt yang sudah diurutkan akan tersimpan di file_baru.urut.

# 5. Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt. 
![jwb5](https://github.com/user-attachments/assets/d23b2fc8-5c5b-4888-b6df-f7a494525372)
- Perintah mkdir latihan6 digunakan untuk membuat direktori bernama latihan6.
- Karena direktori sudah dibuat pada perintah pertama, ketika mencoba membuat lagi, akan ada error yang dialihkan dengan 2> ke file rmdirerror.txt.
- Pada perintah kedua, 2> digunakan untuk menambahkan error (append) tanpa menimpa isi file rmdirerror.txt.
  
# 6. Urutkan kalimat berikut :  
Jakarta  
Bandung  
Surabaya  
Padang  
Palembang  
Lampung  
Dengan menggunakan notasi here document (<@@@ …@@@)  
![jwb6](https://github.com/user-attachments/assets/eb6346ca-3d92-46a1-9224-11721396e8cb)
- Notasi Here Document (<<@@@) memungkinkan kita untuk memberikan input langsung ke dalam perintah tanpa harus menggunakan file.
- Hasil dari perintah sort akan mengurutkan kalimat secara alfabetis.
  
# 7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.  
![jwb7](https://github.com/user-attachments/assets/27a4b743-f1e2-4dd0-8448-bc5b7b18ab81)
- Perintah wc (word count) menghitung jumlah baris, kata, dan karakter dalam file_baru.urut, 
- Simbol >> menambahkan hasilnya ke file_baru.txt. Output: Informasi tentang jumlah baris, kata, dan karakter dari file_baru.urut akan ditambahkan ke file_baru.txt.
  
# 8. Gunakan perintah di bawah ini dan perhatikan hasilnya. 
$ cat /etc/passwd | sort | pr –n | grep tty03  
$ find /etc –print | head  
$ head /etc/passwd | tail –5 | sort  

![jwb8](https://github.com/user-attachments/assets/487a0d26-23e1-4aa9-a12f-1da8b57ff00e)
## $ cat /etc/passwd | sort | pr –n | grep tty03 
- cat /etc/passwd: Menampilkan isi file /etc/passwd, yang berisi daftar pengguna sistem dan informasi terkait.
- | sort: Mengurutkan output dari file /etc/passwd secara alfabetis.
- | pr -n: Menambahkan nomor baris ke output yang sudah diurutkan.
- | grep tty03: Mencari baris yang berisi tty03 di output yang telah dinomori.
## $ find /etc –print | head  
- find /etc –print: Mencari dan menampilkan semua file dan direktori di bawah direktori /etc.
- | head: Menampilkan 10 baris pertama dari hasil pencarian.
##  $ head /etc/passwd | tail –5 | sort  
- head /etc/passwd: Menampilkan 10 baris pertama dari file /etc/passwd.
- | tail –5: Menampilkan 5 baris terakhir dari hasil head, yaitu baris ke-6 hingga ke-10 dari file /etc/passwd.
- | sort: Mengurutkan 5 baris terakhir secara alfabetis.

# 9. Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya. 
![jwb9](https://github.com/user-attachments/assets/96aec9e3-578f-4c8d-a980-863f8752979f)
- 'who' menampilkan siapa yang sedang login ke sistem.
- Dua kali 'cat' tidak mengubah output apapun.
- 'sort' mengurutkan output dari who.
- 'pr' memformat output menjadi kolom-kolom.
- 'head' mengambil 10 baris pertama dari hasil yang diformat.
- 'cat' | 'tail' mengambil 10 baris terakhir (atau lebih jika diubah) dari output sebelumnya.
