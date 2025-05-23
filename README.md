# module-10-tutorial2

## 2.1
![Trying Original Code](./static/image/Trying%20Original%20Code.png)

Pada gambar terlihat bahwa terdapat 1 server dan 3 client yang dibuka. Untuk setiap client baru yang dibuka, server mendapatkan notifikasi koneksi baru, dan jika satu client mengirimkan pesan, maka pesan tersebut akan diterima oleh server dan semua client lain yang terhubung.

## 2.2
Kita dapat memodifikasi port dengan mengubah nomor port pada fungsi `Server::bind` di kode `server.rs`. Kita juga harus mengubah nomor port yang digunakan klien untuk terhubung di fungsi `Client::connect` pada `client.rs`.

`server.rs` akan mendengarkan koneksi masuk ke alamat tersebut, koneksi websocket akan diinisiasi oleh klien. Server akan menerima koneksi masuk dan menangani pesan-pesan yang datang.

Alur Komunikasi:
1. Server mendengarkan pada port tertentu
2. Client inisiasi koneksi ke server pada port tersebut
3. Setelah terhubung, komunikasi dua arah dapat terjadi
4. Pesan dari satu klien diteruskan ke semua klien lain oleh server

Nomor port haruslah sama agar koneksi dapat terhubung pada port tersebut.