# Tutorial testnet Aleo AirdropFinder

<p style="font-size:14px" align="right">
<a href="https://t.me/airdropfind" target="_blank">Join Telegram Airdrop Finder<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" width="30"/></a>
</p>

<p align="center">
  <img height="auto" width="auto" src="https://raw.githubusercontent.com/bayy420-999/airdropfind/main/NavIcon.png">
</p>



## Referensi

[Discord Aleo](https://discord.gg/aleohq)

[Akun github Aleo](https://github.com/AleoHQ/snarkOS)

[Dokumen resmi Aleo](https://developer.aleo.org/testnet/getting_started/installation/)

[Pemasangan rust](https://www.rust-lang.org/tools/install)

## Persyaratan perangkat keras

| Komponen | Spesifikasi minimal |
|----------|---------------------|
|CPU|16 Cores|
|RAM|16 GB DDR4 RAM|
|Penyimpanan|128 GB HDD|
|Koneksi|10Mbit/s port|

| Komponen | Spesifikasi rekomendasi |
|----------|---------------------|
|CPU|32 Cores|
|RAM|32 GB DDR4 RAM|
|Penyimpanan|2 x 1 TB NVMe SSD|
|Koneksi|1 Gbit/s port|

## Persyaratan perangkat lunak

| Komponen | Spesifikasi minimal |
|----------|---------------------|
|Sistem Operasi|Ubuntu 16.04|

| Komponen | Spesifikasi rekomendasi |
|----------|---------------------|
|Sistem Operasi|Ubuntu 18.04 atau lebih tinggi|


## Pemasangan dependensi dan paket snarkOS

### Unduh paket snarkOS

```console
git clone https://github.com/AleoHQ/snarkOS.git --depth 1
```

### Masuk ke folder snarkOS

```console
cd snarkOS
```

### Pasang snarkOS

  ```console
  chmod +x build_ubuntu.sh; ./build_ubuntu.sh
  source ~/.bashrc
  ```

## Jalankan Aleo Node

### Buat akun

```console
snarkos account new
```

Salin dan simpan `Private Key`, `View Key`, dan `Address` yang tampil dilayar, contoh

```console
 Attention - Remember to store this account private key and view key.

  Private Key  APrivateKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me And Use In The Next Step
     View Key  AViewKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me
      Address  aleo1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  <-- Save Me
```

### Jalankan validator

```console
chmod +x run-prover.sh; ./run-prover.sh
```

Lalu masukan private key yang disimpan tadi

## Perintah berguna

### Membuat akun baru

```console
snarkos account new
```


## Troubleshoot

### Node saya tidak bisa dicompile

* Pastikan `Rust v1.64` terpasang di VPS anda, untuk cara pemasangan `Rust` dapat anda baca [disini](https://www.rust-lang.org/tools/install)
* Jika terdapat banyak error saat proses pemasangan, coba jalankan perintah `cargo clean`

### Node saya tidak bisa konek ke jaringan

* Pastikan port `4133/tcp` dan `3033/tcp` terbuka dengan menjalankan perintah
  ```console
  ufw allow 4133/tcp
  ufw allow 3033/tcp
  ```

### Saya tidak dapat membuat address baru

* Sebelum menjalankan perintah `snarkos account new` coba jalankan perintah `source ~/.bashrc`
