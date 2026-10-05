# Step 4: Pasang ffmpeg

Claude tak edit video secara "klik-klik" macam CapCut. Dia guna **ffmpeg**, enjin edit video percuma yang digunakan di seluruh dunia. Dia boleh potong, gabung, resize, tambah subtitle, buang senyap, tukar format, dan banyak lagi, semuanya melalui arahan.

Kau pasang sekali je. Lepas tu Claude yang uruskan.

=== "Windows"

    ```powershell
    winget install --id Gyan.FFmpeg -e
    ```

=== "Mac"

    ```bash
    brew install ffmpeg
    ```

**Tutup terminal dan buka balik**, kemudian semak:

```bash
ffmpeg -version
```

Kalau keluar maklumat versi, jadi.

[Step seterusnya: Buat repo & folder kerja :material-arrow-right:](05-repo.md){ .md-button }
