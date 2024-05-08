# TUTORIAL - 10
## Refleksi

__2.1. Original code of broadcast chat__
![image](https://github.com/rhaken/broadcast/assets/39646450/e776b4d7-1e83-4174-b2f4-85b311ffb3c0)

- Untuk run server: `cargo run --bin server`
- Untuk run client: `cargo run --bin client`

Dari output yang terlihat, awal mula setiap client yang ter run akan terhubung ke server lalu ketika kita memberikan pesan dari satu client maka setiap klien dan server akan menerima pesan siaran dari  klien pertama yang memberikan tersebut. 

Setiap kali seorang klien memasukkan pesan melalui baris perintah, pesan tersebut akan dikirimkan ke server dan kemudian server akan meneruskannya ke semua klien yang terhubung.

__2.2: Modifying port__
![image](https://github.com/rhaken/broadcast/assets/39646450/7a754cdf-9d5a-47ec-af76-ff473579cb4e)
Gambar diatas adalah gambar dari server dan client yang tidak memiliki port yang sama (server 2000, client 8080). Hal ini menyebabkan ketidak konekan antar server dan client sehingga koneksi tidak dapat dijalankan

<hr>

![image](https://github.com/rhaken/broadcast/assets/39646450/ae10e702-614d-4410-8bcb-c9139dab0f7e)
Gambar diatas adalah kondisi ketika client dan server sudha berada di port yang sama yaitu 8080, dengan port yang sama ini menunjukkan bahwa client dan server dapat terkoneksi. Ini menunjukkan bahwa jika client diubah portnya maka server juga harus diubah karena ini adalah komunikasi 2 arah antar server dan client

__2.3 : Small changes, add IP and Port__
![image](https://github.com/rhaken/broadcast/assets/39646450/514ebcec-0883-4f77-bffe-e9bd7c6a9e58)
Output seperti diatas didapatkan dengan menggati satu line dalam server.rs menjadi seperti berikut:

Dengan mengedit kode, diharapkan ketika satu client mengirimkan pesan ke server dan server mengirimkan ke semua clientnya akan dikirim jg IP dan port dari client yang mengirimkan pesan dengan variabel `addr` yang sudah dipersiapkan dalam `bcast_tx` sebgai wadah pesan yang digunakan.
