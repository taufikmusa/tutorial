# Step 5: Buat repo & folder kerja

**Repo** = folder projek yang disimpan kat GitHub. Kita buat satu repo khas untuk kerja edit video kau.

## Buat repo

Dalam terminal, pergi ke tempat kau nak letak projek. Contoh, folder Documents:

=== "Windows"

    ```powershell
    cd ~\Documents
    ```

=== "Mac"

    ```bash
    cd ~/Documents
    ```

Lepas tu buat repo (private, jadi cuma kau boleh nampak) dan terus download ke komputer:

```bash
gh repo create video-saya --private --clone
```

Masuk ke dalam folder tu:

```bash
cd video-saya
```

## Buat folder untuk video

```bash
mkdir mentah siap
```

- `mentah` = letak video asal kau kat sini
- `siap` = Claude simpan video yang dah siap edit kat sini

Sekarang **copy satu video pendek** (30 saat sampai 2 minit cukup) ke dalam folder `mentah`. Kau boleh drag and drop guna File Explorer / Finder. Folder `video-saya` ada dalam Documents.

## Halang video dari masuk GitHub

Fail video besar, dan GitHub tak benarkan fail lebih 100MB. Kita suruh Git **abaikan** folder video:

=== "Windows"

    ```powershell
    "mentah/", "siap/" | Set-Content -Encoding ascii .gitignore
    ```

=== "Mac"

    ```bash
    printf "mentah/\nsiap/\n" > .gitignore
    ```

!!! info "Jadi apa yang masuk GitHub?"
    Nota projek dan arahan kau. Video kekal dalam komputer kau je. Itu memang yang kita nak.

[Step seterusnya: Edit video pertama :material-arrow-right:](06-edit.md){ .md-button }
