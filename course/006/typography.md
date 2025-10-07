# Typography

Typography adalah elemen penting dalam desain web karena berhubungan langsung dengan **tampilan teks** — seperti ukuran huruf, warna, ketebalan, jarak, dan perataan.  
Tailwind CSS menyediakan banyak **utility classes** yang bisa langsung digunakan tanpa menulis CSS manual.

## Font Family

Untuk mengatur **jenis huruf (font family)**.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>font-sans</code></td><td>Font tanpa kait (misal: Helvetica, Arial, sans-serif)</td></tr><tr><td><code>font-serif</code></td><td>Font berkait (misal: Times New Roman, serif)</td></tr><tr><td><code>font-mono</code></td><td>Font monospace (misal: Courier New, monospace)</td></tr></tbody></table>

**Contoh:**

```html
<p class="font-sans">Teks ini menggunakan font sans-serif</p>
<p class="font-serif">Teks ini menggunakan font serif</p>
<p class="font-mono">Teks ini menggunakan font monospace</p>
```

## Font Size (Ukuran Huruf)

Tailwind menyediakan ukuran huruf dari sangat kecil hingga sangat besar.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Ukuran (Default)</strong></td><td><strong>Keterangan</strong></td></tr><tr><td><code>text-xs</code></td><td>0.75rem (12px)</td><td>sangat kecil</td></tr><tr><td><code>text-sm</code></td><td>0.875rem (14px)</td><td>kecil</td></tr><tr><td><code>text-base</code></td><td>1rem (16px)</td><td>normal</td></tr><tr><td><code>text-lg</code></td><td>1.125rem (18px)</td><td>agak besar</td></tr><tr><td><code>text-xl</code></td><td>1.25rem (20px)</td><td>besar</td></tr><tr><td><code>text-2xl</code> s/d <code>text-9xl</code></td><td>1.5rem hingga 8rem</td><td>sangat besar</td></tr><tr><td><code>text-[&lt;value&gt;]</code></td><td>Isi ukuran kustom pada bagian value</td><td>&nbsp;</td></tr></tbody></table>

**Contoh:**

```html
<p class="text-sm">Tulisan kecil</p>
<p class="text-base">Tulisan normal</p>
<p class="text-3xl">Tulisan besar</p>
```

## Font Weight (Ketebalan Huruf)

Untuk mengatur seberapa tebal teks ditampilkan.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Ketebalan Font</strong></td></tr><tr><td><code>font-thin</code></td><td>100</td></tr><tr><td><code>font-extralight</code></td><td>200</td></tr><tr><td><code>font-light</code></td><td>300</td></tr><tr><td><code>font-normal</code></td><td>400</td></tr><tr><td><code>font-medium</code></td><td>500</td></tr><tr><td><code>font-semibold</code></td><td>600</td></tr><tr><td><code>font-bold</code></td><td>700</td></tr><tr><td><code>font-extrabold</code></td><td>800</td></tr><tr><td><code>font-black</code></td><td>900</td></tr></tbody></table>

**Contoh:**

```html
<p class="font-light">Teks ringan</p>
<p class="font-semibold">Teks sedang tebal</p>
<p class="font-bold">Teks tebal</p>
```

## Text Color (Warna Teks)

Gunakan class `text-{color}` untuk memberi warna pada teks.

**Contoh:**

```html
<p class="text-red-500">Teks merah</p>
<p class="text-blue-700">Teks biru tua</p>
<p class="text-gray-400">Teks abu-abu</p>
```

Kamu juga bisa menggunakan warna sesuai tema dark/light mode.

## Text Alignment (Perataan Teks)

Untuk mengatur posisi teks.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Keterangan</strong></td></tr><tr><td><code>text-left</code></td><td>Rata kiri</td></tr><tr><td><code>text-center</code></td><td>Rata tengah</td></tr><tr><td><code>text-right</code></td><td>Rata kanan</td></tr><tr><td><code>text-justify</code></td><td>Rata kanan-kiri</td></tr></tbody></table>

**Contoh:**

```html
<p class="text-center">Teks di tengah</p>
```

## Text Decoration (Garis pada teks)

Untuk menambahkan garis bawah, garis atas, atau menghapus dekorasi teks.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Keterangan</strong></td></tr><tr><td><code>underline</code></td><td>Garis bawah</td></tr><tr><td><code>overline</code></td><td>Garis atas</td></tr><tr><td><code>line-through</code></td><td>Garis coret</td></tr><tr><td><code>no-underline</code></td><td>Menghapus garis</td></tr></tbody></table>

**Contoh:**

```html
<p class="underline">Teks bergaris bawah</p>
<p class="line-through">Teks dicoret</p>
```

## Text Transform (Perubahan Huruf)

Untuk mengubah gaya huruf kapital.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Keterangan</strong></td></tr><tr><td><code>uppercase</code></td><td>Semua huruf kapital</td></tr><tr><td><code>lowercase</code></td><td>Semua huruf kecil</td></tr><tr><td><code>capitalize</code></td><td>Huruf pertama tiap kata besar</td></tr><tr><td><code>normal-case</code></td><td>Normal (default)</td></tr></tbody></table>

**Contoh:**

```html
<p class="uppercase">semua huruf kapital</p>
<p class="capitalize">huruf pertama besar</p>
```

## Letter Spacing (Jarak Antar Huruf)

Gunakan `tracking-{size}` untuk mengatur jarak antar huruf.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>tracking-tighter</code></td><td>Huruf lebih rapat</td></tr><tr><td><code>tracking-normal</code></td><td>Normal</td></tr><tr><td><code>tracking-wide</code></td><td>Huruf agak renggang</td></tr><tr><td><code>tracking-widest</code></td><td>Sangat renggang</td></tr></tbody></table>

**Contoh:**

```html
<p class="tracking-wider">T E K S R E N G G A N G</p>
```

## Line Height (Jarak Antar Baris)

Gunakan `leading-{size}` untuk mengatur jarak antar baris teks.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>leading-none</code></td><td>Tanpa jarak</td></tr><tr><td><code>leading-tight</code></td><td>Rapat</td></tr><tr><td><code>leading-normal</code></td><td>Normal</td></tr><tr><td><code>leading-loose</code></td><td>Longgar</td></tr></tbody></table>

**Contoh:**

```html
<p class="leading-loose">Teks dengan jarak antar baris yang longgar</p>
```

## Text Overflow dan Trucation

Untuk mengatur tampilan teks panjang yang terpotong.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>truncate</code></td><td>Potong teks dengan “...”</td></tr><tr><td><code>overflow-ellipsis</code></td><td>Sama dengan truncate</td></tr><tr><td><code>overflow-clip</code></td><td>Potong tanpa titik tiga</td></tr></tbody></table>

## Contoh Lengkap Typography

```html
<div class="p-6 bg-gray-100 rounded-xl">
  <h1 class="text-3xl font-bold text-center text-blue-600 mb-4">
    Judul Artikel
  </h1>
  <p class="font-sans text-gray-700 leading-relaxed tracking-wide">
    Tailwind CSS menyediakan berbagai utility untuk mengatur tampilan teks
    dengan cepat dan efisien tanpa menulis CSS manual. Kamu dapat mengubah
    ukuran, warna, perataan, serta jarak antar huruf dengan mudah.
  </p>
  <p class="mt-3 text-right italic text-sm text-gray-500">
    - Ditulis oleh Indira
  </p>
</div>
```

Typography di Tailwind CSS memudahkan pengembang untuk mengatur **tampilan teks** secara fleksibel, menghindari CSS manual, membuat desain lebih **konsisten & cepat**.
