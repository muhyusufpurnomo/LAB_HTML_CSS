# Jawaban Praktikum: Muh.Yusuf Purnomo (10224023)

## Bagian 1: Pemanasan

1. Pada aturan `nav a.active:hover { color: red; }`:
   - Selector: `nav a.active:hover`
   - Deklarasi: `color: red;`
   - Property: `color`
   - Value: `red`
   - Pseudo-class: `:hover`

2. Elemen block: `p`, `li`, `h2`. Elemen inline: `span`, `a`, `strong`.

3. Paragraf yang berwarna hijau adalah A dan B karena keduanya merupakan elemen `<p>` yang berada di dalam elemen dengan class `box`. C dan D tidak berwarna hijau dari aturan tersebut.

4. Warna teks menjadi merah karena selector `#title` memiliki specificity paling tinggi dibandingkan `.heading` dan `h1`.

5. Perbaikan susunan tag HTML:
   ```html
   <p>Hello <strong>world</strong></p>
   ```

## Bagian 3: Prediksi Selector Golf

### P1

(a) `Weekly hack nights.`: hijau (`green`), karena cocok dengan selector `section p`.

(b) `Bring your own laptop.`: oranye (`orange`), karena selector `.note` memiliki specificity lebih tinggi daripada `section p`.

(c) `© 2026 Student Affairs`: biru (`blue`), karena cocok dengan selector `p`.

### P2

Urutan specificity tertinggi ke terendah:

1. `#tech p`
2. `.club p`
3. `main section p`
4. `p`

### Setelah diuji (hasil sebenarnya)

(a) `Weekly hack nights.`: hijau (`green`).

(b) `Bring your own laptop.`: oranye (`orange`).

(c) `© 2026 Student Affairs`: biru (`blue`).

*Catatan: cocokkan bagian ini dengan hasil yang benar-benar tampil setelah kamu menjalankan file di browser.*

## Bagian 4: Box Model

### Q1 (content-box)

Lebar yang terlihat dari tepi border ke tepi border:

300px + (16px × 2) + (1px × 2) = **334px**.

Margin 24px pada setiap sisi tidak termasuk lebar kartu. Jika margin kiri dan kanan ikut dihitung, total ruang horizontal adalah 334px + 48px = **382px**.

### Q2 (border-box)

Dengan `box-sizing: border-box`, `width: 300px` sudah mencakup content, padding, dan border. Lebar yang terlihat menjadi **300px**.

Lebar content:

300px − 32px padding − 2px border = **266px**.

Margin tetap 24px pada setiap sisi.

### Pengecekan DevTools

Periksa salah satu elemen di browser menggunakan DevTools, lalu buka bagian **Computed → Box Model**. Tuliskan nilai aktual yang tampil di browser pada bagian ini. Jangan mengisi nilai pemeriksaan aktual hanya berdasarkan perkiraan.

## Bagian 5: Tabel Debug

| # | Baris | Bug | Perbaikan | Cara menemukannya |
|---|---|---|---|---|
| 1 | 555 | Property `colour` tidak dikenal CSS | Ganti menjadi `color: #333;` | Membaca kode dan DevTools |
| 2 | 561 | Deklarasi background tidak diakhiri titik koma | Tambahkan `;` setelah `#dbe7f3` | Membaca kode |
| 3 | 567 | Selector `.Card` tidak cocok dengan class `card` | Gunakan `.card` | Membaca kode |
| 4 | 577 | Penulisan `18 px` salah | Ganti menjadi `18px` | DevTools |
| 5 | 583 | Nilai `centre` tidak valid untuk `text-align` | Ganti menjadi `center` | DevTools |
| 6 | 595 | Tag `<h1>` ditutup dengan `</h2>` | Ganti menjadi `</h1>` | W3C Validator |
| 7 | 601 | Tanda kutip pada atribut `href` tidak lengkap | Gunakan `href="about.html"` | W3C Validator |
| 8 | 609 | Penulisan atribut `class` tidak valid | Gunakan `class="card"` | W3C Validator |
| 9 | 613 | ID `newsList` tidak cocok dengan selector CSS `#news-list` | Samakan ID menjadi `news-list` | Membaca kode |

Catatan: atribut `alt` pada gambar juga perlu ditambahkan agar gambar memiliki deskripsi yang membantu aksesibilitas.

## Bagian 6: Tabel Code Review

| # | Baris | Masalah | Mengapa penting | Perbaikan saya |
|---|---|---|---|---|
| 1 | 653 | Tidak ada `<!DOCTYPE html>` dan atribut `lang` | Deklarasi dokumen dan bahasa tidak dinyatakan dengan benar | Tambahkan `<!DOCTYPE html>` dan `<html lang="id">` |
| 2 | 677 | Menggunakan `<div>` sebagai header | Tidak menggunakan elemen semantik | Ganti dengan `<header>` |
| 3 | 679 | Judul kampus menggunakan `<div>` dan `<b>` | Struktur heading tidak jelas | Gunakan `<h1>` |
| 4 | 681 | Navigasi menggunakan `<div>` | Area navigasi tidak ditandai secara semantik | Gunakan `<nav>` |
| 5 | 661 | Lebar header tetap 1200px | Bisa melampaui layar yang lebih kecil | Gunakan lebar fleksibel dan `max-width` |
| 6 | 663 | Menggunakan `!important` | Menyulitkan pemeliharaan CSS | Hapus `!important` |
| 7 | 691–703 | Judul bagian dibuat dengan `<div>` dan inline CSS | Struktur heading kurang tepat dan gaya tercampur dengan HTML | Gunakan `<h2>` dan CSS |
| 8 | 693–703 | Menggunakan `<br>` untuk mengatur jarak | Presentasi bercampur dengan struktur konten | Atur jarak menggunakan `margin` dan `padding` |
| 9 | 667 | Selector `.sidebar` tidak digunakan | CSS menjadi tidak terpakai | Hapus aturan tersebut jika tidak dibutuhkan |
| 10 | 705–709 | Input tidak memiliki label dan email menggunakan `type="text"` | Mengurangi aksesibilitas dan validasi | Tambahkan `<label for>` dan gunakan `type="email"` |
| 11 | 699 | Gambar tidak memiliki `alt` | Pembaca layar tidak mendapatkan deskripsi gambar | Tambahkan atribut `alt` |
| 12 | 709 | Menggunakan JavaScript inline untuk menampilkan pesan terkirim | Tidak benar-benar mengirim data formulir | Gunakan formulir dan backend jika perlu mengirim data |
| 13 | 713 | Footer dibuat dengan `<div>` | Tidak menggunakan elemen semantik footer | Gunakan `<footer>` |
| 14 | 663–665 | Warna teks abu-abu terang berpotensi kurang kontras | Teks dapat sulit dibaca | Gunakan warna dengan kontras memadai |

### Refleksi

1. Masalah yang paling sulit disadari hanya dengan melihat halaman di browser adalah penggunaan elemen HTML yang tidak semantik. Halaman masih bisa terlihat normal, tetapi struktur dokumennya kurang jelas bagi teknologi bantu.

2. Masalah tersebut tetap penting meskipun halaman berfungsi karena kode harus mudah dirawat, mudah diakses, dan mengikuti standar HTML. Kode yang baik juga memudahkan pengembangan di kemudian hari.

3. Saya akan memeriksa kode menggunakan W3C Validator dan DevTools sebelum mengumpulkannya. Saya juga akan memastikan heading, label formulir, atribut gambar, dan CSS sudah benar.

## Bagian 7: Exit Ticket

1. Anatomi aturan CSS terdiri dari selector dan blok deklarasi. Selector memilih elemen yang akan diberi gaya, sedangkan deklarasi berisi property dan value yang menentukan tampilannya.

2. Konsep yang masih perlu saya pelajari lebih lanjut adalah specificity CSS, terutama ketika beberapa selector memberikan aturan berbeda pada elemen yang sama.

3. Saya sekarang bisa membuat struktur HTML semantik, menghubungkan CSS, menggunakan selector untuk mengatur tampilan, serta memeriksa dan memperbaiki kesalahan dasar pada kode.