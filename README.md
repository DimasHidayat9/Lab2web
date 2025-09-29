# Jawaban Tugas

# Nomor 1
# Eksperimen dengan mengubah dan menambah properti CSS
<img width="1920" height="1080" alt="Screenshot (103)" src="https://github.com/user-attachments/assets/68612715-1ca1-4902-b4fe-635ed28379a1" />

# Nomor 2
# Perbedaan deklarasi CSS h1 {…} dengan #intro h1 {…}
Deklarasi h1 {…} digunakan untuk mengatur seluruh elemen `<h1>` di halaman web, sehingga semua judul utama akan mendapatkan gaya yang sama.
Sedangkan deklarasi #intro h1 {…} lebih spesifik, yaitu hanya mengatur elemen `<h1>` yang berada di dalam elemen dengan atribut id="intro".
Contoh:
```
h1 { color: red; }          /* Semua elemen h1 menjadi merah */
#intro h1 { color: blue; }  /* Hanya h1 di dalam #intro yang biru */
```
Maka, jika terdapat `<h1>` di luar elemen #intro, warnanya tetap merah. Namun `<h1>` di dalam #intro akan menjadi biru. Hal ini menunjukkan bahwa selector dengan ID lebih spesifik dibandingkan selector elemen biasa.

# Nomor 3
# Prioritas antara CSS Internal, Eksternal, dan Inline
Apabila terdapat deklarasi CSS yang sama pada inline CSS, internal CSS, dan eksternal CSS, maka browser akan menampilkan gaya berdasarkan urutan prioritas (specificity) berikut:
1. Inline CSS (ditulis langsung pada atribut elemen HTML, misalnya `<p style="color:red;">`).
2. Internal CSS (ditulis di dalam tag `<style>` pada file HTML).
3. Eksternal CSS (ditulis pada file .css terpisah dan dipanggil melalui `<link>`).
Contoh:
```
<p style="color:red;">Teks ini merah</p>
```


Walaupun pada internal atau eksternal terdapat aturan p { color: blue; }, browser tetap akan menampilkan warna merah karena inline CSS memiliki prioritas tertinggi.

Dengan demikian, inline CSS akan selalu menang jika terjadi konflik, kemudian internal CSS, dan terakhir eksternal CSS.

# Nomor 4
# Prioritas antara ID dan Class pada CSS
Jika sebuah elemen HTML memiliki ID dan Class secara bersamaan, maka deklarasi CSS dengan selector ID akan lebih diutamakan dibandingkan dengan selector Class.
Contoh:
```
<p id="paragraf-1" class="text-paragraf">Contoh Teks</p>
```
```
#paragraf-1 { color: blue; }    /* Lebih kuat */
.text-paragraf { color: red; }  /* Lebih lemah */
```
Hasilnya, teks akan berwarna biru karena selector ID (#paragraf-1) memiliki tingkat spesifisitas lebih tinggi daripada selector Class (.text-paragraf).
Dengan kata lain, semakin spesifik selector CSS, maka semakin besar prioritasnya dalam menentukan gaya elemen.


# Penjelasan dari setiap langkah praktikum beserta penjelasannya.
# 1. Membuat Dokumen HTML
<img width="1920" height="1080" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/7f8cbe50-e3ae-4192-b7c9-9005ccd0e2da" />

# Penjelasan
Belum ada styling khusus selain bawaan browser. Heading `<h1>` masih hitam default, link berwarna biru dengan underline, dan teks paragraf juga default hitam.
Ini menunjukan tampilan dasar HTML tanpa CSS tambahan.

# 2. Mendeklarasikan CSS Internal
<img width="1920" height="1080" alt="Screenshot (104)" src="https://github.com/user-attachments/assets/389d70b2-aa6b-4013-9fb2-68dd7830dc7f" />

# Penjelasan
CSS internal adalah salah satu cara untuk menambahkan gaya atau tampilan ke dalam sebuah halaman web. Berbeda dengan CSS eksternal yang membutuhkan file terpisah dengan ekstensi .css, 
CSS internal dituliskan langsung di dalam file HTML. Penulisan CSS internal ini dilakukan dengan menambahkan tag <style> yang diletakkan di dalam bagian <head> pada dokumen HTML.
Dengan menggunakan CSS internal, kita bisa mengatur tampilan elemen-elemen HTML, seperti mengubah jenis huruf, meratakan teks, menambahkan jarak antar elemen, hingga mengatur ukuran teks. 
Aturan-aturan ini hanya berlaku untuk halaman HTML yang bersangkutan, sehingga cocok digunakan jika kita hanya ingin membuat gaya khusus pada satu halaman saja.

# 3. Menambahkan Inline CSS
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8b13719e-0ed6-452c-9c52-2239dcd21a59" />

# Penjelasan
Inline CSS adalah salah satu cara untuk menambahkan gaya pada elemen HTML dengan menuliskan aturan CSS langsung di dalam tag elemen tersebut menggunakan atribut style. 
Artinya, setiap elemen bisa memiliki gaya khusus tanpa bergantung pada aturan CSS internal atau eksternal.
Pada contoh kode yang sudah dibuat, terdapat beberapa penggunaan inline CSS. Misalnya, pada elemen `<h1>` di dalam `<header>`, diberikan atribut style="font-size: 28px; font-weight: bold;". 
Dengan aturan tersebut, teks judul akan ditampilkan lebih besar dan tebal. Kemudian, pada salah satu tautan di dalam `<nav>`, ditambahkan style="font-size: 18px;" sehingga hanya 
link tersebut yang ukurannya lebih besar dibandingkan link lainnya.

#  4. Membuat CSS Eksternal
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/2f6e9123-bf39-476b-84ad-593f52af9e38" />

# Penjelasan
CSS eksternal adalah cara memisahkan kode tampilan (style) dari struktur HTML dengan menaruh aturan-aturan CSS di file terpisah berekstensi .css. Metode ini membuat kode lebih rapi, mudah dikelola, dan tampilan halaman bisa diubah tanpa perlu menyentuh file HTML. Misalnya, di file style.css kita dapat mendefinisikan aturan sederhana seperti memberi font Arial, sans-serif pada body, membuat header rata tengah dengan padding, mengatur link navigasi agar tanpa garis bawah dan memiliki jarak antar tautan, menambahkan padding serta margin pada bagian konten #intro, hingga membuat tombol .button dengan border melengkung agar terlihat menarik. File CSS eksternal ini kemudian dihubungkan ke HTML menggunakan tag <link rel="stylesheet" href="style.css"> di dalam bagian <head>. Dengan cara ini, halaman web akan lebih terorganisir, konsisten, dan mudah dikembangkan.


# 5. Menambahkan CSS Selector
<img width="1920" height="1080" alt="Screenshot (103)" src="https://github.com/user-attachments/assets/8770c1e5-ae05-4c6c-9989-ba63e14a6bd8" />

# Penjelasan
CSS selector adalah aturan yang digunakan untuk memilih elemen tertentu di dalam HTML agar bisa diberikan gaya. Misalnya, element selector seperti body {} dipakai untuk memberi font pada seluruh isi halaman, sedangkan ID selector dengan #intro {} dipakai khusus untuk elemen yang memiliki atribut id="intro". Lalu ada class selector seperti .button {} yang digunakan untuk menata elemen dengan atribut class="button", sehingga bisa dipakai berulang kali pada elemen berbeda. Selain itu, ada juga descendant selector misalnya nav a {} yang artinya memilih semua link <a> yang ada di dalam elemen <nav>. Tidak ketinggalan, kita bisa menggunakan pseudo-class selector seperti nav a:hover {} untuk menambahkan efek ketika pengguna mengarahkan kursor ke link. Dengan memanfaatkan berbagai selector ini, tampilan halaman web menjadi lebih terarah, fleksibel, dan mudah dikustomisasi.
