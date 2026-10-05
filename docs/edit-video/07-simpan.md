<span class="chip">Langkah 7 / 7</span>

# Simpan kerja ke GitHub

Langkah ini memastikan kerja anda selamat, walaupun komputer rosak.

## Minta Claude uruskan

Cara paling mudah, minta Claude yang buatkan:

```text
Simpan semua perubahan dalam projek ini ke GitHub. Tulis commit message yang ringkas dalam Bahasa Melayu.
```

Claude akan meminta kebenaran untuk setiap arahan Git. Baca dan pilih Yes.

## Atau buat sendiri

Keluar daripada Claude (`/exit`), kemudian:

```bash
git add .
git commit -m "Edit video pertama"
git push
```

## Semak di GitHub

Buka `github.com/<username anda>/video-saya`. Anda akan nampak fail `.gitignore` dan sebarang nota yang ada. Folder video tidak muncul kerana kita sudah arahkan Git mengabaikannya.

!!! success "Tahniah!"
    Anda kini ada Claude Code, GitHub, dan boleh mengedit video menggunakan arahan biasa. Mulai sekarang, buka terminal, `cd` ke folder `video-saya`, taip `claude`, dan minta Claude buat kerja.

## Selepas ini

- Tulis arahan tetap anda (contohnya format TikTok kegemaran) dalam fail bernama `CLAUDE.md` di dalam folder projek. Claude akan membaca fail ini setiap kali anda membukanya, jadi anda tak perlu mengulang arahan.
- Cuba minta Claude menambah subtitle, menukar muzik latar, atau menghasilkan thumbnail.

[Masalah biasa →](08-masalah.md){ .md-button }
