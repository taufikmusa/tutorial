# Step 7: Simpan kerja ke GitHub

Bahagian ni yang buat kau tak hilang kerja walaupun komputer rosak.

## Suruh Claude buat

Paling senang, suruh Claude yang uruskan:

```text
Simpan semua perubahan dalam projek ni ke GitHub. Tulis commit message yang ringkas dalam bahasa Melayu.
```

Dia akan minta kebenaran untuk setiap arahan Git. Baca dan pilih Yes.

## Atau buat sendiri

Keluar dari Claude (`/exit`), kemudian:

```bash
git add .
git commit -m "Edit video pertama"
git push
```

## Semak kat GitHub

Buka `github.com/<username kau>/video-saya`. Kau akan nampak fail `.gitignore` dan apa-apa nota yang ada. Folder video tak muncul sebab kita dah suruh Git abaikan.

!!! success "Tahniah!"
    Kau dah ada Claude Code, GitHub, dan boleh edit video guna arahan biasa. Mulai sekarang, buka terminal, `cd` ke folder `video-saya`, taip `claude`, dan suruh dia buat kerja.

## Seterusnya

- Tulis arahan tetap (contoh: format TikTok kegemaran kau) dalam fail bernama `CLAUDE.md` dalam folder projek. Claude akan baca fail ni setiap kali kau buka dia, jadi kau tak payah ulang arahan.
- Cuba suruh Claude tambah subtitle, tukar background music, atau buat thumbnail.

[Masalah biasa :material-arrow-right:](08-masalah.md){ .md-button }
