# Sizing

**Sizing** dalam Tailwind CSS digunakan untuk mengatur ukuran elemen — yaitu **lebar (width)** dan **tinggi (height)**.  
Dengan utility class ini, kamu bisa menentukan ukuran elemen dengan cepat tanpa menulis CSS manual seperti `width: 100px;` atau `height: 50%;`.

Tailwind menyediakan class bawaan yang **responsif**, **konsisten**, dan bisa juga **dicustom** sesuai kebutuhanmu.

## Width (Lebar)

Untuk mengatur lebar elemen, gunakan prefix `w-`.

### Lebar Tetap (Fixed Width)

Tailwind menyediakan ukuran lebar dari **sangat kecil hingga besar**, dalam satuan rem.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Nilai</strong></td><td><strong>Ukuran (px)</strong></td></tr><tr><td><code>w-0</code></td><td>0rem</td><td>0px</td></tr><tr><td><code>w-1</code></td><td>0.25rem</td><td>4px</td></tr><tr><td><code>w-2</code></td><td>0.5rem</td><td>8px</td></tr><tr><td><code>w-4</code></td><td>1rem</td><td>16px</td></tr><tr><td><code>w-8</code></td><td>2rem</td><td>32px</td></tr><tr><td><code>w-16</code></td><td>4rem</td><td>64px</td></tr><tr><td><code>w-32</code></td><td>8rem</td><td>128px</td></tr><tr><td><code>w-64</code></td><td>16rem</td><td>256px</td></tr><tr><td><code>w-96</code></td><td>24rem</td><td>384px</td></tr></tbody></table>

**Contoh:**

```html
<div class="w-32 bg-blue-300 p-2">Lebar 8rem (128px)</div>
<div class="w-64 bg-green-300 p-2">Lebar 16rem (256px)</div>
```

### Lebar Persentase

Tailwind juga menyediakan class berbasis **persentase**, cocok untuk layout responsif.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Lebar</strong></td></tr><tr><td><code>w-1/2</code></td><td>50%</td></tr><tr><td><code>w-1/3</code></td><td>33.333%</td></tr><tr><td><code>w-2/3</code></td><td>66.666%</td></tr><tr><td><code>w-1/4</code></td><td>25%</td></tr><tr><td><code>w-3/4</code></td><td>75%</td></tr><tr><td><code>w-full</code></td><td>100%</td></tr><tr><td><code>w-screen</code></td><td>100vw (seluruh lebar layar)</td></tr></tbody></table>

**Contoh:**

```html
<div class="w-1/2 bg-purple-300">Lebar 50%</div>
<div class="w-full bg-yellow-300">Lebar penuh (100%)</div>
```

### Lebar Minimum dan Maksimum

Untuk membatasi lebar elemen agar tidak terlalu kecil atau terlalu besar.

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>min-w-0</code></td><td>Lebar minimum 0</td></tr><tr><td><code>min-w-full</code></td><td>Lebar minimum 100%</td></tr><tr><td><code>max-w-xs</code></td><td>Lebar maksimum kecil (20rem / 320px)</td></tr><tr><td><code>max-w-md</code></td><td>Lebar maksimum sedang (28rem / 448px)</td></tr><tr><td><code>max-w-lg</code></td><td>Lebar maksimum besar (32rem / 512px)</td></tr><tr><td><code>max-w-xl</code></td><td>Lebar maksimum lebih besar (36rem / 576px)</td></tr><tr><td><code>max-w-screen-lg</code></td><td>Maksimum sesuai ukuran layar besar</td></tr></tbody></table>

**Contoh:**

```html
<div class="w-full max-w-md bg-pink-200 p-4">
  Lebar ini tidak akan melebihi 28rem meskipun layar besar.
</div>
```

## Height (Tinggi)

Untuk mengatur tinggi elemen, gunakan prefix `h-`.

### Tinggi Tetap (Fixed Height)

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Nilai</strong></td><td><strong>Ukuran (px)</strong></td></tr><tr><td><code>h-0</code></td><td>0rem</td><td>0px</td></tr><tr><td><code>h-4</code></td><td>1rem</td><td>16px</td></tr><tr><td><code>h-8</code></td><td>2rem</td><td>32px</td></tr><tr><td><code>h-16</code></td><td>4rem</td><td>64px</td></tr><tr><td><code>h-32</code></td><td>8rem</td><td>128px</td></tr><tr><td><code>h-64</code></td><td>16rem</td><td>256px</td></tr><tr><td><code>h-96</code></td><td>24rem</td><td>384px</td></tr></tbody></table>

**Contoh:**

```html
<div class="h-32 bg-blue-400 w-32">Tinggi 8rem</div>
```

### Tinggi Persentase dan Layar

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>h-1/2</code></td><td>50% dari tinggi parent</td></tr><tr><td><code>h-full</code></td><td>100% dari tinggi parent</td></tr><tr><td><code>h-screen</code></td><td>100vh (tinggi layar penuh)</td></tr><tr><td><code>h-auto</code></td><td>Tinggi otomatis sesuai isi</td></tr></tbody></table>

**Contoh:**

```html
<div class="h-1/2 bg-green-400">Tinggi 50% dari parent</div>
<div class="h-screen bg-indigo-400">Tinggi penuh 1 layar</div>
```

### Mimimum dan Maksimum Tinggi

<table><tbody><tr><td><strong>Class</strong></td><td><strong>Fungsi</strong></td></tr><tr><td><code>min-h-0</code></td><td>Tinggi minimum 0</td></tr><tr><td><code>min-h-full</code></td><td>Minimum 100% dari parent</td></tr><tr><td><code>min-h-screen</code></td><td>Minimum setinggi layar</td></tr><tr><td><code>max-h-96</code></td><td>Maksimum tinggi 24rem</td></tr><tr><td><code>max-h-screen</code></td><td>Maksimum setinggi layar</td></tr></tbody></table>

**Contoh:**

```html
<div class="min-h-screen bg-gray-300 flex items-center justify-center">
  <p>Elemen ini minimal setinggi layar penuh!</p>
</div>
```

## Custom Sizing

Kalau ukuran bawaan belum cukup, kamu bisa menambahkan ukuran **custom** di file `tailwind.config.js`.

**Tambahkan Custom Width dan Height**

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      width: {
        128: "32rem", // 512px
        144: "36rem", // 576px
      },
      height: {
        128: "32rem", // 512px
        144: "36rem", // 576px
      },
    },
  },
};
```

Sekarang kamu bisa gunakan:

```html
<div class="w-128 h-128 bg-teal-400">
  Elemen dengan ukuran custom (32rem x 32rem)
</div>
```

## Arbitrary Value (Custom Langsung)

Kamu juga bisa langsung memberikan nilai ukuran tanpa ubah konfigurasi.

```html
<div class="w-[450px] h-[200px] bg-orange-400">Ukuran 450x200 px</div>
<div class="w-[50%] h-[30vh] bg-red-400">
  Ukuran 50% lebar dan 30% tinggi layar
</div>
```

Format:

`w-[nilai]` atau `h-[nilai]`  
Nilai bisa dalam satuan `px`, `rem`, `%`, `vh`, atau `vw`.

## Responsive Width dan Height

Gunakan **breakpoint prefix** seperti `sm:`, `md:`, `lg:` untuk membuat elemen lebih fleksibel di berbagai ukuran layar.

**Contoh:**

```html
<div class="w-32 h-32 md:w-64 md:h-64 lg:w-96 lg:h-96 bg-sky-400">
  Ukuran berubah sesuai lebar layar
</div>
```

- `w-32 h-32` → default (mobile)
- `md:w-64 h-64` → tablet
- `lg:w-96 h-96` → desktop

## Contoh Kombinasi Sizing

```html
<div class="max-w-md mx-auto bg-gray-100 rounded-lg shadow-md p-6">
  <img
    class="w-full h-64 object-cover rounded-md"
    src="https://picsum.photos/800/400"
    alt="Gambar"
  />
  <h2 class="text-xl font-bold mt-4">Tailwind CSS Sizing</h2>
  <p class="text-gray-700 mt-2">
    Gunakan utility <code>w-</code> dan <code>h-</code> untuk mengatur ukuran
    elemen dengan cepat. Kamu juga bisa menambahkan ukuran custom di konfigurasi
    atau langsung memakai nilai khusus.
  </p>
</div>
```
