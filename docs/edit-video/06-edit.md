<span class="chip">Langkah 6 / 7</span>

# Edit video pertama

Inilah masa untuk melihat kehebatannya.

## Buka Claude dalam folder projek

Pastikan terminal anda berada dalam folder `video-saya`, kemudian:

```bash
claude
```

Kali pertama dalam folder baharu, Claude akan bertanya **"Do you trust this folder?"**. Pilih **Yes**, kerana ini folder anda sendiri.

## Kenalkan projek kepada Claude

Taip yang berikut (ubah mengikut keperluan anda):

```text
Ini projek edit video saya. Video asal ada dalam folder "mentah", hasil siap simpan dalam folder "siap". Gunakan ffmpeg untuk semua proses edit. Jangan padam atau ubah sebarang fail dalam "mentah". Sebelum buat apa-apa, beritahu saya apa yang awak akan buat.
```

## Cuba arahan-arahan ini

Cuba satu demi satu. Gantikan nama fail dengan video anda.

### Potong bahagian tertentu

```text
Potong video mentah/rakaman.mp4 dari 0:10 hingga 0:45. Simpan sebagai siap/potongan.mp4.
```

### Tukar saiz untuk TikTok / Reels / Shorts

```text
Tukar siap/potongan.mp4 kepada format menegak 9:16 (1080x1920). Letakkan video di tengah, dengan latar belakang kabur daripada video itu sendiri. Simpan sebagai siap/tiktok.mp4.
```

### Buang bahagian senyap

```text
Buang semua bahagian senyap melebihi 1 saat dalam mentah/rakaman.mp4. Simpan sebagai siap/tanpa-senyap.mp4.
```

### Kecilkan saiz fail

```text
Kecilkan saiz mentah/rakaman.mp4 supaya mudah dihantar melalui WhatsApp, tetapi kualiti masih baik. Simpan dalam folder siap.
```

### Gabungkan beberapa klip

```text
Gabungkan semua video dalam folder mentah mengikut susunan nama fail. Simpan sebagai siap/gabungan.mp4.
```

## Bagaimana prosesnya berjalan

1. Anda beri arahan
2. Claude terangkan apa yang akan dibuat dan **meminta kebenaran** untuk menjalankan ffmpeg
3. Anda pilih **Yes**
4. Claude siapkan fail dalam folder `siap`
5. Buka folder `siap` dan lihat hasilnya

!!! tip "Tip untuk hasil yang lebih tepat"
    - Sebut **nama fail** dengan tepat
    - Nyatakan **masa** dalam format `minit:saat`
    - Nyatakan **tujuan** (TikTok, YouTube, WhatsApp). Claude akan pilih saiz dan format yang sesuai.
    - Jika belum berpuas hati, cakap sahaja: *"Terlalu laju, perlahankan sedikit"* atau *"Potong 2 saat lebih awal"*. Claude akan membetulkannya.
    - Claude tidak boleh "menonton" video seperti manusia. Jika anda mahu potong mengikut isi cerita, berikan masa yang anda sudah tonton sendiri.

[Langkah seterusnya: Simpan kerja ke GitHub →](07-simpan.md){ .md-button }
