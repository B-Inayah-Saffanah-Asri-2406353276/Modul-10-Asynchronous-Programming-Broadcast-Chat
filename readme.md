# Modul 10-Asynchronous Programming-Broadcast Chat

### Run original code
![alt text](image.png)

![alt text](image-1.png)
Dijalankan menggunakan command `cargo run --bin server` untuk server dan `cargo run --bin client` untuk client. Server akan membuka port 2000 dan listening koneksi yang masuk. Tiap client yang terhubung akan dimasukkan ke sistem broadcast. Saat salah satu client mengirimkan pesan ke server, server menerima pesan tersebut secara asinkron dan broadcast ke semua client yang aktif secara real-time.

### Modifying Port
**Only modifying client**
![alt text](image-2.png)

**Modifying both client and server**
![alt text](image-3.png)
Perubahan port harus dimodifikasi pada kedua sisi, yaitu client dan server. Port pada server didefinisikan dalam fungsi `let listener = TcpListener::bind("127.0.0.1:8080").await?`. Jika port keduanya berbeda, akan terjadi error `ConnectionRefused` karena client mencoba menghubungi port yang tidak dibuka oleh server.