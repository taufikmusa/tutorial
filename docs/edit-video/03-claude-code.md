<span class="chip">Langkah 3 / 7</span>

# Pasang Claude Code

Ini bahagian terpenting. Claude Code ialah Claude yang boleh bekerja terus di dalam folder komputer anda: membaca fail, menjalankan arahan, dan mengedit untuk anda.

!!! warning "Pastikan anda ada langganan berbayar"
    Anda memerlukan akaun Claude **Pro atau Max**. Jika belum ada, daftar di [claude.ai](https://claude.ai) terlebih dahulu.

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

Setelah siap, **tutup terminal dan buka semula**, kemudian semak:

```bash
claude --version
```

## Log masuk kali pertama

```bash
claude
```

1. Claude akan bertanya pilihan tema (gelap atau cerah). Pilih mana-mana.
2. Browser akan terbuka untuk log masuk. Gunakan akaun Claude anda dan klik **Authorize**.
3. Kembali ke terminal. Jika kotak input untuk menaip sudah muncul, bermakna berjaya.

Cuba taip:

```text
Hai Claude, boleh dengar saya?
```

Jika Claude menjawab, Claude Code anda sudah aktif. Taip `/exit` untuk keluar buat masa ini.

!!! tip "Cara guna yang asas"
    - Anda boleh taip arahan biasa, dalam Bahasa Melayu pun boleh
    - Sebelum menjalankan sesuatu, Claude akan **meminta kebenaran** anda. Baca dahulu, dan pilih Yes jika anda bersetuju.
    - `Ctrl + C` untuk menghentikan, `/exit` untuk keluar

[Langkah seterusnya: Pasang ffmpeg →](04-ffmpeg.md){ .md-button }
