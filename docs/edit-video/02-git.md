# Step 2: Pasang Git & GitHub CLI

Dua benda ni yang sambungkan komputer kau dengan GitHub.

- **Git** = sistem simpan versi kerja kau
- **GitHub CLI (`gh`)** = alat untuk login ke GitHub dari terminal, tanpa pening password

=== "Windows"

    **Buka terminal dulu:** tekan butang Windows, taip `PowerShell`, tekan Enter.

    Copy-paste arahan ni, tekan Enter:

    ```powershell
    winget install --id Git.Git -e
    ```

    Lepas siap, **tutup PowerShell dan buka balik** (penting, supaya Windows kenal Git baru tu). Pastu pasang GitHub CLI:

    ```powershell
    winget install --id GitHub.cli -e
    ```

    Tutup dan buka PowerShell sekali lagi.

=== "Mac"

    **Buka terminal:** tekan `Cmd + Space`, taip `Terminal`, tekan Enter.

    Pasang Homebrew dulu (pengurus aplikasi untuk Mac). Copy-paste arahan dari [brew.sh](https://brew.sh), tekan Enter, dan ikut apa dia suruh (dia akan minta password Mac kau).

    Lepas siap, pasang Git dan GitHub CLI:

    ```bash
    brew install git gh
    ```

## Semak dah jadi ke belum

```bash
git --version
gh --version
```

Kalau keluar nombor versi untuk kedua-duanya, jadi.

## Beritahu Git siapa kau

Tukar nama dan email dengan yang kau guna kat GitHub:

```bash
git config --global user.name "Nama Kau"
git config --global user.email "emailkau@contoh.com"
```

## Login ke GitHub

```bash
gh auth login
```

Dia akan tanya beberapa soalan. Jawab macam ni:

1. **Where do you use GitHub?** → `GitHub.com`
2. **Preferred protocol** → `HTTPS`
3. **Authenticate Git with your GitHub credentials?** → `Yes`
4. **How would you like to authenticate?** → `Login with a web browser`

Dia akan tunjuk **kod 8 huruf**. Copy kod tu, tekan Enter, browser akan terbuka. Tampal kod, klik **Authorize**.

!!! success "Siap bila"
    Terminal tulis `Logged in as <username kau>`.

[Step seterusnya: Pasang Claude Code :material-arrow-right:](03-claude-code.md){ .md-button }
