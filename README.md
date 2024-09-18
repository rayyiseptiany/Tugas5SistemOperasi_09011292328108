# Tugas5SistemOperasi_09011292328108

### 1. Melihat daftar secara lengkap pada direktori aktif, belokkan tampilan output standar ke file baru
![so1](https://github.com/user-attachments/assets/0d62f614-81e7-412a-8979-0b89d743676e)
### Perintah ls -l digunakan untuk menunjukkan daftar file dan direktori. Dengan menggunakan simbol >, output dapat dialihkan ke file baru yang dinamakan daftar_direktori.txt. Dengan demikian, daftar file dan direktori dari lokasi aktif akan disimpan dalam file tersebut.

### 2. Lihat daftar secara lengkap pada direktori /etc/paswd, belokkan tampilan standard output ke file baru tanpa menghapus file baru sebelumnya.
![so2](https://github.com/user-attachments/assets/ef4204ab-85ea-4c26-8818-9ca742b13642)
### Dengan menggunakan `>>`, kita dapat menambahkan hasil ke file `daftar_direktori.txt` tanpa menghapus isinya. Sebagai contoh, hasil dari perintah `ls -l /etc/passwd` akan ditambahkan ke dalam file tersebut.

### 3. Urutkan file baru dengan cara membelokkan standard input.
![so3](https://github.com/user-attachments/assets/40b005e1-a0a4-4917-8a99-39eeccbf7771)
### Perintah `sort` berfungsi untuk mengurutkan konten dari sebuah file. Simbol `<` digunakan untuk mengarahkan file `daftar_direktori.txt` sebagai input bagi perintah `sort`.

### 4. Urutkan file baru dengan cara membelokkan standard input dan standard output ke file baru.urut.
![so4](https://github.com/user-attachments/assets/a462d591-aa47-4187-b21f-58f6f5d3a537)
### Perintah ini akan mengurutkan konten dari `daftar_direktori.txt` dan mengarahkan output yang terurut tersebut ke file baru bernama `file_baru.urut`. Dengan demikian, isi dari `daftar_direktori.txt` yang telah diurutkan akan disimpan di dalam `file_baru.urut`.

### 5. Buatlah direktori latihan6 sebanyak 2 kali dan belokkan standard error ke file rmdirerror.txt.
![so5](https://github.com/user-attachments/assets/e946a51f-15d6-43af-b41b-6bc2c9800fb3)
### Perintah `mkdir latihan6` digunakan untuk membuat direktori baru bernama `latihan6`. Jika direktori tersebut sudah ada, mencoba membuatnya kembali akan menghasilkan error yang bisa dialihkan ke file `rmdirerror.txt` menggunakan `2>`. Pada perintah kedua, Anda dapat menggunakan `2>>` untuk menambahkan error ke file `rmdirerror.txt` tanpa menghapus isi yang sudah ada.

### 6. Urutkan kalimat berikut :
### Jakarta Bandung Surabaya Padang Palembang Lampung

![so6](https://github.com/user-attachments/assets/144ff764-ec3c-46e6-8579-d10da25dbe76)
### Dengan menggunakan notasi here document (`<<@@@ … @@@`), perintah `sort <<@@@` memulai input multi-baris yang bisa dimasukkan langsung ke dalam perintah. Setelah kata `@@@`, perintah akan dieksekusi. Outputnya adalah: kalimat-kalimat tersebut akan diurutkan secara alfabetis.

### 7. Hitung jumlah baris, kata dan karakter dari file baru.urut dengan menggunakan filter dan tambahkan data tersebut ke file baru.
![so7](https://github.com/user-attachments/assets/c4479f99-dc24-4155-b154-3e229612de21)
### Perintah `wc` (word count) digunakan untuk menghitung jumlah baris, kata, dan karakter dalam file `file_baru.urut`. Dengan menggunakan `>>`, hasil perhitungan tersebut akan ditambahkan ke dalam file `file_baru.txt`. Outputnya: informasi mengenai jumlah baris, kata, dan karakter dari `file_baru.urut` akan ditambahkan ke `file_baru.txt`.

### 8. Gunakan perintah di bawah ini dan perhatikan hasilnya.
![so8](https://github.com/user-attachments/assets/30d78a79-4df7-40df-8e11-317e6d3a0446)
### $ cat /etc/passwd | sort | pr -n | grep tty03
- `cat /etc/passwd` menampilkan isi file `/etc/passwd`.
- `sort` mengurutkan output dari `cat`.
- `pr -n` menambahkan nomor baris pada hasil yang telah diurutkan.
- `grep tty03` mencari baris yang mengandung kata `tty03`.

$ find /etc –print | head
- `find /etc –print` mencari semua file dan direktori di dalam `/etc`.
- `head` menampilkan 10 baris pertama dari hasil pencarian. 
- **Output:** 10 file atau direktori pertama yang ditemukan di bawah `/etc` akan ditampilkan.

$ /etc/passwd | tail -5 | sort
- `head /etc/passwd` mengambil 10 baris pertama dari file `/etc/passwd`.
- `tail -5` mengambil 5 baris terakhir dari output yang dihasilkan oleh `head`.
- `sort` mengurutkan baris-baris tersebut.
- **Output:** 5 baris terakhir dari 10 baris pertama dalam file `/etc/passwd` akan diurutkan secara alfabetis.

### 9. Gunakan perintah $ who | cat | cat | sort | pr | head | cat | tail dan perhatikan hasilnya.
![so9](https://github.com/user-attachments/assets/22087df6-68a0-4367-9a6c-822795ca4dd7)
#### Penjelasan Perintah

- **`who`**: Menampilkan daftar pengguna yang sedang login ke sistem.
- **`cat`**: Dua kali penggunaan `cat` tidak mempengaruhi output; hanya menyalin data yang ada.
- **`sort`**: Mengurutkan output dari perintah `who`.
- **`pr`**: Memformat output menjadi kolom-kolom yang lebih terstruktur.
- **`head`**: Mengambil 10 baris pertama dari hasil yang telah diformat.
- **`cat | tail`**: Mengambil 10 baris terakhir (atau lebih, jika diubah) dari output sebelumnya.

Proses ini memungkinkan Anda untuk mendapatkan daftar pengguna yang login, terurut dan terformat, serta mengambil bagian tertentu dari hasil tersebut.
