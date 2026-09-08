# Web Mining — Repositori GitHub + Web Statis Profile

Repositori untuk tugas **Web Mining PPWA**.

## Struktur
```
web-profile/          -> web statis profile (siap GitHub Pages)
  index.html          -> halaman profile (ganti [Nama], [NIM], foto)
  style.css
  assets/profile.jpg  -> taruh foto kamu di sini (340x340)
crawler_detik.ipynb   -> crawler detik.com 200 artikel (100 finance + 100 olahraga)
detik_berita.csv      -> output 3 kolom: id, isi_berita, tema (sep=';' Excel-friendly)
```

## Cara pakai web statis
1. Edit `web-profile/index.html` ganti semua `[Nama Lengkap]`, `[NIM]`, `[email]`, `[username]`.
2. Ganti foto: simpan foto sebagai `web-profile/assets/profile.jpg` atau ganti `src` di hero.
3. Test lokal: double-click `index.html` atau `python -m http.server` di folder `web-profile`.

## Deploy ke GitHub (web statis + web mining)
```bash
# di folder PPWA (sudah ada web-profile/)
git init
git add crawler_detik.ipynb detik_berita.csv web-profile/
git commit -m "feat: web mining 100/tema + web profile statis"
git branch -M main
git remote add origin https://github.com/[username]/web-mining-ppwa.git
git push -u origin main
```
Aktifkan **GitHub Pages**: Repo > Settings > Pages > Source: `main` / `root` atau `/web-profile` -> Save. URL jadi `https://[username].github.io/web-mining-ppwa/`.

Kalau mau Pages hanya dari folder `web-profile`, pindahkan isinya ke root repo atau set Pages folder ke `/web-profile`.

## Checklist pengumpulan
- [ ] Ganti profile di `index.html`
- [ ] Push ke GitHub public repo
- [ ] Aktifkan GitHub Pages
- [ ] Kumpulkan link repo + link Pages ke dosen
