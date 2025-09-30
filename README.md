# Lab2Web

Nama : Abdi Putra Perdana

NIM : 312410426

Kelas : TI 24 A3

### Praktikum  

#### 1. Membuat dokumen HTML dan mendeklarasikan CSS Internal


Input : 
<img width="1510" height="2116" alt="code" src="https://github.com/user-attachments/assets/6601b640-4beb-4599-9790-72e14977cb4f" />




Output :
<img width="1919" height="1076" alt="Screenshot 2025-09-30 105210" src="https://github.com/user-attachments/assets/6d98bf8b-1793-4142-98df-a8dcea3f7034" />




### 2. Menambahkan Inline CSS
Menambahkan deklarasi inline CSS pada tag `<p>`


 <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/c1e69fe9-5b4e-408e-be22-040617943f13" />



### 3. Membuat CSS Eksternal
Membuat file baru dengan nama style_eksternal.css dan kemudian membuat deklarasi CSS.


<img width="710" height="824" alt="code2" src="https://github.com/user-attachments/assets/5232707e-141a-413c-9cb7-d53dd8746ee3" />


Kemudian menambahkan tag `<link>` untuk merujuk file css yang sudah di buat pada bagian `<head>`


<img width="1434" height="558" alt="code3" src="https://github.com/user-attachments/assets/893fa704-5170-4ea9-85de-7071907eee1e" />


output:
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/eca42a8c-a92c-4bbf-83c2-c80132cdad1c" />


### 4. Menambahkan CSS Selector
menggunakan ID dan Class selector pada file style_eksternal.css


Input:
<img width="772" height="1204" alt="code4" src="https://github.com/user-attachments/assets/1981d933-edde-4286-8000-9e15e3a00871" />


Output:<img width="1917" height="1079" alt="Screenshot 2025-09-30 140612" src="https://github.com/user-attachments/assets/1f74e8ac-98fc-4d1b-bac7-65600915573d" />

## Pertanyaan dan Tugas

### 1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
Jawab:
Saya melakukan eksperimen dengan menambahkan beberapa properti CSS:
```
h1 {
    font-size: 32px;
    color: darkgreen;
    text-transform: uppercase;
    text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
    border: 2px solid green;
    border-radius: 8px;
    padding: 10px;
    margin: 20px;
    text-align: center;
}

p {
    font-size: 16px;
    color: #333;
    line-height: 1.5;
    text-align: justify;
    letter-spacing: 1px;
    margin: 15px;
}

a {
    color: #fff;
    background-color: #007BFF;
    padding: 10px 15px;
    text-decoration: none;
    border-radius: 8px;
    display: inline-block;
    transition: background-color 0.3s ease;
}

a:hover {
    background-color: #0056b3;
}
```

Hasilnya:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ee9c2af6-b48b-4064-bab8-c3daf4b9579c" />



### 2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
Jawab:
h1 { ... } → berlaku untuk semua elemen `<h1>` di dokumen HTML.
#intro h1 { ... } → hanya berlaku untuk elemen `<h1>` yang ada di dalam elemen dengan atribut id="intro".
Maka hasilnya jika di jalankan di browser “Judul Umum” biru, “Judul Intro” merah.

<img width="1108" height="466" alt="image" src="https://github.com/user-attachments/assets/68ad8765-30bd-4159-91e5-9767f67a2a03" />



### 3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!

Prioritas CSS (CSS Specificity + urutan):
- Inline CSS (paling kuat) ditulis langsung di atribut `style` pada elemen.
- Internal CSS (di `<style>` dalam `<head>`).
- Eksternal CSS (file `.css` yang dihubungkan).

Contoh :
```
<head>
  <!-- Eksternal CSS -->
  <link rel="stylesheet" href="style.css">
  
  <!-- Internal CSS -->
  <style>
    p { color: green; }
  </style>
</head>
<body>
  <p style="color: red;">Halo Dunia</p>
</body>
```
Jika di `style.css` ada:
```
p { color: blue; }
```

### 4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut
terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya! `( <p id="paragraf-1" class="text-paragraf"> )`

Aturan prioritas CSS berdasarkan specificity:
- ID (`#id`) lebih kuat daripada
- Class (`.class`), lebih kuat daripada
- Selector elemen (`p`, `h1`, dll.)

contoh :
```
<p id="paragraf-1" class="text-paragraph">Halo Dunia</p>
```
```
p { color: blue; }                 /* elemen */
.text-paragraph { color: green; }  /* class */
#paragraf-1 { color: red; }        /* id */
```

Hasil: Teks akan berwarna merah, karena selector `#id` memiliki prioritas lebih tinggi dibanding `.class` atau elemen.
