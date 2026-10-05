<span class="chip">Rujukan</span>

# Masalah biasa

??? question "`claude` / `git` / `ffmpeg` is not recognized"
    Terminal anda belum mengenali program yang baru dipasang. **Tutup terminal dan buka semula.** Jika masih sama, restart komputer.

??? question "`winget` is not recognized (Windows)"
    Winget terdapat pada Windows 10/11 yang telah dikemas kini. Buka **Microsoft Store**, cari **App Installer**, dan klik Update. Atau, muat turun Git terus daripada [git-scm.com](https://git-scm.com/download/win).

??? question "Claude Code minta log masuk berulang kali"
    Pastikan akaun Claude anda mempunyai langganan **Pro atau Max**. Akaun percuma tidak boleh menggunakan Claude Code. Cuba `/logout` dalam Claude, kemudian taip `claude` untuk log masuk semula.

??? question "`git push` gagal: file too large"
    Ada fail video yang termasuk dalam commit. Pastikan `.gitignore` mengandungi `mentah/` dan `siap/`. Jika sudah terlanjur commit, minta Claude: *"Saya terlanjur commit video, tolong keluarkan daripada Git tanpa memadam fail asal."*

??? question "Hasil video tidak seperti yang saya mahu"
    Beritahu Claude apa yang tidak kena menggunakan ayat biasa, dan Claude akan cuba lagi. Fail asal dalam `mentah` tidak pernah disentuh, jadi anda boleh mencuba berkali-kali tanpa risau.

??? question "Mac minta password semasa pasang Homebrew"
    Itu password log masuk Mac anda. Semasa menaip, aksara tidak akan kelihatan di skrin. Itu normal. Taip sahaja dan tekan Enter.
