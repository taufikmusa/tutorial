<span class="chip">Rujukan</span>

# Masalah biasa

??? question "Saya tidak nampak tab Code dalam aplikasi Claude"
    Pastikan aplikasi Claude sudah dikemas kini kepada versi terbaharu, dan akaun anda mempunyai langganan **Pro atau Max**. Akaun percuma tidak boleh menggunakan Claude Code.

??? question "Repo `video-saya` tidak muncul bila saya mahu pilih"
    Claude GitHub App belum diberi akses kepada repo tersebut. Buka `github.com/settings/installations`, pilih **Claude**, tekan **Configure**, dan tambah `video-saya` dalam senarai repositori.

??? question "Muat naik video gagal atau tersekat"
    Kemungkinan fail melebihi **25MB**. Kecilkan video atau potong kepada bahagian lebih pendek, kemudian cuba lagi. Pastikan juga sambungan internet anda stabil.

??? question "Claude kata dia tidak jumpa video saya"
    Semak nama fail dalam repo. Perhatikan huruf besar dan kecil, serta ruang kosong dalam nama. Cuma beritahu Claude nama fail yang tepat, atau minta: *"Senaraikan semua fail dalam repo ini."*

??? question "Hasil video tidak seperti yang saya mahu"
    Beritahu Claude apa yang tidak kena menggunakan ayat biasa, dan Claude akan cuba lagi. Video asal anda tidak diubah, jadi anda boleh mencuba berkali-kali tanpa risau.

??? question "Saya tidak jumpa video siap di GitHub"
    Claude menyimpan hasil dalam cabang berasingan, bukan `main`. Tukar cabang melalui menu di bahagian atas repo (lihat Langkah 7), atau minta Claude buat pull request dan merge ke `main`.
