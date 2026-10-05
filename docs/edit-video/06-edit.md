<span class="chip">Langkah 6 / 7</span>

# Edit video pertama

Inilah masa untuk melihat kehebatannya. Dalam ruangan sembang sesi Claude, taip arahan biasa.

## Kenalkan projek kepada Claude

Taip yang berikut (gantikan `rakaman.mp4` dengan nama video anda):

```text
Ini projek edit video saya. Video asal saya ialah rakaman.mp4 dalam repo ini. Gunakan ffmpeg untuk semua proses edit. Jangan padam atau ubah video asal, dan simpan semua hasil edit dalam folder bernama "siap". Sebelum buat apa-apa, beritahu saya dahulu apa yang awak akan buat.
```

## Cuba arahan-arahan ini

Cuba satu demi satu.

### Potong bahagian tertentu

```text
Potong rakaman.mp4 dari 0:10 hingga 0:25. Simpan sebagai siap/potongan.mp4.
```

### Tukar saiz untuk TikTok / Reels / Shorts

```text
Tukar siap/potongan.mp4 kepada format menegak 9:16 (1080x1920). Letakkan video di tengah, dengan latar belakang kabur daripada video itu sendiri. Simpan sebagai siap/tiktok.mp4.
```

### Buang bahagian senyap

```text
Buang semua bahagian senyap melebihi 1 saat dalam rakaman.mp4. Simpan sebagai siap/tanpa-senyap.mp4.
```

### Kecilkan saiz fail

```text
Kecilkan saiz rakaman.mp4 supaya mudah dihantar melalui WhatsApp, tetapi kualiti masih baik. Simpan dalam folder siap.
```

### Gabungkan beberapa klip

```text
Gabungkan semua video dalam repo ini mengikut susunan nama fail. Simpan sebagai siap/gabungan.mp4.
```

## Bagaimana prosesnya berjalan

1. Anda beri arahan
2. Claude terangkan apa yang akan dibuat, kemudian menjalankan ffmpeg di cloud
3. Jika Claude meminta kebenaran, baca dahulu dan pilih **Allow** atau **Yes** jika anda bersetuju
4. Claude simpan hasil edit dalam folder `siap`, dan menghantarnya ke GitHub

!!! tip "Tip untuk hasil yang lebih tepat"
    - Sebut **nama fail** dengan tepat
    - Nyatakan **masa** dalam format `minit:saat`
    - Nyatakan **tujuan** (TikTok, YouTube, WhatsApp). Claude akan pilih saiz dan format yang sesuai.
    - Jika belum berpuas hati, cakap sahaja: *"Terlalu laju, perlahankan sedikit"* atau *"Potong 2 saat lebih awal"*. Claude akan membetulkannya.
    - Claude tidak boleh "menonton" video seperti manusia. Jika anda mahu potong mengikut isi cerita, berikan masa yang anda sudah tonton sendiri.

[Langkah seterusnya: Ambil video yang siap →](07-ambil.md){ .md-button }
