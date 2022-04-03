## Lab4Web

**Nama  : Fery Affandi**<br>
**NIM   : 312010018**<br>
**Kelas : TI.20.A.1**<br>

## Praktikum 4

![tugas](foto/1.png)
<p align="center">Gambar 4.1

## langkah-langkah praktikum 

Buka text editor yang anda punya, contohnya Visual Studio Code

![VScode](foto/VScode.png)
<p align="center">Gambar 4.2

Persiapan membuat dokumen HTML dengan nama file <b>lab4_box.html</b> seperti berikut.
```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=, initial-scale=1.0">
        <title>Box Element</title>
    </head>
    <body>
        <header>
            <h1>Box Element</h1>
        </header>
    </body>
    </html>
```
## Membuat Box Element

Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.
```html
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
    </section>
```
## CSS Float Property

Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.
```css
    <style>
        div {
            float:left;
            padding: 10px;
        }
        .div1 {
            background: red;
        }
        .div2 {
            background: yellow;
        }
        .div3 {
            background: green;
        }
    </style>
```
kemudian buka browser dan melihat hasilnya.

![hasil](foto/2.png)
<p align="center">Gambar 4.3 Box Element Foat

## Mengatur Clearfix Element

<b>Clearfix</b> digunakan untuk mengatur element setelah float element. 
Property `clear` digunakan untuk mengaturnya.

Tambahkan element div lainnya seteleah div3 seperti berikut.
```html
    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
    </section>
```
Kemudian atur property clear pada CSS, seperti berikut.
```css
    .div4 {
        background-color: blue;
        clear: left;
        float: none;
    }
```
selanjutnya buka browser dan refresh kembali.

![hasil](foto/3.png)
<p align="center">Gambar 4.4 Clearfix

Lakukan eksperimen terhadap penggunaan property clear 
dengan nilai lainnya (<i>left, both, right</i>), dan amati perubahannya.

## Membuat Layout Sederhana

Kita akan membuat layout web sederhana seperti gambar berikut.

![layout sederhana](foto/layout_sederhana.png)
<p align="center">Gambar 4.5 layout sederhana

Buat folder baru dengan nama <b>lab4_layout</b>, kemudian buatlah file baru 
didalamnya dengan nama <b>home.html</b>, dan file css dengan nama <b>style.css.</b>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css" >
</head>
<body>
    <div id="container">
        
    </div>
</body>
</html>
```

Kemudian buat kerangka layout dengan semantics element seperti berikut.

![kerangka layout](foto/kerangka_layout.png)
<p align="center">Gambar 4.6 kerangka layout

Kemudian tulis kode berikut.
```html
<header>
    <h1>Layout Sederhana</h1>
</header>
<nav>
    <a href="home.html" class="active">Home</a>
    <a href="artikel.html">Artikel</a>
    <a href="about.html">About</a>
    <a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
    <section id="main"></section>
    <aside id="sidebar"></aside>
</section>
<footer>
    <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```

Kemudian buka browser dan lihat hasilnya.

![hasil](foto/4.png)
<p align="center">Gambar 4.7 Tampilan Kerangka Layout.

Kemudian tambahkan kode CSS untuk membuat layoutnya.
```css
/* import google font */
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400
;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import
url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0
,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}
body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#5a5a5a;
}
#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```
Kemudian lihat hasilnya pada browser.

![hasil](foto/5.png)
<p align="center">Gambar 4.8 Tampilan Header Layout.

## Membuat Navigasi

Kemudian selanjutnya mengatur navigasi.
```css
/* navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}
nav a.active,
nav a:hover {
    background-color: #2b83ea;
}
```
Kemudian lihat hasilnya.

![hasil](foto/6.png)
<p align="center">Gambar 4.9 Tampilan Navigasi.

## Membuat Hero Panel.

Selanjutnya membuat hero panel. Tambahkan kode HTML dan CSS seperti berikut.

```html
<section id="hero">
    <h1>Hello World!</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
    pretium ac.</p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
```css
/* Hero Panel */
#hero {
background-color: #e4e4e5;
padding: 50px 20px;
margin-bottom: 20px;
}
#hero h1 {
margin-bottom: 20px;
font-size: 35px;
}
#hero p {
margin-bottom: 20px;
font-size: 18px;
line-height: 25px;
}
```
![hasil](foto/8.png)
<p aalign="center">Gambar 4.10 tampilan hero Panel.

