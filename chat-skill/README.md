# Skill untuk Claude Chat

Skill `tutorial-taufik-fyi-chat` membantu Claude (sembang biasa) menyediakan draf tutorial baharu dalam format tutorial.taufik.fyi.

## Cara install

1. Download fail `tutorial-taufik-fyi-chat.zip` daripada folder ini (buka fail di GitHub, kemudian tekan **Download**)
2. Buka [claude.ai](https://claude.ai) di browser
3. Pergi ke **Settings**, kemudian **Capabilities**, dan cari bahagian **Skills**
4. Tekan untuk **upload skill** dan pilih fail zip tadi
5. Hidupkan skill itu

Nama menu boleh berubah. Cari tetapan **Skills** dalam Settings.

## Cara guna

Dalam sembang baharu, taip contohnya:

> Tambah tutorial baharu: cara guna Canva untuk buat thumbnail, telefon sahaja.

Claude akan menghasilkan halaman, baris menu, kad homepage, dan satu arahan untuk dihantar kepada Claude Code (tab Code, repo `tutorial`).

## Penyelenggaraan

Skill ini ialah versi sembang bagi skill projek di `.claude/skills/tutorial-taufik-fyi/`. Jika format tutorial berubah, kemas kini **kedua-duanya**, kemudian bina semula zip:

```bash
cd chat-skill && zip -r tutorial-taufik-fyi-chat.zip tutorial-taufik-fyi-chat
```
