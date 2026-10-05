---
name: tutorial-taufik-fyi
description: Tulis tutorial baharu untuk tutorial.taufik.fyi (MkDocs Material) dalam format tetap Taufik, iaitu satu halaman panjang, nada saya/anda/kita, sasaran beginner telefon sahaja, tema Nukilan. Guna bila Taufik minta "tambah tutorial", "tutorial baru", "buat tutorial tentang ...", "tambah page tutorial", atau menyebut tutorial.taufik.fyi. Termasuk daftar nav, kad homepage, dan buat Pull Request.
---

# Skill: Tutorial baharu untuk tutorial.taufik.fyi

Skill ini memastikan setiap tutorial baharu mempunyai **format yang sama**: satu halaman panjang, mudah diskrol di telefon, dan didaftarkan dengan betul supaya muncul di tapak.

Baca juga `CLAUDE.md` di akar repo untuk peraturan umum.

## Aliran kerja (ikut mengikut susunan)

1. **Fahami permintaan.** Jika topik, sasaran pembaca, atau platform (telefon/komputer) tidak jelas, tanya Taufik **satu soalan ringkas** sebelum menulis. Jika jelas, terus tulis.
2. **Semak fakta.** Jangan reka nama menu, butang, had saiz, harga, atau langkah yang anda tidak pasti. Jika ragu, tulis nota "nama menu boleh berubah" atau tanya Taufik. Jika langkah bergantung pada ciri yang tidak dapat disahkan, sediakan **laluan alternatif** (bahagian lipat `??? tip`) dan beritahu Taufik apa yang perlu diuji.
3. **Mulakan daripada `main` yang terkini.**
   ```bash
   git fetch origin main && git checkout -B claude/<nama-ringkas> origin/main
   ```
   Jika branch sebelum ini sudah di-merge, mulakan semula daripada `main`. Jangan tindih commit lama.
4. **Buat tiga perkara wajib** (lihat bawah). Jika satu tertinggal, tutorial tidak akan kelihatan atau tidak boleh dicapai.
5. **Semak** dengan checklist di bahagian akhir.
6. **Commit, push ke branch `claude/...`, dan buat Pull Request.** Jangan push ke `main`. Selepas PR dibuat, beritahu Taufik untuk merge dan semak tab Actions. Tapak akan auto deploy dalam lebih kurang 30 saat selepas merge.

## Tiga perkara wajib

### 1. Halaman: `docs/<slug>/index.md`

Slug: huruf kecil, sengkang, tiada ruang (contoh `edit-video-chat`). **Satu halaman sahaja**, tiada halaman berasingan per langkah, tiada butang "Langkah seterusnya".

Gunakan kerangka ini:

````markdown
---
hide:
  - navigation
  - footer
---

<span class="chip">Kategori · Telefon sahaja</span>

# Tajuk Tutorial

Ayat pembuka: apa yang pembaca akan capai, dan untuk siapa. Nyatakan jika tiada komputer atau akaun diperlukan. Tambah: "Skrol sahaja ke bawah, atau guna menu di sebelah kanan untuk melompat."

## Apa yang anda akan dapat

Hasil akhir yang konkrit. Boleh letak petikan arahan contoh dalam blockquote.

## Bagaimana ia berfungsi

Penerangan ringkas dalam 3 hingga 4 langkah bernombor, tanpa jargon.

## Apa yang perlu disediakan

- Senarai ringkas: peranti, akaun, langganan, bahan

## <Bahagian utama, satu ## per fasa>

### 1. Tindakan kecil

1. Langkah bernombor
2. Langkah bernombor

!!! success "Anda berjaya jika"
    Apa yang pembaca patut nampak.

### 2. Tindakan kecil

...

## Masalah biasa

??? question "Soalan masalah"
    Jawapan ringkas dan boleh dipraktikkan.
````

Peraturan halaman:

- `##` untuk bahagian besar, `###` untuk langkah kecil. Menu kanan (TOC) dijana daripada kedua-duanya, jadi tajuk mesti jelas dan pendek.
- Setiap `###` langkah berakhir dengan `!!! success "Anda berjaya jika"`.
- **Arahan (prompt) untuk disalin** diletakkan dalam blok ```` ```text ````, supaya ada butang copy. Satu arahan = satu blok lengkap yang boleh terus disalin. Elak ruang letak (placeholder) kecuali perlu, dan jika perlu, namakannya jelas (contoh `rakaman.mp4`).
- Jangan letak "Langkah N / TOTAL" atau butang navigasi antara langkah.
- Pautan antara tutorial: laluan relatif, contoh `[tajuk](../edit-video/index.md)`.
- Pautan dalam halaman: anchor, contoh `[Hantar kepada Claude](#hantar-kepada-claude)`.

### 2. Menu: `mkdocs.yml`

Tambah **satu baris** bawah `nav:`, selepas "Utama", dengan yang terbaru **di atas**:

```yaml
nav:
  - Utama: index.md
  - "Nama Pendek Baharu": <slug>/index.md
  - "Edit Video (Chat)": edit-video-chat/index.md
  - "Edit Video (Claude Code)": edit-video/index.md
```

Nama pendek mesti ringkas supaya muat dalam tab atas.

### 3. Kad homepage: `docs/index.md`

Dalam blok `<div class="grid cards" markdown>`, letak kad baharu **paling atas**:

```markdown
- <span class="chip">Kategori</span>

    **[Tajuk Tutorial](<slug>/index.md)**

    Satu atau dua ayat: apa yang pembaca akan dapat.

    *Satu halaman · anggaran masa · telefon sahaja*

    [Baca tutorial →](<slug>/index.md)
```

Kad mesti ada pautan, kerana CSS menjadikan seluruh kad boleh diklik melalui pautan itu. Jika tutorial ini yang terbaru, kemas kini juga butang hero "Mulakan Tutorial Terkini" supaya menuju ke halaman ini.

## Nada bahasa

Bahasa Melayu Malaysia, **profesional tetapi santai**.

- Guna **saya / anda / kita**. Tidak guna aku / kau / korang.
- Istilah teknikal kekal dalam bahasa Inggeris: repo, branch, commit, upload, download, prompt, tab Code.
- Ayat pendek, mesra, terus kepada isi. Tiada ayat berbunga-bunga.
- Terangkan istilah baharu dalam ayat yang sama, contohnya "**Repo** ialah folder projek di GitHub."
- Jangan guna bahasa Indonesia.
- Dalam arahan yang disalin untuk Claude, guna "kamu" untuk Claude dan "saya" untuk pembaca.

## Sasaran pembaca

**Beginner, kebanyakannya telefon sahaja.** Utamakan browser, aplikasi Claude, dan laman web. Elak terminal. Jika sesuatu hanya boleh dibuat di komputer, nyatakan dengan jelas di bahagian "Apa yang perlu disediakan".

## Komponen yang tersedia

| Komponen | Sintaks |
|---|---|
| Chip kategori | `<span class="chip">Teks</span>` |
| Nota tip, amaran, info, berjaya | `!!! tip "Tajuk"`, `!!! warning`, `!!! info`, `!!! success` |
| Boleh lipat | `??? question "Soalan"`, `??? tip "Tajuk"` |
| Blok kod dengan butang copy | ```` ```text ```` |
| Jadual | jadual Markdown biasa |
| Butang | `[Teks](pautan){ .md-button }` dan `{ .md-button .md-button--primary }` |

Kandungan di dalam `!!!` dan `???` mesti **diindent 4 ruang**.

Jangan tambah warna, fon, atau CSS baharu. Tema (navy `#12233D`, gold `#A9812F`, cream) ada dalam `docs/stylesheets/extra.css`.

## Kandungan niche emas dan kewangan

Jika tutorial menyentuh emas atau kewangan:

- Jangan menjanjikan **keuntungan pasti**. Gunakan bahasa pendidikan dan maklumat.
- Jika menyebut harga, nyatakan pembaca perlu **menyemak harga semasa**.
- Kisah atau testimoni pelanggan memerlukan **izin**.

## Kejujuran tentang keupayaan Claude

- Claude **tidak menonton video**. Ia menganalisis frame dan ukuran masa, jadi tiru gaya bersifat anggaran.
- Subtitle yang selaras dengan suara bergantung pada transkrip. Jika Claude tidak dapat menyalin suara, ia perlu meminta skrip.
- Jangan janjikan keputusan yang tidak dapat disahkan. Tulis had dengan terang, dan sediakan laluan alternatif.

## Fakta yang diketahui

- Upload fail melalui browser GitHub dihadkan kepada **25MB** setiap fail.
- Claude Code memerlukan langganan Claude **Pro atau Max**.
- Build MkDocs **tidak boleh diuji di sandbox** (PyPI disekat). Jangan cuba `pip install` atau `mkdocs build`. GitHub Actions yang membina tapak selepas merge.

## Checklist sebelum Pull Request

- [ ] `docs/<slug>/index.md` wujud, dengan front matter `hide: navigation, footer`
- [ ] Satu baris baharu dalam `nav:` di `mkdocs.yml`
- [ ] Kad baharu paling atas dalam `docs/index.md` (dan butang hero dikemas kini jika perlu)
- [ ] Tiada "aku / kau / korang"; guna saya / anda / kita
- [ ] Setiap `###` langkah ada "Anda berjaya jika"
- [ ] Semua arahan untuk disalin berada dalam blok ```` ```text ````
- [ ] Tiada "Langkah N / TOTAL" atau butang "Langkah seterusnya"
- [ ] Indentasi 4 ruang untuk kandungan `!!!` / `???` / senarai bersarang
- [ ] Tiada fakta yang direka; keraguan ditandakan sebagai nota atau soalan kepada Taufik
- [ ] Tidak menyentuh `docs/CNAME`, `.github/workflows/`, atau `docs/stylesheets/extra.css`
- [ ] Tajuk PR dalam Bahasa Melayu dan ringkas

## Selepas buat PR

Beritahu Taufik, dalam gaya santai dan ringkas:

1. Pautan PR
2. Apa yang ditulis (struktur dan bahagian utama)
3. **Apa yang tidak dapat disahkan** dan perlu diuji sendiri oleh Taufik
4. Selepas merge, semak tab **Actions** dan buka halaman baharu dengan hard refresh

Jangan merge sendiri melainkan Taufik meminta secara jelas.
