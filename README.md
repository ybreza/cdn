# CDN Assets

Satu repositori publik untuk **semua aset gambar/statis** dari situs-situs yang saya kelola.
File di sini disajikan lewat **jsDelivr** (CDN global, gratis, dengan cache).

## Pola URL

```
https://cdn.jsdelivr.net/gh/ybreza/cdn@main/<situs>/<nama-file>
```

- `@main` → selalu mengikuti branch `main` (cache ±12 jam).
- Untuk URL yang benar-benar permanen (mis. untuk produksi jangka panjang), buat tag
  rilis, lalu ganti `@main` menjadi `@v1`:

```
https://cdn.jsdelivr.net/gh/ybreza/cdn@v1/<situs>/<nama-file>
```

## Struktur

```
cdn/
├─ reseprosa/          # aset untuk reseprosa.my.id
│  ├─ logo.png
│  ├─ favicon.ico
│  └─ favicon_io/
└─ (situs lain)/       # tambahkan folder baru per situs
```

## Aset `reseprosa`

| File | URL |
|---|---|
| logo.png | https://cdn.jsdelivr.net/gh/ybreza/cdn@main/reseprosa/logo.png |
| favicon.ico | https://cdn.jsdelivr.net/gh/ybreza/cdn@main/reseprosa/favicon.ico |
| android-chrome-192x192.png | https://cdn.jsdelivr.net/gh/ybreza/cdn@main/reseprosa/favicon_io/android-chrome-192x192.png |
| android-chrome-512x512.png | https://cdn.jsdelivr.net/gh/ybreza/cdn@main/reseprosa/favicon_io/android-chrome-512x512.png |
| apple-touch-icon.png | https://cdn.jsdelivr.net/gh/ybreza/cdn@main/reseprosa/favicon_io/apple-touch-icon.png |
| favicon-16x16.png | https://cdn.jsdelivr.net/gh/ybreza/cdn@main/reseprosa/favicon_io/favicon-16x16.png |
| favicon-32x32.png | https://cdn.jsdelivr.net/gh/ybreza/cdn@main/reseprosa/favicon_io/favicon-32x32.png |

> Favicon di Blogger sudah memakai fitur bawaan Blogger, jadi aset favicon di sini
> hanya arsip/cadangan dan tidak dipakai oleh tema.

## Cara menambah aset baru

1. Buat/ masuk ke folder situs yang sesuai (mis. `reseprosa/`).
2. Upload file (lewat web GitHub, atau `git add` + commit + push).
3. Referensikan lewat pola URL di atas.
4. (Opsional) Buat tag `v1`, `v2`, dst. untuk URL permanen.

Disarankan memakai nama file yang deskriptif dan menghindari spasi
(gunakan `-` atau `_`).