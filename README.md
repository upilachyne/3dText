#   Gawe Tèks 3D Saka SVG

Proyèk iki alat neng web sing isa nggawèné kowé nggawe tèks 3D saka font SVG utawa file SVG sing diunggah déwé. Iki nganggo Three.js nggo ngrènder 3D lan nyediakné kontrol nggo ngatur tampilan lan scènè.

##   Fitur-Fitur

* **Milih/Unggah Font SVG:** Isa milih saka font SVG sing wis disediakné utawa ngunggah file SVG duwèkmèdèwé nggo nemtokaké wujud tèksè.
* **Input Tèks:** Nglebokké tèks sing pengin dirènder dadi 3D.
* **Milih Matèrial:** Nganggo macem-macem prèset matèrial (umpamané, emas, pérak) neng tèks 3D.
* **Nyimpen/Ngunggah Scènè:** Nyimpen lan ngunggah kabèh konfigurasi scènè (tèks, font, posisi objèk, matèrial) dadi file JSON.
* **Interaksi Objèk:** Milih, nyèrèt, lan mindahné objèk tèks 3D siji-siji neng njero scènè.
* **Fungsi Undo:** Dhukungan undo dasar nggo mindahné objèk.
* **Dhèsain Rèsponsif:** Aplikasi iki isa ganti ukuran nggo nyocogaké ukuran layar sing béda-béda.

##   Tèknologi Sing Dienggo

* **Three.js:** Pustaka JavaScript nggo nggawe lan nampilné grafik 3D neng browser web.
* **HTML/CSS:** Nggo nyusun lan ngèstail kaca web.
* **JavaScript:** Nggo logika lan interaktivitas aplikasi.

##   Cara Nyiyapné

1.  **Nglonè Repositori:**

    ```bash
    git clone [repository_url]
    cd [repository_name]
    ```

2.  **Nyiyapné File Font:**

    * Pastèkné kowé nduwé direktori jenengé `fonts/` neng akar proyèk.
    * Ngonokké file font SVG duwèkmèdèwé neng direktori `fonts/`.
    * Nggawe file `list.json` neng direktori `fonts/`. File iki kudu isiné array JSON saka jeneng file font SVG (umpamané, `["arial.svg", "myfont.svg"]`). Nek file iki ilang utawa ora valid, aplikasi iki mungkin ora isa ngunggah font kanthi bener.
    * Lebokké `bg.hdr` (peta lingkungan HDRI) neng direktori `fonts/`.

3.  **Njalanké Sèrver Lokal:**

    * Merga watesan keamanan browser (CORS), ngunggah file lokal (utamane font lan peta lingkungan HDRI) mungkin butuh njalanké aplikasi saka sèrver web lokal.
    * Kowé isa nganggo sèrver HTTP bawaanè Python. Bukak tèrminal, lunga neng direktori proyèkmu, terus jalanaké:

        ```bash
        python -m http.server
        ```

    * Terus, bukak browser webmu lan kunjungi `http://localhost:8000` (utawa alamat lan port sing ditampilné neng tèrminal).

4.  **Mbukak `index.html`:**

    * Sakwisé sèrver lokal mlaku, bukak `index.html` neng browser webmu.

##   Cara Nganggoné

1.  **Milih font:** Milih font SVG saka menu dropdown utawa ngunggah file SVG duwèkmèdèwé.
2.  **Nglebokké tèks:** Ngetik tèks sing dikarepké neng kolom input neng ngisor.
3.  **Ngeklik "RENDER":** Nggawe tèks 3D.
4.  **Ngatur matèrial:** Milih prèset matèrial saka dropdown.
5.  **Interaksi karo scènè:**

    * Ngeklik objèk tèks nggo milih. Kothak kuning bakal muncul neng sakiteré.
    * Nyèrèt objèk sing dipilih nggo mindahné.
    * Ngeklik ruang kosong nggo mbatalné pilihan.
    * Nganggo kontrol orbit nggo muter lan nggedhèkné tampilan.

6.  **Nyimpen/Ngunggah scènè:** Nganggo tombol "Save Scene" lan "Load Scene" nggo nyimpen lan mulihné gawéanmu.
7.  **Ngganti Kontrol:** Nganggo tombol "Toggle Controls" nggo nuduhné/ngumpètné panel kontrol.

##   Cathetan Penting

* **File Font:** Aplikasi iki ngarepné file font SVG ing format tartamtu sing isa diurai karo `SVGLoader` Three.js. Pastèkné file SVG duwèkmèdèwé kompatibel.
* **`list.json`:** Njaga `list.json` sing akurat neng direktori `fonts/` kuwi penting banget nggo dropdown pilihan font isa mlaku kanthi bener.
* **Sèrver Lokal:** Merga watesan keamanan browser (CORS), ngunggah file lokal (utamane font lan peta lingkungan HDRI) mungkin butuh njalanké aplikasi saka sèrver web lokal. `python -m http.server` kuwi salah sijiné cara nggo nglakoni kuwi.
* **HDRI:** File `bg.hdr` dienggo nggo cahya lingkungan. Nek ilang, pantulan mungkin katoné sèdèrhana.

##   Krèdit

* yosepsoe 2025 (may)
* Kontributor Three.js

##   Lisènsi

[Sebutné lisènsimu neng kéné]
