<span class="chip">Langkah 4 / 7</span>

# Pasang ffmpeg

Claude tidak mengedit video secara "klik-klik" seperti CapCut. Beliau menggunakan **ffmpeg**, enjin edit video percuma yang digunakan di seluruh dunia. Dengan ffmpeg, Claude boleh memotong, menggabung, resize, menambah subtitle, membuang bahagian senyap, menukar format, dan banyak lagi.

Anda hanya perlu pasang sekali. Selepas itu, Claude yang menguruskannya.

=== "Windows"

    ```powershell
    winget install --id Gyan.FFmpeg -e
    ```

=== "Mac"

    ```bash
    brew install ffmpeg
    ```

**Tutup terminal dan buka semula**, kemudian semak:

```bash
ffmpeg -version
```

Jika maklumat versi dipaparkan, bermakna berjaya.

[Langkah seterusnya: Buat repo & folder kerja →](05-repo.md){ .md-button }
