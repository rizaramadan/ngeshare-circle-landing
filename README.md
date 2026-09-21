# NgeShare Circle — Landing Page (AlpineJS + JSON)

Landing statis. Semua teks mudah diubah tanpa sentuh HTML.

## File
- `index.html` — template + AlpineJS + Tailwind CDN. Jangan edit teks di sini.
- `content.json` — SEMUA data landing. Edit file ini saja.
- `images/` — foto lokal (sudah terisi, tinggal timpa kalau ada foto asli):
  - `hero.jpg` — FOTO ASLI dari desain (crop kanan foto hangout, tanpa teks)
  - `pengenalan.jpg` — kyai ceramah di panggung (mirip thumbnail video)
  - `komunitas-1.jpg` — santri ngaji bersama ustadz
  - `komunitas-2.jpg` — foto grup pemuda pengajian
  - `komunitas-3.jpg` — suasana kajian di masjid
  - `fasilitator.jpg` — ustadz di depan mushola (slot potrait)
  - `app-phone.png` — BELUM ADA, masih pakai fallback internet. Ganti dengan mockup HP NgeShare asli.

Jika file di `images/` belum ada, otomatis pakai gambar fallback dari internet (lihat field `*Fallback` di JSON).

## Sumber foto (milik NgeShare sendiri)
- `hero.jpg` — crop dari screenshot desain (adegan sama seperti `moment-2`)
- `pengenalan.jpg`, `komunitas-1..4.jpg`, `fasilitator.jpg` — diambil dari https://www.ngeshare.id/landing (`/landing/moment-1..6.jpg`, thumbnail YouTube `L33nYyXrD6o`)
- `app-phone.png` — BELUM ADA, masih pakai fallback internet. Ganti dengan mockup HP NgeShare asli.

Tidak ada masalah lisensi karena semua foto milik NgeShare.

## Cara edit
1. Buka `content.json`
2. Ubah `title`, `desc`, `label`, `href`, `value`
3. Refresh browser. Selesai.

Struktur JSON:
- `nav`, `hero (+stats)`, `duluSekarang`, `kenalan`, `fitur`, `caraKerja`, `komunitas`, `fasilitator`, `testimoni`, `faq`, `download`, `footer`

FAQ tambah/hapus: tambah/hapus object `{q,a}` di `faq.items`.
Testimoni tambah/hapus: tambah/hapus object di `testimoni.items`.
Fitur / langkah / statistik sama polanya.

## Cara jalan
Opsi 1 — buka langsung (butuh server lokal karena fetch JSON):
```bash
npx serve .
# atau
python3 -m http.server 8000
# buka http://localhost:8000
```

Opsi 2 — deploy ke Vercel / Netlify / GitHub Pages: upload folder ini apa adanya.

## Tech
- Tailwind via CDN
- AlpineJS 3 via CDN (`x-data`, `x-for`, `x-text`, `x-show`)
- Tidak ada build step.
