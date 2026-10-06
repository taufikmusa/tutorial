---
name: tutorial-taufik-fyi-chat
description: Sediakan tutorial baharu untuk tutorial.taufik.fyi dalam format tetap Taufik (satu halaman MkDocs Material, nada saya/anda/kita, sasaran beginner telefon sahaja) di dalam sembang Claude biasa. Hasilkan satu bundle siap salin, iaitu halaman index.md, baris nav, dan kad homepage, serta arahan untuk dihantar kepada Claude Code supaya dimasukkan ke repo. Guna bila Taufik minta "tambah tutorial", "tutorial baru", "buat tutorial tentang ...", "draf tutorial", atau menyebut tutorial.taufik.fyi.
---

# Skill: Draf tutorial untuk tutorial.taufik.fyi (Claude Chat)

Dalam sembang biasa, Claude **tidak boleh menyunting repo** tutorial.taufik.fyi secara langsung. Jadi tugas skill ini ialah menghasilkan **bundle siap pakai** dalam format tetap, yang kemudian Taufik hantar kepada Claude Code (tab Code, repo `tutorial`) untuk dimasukkan ke tapak.

Tapak: MkDocs Material, tema Nukilan, domain tutorial.taufik.fyi, auto deploy melalui GitHub Actions apabila Pull Request di-merge ke `main`.

## Aliran kerja

1. **Fahami permintaan.** Jika topik, sasaran pembaca, atau platform (telefon/komputer) tidak jelas, tanya **tidak lebih daripada dua soalan ringkas**. Jika jelas, terus tulis.
2. **Semak fakta.** Jangan reka nama menu, butang, had saiz, harga, atau langkah yang anda tidak pasti. Jika ragu, tulis nota "nama menu boleh berubah". Jika sesuatu langkah bergantung pada ciri yang tidak dapat disahkan, sediakan **laluan alternatif** (bahagian lipat `??? tip`) dan senaraikan apa yang Taufik perlu uji sendiri.
3. **Tulis bundle** (lihat bahagian "Bundle yang dihasilkan").
4. **Semak** dengan checklist di bahagian akhir.
5. **Serahkan** kepada Taufik dalam gaya santai dan ringkas: apa yang ditulis, apa yang perlu diuji, dan cara memasukkannya ke repo.

## Bundle yang dihasilkan

Hasilkan **tiga bahagian** dalam satu mesej. Jika ciri penciptaan fail tersedia, simpan halaman sebagai fail `<slug>-index.md` untuk di-download. Jika tidak, letak dalam blok kod.

### Bahagian A: halaman `docs/<slug>/index.md`

Slug: huruf kecil, sengkang, tiada ruang (contoh `edit-video-chat`). **Satu halaman sahaja**, tiada halaman berasingan per langkah, tiada butang "Langkah seterusnya".

Kerangka:

````markdown
---
hide:
  - navigation
  - footer
---

<span class="chip">Kategori · Telefon sahaja</span>

# Tajuk Tutorial

Ayat pembuka: apa yang pembaca akan capai, dan untuk siapa. Nyatakan jika tiada komputer atau akaun diperlukan.

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

## Masalah biasa

??? question "Soalan masalah"
    Jawapan ringkas dan boleh dipraktikkan.
````

Peraturan halaman:

- `##` untuk bahagian besar, `###` untuk langkah kecil. Menu kanan (TOC) dijana daripada kedua-duanya.
- Setiap `###` langkah berakhir dengan `!!! success "Anda berjaya jika"`.
- **Arahan (prompt) untuk disalin** diletakkan dalam blok ```` ```text ````, supaya ada butang copy. Satu arahan = satu blok lengkap yang boleh terus disalin.
- Jangan letak "Langkah N / TOTAL" atau butang navigasi antara langkah.
- Pautan antara tutorial: laluan relatif, contoh `[tajuk](../edit-video/index.md)`. Pautan dalam halaman: anchor, contoh `[Hantar kepada Claude](#hantar-kepada-claude)`.
- Kandungan di dalam `!!!`, `???`, dan senarai bersarang mesti **diindent 4 ruang**.

### Bahagian B: baris menu untuk `mkdocs.yml`

Satu baris bawah `nav:`, selepas "Utama", dengan yang terbaru di atas:

```yaml
  - "Nama Pendek": <slug>/index.md
```

Nama pendek mesti ringkas supaya muat dalam tab atas.

### Bahagian C: kad untuk `docs/index.md`

Letak paling atas dalam blok `<div class="grid cards" markdown>`:

```markdown
- <span class="chip">Kategori</span>

    **[Tajuk Tutorial](<slug>/index.md)**

    Satu atau dua ayat: apa yang pembaca akan dapat.

    *Satu halaman · anggaran masa · telefon sahaja*

    [Baca tutorial →](<slug>/index.md)
```

Kad mesti ada pautan, kerana CSS menjadikan seluruh kad boleh diklik melalui pautan itu.

## Arahan untuk Claude Code

Selepas bundle, sediakan satu blok ```` ```text ```` yang Taufik boleh tampal dalam sesi **tab Code, repo `tutorial`**. Blok ini mesti **mengandungi kandungan halaman penuh**, supaya tidak bergantung pada lampiran. Gunakan susunan ini:

````text
Tambah tutorial baharu ke tapak ini mengikut skill tutorial-taufik-fyi.

Slug: <slug>
Nama menu: <Nama Pendek>
Kategori kad: <Kategori>
Ayat kad: <satu atau dua ayat>
Meta kad: Satu halaman · <anggaran masa> · telefon sahaja

Kandungan penuh docs/<slug>/index.md (gunakan seperti sedia ada, jangan ubah nada atau susunan, hanya betulkan ralat format jika ada):

<tampal seluruh halaman, termasuk front matter>

Buat Pull Request ke main dan beritahu saya apa yang tidak dapat disahkan.
````

Jika halaman terlalu panjang untuk dimuatkan dalam satu blok, pecahkan kepada dua mesej dan beritahu Taufik supaya menghantar kedua-duanya dalam satu sesi.

## Nada bahasa

Bahasa Melayu Malaysia, **profesional tetapi santai**, boleh campur dengan English yang biasa orang Malaysia guna.

- Guna **saya / anda / kita**. Tidak guna aku / kau / korang.
- Istilah teknikal kekal dalam bahasa Inggeris: repo, branch, commit, upload, download, prompt, tab Code.
- Campur dengan English yang lazim orang Malaysia guna. Tulis **install** (bukan "pasang"), **download** (bukan "muat turun"), **upload** (bukan "muat naik"), **login** (bukan "log masuk"), dan juga app, update, setting, link, account, TAC.
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
| Nota | `!!! tip "Tajuk"`, `!!! warning`, `!!! info`, `!!! success` |
| Boleh lipat | `??? question "Soalan"`, `??? tip "Tajuk"` |
| Blok kod dengan butang copy | ```` ```text ```` |
| Jadual | jadual Markdown biasa |
| Butang | `[Teks](pautan){ .md-button }` dan `{ .md-button .md-button--primary }` |

Jangan cadangkan warna, fon, atau CSS baharu. Tema (navy `#12233D`, gold `#A9812F`, cream) sudah ditetapkan.

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
- Tapak dibina oleh GitHub Actions selepas merge. Claude Chat tidak dapat menguji build, jadi jangan dakwa halaman "sudah diuji".

## Checklist sebelum menyerahkan

- [ ] Bahagian A, B, dan C semuanya ada
- [ ] Front matter `hide: navigation, footer` ada pada halaman
- [ ] Tiada "aku / kau / korang"; guna saya / anda / kita
- [ ] Setiap `###` langkah ada "Anda berjaya jika"
- [ ] Semua arahan untuk disalin berada dalam blok ```` ```text ````
- [ ] Tiada "Langkah N / TOTAL" atau butang "Langkah seterusnya"
- [ ] Indentasi 4 ruang untuk kandungan `!!!` / `???`
- [ ] Tiada fakta yang direka; keraguan ditandakan sebagai nota
- [ ] Arahan untuk Claude Code disertakan, dengan kandungan halaman penuh

## Selepas menyerahkan

Beritahu Taufik, dalam gaya santai dan ringkas:

1. Apa yang ditulis (struktur dan bahagian utama)
2. **Apa yang tidak dapat disahkan** dan perlu diuji sendiri
3. Langkah seterusnya: buka tab **Code**, pilih repo `tutorial`, tampal arahan, kemudian merge Pull Request di GitHub. Tapak auto deploy dalam lebih kurang 30 saat. Semak tab **Actions** jika halaman tidak muncul.
