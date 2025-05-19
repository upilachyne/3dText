# SVG to 3D Text Generator

This project is a web-based tool that allows users to generate 3D text from SVG fonts or user-uploaded SVG files. It utilizes Three.js for 3D rendering and provides controls for customizing the appearance and scene.

## Features

* **SVG Font Selection/Upload:** Choose from a selection of provided SVG fonts or upload your own SVG file to define the text's shape.
* **Text Input:** Enter the text you want to render in 3D.
* **Material Selection:** Apply different material presets (e.g., gold, silver) to the 3D text.
* **Scene Saving/Loading:** Save and load the entire scene configuration (text, font, object positions, material) as a JSON file.
* **Object Interaction:** Select, drag, and move individual 3D text objects within the scene.
* **Undo Functionality:** Basic undo support for object movements.
* **Responsive Design:** The application adapts to different screen sizes.

## Technologies Used

* **Three.js:** A JavaScript library for creating and displaying 3D graphics in a web browser.
* **HTML/CSS:** For structuring and styling the web page.
* **JavaScript:** For application logic and interactivity.

## Setup

1.  **Clone the Repository:**
    ```bash
    git clone [repository_url]
    cd [repository_name]
    ```
2.  **Prepare Font Files:**
    * Ensure you have a directory named `fonts/` in the project root.
    * Place your SVG font files in the `fonts/` directory.
    * Create a `list.json` file in the `fonts/` directory. This file should contain a JSON array of the SVG font filenames (e.g., `["arial.svg", "myfont.svg"]`).  If this file is missing or invalid, the application may not load fonts correctly.
    * Include `bg.hdr` (HDRI environment map) in the `fonts/` directory.
3.  **Open `index.html`:** Open the `index.html` file in a web browser.  You may need to run this from a local web server to avoid CORS issues when loading local files.

## Usage

1.  **Select a font:** Choose an SVG font from the dropdown menu or upload your own SVG file.
2.  **Enter text:** Type the desired text into the input field at the bottom.
3.  **Click "RENDER":** Generate the 3D text.
4.  **Customize the material:** Select a material preset from the dropdown.
5.  **Interact with the scene:**
    * Click on a text object to select it. A yellow box will appear around it.
    * Drag the selected object to move it.
    * Click on empty space to deselect.
    * Use the orbit controls to rotate and zoom the view.
6.  **Save/Load the scene:** Use the "Save Scene" and "Load Scene" buttons to persist and restore your work.
7.  **Toggle Controls:** Use the "Toggle Controls" button to show/hide the controls panel.

## Important Notes
* **RUN** python -m http.server
* **Font Files:** The application expects SVG font files to be in a specific format that Three.js's `SVGLoader` can parse. Ensure your SVG files are compatible.
* **`list.json`:** Maintaining an accurate `list.json` in the `fonts/` directory is crucial for the font selection dropdown to work correctly.
* **Local Server:** Due to browser security restrictions (CORS), loading local files (especially fonts and the HDRI environment map) might require running the application from a local web server (e.g., using Python's `http.server` or Node.js's `http-server`).
* **HDRI:** The `bg.hdr` file is used for environment lighting. If it's missing, reflections might appear basic.

## Credits

* yosepsoe 2025 (as mentioned in the original code)
* Three.js contributors

## License

[bebas]

# Generator Teks SVG ke 3D

Proyek ini adalah alat berbasis web yang memungkinkan pengguna untuk menghasilkan teks 3D dari font SVG atau berkas SVG yang diunggah pengguna. Ia menggunakan Three.js untuk rendering 3D dan menyediakan kontrol untuk menyesuaikan tampilan dan scene.

## Fitur

* **Pemilihan/Unggah Font SVG:** Pilih dari pilihan font SVG yang disediakan atau unggah berkas SVG Anda sendiri untuk menentukan bentuk teks.
* **Input Teks:** Masukkan teks yang ingin Anda render dalam 3D.
* **Pemilihan Material:** Terapkan berbagai preset material (misalnya, emas, perak) ke teks 3D.
* **Penyimpanan/Pemuatan Scene:** Simpan dan muat seluruh konfigurasi scene (teks, font, posisi objek, material) sebagai berkas JSON.
* **Interaksi Objek:** Pilih, seret, dan pindahkan objek teks 3D individual di dalam scene.
* **Fungsi Undo:** Dukungan undo dasar untuk pergerakan objek.
* **Desain Responsif:** Aplikasi beradaptasi dengan berbagai ukuran layar.

## Teknologi yang Digunakan

* **Three.js:** Pustaka JavaScript untuk membuat dan menampilkan grafik 3D di peramban web.
* **HTML/CSS:** Untuk menyusun dan menata halaman web.
* **JavaScript:** Untuk logika dan interaktivitas aplikasi.

## Penyiapan

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
3.  **Buka `index.html`:** Buka berkas `index.html` di peramban web. Anda mungkin perlu menjalankannya dari server web lokal untuk menghindari masalah CORS saat memuat berkas lokal.

## Penggunaan

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

## Catatan Penting

* **Berkas Font:** Aplikasi mengharapkan berkas font SVG dalam format tertentu yang dapat diurai oleh `SVGLoader` Three.js. Pastikan berkas SVG Anda kompatibel.
* **`list.json`:** Mempertahankan `list.json` yang akurat di direktori `fonts/` sangat penting agar dropdown pemilihan font berfungsi dengan benar.
* **Server Lokal:** Karena batasan keamanan peramban (CORS), memuat berkas lokal (terutama font dan peta lingkungan HDRI) mungkin memerlukan menjalankan aplikasi dari server web lokal (misalnya, menggunakan `http.server` Python atau `http-server` Node.js).
* **HDRI:** Berkas `bg.hdr` digunakan untuk pencahayaan lingkungan. Jika hilang, pantulan mungkin tampak dasar.

## Kredit

* yosepsoe 2025 (seperti yang disebutkan dalam kode asli)
* Kontributor Three.js

## Lisensi

[bebas]


