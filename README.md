# Kalkulator Bayar Midtrans

Website kalkulator sederhana berbasis Node.js. Pengguna dapat mengetik perhitungan, tetapi hasil baru tampil setelah pembayaran Midtrans berhasil.

## Menjalankan

```bash
npm install
copy .env.example .env
npm run dev
```

Buka `http://localhost:3000`.

## Konfigurasi Midtrans

Isi `.env` dengan key dari dashboard Midtrans:

```env
MIDTRANS_IS_PRODUCTION=false
MIDTRANS_SERVER_KEY=SB-Mid-server-...
MIDTRANS_CLIENT_KEY=SB-Mid-client-...
RESULT_PRICE=5000
```

Untuk produksi:

```env
MIDTRANS_IS_PRODUCTION=true
ENABLE_CLIENT_PAYMENT_CONFIRM=false
```

Daftarkan URL notifikasi pembayaran di dashboard Midtrans:

```text
https://domain-kamu.com/api/midtrans/notification
```

`ENABLE_CLIENT_PAYMENT_CONFIRM=true` hanya untuk demo lokal, karena Midtrans tidak bisa mengirim webhook ke `localhost` tanpa tunnel.
