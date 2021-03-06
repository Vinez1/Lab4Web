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
<p align="center">Gambar 4.10 tampilan hero Panel.

## Mengatur Layout Main dan Sidebar

Selanjutnya mengatur main content dan sidebar, tambahkan CSS float.
```css
/* main content */
#wrapper {
margin: 0;
}
#main {
float: left;
width: 640px;
padding: 20px;
}
/* sidebar area */
#sidebar {
float: left;
width: 260px;
padding: 20px;
}
```

## Membuat Sidebar Widget

Kemudian selanjutnya menambahkan element lain dalam sidebar.
```html
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
        </ul>
        </div>
        <div class="widget-box">
            <h3 class="title">Widget Text</h3>
            <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
            arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
            pharetra est nunc, nec pretium nunc pretium ac.</p>
</div>
</aside>
```
kemudian tambahkan CSS.
```css
/* widget */
.widget-box {
    border:1px solid #eee;
    margin-bottom:20px;
}
.widget-box .title {
    padding:10px 16px;
    background-color:#428bca;
    color:#fff;
}
.widget-box ul {
    list-style-type:none;
}
.widget-box li {
    border-bottom:1px solid #eee;
}
.widget-box li a {
    padding:10px 16px;
    color:#333;
    display:block;
    text-decoration:none;
}
.widget-box li:hover a {
    background-color:#eee;
}
.widget-box p {
    padding:15px;
    line-height:25px;
}
```
dan hasil pada browsernya seperti ini.

![hasil](foto/9.png)
<p align="center">Gambar 4.11 Tampilan Sidebar Widget.

## Mengatur Footer

Selanjutnya mengatur tampilan footer. Tambahkan CSS untuk footer.
```css
/* footer */
footer {
clear:both;
background-color:#1d1d1d;
padding:20px;
color:#eee;
}
```
hasilnya adalah

![hasil](foto/10.png)
<p align="center">Gambar 4.12 Tampilan Footer.

## Menambahkan Elemen lainnya pada Main Content

```css
<section id="main">
    <div class="row">
        <div class="box">
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt=""class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna molliseuismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt=""class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna molliseuismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
        <div class="box">
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt=""class="image-circle">
            <h3>Heading</h3>
            <p>Donec sed odio dui. Etiam porta sem malesuada magna molliseuismod.</p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
    </div>
</section>
```

Kemudian tambahkan CSS.

```css
/* box */
.box {
    display:block;
    float:left;
    width:33.333333%;
    box-sizing:border-box;
    -moz-box-sizing:border-box;
    -webkit-box-sizing:border-box;
    padding:0 10px;
    text-align:center;
}
.box h3 {
    margin: 15px 0;
}
.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}
box img {
    border: 0;
    vertical-align: middle;
}
.image-circle {
    border-radius: 50%;
}
.row {
    margin: 0 -10px;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
    content:'';
    display:table;
}
.row:after,
.entry:after {
    clear:both;
}
```

Lihat hasilnya di browser.

![hasil](foto/11.png)
<p align="center">Gambar 4.13 Tampilan Content.

## Menambahkan Content Artikel

Selanjutnya membuat content artikel. Tambahkan HTML berikut pada main content.
```html
<hr class="divider" />
<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
    pretium ac.</p>
</article>
<hr class="divider" />
<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt=""
    class="right-img">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
    elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
    vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
    pretium ac.</p>
</article>
```

Kemudian tambahkan CSS
```css
.divider {
    border:0;
    border-top:1px solid #eeeeee;
    margin:40px 0;
}
/* entry */
.entry {
    margin: 15px 0;
}
.entry h2 {
    margin-bottom: 20px;
}
.entry p {
    line-height: 25px;
}
.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}
.entry .right-img {
    float: right;
}
```

refresh pada browser dan hasilnya seperti ini.

![hasil](foto/12.png)
<p align="center">Gambar 4.14 Tampilan Artikel.

## Pertanyaan dan Tugas

<br>

### 1. Tambahkan Layout untuk menu About

=> buat single layout yang berisi deskripsi, portfolio, dll

### Tambahkan layout untuk menu Contact

=> yang berisi form isian: nama, email, message, dll

<br>

## Jawaban

### 1. membuat About

- _HTML_

```html
<div class="about">
    <div class="section-title">
        <h1>About me</h1>
        <br>
        <p>Nama saya Fery Affandi. Saya kuliah di Universitas Pelita Bangsa 
        yang terletak di Cikarang,Bekasi.
        Jurusan saya adalah Teknik Informatika dengan NIM 312010018.
        </p>
    </div>
    <div>
        <img class="avatar" src="asset/img/profile_img.jpg">
    </div>
</div>
```

- _CSS_

```css
/*layout About*/
.about {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #c0bdbd;
  clear: both;
  padding: 35px;
  line-height: 25px;
}
.avatar {
  width: 110px;
  border-radius: 50%;
  -webkit-border-radius: 50%;
  -moz-border-radius: 50%;
  -ms-border-radius: 50%;
  -o-border-radius: 50%;
}
```

dan hasil  di webnya adalah

![hasil](foto/14.png)
<p align="center">Gambar 4.15

### 2. Buat HTML seperti ini.

- _HTML_

```html
<div class="kontak-body">
  <h1>Contact</h1>
  <form class="kontak-form-class">
    <div class="form-form-group">
      <label for="name" class="kontak-label">Your Name</label>
      <input
        type="text"
        id="name"
        name="name"
        class="kontak-form-control"
        required
      />
    </div>
    <div class="kontak-form-group">
      <label for="name" class="kontak-label">Your Email</label>
      <div class="kontak-input-group">
        <input
          type="email"
          id="email"
          name="name"
          class="kontak-form-control"
          required
        />
      </div>
    </div>
  </form>
  <div class="kontak-form-group">
    <label for="name" class="kontak-label">Subject</label>
    <input
      type="text"
      id="name"
      name="name"
      class="kontak-form-control"
      required
    />
  </div>
  <div class="kontak-form-group">
    <label for="name" class="kontak-label">Message</label>
    <div class="kontak-input-group">
      <textarea
        id="message"
        name="message"
        class="kontak-form-control"
        rows="6"
        maxlength="3000"
        required
      ></textarea>
    </div>
  </div>
  <div class="kontak-form-group">
    <div class="loading">Loading</div>
    <div class="error-message"></div>
    <div class="sent-message">Your message has been sent. Thank you!</div>
  </div>
  <div class="text-center">
    <button type="submit">Send Message</button>
  </div>
</div>
```
dan CSSnya

```css
/*layout About*/
.about {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #e0dede;
  clear: both;
  padding: 35px;
  line-height: 25px;
}
.avatar {
  width: 110px;
  border-radius: 50%;
}
/*Layout Kontak*/
.kontak-body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
    Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  text-align: left;
  padding: 30px;
  padding-bottom: 10px;
  border: 1px solid #e0dede;
  border-radius: 0.25rem;
  max-width: 100%;
}
.kontak-form-group {
  margin-bottom: 1rem;
}
.kontak-input-group {
  position: relative;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
  -ms-flex-align: stretch;
  align-items: stretch;
  width: 100%;
}
.kontak-form-control {
  display: block;
  width: 100%;
  height: calc(1.5em + 0.75rem + 2px);
  padding: 0.375rem 0.75rem;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  color: rgb(56, 54, 54);
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #c6c6c6;
  outline: none;
  border-radius: 00.25rem;
  transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}

.kontak-form-control:focus {
  border: 1px solid #313131;
}

textarea.kontak-form-control {
  height: auto;
}

label.kontak-label {
  display: inline-block;
  margin-bottom: 0.5rem;
}
.loading {
  display: none;
  color: #ffffff;
  text-align: center;
  padding: 15px;
}
.loading:before {
  color: "";
  display: inline-block;
  border-radius: 50%;
  -webkit-border-radius: 50%;
  -moz-border-radius: 50%;
  -ms-border-radius: 50%;
  -o-border-radius: 50%;
  width: 24px;
  height: 24px;
  margin: 0 10px -6px 0;
  border: 3px solid #44e917;
  border-top-color: #eee;
  animation: animate-loading 1s linear infinite;
  -webkit-animation: animate-loading 1s linear infinite;
}
@-webkit-keyframes animate-loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes animate-loading {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.sent-message {
  display: none;
  color: #fff;
  background: chartreuse;
  text-align: center;
  padding: 15px;
  font-weight: 600;
}

.error-message {
  display: none;
  color: #fff;
  background: red;
  text-align: left;
  padding: 15px;
  font-weight: 600;
}

.error-message br + br {
  margin: 25px;
}

.sent-message {
  display: none;
  color: #fffefe;
  background: #fff;
  text-align: center;
  padding: 15px;
  font-weight: 600;
}
button[type="submit"] {
  background: #27a803;
  border: 0;
  padding: 10px 24px;
  color: rgb(255, 255, 255);
  transition: 0, 4s;
  border-radius: 4px;
}
button[type="submit"]:hover {
  background: rgb(98, 192, 54);
}
```

Kemudian refresh browser untuk melihat hasilnya.

![hasil](foto/15.png)
<p align="center">Gambar 4.16