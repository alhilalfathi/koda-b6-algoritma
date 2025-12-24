# Algoritma Chekout Tokopedia
## Deskriptif
1. Mulai
2. Login akun Tokopedia, masukan no hp yang terdaftar
3. cari barang yang akan dibeli
4. pilih barang yang akan dibeli
5. cek ukuran atau spesifikasi dari barang yang akan dibeli
6. jika tidak ada ukuran atau spesifikasi yang diinginkan, cari di toko lain
7. jika ukuran atau spesifikasi sudah sesuai, klik tombol beli langsung
8. sesuaikan alamat pengiriman
9. kemudian pilih metode pembayaran, melalui virtual account atau gopay
10. lakukan pembayaran sesuai dengan waktu yang ditentukan 
11. jika pembayaran melewati batas waktu yang ditentukan maka pembayaran gagal
12. jika pembayaran dilakukan tepat waktu, pembayaran berhasil
13. selesai


## Flowchart
```mermaid
flowchart TD
    mulai@{ shape: circle,}
    login@{ shape: lean-r, label: "Input: nomorhp"}
    verif@{ label: "nomor=#quot;verified#quot;"}
    logincek@{ shape: diamond, label: "nomorhp == nomor"}
    cariitem@{ label: "caribarang"}
    pilihitem@{ label: "pilihbarang"}
    keinginan@{ label: "keinginan = #quot;spesifikasi#quot;"}
    spek@{ shape: diamond, label: "spek = keinginan"}
    false1@{ shape: lean-r, label: "Output: #quot;cari di toko lain#quot;"}
    true1@{ label: "klik beli langsung"}
    alamat@{ label: "sesuaikan alamat"}
    pembayaran@{ shape: diamond, label: "pilih pembayaran"}
    gopay@{ label: "gopay"}
    va@{ label: "virtual account"}
    pembayaran2@{shape: diamond, label: "pembayaran sesuai waktu"}
    false2@{shape: lean-r, label: "Output:#quot;Pembayaran Gagal#quot;"}
    true2@{shape: lean-r, label: "Output:#quot;Pembayaran Berhasil#quot;"}
    selesai@{ shape: dbl-circ,}

mulai-->login-->verif-->logincek
logincek--true-->cariitem-->pilihitem-->keinginan-->spek
logincek--false-->login
spek--false-->false1-->cariitem
spek--true-->true1-->alamat-->pembayaran
pembayaran-->gopay-->pembayaran2
pembayaran-->va-->pembayaran2
pembayaran2--false-->false2-->pembayaran
pembayaran2--true-->true2-->selesai

```