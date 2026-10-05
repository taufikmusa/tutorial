# CLAUDE.md

Repo ini ialah **tutorial.taufik.fyi**, tapak tutorial howto milik Taufik. Dibina dengan MkDocs Material dan di-deploy ke GitHub Pages melalui GitHub Actions.

## Peraturan utama

- **Jangan push terus ke `main`.** Kerja di branch `claude/...`, kemudian buat Pull Request. Taufik sendiri yang akan merge.
- Setiap merge ke `main` akan **auto deploy** (`.github/workflows/deploy.yml`). Jangan ubah workflow itu melainkan diminta.
- Jangan sentuh `docs/CNAME`. Ia mengekalkan domain `tutorial.taufik.fyi`.
- Jangan pasang Python atau jalankan `mkdocs build` secara lokal. Persekitaran sandbox menyekat PyPI. GitHub Actions yang akan build. Selepas PR dibuat, beritahu Taufik untuk semak tab Actions.

## Pembaca sasaran

**Beginner**, kebanyakannya guna **telefon sahaja** (tiada komputer). Jadi:

- Utamakan langkah yang boleh dibuat di telefon: browser, aplikasi Claude (tab Code), laman github.com
- Jangan andaikan pembaca tahu terminal, Git, atau istilah teknikal. Jika perlu guna istilah, terangkan dalam ayat yang sama.
- Satu langkah = satu tindakan jelas. Nyatakan apa yang pembaca patut nampak apabila berjaya.

## Nada bahasa

Bahasa Melayu Malaysia, **profesional tetapi santai**.

- Guna **saya / anda / kita**. Jangan guna aku / kau / korang.
- Istilah teknikal kekal dalam bahasa Inggeris (repo, branch, commit, upload, download, prompt)
- Ayat pendek, mesra, terus kepada isi. Tiada ayat berbunga-bunga atau terlalu formal.
- Jangan guna bahasa Indonesia.

## Struktur fail

```
mkdocs.yml                 # tetapan tapak + nav (menu)
docs/
  index.md                 # homepage (hero + kad tutorial)
  CNAME                    # JANGAN ubah
  stylesheets/extra.css    # tema Nukilan (navy/gold/cream)
  <slug-tutorial>/
    index.md               # pengenalan tutorial
    01-<slug>.md           # langkah 1
    02-<slug>.md           # langkah 2
    ...
    NN-masalah.md          # masalah biasa
```

Tutorial sedia ada: `docs/edit-video/` (Edit Video dengan Claude Code, telefon sahaja).

## Checklist bila tambah tutorial baru

Setiap tutorial baru **wajib** lengkapkan ketiga-tiga ini, atau ia tidak akan kelihatan di tapak:

1. **Buat folder** `docs/<slug-tutorial>/` (slug huruf kecil, guna sengkang, tanpa ruang) dengan `index.md` dan satu fail per langkah, dinomborkan `01-`, `02-`, dan seterusnya.
2. **Daftar dalam `mkdocs.yml` bawah `nav:`**, selepas "Utama", dengan format sama seperti tutorial sedia ada:
   ```yaml
   - "Nama Pendek Tutorial":
       - Pengenalan: <slug>/index.md
       - "1. Tajuk langkah": <slug>/01-<slug-langkah>.md
       - "Masalah biasa": <slug>/NN-masalah.md
   ```
3. **Tambah kad di `docs/index.md`** dalam blok `<div class="grid cards" markdown>`. Letak tutorial terbaru **di atas**. Salin format kad sedia ada:
   ```markdown
   - <span class="chip">Kategori</span>

       **[Tajuk Tutorial](slug/index.md)**

       Satu atau dua ayat ringkas tentang apa yang pembaca akan dapat.

       *N langkah · lebih kurang X minit*

       [Baca tutorial →](slug/index.md)
   ```
   Kad mesti ada pautan kerana seluruh kad dijadikan klik melalui pautan itu.

## Templat satu halaman langkah

```markdown
<span class="chip">Langkah N / TOTAL</span>

# Tajuk Langkah

Satu dua ayat: apa langkah ini dan kenapa perlu.

1. Tindakan pertama
2. Tindakan kedua

!!! success "Anda berjaya jika"
    Apa yang pembaca patut nampak.

[Langkah seterusnya: Tajuk →](NN-slug.md){ .md-button }
```

Halaman `index.md` tutorial mesti ada: apa yang pembaca akan dapat, apa yang perlu disediakan, dan jadual "Peta perjalanan" (langkah, apa yang dibuat, anggaran masa), serta butang ke langkah 1 dengan `{ .md-button .md-button--primary }`.

Halaman "Masalah biasa" guna format `??? question "Soalan"` (boleh lipat).

## Komponen yang boleh digunakan

- Admonition: `!!! tip`, `!!! warning`, `!!! info`, `!!! success`
- Boleh lipat: `??? question "..."`, `??? tip "..."`
- Tab Windows/Mac: `=== "Windows"` (hanya jika benar-benar perlu arahan komputer)
- Blok kod dengan butang copy: gunakan ``` dan nyatakan bahasa (`text`, `bash`)
- Jadual dan senarai bernombor

## Fakta yang perlu dijaga

- Jangan reka nama menu, butang, atau had yang anda tidak pasti. Jika ragu, tulis nota "nama menu boleh berubah" atau tanya Taufik.
- Had upload fail melalui browser GitHub ialah **25MB**. Claude Code memerlukan langganan Claude **Pro atau Max**.
- Jangan tulis tarikh, harga, atau nombor versi yang cepat lapuk kecuali perlu.

## Gaya visual (jangan ubah tanpa diminta)

Tema mengikut Nukilan: navy `#12233D`, gold `#A9812F`, latar cream. Tajuk Cormorant Garamond, isi Lora, UI Inter. Semua ada dalam `docs/stylesheets/extra.css`. Gunakan komponen sedia ada dan jangan tambah warna atau gaya baharu.

## Sebelum buat Pull Request

- [ ] Nada: tiada "aku/kau/korang", guna saya/anda/kita
- [ ] Folder tutorial + `mkdocs.yml` nav + kad di `docs/index.md` semuanya dikemas kini
- [ ] Semua pautan antara halaman guna laluan relatif yang betul (`01-slug.md`, bukan URL penuh)
- [ ] Setiap langkah ada "Anda berjaya jika"
- [ ] Tajuk PR dalam Bahasa Melayu dan ringkas, dan beritahu Taufik untuk semak tab Actions selepas merge
