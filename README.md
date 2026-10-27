# EcoWrap
Website Edukasi dan Katalog Kemasan Ramah Lingkungan (proyek bisnis konseptual)
Tema: UMKM Berkelanjutan – SDG 12 (Konsumsi dan Produksi yang Bertanggung Jawab)

## Anggota Kelompok
| Nama | NIM | Tugas |
|------|-----|-------|
| Ni Made Dwindayani | 2515091016 | Koordinator, halaman Home dan CSS utama |
| Ni Wayan Ami Pratiwi | 2515091049 | Halaman Shop Products dan Sustainability |
| Arminta Aprilailia Arumsari | 2515091083 | Halaman Green Guides, Business Solutions, dan About & Contact |

## Deskripsi Website
EcoWrap adalah pemasok kemasan fiktif untuk coffee shop, restoran, dan UMKM kuliner. Website memadukan katalog produk dengan edukasi agar pengunjung memahami alasan memilih kemasan berkelanjutan. Produk dan harga hanya simulasi.
Sasaran pengguna: pemilik usaha kuliner dan masyarakat umum.

## Halaman Website
| File | Fungsi |
|------|--------|
| index.html | Beranda: hero, produk unggulan, kategori, keunggulan, ajakan UMKM |
| products.html | Katalog 5 kategori dengan material, ukuran, isi, harga simulasi, tombol Order Now / Request a Quote |
| sustainability.html | Edukasi masalah kemasan, material, reusable/recyclable/compostable, SDG 12 |
| business.html | Paket B2B, custom branding, panduan memilih paket |
| guides.html | Lima artikel tips praktis |
| about.html | Cerita, visi misi, formulir, FAQ, tim, referensi |

## Teknologi
HTML5 semantik, CSS3 eksternal, Flexbox, CSS Grid, CSS Media Queries. Tanpa framework dan tanpa JavaScript.

## Penjelasan Implementasi
**1. CSS variables (satu sumber warna).** Semua warna ada di `:root` pada `css/style.css`. Mengubah palet cukup di satu tempat.
```css
:root { --forest:#294936; --cream:#F7F3EB; --charcoal:#26312A; }
body  { background: var(--cream); color: var(--charcoal); }
```
**2. Navigasi dengan Flexbox.** `.nav` memakai `display:flex` dan `justify-content:space-between` agar logo di kiri dan menu di kanan. `flex-wrap:wrap` membuat menu turun ke baris baru di layar sempit. Halaman aktif ditandai `aria-current="page"`.
**3. Layout dengan Grid.** Kartu produk memakai `display:grid` dengan `grid-template-columns: repeat(3, 1fr)`.
**4. Media queries.** Pada lebar ≤ 960px kolom menjadi 2, pada ≤ 768px menjadi 1 dan hero ditumpuk, pada ≤ 480px tombol dibuat selebar kartu.
```css
@media (max-width: 768px) { .g2, .g3 { grid-template-columns: 1fr; } }
```
**5. HTML semantik.** Setiap halaman memakai `header`, `nav`, `main`, `section`, `article`, dan `footer`, dengan satu `h1` per halaman dan atribut `alt` pada gambar informatif.
**6. Formulir.** Memakai `label` terhubung ke `input` lewat `for` dan `id`. Belum ada backend, sehingga `action` memakai `mailto:`.

## Struktur Folder
```
ecowrap-site/
|-- index.html
|-- products.html
|-- sustainability.html
|-- business.html
|-- guides.html
|-- about.html
|-- css/style.css
|-- images/ (logo dan ilustrasi SVG)
`-- README.md
```

## Website dan Repository
- Website: https://dwindayani.github.io/ecowrap/
- Repository: https://github.com/dwindayani/ecowrap

## Referensi
- UN, SDG 12: sdgs.un.org/goals/goal12
- KLHK, SIPSN: sipsn.menlhk.go.id
- Ellen MacArthur Foundation: ellenmacarthurfoundation.org
- Ilustrasi dan logo: dibuat sendiri (SVG). Font: Inter dan Playfair Display (Google Fonts, SIL OFL).
