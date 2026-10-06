# CLAUDE.md

Repo ini ialah **tutorial.taufik.fyi**, tapak tutorial howto milik Taufik. Dibina dengan MkDocs Material dan di-deploy ke GitHub Pages melalui GitHub Actions.

> **Menambah tutorial baharu?** Guna skill `tutorial-taufik-fyi` (`.claude/skills/tutorial-taufik-fyi/SKILL.md`). Ia mengandungi kerangka halaman, templat kad, dan checklist penuh.

## Peraturan utama

- **Jangan push terus ke `main`.** Kerja di branch `claude/...`, kemudian buat Pull Request. Taufik sendiri yang akan merge.
- Setiap merge ke `main` akan **auto deploy** (`.github/workflows/deploy.yml`). Jangan ubah workflow itu melainkan diminta.
- Jangan sentuh `docs/CNAME`. Ia mengekalkan domain `tutorial.taufik.fyi`.
- Jangan install Python atau jalankan `mkdocs build` secara lokal. Persekitaran sandbox menyekat PyPI. GitHub Actions yang akan build. Selepas PR dibuat, beritahu Taufik untuk semak tab Actions.

## Pembaca sasaran

**Beginner**, kebanyakannya guna **telefon sahaja** (tiada komputer). Jadi:

- Utamakan langkah yang boleh dibuat di telefon: browser, aplikasi Claude (tab Code), laman github.com
- Jangan andaikan pembaca tahu terminal, Git, atau istilah teknikal. Jika perlu guna istilah, terangkan dalam ayat yang sama.
- Satu langkah = satu tindakan jelas. Nyatakan apa yang pembaca patut nampak apabila berjaya.

## Nada bahasa

Bahasa Melayu Malaysia, **profesional tetapi santai**, boleh campur dengan English yang biasa orang Malaysia guna.

- Guna **saya / anda / kita**. Jangan guna aku / kau / korang.
- Istilah teknikal kekal dalam bahasa Inggeris (repo, branch, commit, upload, download, prompt)
- Campur dengan English yang lazim orang Malaysia guna. Tulis **install** (bukan "pasang"), **download** (bukan "muat turun"), **upload** (bukan "muat naik"), **login** (bukan "log masuk"), dan juga app, update, setting, link, account, TAC.
- Ayat pendek, mesra, terus kepada isi. Tiada ayat berbunga-bunga atau terlalu formal.
- Jangan guna bahasa Indonesia.

## Struktur fail

```
mkdocs.yml                 # tetapan tapak + nav (menu atas)
docs/
  index.md                 # homepage (hero + kad tutorial)
  CNAME                    # JANGAN ubah
  stylesheets/extra.css    # tema Nukilan (navy/gold/cream)
  <slug-tutorial>/
    index.md               # SATU halaman penuh untuk tutorial itu
```

**Setiap tutorial ialah SATU halaman panjang** (`docs/<slug>/index.md`), bukan banyak halaman langkah. Pembaca skrol dari atas ke bawah, dan menu di sebelah kanan (daftar kandungan, dijana daripada tajuk `##` dan `###`) membantu mereka melompat. Jangan buat butang "Langkah seterusnya" atau halaman berasingan per langkah.

Tutorial sedia ada:

- `docs/share-slide-zoom/index.md`: Cara Share Slide dalam Zoom Meeting (laptop Windows dan MacBook, bukan telefon)
- `docs/simpan-emas-public-gold/index.md`: Cara Simpan Emas di Public Gold (telefon sahaja)
- `docs/edit-video-chat/index.md`: Edit Video Emas & Kewangan dalam Claude Chat (tanpa GitHub, telefon sahaja)
- `docs/edit-video/index.md`: Tiru Gaya Video dengan Claude Code (telefon sahaja)

## Checklist bila tambah tutorial baru

Setiap tutorial baru **wajib** lengkapkan ketiga-tiga ini, atau ia tidak akan kelihatan di tapak:

1. **Buat `docs/<slug>/index.md`** (slug huruf kecil, guna sengkang, tanpa ruang). Mulakan dengan front matter ini supaya tiada menu kiri dan tiada butang sebelum/seterusnya:
   ```yaml
   ---
   hide:
     - navigation
     - footer
   ---
   ```
2. **Daftar dalam `mkdocs.yml` bawah `nav:`**, selepas "Utama", satu baris sahaja:
   ```yaml
   - "Nama Pendek": <slug>/index.md
   ```
3. **Tambah kad di `docs/index.md`** dalam blok `<div class="grid cards" markdown>`. Letak tutorial terbaru **di atas**. Salin format kad sedia ada:
   ```markdown
   - <span class="chip">Kategori</span>

       **[Tajuk Tutorial](slug/index.md)**

       Satu atau dua ayat ringkas tentang apa yang pembaca akan dapat.

       *Satu halaman · anggaran masa · telefon sahaja*

       [Baca tutorial →](slug/index.md)
   ```
   Kad mesti ada pautan kerana seluruh kad dijadikan klik melalui pautan itu.

## Susunan satu halaman tutorial

```markdown
<span class="chip">Kategori</span>

# Tajuk Tutorial

Ayat pembuka: apa yang pembaca akan capai, dan untuk siapa.

## Apa yang anda akan dapat
## Bagaimana ia berfungsi
## Apa yang perlu disediakan
## <Bahagian utama, satu ## per fasa>
### 1. Langkah kecil
### 2. Langkah kecil
## Masalah biasa
```

- Guna `##` untuk bahagian besar dan `###` untuk langkah kecil, supaya menu kanan kemas.
- Setiap langkah: satu tindakan jelas, kemudian `!!! success "Anda berjaya jika"` yang menyatakan apa yang pembaca patut nampak.
- Arahan (prompt) untuk disalin: letak dalam blok ```` ```text ```` supaya ada butang copy.
- Bahagian "Masalah biasa" guna `??? question "Soalan"` (boleh lipat).
- Jangan letak "Langkah N / TOTAL" atau butang "Langkah seterusnya".

## Komponen yang boleh digunakan

- Admonition: `!!! tip`, `!!! warning`, `!!! info`, `!!! success`
- Boleh lipat: `??? question "..."`, `??? tip "..."`
- Tab Windows/Mac: `=== "Windows"` (hanya jika benar-benar perlu arahan komputer)
- Jangan janjikan perkara yang Claude tidak boleh buat. Claude menganalisis video melalui frame dan ukuran masa, bukan menonton, jadi tiru gaya bersifat anggaran.
- Blok kod dengan butang copy: gunakan ``` dan nyatakan bahasa (`text`, `bash`)
- Jadual dan senarai bernombor

## Fakta yang perlu dijaga

- Jangan reka nama menu, butang, atau had yang anda tidak pasti. Jika ragu, tulis nota "nama menu boleh berubah" atau tanya Taufik.
- Had upload fail melalui browser GitHub ialah **25MB**. Claude Code memerlukan langganan Claude **Pro atau Max**.
- Jangan tulis tarikh, harga, atau nombor versi yang cepat lapuk kecuali perlu.

## WhatsApp

Setiap halaman automatik ada **kad WhatsApp di atas** dan **butang WhatsApp terapung** (dalam `overrides/main.html`). Jangan tambah butang WhatsApp kedua dalam kandungan melainkan perlu. Mesej pra-isi: "Boleh guide saya simpan emas Public Gold".

## Gaya visual (jangan ubah tanpa diminta)

Tema mengikut Nukilan: navy `#12233D`, gold `#A9812F`, latar cream. Tajuk Cormorant Garamond, isi Lora, UI Inter. Semua ada dalam `docs/stylesheets/extra.css`. Gunakan komponen sedia ada dan jangan tambah warna atau gaya baharu.

## Sebelum buat Pull Request

- [ ] Nada: tiada "aku/kau/korang", guna saya/anda/kita
- [ ] `docs/<slug>/index.md` + satu baris `nav` dalam `mkdocs.yml` + kad di `docs/index.md` semuanya dikemas kini
- [ ] Front matter `hide: navigation, footer` ada pada halaman tutorial
- [ ] Pautan dalam halaman guna anchor (`#tajuk-bahagian`) atau laluan relatif yang betul, bukan URL penuh
- [ ] Setiap langkah ada "Anda berjaya jika"
- [ ] Tajuk PR dalam Bahasa Melayu dan ringkas, dan beritahu Taufik untuk semak tab Actions selepas merge
