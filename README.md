#   Generator Teks SVG ke 3D

Proyek ini adalah alat berbasis web yang memungkinkan pengguna untuk menghasilkan teks 3D dari font SVG atau berkas SVG yang diunggah pengguna. Ia menggunakan Three.js untuk rendering 3D dan menyediakan kontrol untuk menyesuaikan tampilan dan scene.

##   Fitur

* **Pemilihan/Unggah Font SVG:** Pilih dari pilihan font SVG yang disediakan atau unggah berkas SVG Anda sendiri untuk menentukan bentuk teks.
* **Input Teks:** Masukkan teks yang ingin Anda render dalam 3D.
* **Pemilihan Material:** Terapkan berbagai preset material (misalnya, emas, perak) ke teks 3D.
* **Penyimpanan/Pemuatan Scene:** Simpan dan muat seluruh konfigurasi scene (teks, font, posisi objek, material) sebagai berkas JSON.
* **Interaksi Objek:** Pilih, seret, dan pindahkan objek teks 3D individual di dalam scene.
* **Fungsi Undo:** Dukungan undo dasar untuk pergerakan objek.
* **Desain Responsif:** Aplikasi beradaptasi dengan berbagai ukuran layar.

##   Teknologi yang Digunakan

* **Three.js:** Pustaka JavaScript untuk membuat dan menampilkan grafik 3D di peramban web.
* **HTML/CSS:** Untuk menyusun dan menata halaman web.
* **JavaScript:** Untuk logika dan interaktivitas aplikasi.

##   Penyiapan

1.  **Kloning Repositori:**

    ```bash
    git clone [repository_url]
    cd [repository_name]
    ```

2.  **Siapkan Berkas Font:**

    * Pastikan Anda memiliki direktori bernama `fonts/` di akar proyek.
    * Letakkan berkas font SVG Anda di direktori `fonts/`.
    * Buat berkas `list.json` di direktori `fonts/`. Berkas ini harus berisi array JSON dari nama berkas font SVG (misalnya, `["arial.svg", "myfont.svg"]`). Jika berkas ini hilang atau tidak valid, aplikasi mungkin tidak memuat font dengan benar.
    * Sertakan `bg.hdr` (peta lingkungan HDRI) di direktori `fonts/`.

3.  **Jalankan Server Lokal:**

    * Karena batasan keamanan peramban (CORS), memuat berkas lokal (terutama font dan peta lingkungan HDRI) mungkin memerlukan menjalankan aplikasi dari server web lokal.
    * Anda dapat menggunakan server HTTP bawaan Python. Buka terminal, arahkan ke direktori proyek Anda, dan jalankan:

        ```bash
        python -m http.server
        ```

    * Kemudian, buka peramban web Anda dan kunjungi `http://localhost:8000` (atau alamat dan port yang ditampilkan di terminal).

4.  **Buka `index.html`:**

    * Setelah server lokal berjalan, buka `index.html` di peramban web Anda.

##   Penggunaan

1.  **Pilih font:** Pilih font SVG dari menu dropdown atau unggah berkas SVG Anda sendiri.
2.  **Masukkan teks:** Ketik teks yang diinginkan ke dalam bidang input di bagian bawah.
3.  **Klik "RENDER":** Hasilkan teks 3D.
4.  **Sesuaikan material:** Pilih preset material dari dropdown.
5.  **Berinteraksi dengan scene:**

    * Klik pada objek teks untuk memilihnya. Kotak kuning akan muncul di sekitarnya.
    * Seret objek yang dipilih untuk memindahkannya.
    * Klik pada ruang kosong untuk membatalkan pilihan.
    * Gunakan kontrol orbit untuk memutar dan memperbesar tampilan.

6.  **Simpan/Muat scene:** Gunakan tombol "Save Scene" dan "Load Scene" untuk menyimpan dan memulihkan pekerjaan Anda.
7.  **Alihkan Kontrol:** Gunakan tombol "Toggle Controls" untuk menampilkan/menyembunyikan panel kontrol.

##   Catatan Penting

* **Berkas Font:** Aplikasi mengharapkan berkas font SVG dalam format tertentu yang dapat diurai oleh `SVGLoader` Three.js. Pastikan berkas SVG Anda kompatibel.
* **`list.json`:** Mempertahankan `list.json` yang akurat di direktori `fonts/` sangat penting agar dropdown pemilihan font berfungsi dengan benar.
* **Server Lokal:** Karena batasan keamanan peramban (CORS), memuat berkas lokal (terutama font dan peta lingkungan HDRI) mungkin memerlukan menjalankan aplikasi dari server web lokal.  `python -m http.server` adalah salah satu cara untuk melakukannya.
* **HDRI:** Berkas `bg.hdr` digunakan untuk pencahayaan lingkungan. Jika hilang, pantulan mungkin tampak dasar.

##   Kredit

* yosepsoe 2025 ()
* Kontributor Three.js

##   Lisensi

[Tentukan lisensi Anda di sini]
