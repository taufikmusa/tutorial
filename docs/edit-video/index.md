---
hide:
  - navigation
  - footer
---

<span class="chip">Claude Code · Telefon sahaja</span>

# Tiru Gaya Video Kegemaran Anda dengan Claude Code

Anda ada video yang anda suka gayanya? Lampirkan video itu, lampirkan rakaman anda sendiri, tambah B-roll, taip **satu arahan**, dan Claude akan edit video anda supaya bergaya sama. Semuanya dari **telefon**, tanpa komputer.

Tutorial ini untuk anda yang **belum ada Claude** dan **belum ada akaun GitHub**. Kita mulakan dari kosong.

## Apa yang anda akan dapat

Anda lampirkan tiga jenis video dalam sembang Claude, kemudian hantar satu arahan seperti ini:

> "Tiru gaya video rujukan ini dan terapkan pada video rakaman saya. Selitkan B-roll yang saya lampirkan."

Beberapa minit kemudian, video siap anda tersedia untuk di-download.

## Bagaimana ia berfungsi

Claude Code di telefon berjalan di **awan (cloud)**, bukan di dalam telefon anda. Telefon hanya menjadi remote. Kerja berat dilakukan oleh komputer Claude di atas talian, dan alat edit video (ffmpeg) sudah tersedia di sana.

1. **Anda** lampirkan video rujukan, video rakaman dan B-roll dalam sembang
2. **Anda** hantar satu arahan lengkap
3. **Claude** menganalisis gaya video rujukan, kemudian mengedit video anda
4. **Anda** download hasilnya

## Apa yang perlu disediakan

- Telefon (iPhone atau Android) dengan internet
- Alamat email
- Langganan **Claude berbayar** (Pro atau Max). Claude Code tidak boleh digunakan dengan akaun percuma.
- Tiga jenis video (kita bincang di bawah)

## Persediaan sekali sahaja

Bahagian ini hanya perlu dibuat **sekali**. Selepas ini, setiap kali mahu edit video, anda terus ke bahagian [Hantar kepada Claude](#hantar-kepada-claude).

### 1. Buat akaun GitHub

GitHub ibarat Google Drive untuk projek. Di sinilah Claude menyimpan video siap anda.

1. Buka browser telefon (Safari atau Chrome), pergi ke [github.com/signup](https://github.com/signup)
2. Masukkan **email**, **password**, dan pilih **username**
    - Username akan jadi sebahagian daripada pautan anda, jadi pilih yang kemas. Contoh: `ahmad-edits`
3. Selesaikan pengesahan (puzzle kecil) dan masukkan kod yang dihantar ke email anda
4. Jika ada soalan survey, pilih **Skip**
5. Pilih pelan **Free**. Memadai untuk tutorial ini.

!!! tip "Guna browser, bukan aplikasi GitHub"
    Untuk tutorial ini, kita guna **laman web github.com** dalam browser. Aplikasi GitHub di telefon tidak sesuai untuk membuat repo.

!!! success "Anda berjaya jika"
    Anda nampak halaman utama GitHub dengan ikon profil anda di penjuru atas.

### 2. Langgan Claude & install aplikasi

1. Install aplikasi **Claude** daripada App Store (iPhone) atau Google Play (Android)
2. Buka aplikasi dan daftar akaun. Anda boleh guna email atau akaun Google/Apple.
3. Langgan pelan **Pro** (atau Max). Anda boleh buat melalui aplikasi, atau melalui [claude.ai](https://claude.ai) di browser.

!!! success "Anda berjaya jika"
    Dalam aplikasi Claude, anda nampak menu atau tab **Code**. Jika tab itu tidak muncul, kemas kini aplikasi kepada versi terbaharu, dan pastikan langganan anda sudah aktif.

!!! info "Nama menu boleh berubah"
    Aplikasi dikemas kini dari semasa ke semasa, jadi nama atau kedudukan butang mungkin sedikit berbeza. Jika buntu, cari perkataan **Code**.

### 3. Buat repo

**Repo** ialah folder projek di GitHub. Kita buat satu repo khas untuk kerja edit video anda.

1. Dalam browser telefon, pergi ke [github.com/new](https://github.com/new)
2. **Repository name**: taip `video-saya`
3. Pilih **Private**, supaya hanya anda yang boleh melihat video anda
4. Tandakan **Add a README file**
5. Tekan **Create repository**

!!! warning "Jangan skip README"
    Repo kosong akan menyukarkan Claude. Dengan README, repo anda sudah ada fail pertama dan Claude boleh terus bekerja.

!!! success "Anda berjaya jika"
    Anda nampak halaman repo `video-saya` dengan fail `README.md`.

### 4. Sambung Claude ke GitHub

1. Buka aplikasi **Claude**, pergi ke tab **Code**
2. Tekan untuk **menyambung ke GitHub** (Connect GitHub)
3. Browser akan terbuka. Login ke GitHub jika diminta, dan tekan **Authorize**
4. Install **Claude GitHub App** apabila diminta. Pada bahagian repositori, pilih **Only select repositories**, kemudian pilih `video-saya`. Tekan **Install**.
5. Kembali ke aplikasi Claude dan pilih repo **video-saya** untuk memulakan sesi baharu

!!! tip "Kenapa pilih repo tertentu sahaja?"
    Lebih selamat. Claude hanya boleh melihat repo `video-saya`, bukan semua repo anda.

!!! success "Anda berjaya jika"
    Anda nampak ruangan sembang untuk sesi baharu, dengan nama repo `video-saya` kelihatan.

## Sediakan tiga jenis video

Sebelum menghantar arahan, siapkan tiga jenis video ini dalam galeri telefon anda.

| Video | Fungsi | Tip |
|---|---|---|
| **1. Video rujukan** | Gaya yang anda mahu tiru | Pilih yang **pendek** (15 hingga 60 saat) dan gayanya jelas. Satu video sahaja. |
| **2. Video rakaman anda** | Kandungan sebenar, iaitu cakap atau aksi anda | Rakam seperti biasa. Pastikan bunyi jelas. |
| **3. B-roll** | Klip tambahan untuk diselitkan (produk, suasana, pemandangan) | Pilihan. Satu atau beberapa klip pendek. |

!!! warning "Saiz fail"
    Video yang terlalu besar mungkin gagal di-upload. Untuk permulaan, gunakan klip pendek dan resolusi **1080p** (bukan 4K). Di iPhone: Settings → Camera → Record Video. Di Android: tetapan resolusi dalam aplikasi kamera.

## Hantar kepada Claude

Inilah langkah utama. Dalam tab **Code**, dalam sesi repo `video-saya`:

1. Tekan butang **lampir** (ikon klip kertas atau `+`) di sebelah kotak mesej
2. Pilih ketiga-tiga video: rujukan, rakaman anda, dan B-roll
3. Salin arahan di bawah dan tampal dalam kotak mesej
4. Tekan **hantar**

### Arahan lengkap (salin semua)

```text
Saya lampirkan tiga jenis video:
1. VIDEO RUJUKAN: gaya yang saya mahu tiru.
2. VIDEO RAKAMAN SAYA: kandungan sebenar yang perlu diedit.
3. B-ROLL: klip tambahan untuk diselitkan.

Tugas: edit video rakaman saya supaya gayanya sama seperti video rujukan.

Ikut langkah ini:
1. Analisis video rujukan dahulu menggunakan ffmpeg. Ambil beberapa frame dan ukur masa potongan. Catat dengan ringkas: nisbah skrin, purata tempoh setiap shot, kekerapan potongan, kesan zoom atau transisi, nada warna (terang, gelap, hangat, sejuk), gaya teks atau subtitle (saiz, warna, kedudukan), dan kelantangan muzik berbanding suara.
2. Edit video rakaman saya mengikut analisis itu: buang bahagian senyap dan percakapan yang berulang, laraskan kelajuan potongan, nisbah skrin, dan nada warna supaya sama dengan rujukan.
3. Selitkan B-roll pada bahagian yang sesuai supaya video tidak membosankan. Jangan letak B-roll melebihi 3 saat pada satu-satu masa.
4. Tambah subtitle mengikut gaya rujukan. Jika kamu tidak dapat menyalin suara kepada teks, tanya saya teks yang dituturkan.
5. Simpan hasil akhir dalam folder "siap" dengan nama "hasil.mp4" (format mp4), dalam nisbah skrin yang sama dengan rujukan. Jangan ubah atau padam video asal saya.

Beritahu saya ringkasan rancangan kamu dahulu, kemudian terus laksanakan tanpa menunggu jawapan saya. Jika ada elemen dalam rujukan yang tidak dapat ditiru dengan tepat, beritahu saya apa yang kamu lakukan sebagai ganti.
```

### Apa yang berlaku selepas itu

1. Claude menerangkan apa yang dia nampak dalam video rujukan
2. Claude menjalankan ffmpeg di cloud untuk mengedit video anda
3. Jika Claude meminta kebenaran, baca dahulu dan pilih **Allow** atau **Yes** jika anda bersetuju
4. Claude menyimpan hasil dalam folder `siap`, dan menghantarnya ke GitHub

!!! info "Claude tidak menonton video seperti manusia"
    Claude menganalisis video melalui gambar (frame) yang diambil, serta ukuran masa potongan. Jadi peniruan gaya bersifat **anggaran**: rentak potongan, nisbah skrin, warna, dan gaya teks biasanya boleh ditiru dengan baik. Animasi grafik yang rumit mungkin tidak sama persis.

??? tip "Kalau butang lampir tidak menerima video"
    Jika aplikasi tidak membenarkan lampiran video, atau video terlalu besar, gunakan laluan GitHub:

    1. Buka `github.com/<username anda>/video-saya` dalam browser
    2. Tekan **Add file**, kemudian **Upload files**
    3. Pilih ketiga-tiga video, tunggu upload selesai, dan tekan **Commit changes**
    4. Dalam sesi Claude, hantar arahan yang sama, dan tambah satu baris di permulaan: *"Video saya sudah ada dalam repo ini. Sila senaraikan fail untuk mengenal pasti yang mana rujukan, rakaman, dan B-roll."*

    Melalui browser, GitHub hanya menerima fail sehingga **25MB** setiap satu.

### Tambah baris ini jika perlu

Anda boleh tambah baris-baris ini di hujung arahan:

- **Jika mahu B-roll di tempat tertentu:** *"Letakkan B-roll produk semasa saya menyebut tentang harga, kira-kira pada 0:12 hingga 0:15."*
- **Untuk platform tertentu:** *"Ini untuk TikTok, maksimum 30 saat."*
- **Jika mahu muzik:** *"Kekalkan muzik latar daripada video rujukan pada kelantangan yang rendah."*

## Semak hasil & minta ubah

Selepas Claude siap, anda boleh minta pembetulan dengan ayat biasa dalam sembang yang sama:

- *"Terlalu laju, perlahankan sedikit."*
- *"Potong 2 saat lebih awal."*
- *"Subtitle terlalu kecil, besarkan."*
- *"Buang B-roll yang kedua."*

Video asal anda tidak pernah diubah, jadi anda boleh mencuba berkali-kali tanpa risau.

## Ambil video yang siap

Claude menyimpan hasil kerja di GitHub, bukan terus dalam galeri telefon. Jadi kita download dari sana.

Claude biasanya menyimpan hasil dalam **cabang (branch)** berasingan, dengan nama bermula `claude/`.

1. Buka repo anda di browser: `github.com/<username anda>/video-saya`
2. Tekan menu cabang (biasanya tertulis **main**) dan pilih cabang yang bermula `claude/`
3. Buka folder `siap`
4. Tekan `hasil.mp4`. Anda boleh menontonnya terus di situ.
5. Tekan ikon **Download** (anak panah ke bawah) untuk simpan ke telefon

??? tip "Mahu video siap berada di cabang utama (main)?"
    Minta Claude: *"Buat pull request untuk perubahan ini ke main."* Kemudian buka pull request itu di GitHub dan tekan **Merge pull request**.

!!! success "Tahniah!"
    Anda kini boleh meniru gaya video yang anda suka, hanya dengan telefon. Mulai sekarang, buka tab **Code**, lampirkan video, tampal arahan yang sama, dan Claude buat kerja.

## Masalah biasa

??? question "Saya tidak nampak tab Code dalam aplikasi Claude"
    Pastikan aplikasi Claude sudah dikemas kini kepada versi terbaharu, dan akaun anda mempunyai langganan **Pro atau Max**. Akaun percuma tidak boleh menggunakan Claude Code.

??? question "Repo `video-saya` tidak muncul bila saya mahu pilih"
    Claude GitHub App belum diberi akses kepada repo tersebut. Buka `github.com/settings/installations`, pilih **Claude**, tekan **Configure**, dan tambah `video-saya` dalam senarai repositori.

??? question "Lampiran video gagal atau tersekat"
    Kemungkinan fail terlalu besar. Kecilkan video atau potong kepada bahagian lebih pendek, kemudian cuba lagi. Pastikan juga sambungan internet anda stabil. Atau gunakan laluan GitHub di atas.

??? question "Hasil video tidak seperti rujukan"
    Beritahu Claude secara spesifik apa yang berbeza, contohnya *"Rujukan memotong setiap 1.5 saat, tetapi hasil awak 4 saat."* Semakin spesifik, semakin tepat pembetulan.

??? question "Saya tidak jumpa video siap di GitHub"
    Claude menyimpan hasil dalam cabang berasingan, bukan `main`. Tukar cabang melalui menu di bahagian atas repo, atau minta Claude buat pull request dan merge ke `main`.
