# Modul 10-Asynchronous Programming-Broadcast Chat

### Run original code
![alt text](image.png)
![alt text](image-1.png)
Dijalankan menggunakan command `cargo run --bin server` untuk server dan `cargo run --bin client` untuk client. Server akan membuka port 2000 dan listening koneksi yang masuk. Tiap client yang terhubung akan dimasukkan ke sistem broadcast. Saat salah satu client mengirimkan pesan ke server, server menerima pesan tersebut secara asinkron dan broadcast ke semua client yang aktif secara real-time.



