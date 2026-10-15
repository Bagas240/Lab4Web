  # Lab4Web: Praktikum 4 

Nama : Bagas Arya Ramadhan Nim : 312510328 Kelas : I251D

## Struktur Direktori Project

```text
Lab4Web/
├── lab4_box.html
└── lab4_layout/
    ├── home.html
    ├── artikel.html
    ├── about.html
    ├── kontak.html
    └── style.css
```
###  1: Eksperimen Box Element & Float (`lab4_box.html`)

File `lab4_box.html` bertujuan untuk mendemonstrasikan bagaimana elemen `<div>` bertindak sebagai *box* serta bagaimana properti `float` dan `clear` mengatur posisi *box* tersebut[cite: 2, 3, 4, 5].

#### Kode `lab4_box.html`:
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20225100.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20223517.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20223534.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20223605.png?raw=true)

#### Penjelasan :
1. **Aturan `div { float: left; padding: 10px; }`**[cite: 3, 4]:
   * Elemen `<div>` secara *default* berjenis *block-level* (memakan satu baris penuh)[cite: 1].
   * Dengan `float: left;`, sifat *block* dibatalkan sehingga `.div1`, `.div2`, dan `.div3` mengambang ke kiri dan tersusun sejajar secara horizontal[cite: 3].
   * `padding: 10px;` memberikan jarak dalam sebesar `10px` di antara teks dengan tepi dalam masing-masing *box*[cite: 1, 3].
2. **Kelas Warna (`.div1`, `.div2`, `.div3`)**[cite: 3, 4]:
   * Properti `background` memberi warna latar merah (`red`), kuning (`yellow`), dan hijau (`green`) untuk membedakan visual tiap *box*[cite: 3, 4].
3. **Kelas `.div4 { background-color: blue; clear: left; float: none; }`**[cite: 5]:
   * `float: none;` memastikan `.div4` tidak ikut mengambang[cite: 5].
   * `clear: left;` adalah instruksi kunci yang membatalkan pengaruh `float: left` dari elemen di atasnya[cite: 5]. Efeknya, `.div4` dipaksa turun dan berada tepat di baris baru di bawah `.div1`, `.div2`, dan `.div3`[cite: 5].

---

### 2: Web Layout Sederhana (`lab4_layout/`)

Pembuatan struktur *layout* web utama menggunakan elemen semantik HTML5 yang ditata menggunakan file CSS eksternal `style.css`[cite: 3, 6].

#### 1. Struktur Dokumen HTML (`home.html`)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230127.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230136.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230146.png?raw=true)

#### 2. Lembar Gaya CSS (`style.css`)

![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230423.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230432.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230514.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230549.png?raw=true)


---

#### Penjelasan PerKelompok Kode CSS (`style.css`):

1. **Reset CSS (`* { margin: 0; padding: 0; }`)**[cite: 8]:
   * Mengatur ulang (*reset*) nilai `margin` dan `padding` bawaan dari semua *browser* ke angka `0`[cite: 8].
   * Bertujuan menghilangkan inkonsistensi spasi bawaan antar *browser*[cite: 8].

2. **Dasar Dokumen & Container (`body`, `#container`)**[cite: 8]:
   * `body`: Menentukan *font* utama `'Open Sans'`, tinggi baris `line-height: 1;`, dan warna teks `#5a5a5a`[cite: 8].
   * `#container`: Mengunci lebar situs sebesar `width: 980px;`[cite: 8].
   * `margin: 0 auto;`: Menggunakan teknik pengetengan otomatis (margin atas-bawah `0`, kiri-kanan `auto`) sehingga elemen berada di tengah-tengah layar[cite: 8].
   * `box-shadow: 0 0 1em #cccccc;`: Memberikan efek bayangan di luar *container*[cite: 8].

3. **Menu Navigasi (`nav`, `nav a`)**[cite: 9]:
   * `nav`: Bertindak sebagai bilah navigasi berlatar biru `#1f5faa`[cite: 9].
   * `nav a`: Menggunakan `display: inline-block;` agar setiap elemen tautan `<a>` dapat diatur nilainya menggunakan `padding: 15px 30px;`[cite: 9]. Ini memperluas area sentuh (*clickable area*) dari tautan[cite: 9].
   * `nav a.active, nav a:hover`: Mengubah latar tautan menjadi lebih terang (`#2b83ea`) saat kursor melintas (*hover*) atau saat status halaman aktif (`.active`)[cite: 9].

4. **Hero Panel (`#hero`)**[cite: 10]:
   * Berfungsi sebagai area promosi/selamat datang dengan latar abu-abu `#e4e4e5`[cite: 10].
   * `padding: 50px 20px;` memberikan ruang udara yang luas di dalam banner[cite: 10].

5. **Layout Utama & Sidebar (`#main`, `#sidebar`)**[cite: 10]:
   * `#main`: Menggunakan `float: left;` dengan lebar `width: 640px;` dan `padding: 20px;`[cite: 10].
   * `#sidebar`: Menggunakan `float: left;` dengan lebar `width: 260px;` dan `padding: 20px;`[cite: 10].
   * **Kalkulasi Presisi**: 
     - Lebar `#main` total: `640px + 20px (pad-kiri) + 20px (pad-kanan) = 680px`[cite: 10].
     - Lebar `#sidebar` total: `260px + 20px (pad-kiri) + 20px (pad-kanan) = 300px`[cite: 10].
     - Total gabungan: `680px + 300px = 980px` (mencukupi lebar `#container` secara pas)[cite: 8, 10].

6. **Widget Sidebar (`.widget-box`)**[cite: 11]:
   * `.widget-box`: Kotak modul dengan batas `border: 1px solid #eee;`[cite: 11].
   * `.widget-box li a`: Diberi `display: block;` agar setiap opsi menu memenuhi seluruh lebar baris daftar (`<li>`)[cite: 11].

7. **Grid 3 Kolom & Box Model (`.box`, `.row`)**[cite: 13]:
   * `.box`: Diberi `float: left;` dan `width: 33.333333%;` untuk membagi area `#main` menjadi 3 kolom sejajar[cite: 13].
   * `box-sizing: border-box;`: Properti sangat penting yang memastikan `padding: 0 10px;` dihitung ke dalam (*internal*), bukan menambah lebar luar elemen[cite: 13].
   * `.image-circle`: Menggunakan `border-radius: 50%;` untuk memotong gambar menjadi bentuk lingkaran[cite: 13].

8. **Teknik Clearfix Hack (`.row:after`, `.entry:after`)**[cite: 13, 14]:
   * Ketika elemen anak menggunakan `float`, elemen induk akan kehilangan tingginya (*collapse*)[cite: 13, 14].
   * `content: ''; display: table; clear: both;`: Membuat *pseudo-element* tak terlihat di akhir kontainer yang bertugas membersihkan status `float`, sehingga tinggi elemen induk kembali normal menyelimuti elemen anaknya[cite: 13, 14].

9. **Konten Artikel (`.entry`, `.entry img`)**[cite: 14, 15]:
   * `.entry img`: Menggunakan `float: left;` dan `margin-right: 15px;` agar paragraf mengalir di sebelah kanan gambar[cite: 15].
   * `.entry .right-img`: Menggunakan `float: right;` dan `margin-left: 15px;` agar paragraf mengalir di sebelah kiri gambar[cite: 15].

10. **Footer (`footer`)**[cite: 12]:
    * `clear: both;`: Memastikan `<footer>` selalu berada paling bawah setelah seluruh area `float` pada `#main` dan `#sidebar` selesai disapu[cite: 12].


### 3. Halaman Beranda (`home.html`)

![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230127.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230136.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-15%20230146.png?raw=true)

#### Penjelasan:
* **`<div id="container">`**: Pembungkus utama seluruh elemen halaman agar lebar website terkontrol di tengah.
* **`<nav>` & `class="active"`**: Mengelompokkan tautan navigasi. Kelas `active` pada `home.html` memberi tanda visual halaman mana yang sedang dibuka.
* **`<section id="hero">`**: Bagian banner utama untuk menyampaikan pesan *welcome* atau *Call to Action*.
* **`<div class="row">` & `<div class="box">`**: Menampung 3 kolom fitur berjejer.
* **`<aside id="sidebar">`**: Elemen semantik pendukung di samping area konten utama yang memuat widget daftar tautan.

---


### 4. Halaman about (`about.html`)

Halaman informasi profil pribadi dan daftar keahlian/portofolio sesuai instruksi tugas modul.

![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20000133.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20000147.png?raw=true)

#### Penjelasan:
* **`style="width: 100%;"` pada `#main`**: Membuat tampilan berformat *single-layout* (layout tunggal) tanpa sidebar agar area informasi terbaca lebih luas.
* **`<article>` profil & portofolio**: Memisahkan bagian biografi singkat dengan daftar riwayat proyek/kemampuan teknis.
* **`<ul>` dan `<li>`**: Menampilkan poin-poin keahlian secara rapi dan mudah dibaca.

---

### 5. Halaman Kontak (`kontak.html`)

Halaman yang menyediakan formulir interaktif bagi pengunjung untuk mengirimkan nama, email, dan pesan.

![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20000609.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20000621.png?raw=true)

#### Penjelasan:
* **`<form action="#" method="post">`**: Elemen pembungkus tempat penampungan input data pengguna.
* **`<div class="form-group">`**: Wadah pemisah untuk setiap pasang baris *label* dan *input* agar spasi antar-field konsisten (`margin-bottom: 15px;`).
* **`<label for="...">` & `<input id="...">`**: Menghubungkan judul field dengan kotak pengisian data secara tepat.
* **`input` & `textarea` (`width: 100%; box-sizing: border-box;`)**: Memaksa lebar kolom input memenuhi seluruh area elemen `#main` tanpa berlebih.
* **`required`**: Atribut validasi HTML5 untuk memastikan form tidak dikirim dalam keadaan kosong.

---

### 6. File Style Pusat (`style.css`)

![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20001339.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20001350.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20001359.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20001410.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20001423.png?raw=true)
![image alt](https://github.com/Bagas240/Lab4Web/blob/main/image/Screenshot%202026-10-16%20001435.png?raw=true)
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()
![image alt]()


#### Penjelasan :

#### 1. Import Tipografi (`@import`)[cite: 8]
* `@import url(...)`: Mengambil aset font eksternal 'Open Sans' dan 'Open Sans Condensed' langsung dari CDN Google Fonts[cite: 8].
* Parameter `wght`: Mengunduh variasi ketebalan font dari `300` (*Light*), `400` (*Regular*), `600` (*Semi-Bold*), hingga `700` (*Bold*) beserta gaya miring (*italic*)[cite: 8].

#### 2. Universal Reset CSS (`*`)[cite: 8]
* `*`: Selector asterisk memilih **semua elemen HTML** di seluruh dokumen[cite: 8].
* `margin: 0; padding: 0;`: Menghapus *default margin* dan *padding* bawaan browser (*User Agent Stylesheet*)[cite: 8]. Langkah ini wajib dilakukan agar ukuran dan jarak antar-elemen presisi di semua jenis browser[cite: 8].

#### 3. Styling Utama Dokumen (`body`)[cite: 8]
* `line-height: 1;`: Menentukan jarak ketinggian antarbaris kalimat secara proporsional[cite: 8].
* `font-size: 100%;`: Menyesuaikan ukuran font dasar mengikuti preferensi sistem bawaan pengguna (standarnya 16px)[cite: 8].
* `font-family: 'Open Sans', sans-serif;`: Menetapkan jenis huruf 'Open Sans' sebagai font utama, serta `sans-serif` sebagai font cadangan (*fallback*)[cite: 8].
* `color: #5a5a5a;`: Mengatur warna teks menjadi abu-abu gelap agar nyaman dibaca dan tidak terlalu kontras dibanding hitam pekat[cite: 8].

#### 4. Pembungkus Situs (`#container`)[cite: 8]
* `width: 980px;`: Mengunci lebar total halaman web secara tetap pada `980px`[cite: 8].
* `margin: 0 auto;`: Formula margin top/bottom `0` dan left/right `auto` untuk memosisikan kontainer persis di tengah-tengah layar browser (*center alignment*)[cite: 8].
* `box-shadow: 0 0 1em #cccccc;`: Memberikan efek bayangan menyebar sebesar `1em` berwarna abu-abu `#cccccc` di sekeliling pembungkus untuk menciptakan efek kedalaman visual (*elevation*)[cite: 8].

#### 5. Bagian Kepala (`header`, `header h1`)[cite: 8]
* `header { padding: 20px; }`: Memberi spasi ruang dalam sebesar `20px` di sekeliling area header[cite: 8].
* `header h1`: Memberi margin vertikal `20px`, margin horizontal `10px`, serta warna teks abu-abu terang `#b5b5b5`[cite: 8].

#### 6. Bilah Navigasi (`nav`, `nav a`, `nav a:hover`, `nav a.active`)[cite: 9]
* `nav { display: block; background-color: #1f5faa; }`: Menjadikan bilah navigasi berstatus *block* dengan warna latar biru pekat `#1f5faa`[cite: 9].
* `nav a`:
  * `padding: 15px 30px;`: Memberikan area sentuh/klik yang lapang di sekitar teks menu[cite: 9].
  * `display: inline-block;`: **Penting!** Tag `<a>` secara bawaan bertipe *inline*[cite: 9]. Mengubahnya ke `inline-block` memungkinkan properti `padding` dapat diatur ukurannya tanpa membuat menu runtuh ke baris baru[cite: 9].
  * `color: #ffffff; text-decoration: none; font-weight: bold;`: Teks berwarna putih, menghilangkan garis bawah tautan, dan menebalkan teks menu[cite: 9].
* `nav a.active, nav a:hover`: Mengubah warna background menjadi biru lebih terang (`#2b83ea`) saat kursor melintas (*hover*) atau saat halaman dalam posisi aktif (`.active`)[cite: 9].

#### 7. Spanduk Promosi / Hero Panel (`#hero`, `#hero h1`, `#hero p`)[cite: 9, 10]
* `#hero`: Area promo berlatar abu-abu terang `#e4e4e5` dengan padding dalam `50px` (vertikal) dan `20px` (horizontal) serta jarak bawah `20px`[cite: 9, 10].
* `#hero h1`: Ukuran judul besar `35px` dengan spasi bawah `20px`[cite: 10].
* `#hero p`: Ukuran teks penjelasan `18px` dengan spasi tinggi baris `25px` agar sangat nyaman dibaca[cite: 10].

#### 8. Pembagi Layout Kolom (`#wrapper`, `#main`, `#sidebar`)[cite: 10]
* `#wrapper`: Pembungkus utama untuk memisahkan area konten kiri dan sidebar kanan[cite: 10].
* `#main`:
  * `float: left;`: Menggeser area konten utama ke posisi mengambang di sebelah kiri[cite: 10].
  * `width: 640px; padding: 20px;`: Lebar bersih konten `640px` ditambah padding `40px` (kiri-kanan) = **Total Lebar 680px**[cite: 10].
* `#sidebar`:
  * `float: left;`: Menggeser area sidebar ke sebelah kiri (berjajar persis di samping `#main`)[cite: 10].
  * `width: 260px; padding: 20px;`: Lebar bersih sidebar `260px` ditambah padding `40px` (kiri-kanan) = **Total Lebar 300px**[cite: 10].
  * **Analisis Kalkulasi Layout**: `680px (#main) + 300px (#sidebar) = 980px` (Pas sesuai lebar `#container`, sehingga kedua kolom bersisian presisi tanpa terdorong ke bawah)[cite: 8, 10].

#### 9. Komponen Widget Sidebar (`.widget-box`)[cite: 11]
* `.widget-box`: Kotak pembungkus widget berbatas garis `border: 1px solid #eee;`[cite: 11].
* `.widget-box .title`: Judul widget berlatar biru `#428bca` dengan teks putih[cite: 11].
* `.widget-box ul`: `list-style-type: none;` menghapus bulatan (*bullet points*) daftar bawaan[cite: 11].
* `.widget-box li a`: Diberi `display: block;` agar seluruh area baris pilihan menu dapat diklik, tidak hanya teksnya saja[cite: 11].
* `.widget-box li:hover a`: Berubah warna latar menjadi abu-abu halus (`#eee`) saat disorot kursor[cite: 11].

#### 10. Sistem Grid 3 Kolom & Box Model (`.box`, `.image-circle`, `.row`)[cite: 13, 14]
* `.box`:
  * `float: left; width: 33.333333%;`: Membagi area `#main` secara rata menjadi 3 kolom sejajar secara presisi[cite: 13].
  * `box-sizing: border-box;`: **Fitur Kunci CSS!** Memastikan `padding: 0 10px;` dihitung ke dalam (*internal*), sehingga penambahan padding tidak akan menambah lebar luar kotak dan tidak akan merusak tatanan grid[cite: 13].
  * Vendor prefixes (`-moz-box-sizing`, `-webkit-box-sizing`): Menjamin dukungan fitur `box-sizing` pada browser Mozilla Firefox dan Safari/WebKit versi lama[cite: 13].
* `.image-circle`: `border-radius: 50%;` memotong gambar persegi menjadi lingkaran sempurna[cite: 13].
* `.row`: `margin: 0 -10px;` adalah trik *negative margin* untuk menetralkan padding luar dari elemen `.box`[cite: 13].

#### 11. Teknik Clearfix Hack (`.row:after`, `.entry:after`)[cite: 13, 14]
* Masalah Float: Ketika elemen anak diberi `float`, elemen pembungkus induknya akan kehilangan ketinggian (*height collapse*)[cite: 13, 14].
* `content: ''; display: table; clear: both;`: Membuat elemen semu (*pseudo-element*) tak terlihat di akhir pembungkus untuk membersihkan status `float` secara otomatis[cite: 13, 14]. Ini memaksa pembungkus induk tetap mempertahankan ukurannya menyelimuti seluruh elemen anak[cite: 13, 14].

#### 12. Format Posting Artikel (`.divider`, `.entry`, `.entry img`)[cite: 14, 15]
* `.divider`: Garis pemisah antar-artikel berupa garis tipis `#eeeeee` dengan margin vertikal `40px`[cite: 14].
* `.entry img`:
  * `float: left; margin-right: 15px;`: Gambar mengambang di kiri, memaksa teks paragraf mengalir di sisi kanannya[cite: 15].
* `.entry .right-img`:
  * `float: right; margin-left: 15px; margin-right: 0;`: Gambar mengambang di kanan, memaksa teks paragraf mengalir di sisi kirinya[cite: 15].

#### 13. Area Kaki Halaman (`footer`)[cite: 12]
* `clear: both;`: **Aturan Krusial!** Menjamin `<footer>` mutlak ditempatkan di bagian paling bawah halaman, terbebas dari dorongan elemen `float` di atasnya[cite: 12].
* `background-color: #1d1d1d; color: #eee; padding: 20px;`: Memberikan warna latar abu-abu sangat gelap dengan teks terang dan padding `20px`[cite: 12].

---
