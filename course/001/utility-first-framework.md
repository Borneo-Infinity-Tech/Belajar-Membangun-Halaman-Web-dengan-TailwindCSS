# Apa itu _utility-first framework?_

**Utility-first framework** (sering disebut _utility CSS_) adalah cara menata tampilan (styling) dengan **kelas-kelas kecil** yang masing-masing punya satu tugas jelas. Contoh: `p-4` (padding), `text-center` (tulisan rata tengah), `bg-blue-500` (latar biru).

Alih-alih bikin banyak kelas CSS khusus, kita **merangkai tampilan langsung di HTML/JSX** dengan menggabungkan kelas-kelas kecil itu.

Contoh:

```css
<button class="px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700">
  Simpan
</button>
```

Tanpa bikin `.btn-primary`, tombol sudah punya warna, jarak, sudut membulat, dan efek hover.

## Latar dan Filosofi

- **Fokus pada komposisi, bukan penamaan**: Kita menyusun UI dari blok-blok kecil yang konsisten, bukan memikirkan “nama kelas apa ya?”.
- **Desain sebagai token**: Skala spacing, warna, radius, font size didefinisikan di **konfigurasi** lalu dipakai konsisten lewat nama utilitas.
- **Lebih rapi & konsisten**: Karena pilihan sudah dibatasi skala, desain jadi seragam dan mudah direview.
- **CSS jadi kecil**: Compiler modern (JIT) cuma mengikutkan CSS yang benar-benar dipakai.

## Kelebihan

- **Cepat**: Styling langsung di tempat kamu bikin elemen.
- **Rapi & konsisten**: Ukuran, warna, jarak sudah disediakan skala yang seragam.
- **File kecil**: Yang dipakai saja yang akab masuk ke CSS final.
- **Responsif gampang**: Pakai `sm:`, `md:`, `lg:` buat layar yang berbeda.
- **State mudah**: Pakai `hover:`, `focus:`, `active:` buat efek.

## Kekurangan

- **Markup lebih panjang**: Kelas bisa banyak. Solusi: ekstrak menjadi _component_ UI atau pakai `@apply`/komponen desain.
- **Butuh adaptasi**: Harus hafal nama-nama kelas umum (biasanya cepat kebiasa).
- **Perlu build tool**: Biasanya lewat Vite/Webpack, tapi setup-nya sekali aja.

Intinya, **utility-first** itu menyusun tampilan dari **kelas-kelas kecil siap pakai** langsung di HTML, supaya bikin UI **lebih cepat, konsisten, dan mudah dirawat**; kamu tinggal merangkai “blok” seperti `p-4`, `text-center`, `bg-blue-500` tanpa harus menulis CSS panjang.
