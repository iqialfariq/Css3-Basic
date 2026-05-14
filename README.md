# 🧠 Penjelasan CSS 3
<p align="justify">
CSS3 adalah istilah untuk versi lanjutan dari CSS yang memperkenalkan banyak fitur modern seperti animasi, transformasi, transisi, dan layout fleksibel (Flexbox, Grid). 
</p>

---

## 📌 Property dan Value CSS 3

### 🔲 Border Radius
<p align="justify">
Untuk membuat sudut elemen menjadi melingkar atau membulat. Dengan kata lain, ia mengontrol tingkat kelengkungan sudut pada sebuah box (misalnya div, button, img). 
</p>

value Grid Template Column ada 2 yaitu:
1) px.
2) %.

Cara menuliskan value Border Radius:
1) nilai → semua sudut sama.
2) nilai → sudut atas-kiri & bawah-kanan | sudut atas-kanan & bawah-kiri.
3) nilai → sudut atas-kiri | sudut atas-kanan & bawah-kiri | sudut bawah-kanan.
4) nilai → sudut atas-kiri | sudut atas-kanan | sudut bawah-kanan | sudut bawah-kiri.
   
  Contoh:
  ```css
      div {
        width: 100px;
        height: 100px;
        border-radius: 10px;
        background-color: salmon;
      }
  ```

---

### 🌫️ Opacity
<p align="justify">
Untuk mengatur tingkat transparansi suatu elemen. Nilainya berupa angka antara 0.0 (sepenuhnya transparan) hingga 1.0 (sepenuhnya terlihat). value
opacity ada diantara nilai nol dan satu, seperti 0,5. untuk nol transparan sekali, dan untuk 1 solid sekali. 
</p>

  Contoh:
  ```css
      div {
        width: 100px;
        height: 100px;
        border-radius: 10px;
        opacity: 0.5;
        background-color: salmon;
      }
  ```

---

### 🎨 Rgba dan Hsla 
<p align="justify">
Rgba: Digunakan untuk membuat warna transparan tanpa memengaruhi teks atau konten lain. Misalnya background transparan tapi teks tetap jelas.
</p>
<p align="justify">
Hsla: Digunakan untuk membuat palet warna konsisten cukup ubah nilai hue untuk variasi warna. Misalnya branding dengan satu hue, lalu variasi
terang/gelap. 
</p>

  Contoh:
  ```css
      .rgba {
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      }

      .hsla {
        border: 3px solid hsla(200, 100%, 50%, 0.5);
      }
  ```

---

### 🪞 Box Shadow
<p align="justify">
Untuk menambahkan bayangan pada elemen. Bayangan ini bisa diatur arah, ukuran, warna, dan tingkat blur-nya sehingga memberi efek kedalaman (depth) atau
tampilan modern pada desain. 
</p>

value Box Shadow ada 6 yaitu:
1) offset-x → posisi bayangan secara horizontal (positif = kanan, negatif = kiri).
2) offset-y → posisi bayangan secara vertikal (positif = bawah, negatif = atas).
3) blur-radius → tingkat kabur bayangan (semakin besar nilainya, semakin blur).
4) spread-radius → ukuran sebaran bayangan (positif = melebar, negatif = mengecil).
5) color → warna bayangan (bisa pakai nama warna, hex, rgba, hsla).
6) inset → menjadikan bayangan di dalam elemen (inner shadow). 

  Contoh:
  ```css
      div {
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      }
  ```

---

### ✍️ Text Shadow 
<p align="justify">
Untuk memberikan bayangan pada teks. Dengan ini, teks bisa terlihat lebih menonjol, memiliki efek 3D, glow, atau artistik sesuai kebutuhan desain.  
</p>

value Text Shadow ada 4 yaitu:
1) offset-x → posisi bayangan secara horizontal (positif = kanan, negatif = kiri).
2) offset-y → posisi bayangan secara vertikal (positif = bawah, negatif = atas).
3) blur-radius → tingkat kabur bayangan (opsional, default = 0 → bayangan tajam).
4) color → warna bayangan (nama warna, hex, rgba, hsla).  

  Contoh:
  ```css
      div {
        text-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
      }
  ```

---

### 🔤 Font Face 
<p align="justify">
Adalah aturan CSS yang memungkinkan kita memuat dan menggunakan custom font di website, meskipun font tersebut tidak terpasang di komputer pengguna. 
Dengan ini, desainer bisa menjaga konsistensi tipografi sesuai branding tanpa bergantung pada font bawaan sistem.  
</p>

  Contoh:
  ```css
      @font-face {
        font-family: 'NamaFont';
        src: url('./fonts/NamaFont-Regular.woff2') format('woff2'),
        url('./fonts/NamaFont-Regular.woff') format('woff');
        font-weight: 400;
        font-style: normal;
      }
  ```

---

### 🧪 Filter 
<p align="justify">
Untuk memberikan efek visual pada elemen, terutama gambar, teks, atau container. Efek ini mirip dengan filter di aplikasi editing foto (blur, 
brightness, contrast, dll). 
</p>

value Filter ada 9  yaitu:
1) Blur.
2) Brightness.
3) Contrast.
4) Grayscale.
5) Invert.
6) Opacity.
7) Saturate.
8) Sepia.
9) drop-shadow.

  Contoh:
  ```css
      img {
        filter: blur(5px);
      }
  ```

---

### 🔄 Transform 
<p align="justify">
Untuk mengubah tampilan elemen dengan operasi 2D atau 3D, seperti memutar, memperbesar, memperkecil, memiringkan, atau menggeser. Transformasi ini
tidak memengaruhi layout elemen lain, hanya tampilan visual elemen tersebut.
</p>

value Transform ada 5 yaitu:
1) translate.
2) rotate.
3) scale.
4) skew.
5) matrix.

  Contoh:
  ```css
      div {
        transform: rotate(45deg); /* putar 45 derajat */
      }
  ```

---

### ⏩ Transition  
<p align="justify">
Untuk membuat efek animasi halus ketika suatu elemen berubah dari satu state ke state lain. Misalnya saat hover, focus, atau ketika class berubah. 
Tanpa transition, perubahan terjadi seketika. Dengan transition, perubahan berlangsung perlahan sesuai durasi dan pola yang ditentukan.
</p>

  Contoh:
  ```css
      div {
        width: 100px;
        height: 100px;
        background-color: salmon;
        transition: background-color 0.5s ease, transform 0.3s ease-in-out;
      }
  ```

---

### 🎬 Animation 
<p align="justify">
Untuk membuat animasi kompleks dengan mengontrol perubahan gaya elemen dari waktu ke waktu. Animasi ini biasanya didefinisikan menggunakan @keyframes,
lalu dipanggil dengan animation. 
</p>

value animation ada 8 yaitu :
1) name → nama animasi yang didefinisikan di @keyframes. Contoh: fadeIn, slideUp.
2) duration → lama animasi berlangsung. Contoh: 2s, 500ms.
3) timing-function → pola kecepatan animasi.
   - linear → kecepatan konstan. 
   - ease → default, halus di awal dan akhir. 
   - ease-in → mulai lambat, lalu cepat. 
   - ease-out → mulai cepat, lalu melambat. 
   - ease-in-out → kombinasi lambat → cepat → lambat.
4) delay → jeda sebelum animasi dimulai.
   Contoh: 1s.
5) iteration-count → jumlah pengulangan. 
   - Angka (1, 3, dll). 
   - infinite → berulang tanpa henti.
6) direction → arah animasi.
   - normal → default. 
   - reverse → berjalan mundur. 
   - alternate → maju lalu mundur. 
   - alternate-reverse → mundur lalu maju.
7) fill-mode → menentukan gaya elemen sebelum / sesudah animasi.
   - none → tidak ada efek tambahan. 
   - forwards → tetap pada kondisi akhir animasi. 
   - backwards → mengambil kondisi awal animasi saat delay. 
   - both → gabungan forwards + backwards.
8) play-state → status animasi.
   - running → berjalan. 
   - paused → berhenti sementara. 


  Contoh:
  ```css
      @keyframes geser {
         from {
          transform: translateX(0);
         }

         to {
          transform: translateX(200px);
         }
      }

      div {
         width: 100px;
         height: 100px;
         background-color: salmon;
         animation: geser 2s ease-in-out infinite alternate;
      }
  ```
