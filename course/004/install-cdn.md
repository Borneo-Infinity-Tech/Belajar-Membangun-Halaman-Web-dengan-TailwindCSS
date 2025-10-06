# Menggunakan Tailwind CSS dengan CDN

Pada materi sebelumnya, kamu sudah belajar teori singkat tentang **utility-first framework** dan juga perbedaan antara **Tailwind CSS** dengan **CSS vanilla**.  
Sekarang, kita akan mempraktikkan cara menggunakan **Tailwind CSS**, dimulai dari metode paling sederhana, yaitu **menggunakan CDN (Content Delivery Network)**.

Tailwind menyediakan link **CDN** agar kita bisa langsung menggunakannya tanpa instalasi atau konfigurasi tambahan. Metode ini cocok untuk belajar atau membuat proyek kecil.

Berikut langkah-langkah menggunakan TailwindCSS dengan CDN.

1.  Buat file HTML baru, misal `index.html`
2.  Tambahkan link CDN Tailwind ke dalam tag `<head>` seperti berikut:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
  </head>
  <body>
    <h1 class="text-3xl font-bold underline">Hello world!</h1>
  </body>
</html>
```

Kelebihan menggunakan CDN yaitu tidak perlu instalasi atau konfigurasi tambahan, cocok untuk pemula dan eksperimen cepat, dan langsung bisa digunakan hanya dengan menambahkan satu baris script. Namun, untuk proyek yang lebih besar, disarankan menggunakan **instalasi lokal (CLI atau PostCSS)** agar bisa mengatur konfigurasi dan performa dengan lebih baik.
