# Apa itu _utility-first framework?_

**Utility-first framework** (sering disebut _utility-CSS_) adalah pendekatan styling UI yang menyediakan \*\*kelas-kelas kecil (utilities)\*\*—misalnya `p-4`, `text-center`, `bg-blue-500`—untuk **satu tugas spesifik**. Alih-alih menulis banyak selector dan nama kelas semantik di file CSS terpisah. Kita dapat **merakit tampilan langsung di markup** (HTML/JSX) dengan menggabungkan utilities tersebut.

Contoh (Tailwind CSS, salah satu utility-first paling populer):

```html
<button class="px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700">
  Simpan
</button>
```

Tanpa membuat kelas kustom seperti `.btn-primary`, tombol sudah rapi, responsif, dan punya state hover.

## Latar dan Filosofi

- **Fokus pada komposisi, bukan penamaan**: Kita menyusun UI dari blok-blok kecil yang konsisten, bukan memikirkan “nama kelas apa ya?”.
- **Desain sebagai token**: Skala spacing, warna, radius, font size didefinisikan di **konfigurasi** lalu dipakai konsisten lewat nama utilitas.
- **Skalabilitas via constraint**: Karena pilihan sudah “dipagari” oleh skala/tokens, desain lebih konsisten, review lebih mudah, dan _drift_ visual berkurang.
- **Build-time optimization**: Modern utility-first memakai _JIT compiler_ yang hanya mengirim CSS yang benar-benar dipakai, sehingga ukuran CSS kecil.

## Ciri Khas Utama

- **Kelas atomik**: Satu kelas = satu properti (atau satu set kecil), contoh mt-6, grid, shadow, flex.
- **Kombinasi di HTML/JSX**: Styling dirakit di tempat komponen ditulis.
- **Variant & state**: Utilities siap pakai untuk responsive (sm:, md:), state (hover:, focus:), mode (dark:), rtl/ltr, hingga data/aria state.
- **Konfigurasi global**: tailwind.config.js (atau setara) sebagai “sumber kebenaran” design tokens (warna, spacing, typografi).
- **Purging/JIT**: Hanya utilities yang muncul di source Anda yang ikut dibundel.

## Kelebihan

1.  **Kecepatan pengembangan**: Tidak perlu bolak-balik file CSS; hasil terlihat instan di komponen.
2.  **Konsistensi desain**: Skala spacing/warna terstandar mengurangi variasi liar.
3.  **Ukuran bundle efisien**: JIT menghasilkan CSS sangat kecil karena _tree-shaken_.
4.  **Maintainability**: Tidak ada “\_dead CSS\_” yang tertinggal; hapus markup → styling ikut hilang.
5.  **Predictable**: Nama utilitas → properti CSS satu-satu, mudah ditebak dan dicari.

## Kekurangan

1.  **Markup lebih panjang**: Kelas bisa banyak. Solusi: ekstrak menjadi _component_ UI atau pakai `@apply`/komponen desain.
2.  **Kurva belajar**: Perlu hapal skala dan _prefix_ variant.
3.  **“Deklaratif di markup”**: Bagi sebagian tim, memisahkan concerns (HTML vs CSS) terasa kabur. Biasanya teratasi lewat komponen terabstraksi.
4.  **Ketergantungan toolchain**: Butuh build step (PostCSS/Vite/Webpack) untuk JIT & purging/

---
