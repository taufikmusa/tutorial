<span class="chip">Langkah 5 / 7</span>

# Buat repo & folder kerja

**Repo** ialah folder projek yang disimpan di GitHub. Kita akan buat satu repo khas untuk kerja edit video anda.

## Buat repo

Dalam terminal, pergi ke lokasi yang anda mahu simpan projek. Sebagai contoh, folder Documents:

=== "Windows"

    ```powershell
    cd ~\Documents
    ```

=== "Mac"

    ```bash
    cd ~/Documents
    ```

Kemudian buat repo (private, jadi hanya anda yang boleh melihatnya) dan terus muat turun ke komputer:

```bash
gh repo create video-saya --private --clone
```

Masuk ke dalam folder tersebut:

```bash
cd video-saya
```

## Sediakan folder untuk video

```bash
mkdir mentah siap
```

- `mentah` = tempat anda letak video asal
- `siap` = tempat Claude simpan video yang sudah diedit

Sekarang **salin satu video pendek** (30 saat hingga 2 minit memadai) ke dalam folder `mentah`. Anda boleh drag and drop menggunakan File Explorer atau Finder. Folder `video-saya` terletak di dalam Documents.

## Halang video daripada masuk GitHub

Fail video bersaiz besar, dan GitHub tidak membenarkan fail melebihi 100MB. Jadi kita arahkan Git **mengabaikan** folder video:

=== "Windows"

    ```powershell
    "mentah/", "siap/" | Set-Content -Encoding ascii .gitignore
    ```

=== "Mac"

    ```bash
    printf "mentah/\nsiap/\n" > .gitignore
    ```

!!! info "Jadi apa yang masuk ke GitHub?"
    Hanya nota projek dan arahan anda. Video kekal di dalam komputer anda. Itulah yang kita mahu.

[Langkah seterusnya: Edit video pertama →](06-edit.md){ .md-button }
