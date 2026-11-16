# BimbelCerdas – UTS Pemrograman Antarmuka Web

## Anggota Kelompok

| No | NPM | Nama | Akun GitHub | Halaman yang Dikerjakan |
|----|-----|------|-------------|-------------------------|
| 1  | 06.2025.1.82014 |  | _(isi akun GitHub)_ | Semua halaman (P1, P2, P3) |

> *Catatan: kelompok terdiri dari 1 orang, mengerjakan minimal 3 halaman sesuai ketentuan.*

---

## Sub-tema & Nama Usaha

| Item | Detail |
|------|--------|
| **Sub-tema** | No. 5 – Lembaga Kursus / Les Privat |
| **Nama Usaha** | BimbelCerdas (fiktif) |
| **Target Pengguna** | Pelajar SD–SMA dan orang tua yang mencari lembaga kursus berkualitas |
| **Framework CSS** | Bootstrap 5.3 |

---

## Sitemap

```
BimbelCerdas/
├── index.html          (P1 - Beranda: hero, layanan, testimoni, CTA)
├── katalog.html        (P2 - Katalog: program cards, tabel harga, galeri, pengajar)
├── pendaftaran.html    (P3 - Form Pendaftaran Siswa)
├── terima-kasih.html   (Halaman terima kasih — tidak dihitung sebagai halaman wajib)
├── css/
│   └── style.css       (1 file CSS utama)
└── img/
    └── (placeholder — gambar menggunakan Unsplash CDN)
```

---

## Sketsa Denah (Mobile & Desktop)

### Mobile (360px)
```
[Navbar: Logo | ☰]
[Hero: Text stack vertikal]
[Cards: 1 kolom]
[Tabel: scroll horizontal]
[Footer: 1 kolom]
```

### Desktop (1280px)
```
[Navbar: Logo | Links | CTA button]
[Hero: Text (60%) | Card visual (40%)]
[Cards: 3 kolom auto-fit]
[Tabel: full width]
[Footer: 4 kolom]
```

---

## Token CSS (Custom Properties)

| Nama Token | Nilai | Kegunaan |
|------------|-------|----------|
| `--color-primary` | `#2563eb` | Warna utama (tombol, link, aksen) |
| `--color-primary-dark` | `#1d4ed8` | Hover state tombol utama |
| `--color-primary-light` | `#dbeafe` | Background ringan, dark mode |
| `--color-secondary` | `#f59e0b` | CTA sekunder, badge, bintang |
| `--color-secondary-dark` | `#d97706` | Hover secondary |
| `--color-accent` | `#10b981` | Checklist, indikator sukses |
| `--color-bg` | `#ffffff` / `#0f172a` (dark) | Background utama |
| `--color-bg-alt` | `#f8fafc` / `#1e293b` (dark) | Background section bergantian |
| `--color-text` | `#1e293b` / `#f1f5f9` (dark) | Teks utama |
| `--color-text-muted` | `#64748b` | Teks sekunder/deskripsi |
| `--font-heading` | `'Poppins', sans-serif` | Judul & heading |
| `--font-body` | `'Inter', sans-serif` | Teks isi |
| `--radius-md` | `0.75rem` | Border radius umum |
| `--space-xl` | `2rem` | Spasi section |
| `--transition` | `0.25s ease` | Transisi hover/fokus |

---

## Tabel Breakpoint

| Nama | Nilai | Perubahan Layout |
|------|-------|-----------------|
| Mobile (default) | < 40em (< 640px) | 1 kolom, navbar collapsible |
| Tablet | ≥ 40em (≥ 640px) | 2 kolom form-row, footer 2 kolom, hero 2 kolom |
| Desktop | ≥ 60em (≥ 960px) | Footer 4 kolom, nav tampil penuh |

---

## Framework vs CSS Sendiri (E4)

### Bagian yang menggunakan Bootstrap 5.3:
- **Grid system** (`row`, `col-*`, `g-*`) di galeri pengajar (katalog.html)
- **Komponen**: navbar collapse (via JS), card `.h-100`, spacing utilities
- **Responsive breakpoints** untuk galeri foto

### Bagian yang ditulis dengan CSS sendiri (`css/style.css`):
- Semua layout utama (hero, program cards, form layout, footer)
- Custom properties (token desain)
- Navbar sticky + toggle mobile
- Form controls & validasi styling
- Animasi hover pada kartu
- Dark mode via `prefers-color-scheme`

### Perbandingan: Galeri Pengajar
**Dengan Bootstrap:**
```html
<div class="row g-3">
  <div class="col-6 col-md-4 col-lg-3">...</div>
</div>
```
**Dengan CSS murni:**
```css
.teachers-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: var(--space-lg);
}
```
**Alasan memilih Bootstrap untuk galeri ini:** Karena membutuhkan kontrol kolom yang presisi pada setiap breakpoint (6, 4, 3 kolom berbeda), Bootstrap memberikan kelas utilitas yang lebih mudah dibaca dan konsisten. CSS murni dengan `auto-fit` lebih cocok untuk grid yang fleksibel tanpa jumlah kolom pasti.

---

## Tangkapan Layar

> *Isi setelah deploy ke GitHub Pages:*
> - 360px screenshot
> - 768px screenshot
> - 1280px screenshot
> - Mode gelap screenshot

---

## Skor Lighthouse & Validasi

> *Isi setelah deploy:*
> - Lighthouse Accessibility: ≥ 90
> - Lighthouse Performance: ≥ 80
> - W3C Markup Validator: 0 error
> - Uji keyboard: semua fungsi dapat diakses via keyboard

---

## Sumber Gambar & Ikon

| Gambar | Sumber | Lisensi |
|--------|--------|---------|
| Foto siswa diskusi kelompok | [Unsplash – Annie Spratt](https://unsplash.com/photos/QckxruozjRg) | Unsplash Free |
| Foto pengajar di papan tulis | [Unsplash – Jeswin Thomas](https://unsplash.com/photos/hecib2an4T4) | Unsplash Free |
| Foto kelas laptop | [Unsplash – stem.T4L](https://unsplash.com/photos/UObRtRjKgwk) | Unsplash Free |
| Ikon emoji | Sistem (platform native) | — |

---