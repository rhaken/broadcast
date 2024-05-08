# TUTORIAL - 10
## Refleksi

__2.1. Original code of broadcast chat__
![image](https://github.com/rhaken/broadcast/assets/39646450/4f8368c9-266b-4a84-9888-f19b28df60ef)


- Untuk run server: `cargo run --bin server`
- Untuk run client: `cargo run --bin client`

Dari output yang terlihat, awal mula setiap client yang ter run akan terhubung ke server lalu ketika kita memberikan pesan dari satu client maka setiap klien dan server akan menerima pesan siaran dari  klien pertama yang memberikan tersebut. 

Setiap kali seorang klien memasukkan pesan melalui baris perintah, pesan tersebut akan dikirimkan ke server dan kemudian server akan meneruskannya ke semua klien yang terhubung.
