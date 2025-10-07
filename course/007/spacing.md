# Spacing

Dalam dunia web, **spacing** digunakan untuk mengatur **jarak antar elemen** agar tampilan website lebih rapi dan enak dilihat.  
Tailwind CSS menyediakan **utility classes** untuk mengatur _margin_ dan _padding_ dengan sangat cepat tanpa menulis CSS manual.

## Margin dan Padding

Margin digunakan untuk mengatur jarak diluar antar elemen. Padding digunakan untuk mengatur ruang antara isi elemen dan batas elemen.

Ilustrasi sederhana:

![margin-padding](/images/margin-padding.png)

## Skala Spacing di Tailwind

Tailwind menggunakan sistem angka (skala) untuk menentukan ukuran jarak.  
Contohnya: `1`, `2`, `4`, `8`, `10`, `12`, `16`, dll.

<table><tbody><tr><td><strong>Nilai</strong></td><td><strong>Ukuran (px)</strong></td><td><strong>Keterangan</strong></td></tr><tr><td><code>0</code></td><td>0px</td><td>tanpa jarak</td></tr><tr><td><code>1</code></td><td>0.25rem (4px)</td><td>sangat kecil</td></tr><tr><td><code>2</code></td><td>0.5rem (8px)</td><td>kecil</td></tr><tr><td><code>4</code></td><td>1rem (16px)</td><td>sedang</td></tr><tr><td><code>8</code></td><td>2rem (32px)</td><td>besar</td></tr><tr><td><code>16</code></td><td>4rem (64px)</td><td>sangat besar</td></tr></tbody></table>

**Catatan**: `1rem` = 16px (umumnya di browser).

## Margin (m)

Gunakan prefix `m` untuk memberi jarak di luar elemen.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>m-4</code></td><td>Semua sisi diberi margin 1rem</td></tr><tr><td><code>mt-4</code></td><td>Margin atas</td></tr><tr><td><code>mb-4</code></td><td>Margin bawah</td></tr><tr><td><code>ml-4</code></td><td>Margin kiri</td></tr><tr><td><code>mr-4</code></td><td>Margin kanan</td></tr><tr><td><code>mx-4</code></td><td>Margin kiri dan kanan</td></tr><tr><td><code>my-4</code></td><td>Margin atas dan bawah</td></tr></tbody></table>

**Contoh:**

```html
<div class="m-4 bg-blue-200">Margin di semua sisi</div>
<div class="mt-8 bg-green-200">Margin atas lebih besar</div>
<div class="mx-auto w-1/2 bg-yellow-200">
  Margin kiri-kanan otomatis (center)
</div>
```

## Margin Negatif

Kamu juga bisa memberikan margin negatif untuk “menarik” elemen lebih dekat ke arah tertentu.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>-m-2</code></td><td>Margin negatif semua sisi</td></tr><tr><td><code>-mt-4</code></td><td>Margin atas negatif</td></tr><tr><td><code>-ml-8</code></td><td>Margin kiri negatif</td></tr></tbody></table>

**Contoh:**

```html
<div class="-mt-4 bg-red-300">Tergeser ke atas</div>
```

## Padding (p)

Gunakan prefix `p` untuk memberi jarak di dalam elemen (antara konten dan tepi elemen).

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>p-4</code></td><td>Padding di semua sisi</td></tr><tr><td><code>pt-4</code></td><td>Padding atas</td></tr><tr><td><code>pb-4</code></td><td>Padding bawah</td></tr><tr><td><code>pl-4</code></td><td>Padding kiri</td></tr><tr><td><code>pr-4</code></td><td>Padding kanan</td></tr><tr><td><code>px-4</code></td><td>Padding kiri-kanan</td></tr><tr><td><code>py-4</code></td><td>Padding atas-bawah</td></tr></tbody></table>

**Contoh:**

```html
<div class="p-6 bg-gray-300">Padding di semua sisi</div>
<div class="py-8 px-4 bg-green-300">
  Padding atas-bawah besar, kiri-kanan kecil
</div>
```

## Kombinasi Margin dan Padding

Kamu bisa menggabungkan margin dan padding dalam satu elemen untuk mengatur jarak luar dan dalam sekaligus.

**Contoh:**

```html
<div class="m-8 p-4 bg-blue-400 text-white">
  Elemen ini memiliki margin luar 2rem dan padding dalam 1rem.
</div>
```

## Auto Margin untuk Centering

Gunakan `mx-auto` untuk membuat elemen **tengah secara horizontal**, biasanya pada elemen dengan `width` tertentu.

**Contoh:**

```html
<div class="mx-auto w-1/2 bg-indigo-300 text-center p-4">
  Elemen ini berada di tengah secara horizontal.
</div>
```

## Custom Nilai Margin dan Padding

Tailwind juga mendukung **arbitrary value**, artinya kamu bisa langsung menentukan nilai custom di dalam class.

**Contoh:**

```html
<div class="mt-[50px] bg-red-200">Margin atas 50px</div>
<div class="p-[3.5rem] bg-green-200">Padding 3.5rem</div>
<div class="mx-[10%] bg-blue-200">Margin horizontal 10%</div>
```

**Format:**

`m-[nilai]`, `p-[nilai]`, `mt-[nilai]`, `px-[nilai]`, dst.  
Nilainya bisa berupa `px`, `rem`, `em`, `%`, `vh`, atau `vw`.

## Responsive Spacing

Tailwind mendukung **responsive design**, sehingga kamu bisa mengatur spacing berbeda untuk ukuran layar berbeda.

**Contoh:**

```html
<div class="p-2 md:p-6 lg:p-12 bg-pink-300">
  Padding kecil di HP, sedang di tablet, besar di desktop.
</div>
```

Keterangan:

- `p-2` → padding 0.5rem (default untuk layar kecil)
- `md:p-6` → padding 1.5rem (medium screen)
- `lg:p-12` → padding 3rem (large screen)

## Contoh Lengkap Kombinasi Spacing

```html
<div class="m-10 p-6 bg-gray-200 rounded-xl">
  <h1 class="text-xl font-bold mb-4">Judul Artikel</h1>
  <p class="text-gray-700 mb-6">
    Tailwind CSS menyediakan utility untuk mengatur jarak antar elemen dengan
    mudah. Kamu bisa menggunakan margin untuk jarak luar dan padding untuk jarak
    dalam elemen.
  </p>
  <button class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">
    Baca Selengkapnya
  </button>
</div>
```
