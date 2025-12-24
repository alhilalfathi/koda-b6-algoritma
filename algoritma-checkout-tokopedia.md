# Algoritma Checkout Tokopedia

## Deskriptif
1. mulai
2. memilih product yang akan dicheckout
3. memasukan product ke dalama keranjang
4. lakukan pembayaran barang yang akan dicheckout
5. jika pembayaran berhasil, menampilkan output pembayaran berhasil
6. jika pembayaran gagal maka kembali ke pembayaran
7. selesai

## Flowchart
```mermaid
flowchart TD
    mulai@{ shape: circle}
    inputProduct@{ shape: lean-r, label: "Input:#quot;product#quot;"}
    cart@{ label: "cart += product"}
    isPaid@{ shape: diamond, label: "isPaid"}
    falseIsPaid@{ shape: diamond, label: "Output:#quot;Menunggu pembayaran#quot;"}
    trueIsPaid@{ shape: lean-r, label: "Output:#quot;Pembayaran Berhasil#quot;"}
    selesai@{ shape: dbl-circ}

mulai-->inputProduct-->cart-->isPaid
isPaid--false-->falseIsPaid
falseIsPaid-->isPaid
isPaid--true-->trueIsPaid
trueIsPaid-->selesai

```