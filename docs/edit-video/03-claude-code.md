# Step 3: Pasang Claude Code

Ni bahagian utama. Claude Code ialah Claude yang boleh bekerja terus dalam folder komputer kau: baca fail, jalankan arahan, dan edit benda untuk kau.

!!! warning "Pastikan kau ada langganan berbayar"
    Kau perlu akaun Claude **Pro atau Max**. Daftar/langgan kat [claude.ai](https://claude.ai) dulu kalau belum.

=== "Windows"

    Dalam PowerShell:

    ```powershell
    irm https://claude.ai/install.ps1 | iex
    ```

=== "Mac"

    Dalam Terminal:

    ```bash
    curl -fsSL https://claude.ai/install.sh | bash
    ```

Lepas siap, **tutup terminal dan buka balik**, kemudian semak:

```bash
claude --version
```

## Login kali pertama

```bash
claude
```

1. Dia akan tanya pilihan tema (gelap/cerah). Pilih mana-mana.
2. Dia buka browser untuk login. Login dengan akaun Claude kau dan klik **Authorize**.
3. Balik ke terminal. Kalau nampak kotak input untuk kau taip, jadi.

Cuba taip:

```text
Hai Claude, kau boleh dengar aku?
```

Kalau dia jawab, Claude Code kau dah hidup. Taip `/exit` untuk keluar buat masa ni.

!!! tip "Cara guna asas"
    - Taip arahan biasa dalam bahasa Melayu pun boleh
    - Bila Claude nak jalankan sesuatu, dia **minta kebenaran** dulu. Baca, dan pilih Yes kalau kau setuju.
    - `Ctrl + C` untuk hentikan, `/exit` untuk keluar

[Step seterusnya: Pasang ffmpeg :material-arrow-right:](04-ffmpeg.md){ .md-button }
