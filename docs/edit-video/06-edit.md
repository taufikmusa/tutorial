# Step 6: Edit video pertama

Masa untuk tengok magic.

## Buka Claude dalam folder projek

Pastikan terminal kau berada dalam folder `video-saya`, kemudian:

```bash
claude
```

Kali pertama dalam folder baru, dia akan tanya **"Do you trust this folder?"**. Pilih **Yes** sebab ni folder kau sendiri.

## Kenalkan projek pada Claude

Taip ni (ubah ikut keperluan kau):

```text
Ni projek edit video aku. Video asal dalam folder "mentah", hasil siap simpan dalam folder "siap". Guna ffmpeg untuk semua edit. Jangan sekali-kali padam atau ubah fail dalam "mentah". Sebelum buat apa-apa, beritahu aku apa yang kau nak buat.
```

## Cuba arahan-arahan ni

Satu demi satu. Tukar nama fail dengan video kau.

### Potong bahagian tertentu

```text
Potong video mentah/rakaman.mp4 dari 0:10 sampai 0:45. Simpan sebagai siap/potongan.mp4.
```

### Tukar saiz untuk TikTok / Reels / Shorts

```text
Tukar siap/potongan.mp4 jadi format menegak 9:16 (1080x1920). Letak video kat tengah, dan latar belakang kabur dari video sendiri. Simpan sebagai siap/tiktok.mp4.
```

### Buang bahagian senyap

```text
Buang semua bahagian senyap lebih 1 saat dalam mentah/rakaman.mp4. Simpan sebagai siap/tanpa-senyap.mp4.
```

### Kecilkan saiz fail

```text
Kecilkan saiz mentah/rakaman.mp4 supaya boleh hantar melalui WhatsApp, tapi kualiti masih elok. Simpan dalam siap/.
```

### Gabung beberapa klip

```text
Gabung semua video dalam folder mentah ikut susunan nama fail. Simpan sebagai siap/gabungan.mp4.
```

## Cara dia kerja

1. Kau bagi arahan
2. Claude terangkan apa dia nak buat dan **minta kebenaran** untuk jalankan ffmpeg
3. Kau pilih **Yes**
4. Dia siapkan fail dalam folder `siap`
5. Buka folder `siap` dan tengok hasilnya

!!! tip "Tips supaya hasil lagi tepat"
    - Sebut **nama fail** dengan tepat
    - Sebut **masa** dalam format `minit:saat`
    - Sebut **tujuan** (TikTok, YouTube, WhatsApp). Claude akan pilih saiz dan format yang sesuai.
    - Kalau tak puas hati, cakap je: *"Terlalu laju, perlahankan sikit"* atau *"Potong 2 saat lebih awal"*. Claude akan betulkan.
    - Claude tak boleh "tengok" video macam mata manusia. Kalau kau nak potong ikut isi cerita, bagi dia masa yang kau dah tengok sendiri.

[Step seterusnya: Simpan kerja ke GitHub :material-arrow-right:](07-simpan.md){ .md-button }
