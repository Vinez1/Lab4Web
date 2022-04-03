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

## Membuat Box Element

Kemudian tambahkan kode untuk membuat box element dengan tag div seperti berikut.

    <section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
    </section>

## CSS Float Property

Selanjutnya tambahkan deklarasi CSS pada head untuk membuat float element, seperti berikut.

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

kemudian buka browser dan melihat hasilnya.

![hasil](foto/2.png)
<p align="center">Gambar 4.3

