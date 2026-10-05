<span class="chip">Langkah 2 / 7</span>

# Pasang Git & GitHub CLI

Dua alat ini yang menghubungkan komputer anda dengan GitHub.

- **Git** = sistem menyimpan versi kerja anda
- **GitHub CLI (`gh`)** = alat untuk log masuk ke GitHub dari terminal, tanpa pening urus password

=== "Windows"

    **Buka terminal dahulu:** tekan butang Windows, taip `PowerShell`, kemudian tekan Enter.

    Copy-paste arahan ini dan tekan Enter:

    ```powershell
    winget install --id Git.Git -e
    ```

    Selepas siap, **tutup PowerShell dan buka semula** (penting, supaya Windows mengenali Git yang baru dipasang). Kemudian pasang GitHub CLI:

    ```powershell
    winget install --id GitHub.cli -e
    ```

    Tutup dan buka PowerShell sekali lagi.

=== "Mac"

    **Buka terminal:** tekan `Cmd + Space`, taip `Terminal`, kemudian tekan Enter.

    Pasang Homebrew dahulu (pengurus aplikasi untuk Mac). Copy arahan daripada [brew.sh](https://brew.sh), tampal dalam terminal, dan ikut apa yang diminta. Mac akan meminta password anda.

    Selepas siap, pasang Git dan GitHub CLI:

    ```bash
    brew install git gh
    ```

## Semak sama ada berjaya

```bash
git --version
gh --version
```

Jika nombor versi muncul untuk kedua-duanya, bermakna berjaya.

## Beritahu Git siapa anda

Gantikan nama dan email dengan yang anda gunakan di GitHub:

```bash
git config --global user.name "Nama Anda"
git config --global user.email "emailanda@contoh.com"
```

## Log masuk ke GitHub

```bash
gh auth login
```

Beberapa soalan akan muncul. Jawab seperti berikut:

1. **Where do you use GitHub?** → `GitHub.com`
2. **Preferred protocol** → `HTTPS`
3. **Authenticate Git with your GitHub credentials?** → `Yes`
4. **How would you like to authenticate?** → `Login with a web browser`

Terminal akan memaparkan **kod 8 aksara**. Salin kod itu, tekan Enter, dan browser akan terbuka. Tampal kod tersebut, kemudian klik **Authorize**.

!!! success "Anda berjaya jika"
    Terminal memaparkan `Logged in as <username anda>`.

[Langkah seterusnya: Pasang Claude Code →](03-claude-code.md){ .md-button }
