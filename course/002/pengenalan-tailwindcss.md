# Pengenalan TailwindCSS

Tailwind CSS adalah framework CSS berbasis utility-first, artinya styling dilakukan dengan menggunakan kelas-kelas kecil (utility classes) yang mewakili satu properti CSS tertentu.

Contoh:

- `text-center` → membuat teks rata tengah.
- `bg-blue-500` → memberi background biru.
- `p-4` → memberi padding 1rem (16px)

Dengan menggabungkan utilitas, kita bisa membuat tampilan UI tanpa harus menulis CSS manual.

## Filosofi Dasar Tailwind

- Utility-first → styling langsung dengan kelas kecil, tanpa bikin file CSS panjang.
- Konfigurasi sebagai pusat → semua warna, ukuran, font, dan spacing ditentukan dalam satu file config (tailwind.config.js).
- Cepat dan konsisten → developer bisa fokus ke logika, tidak ribet dengan penamaan kelas.

## Kelebihan Tailwind CSS

1.  **Produktif**: Bisa langsung styling di HTML/JSX tanpa pindah ke file CSS.
2.  **Konsisten**: Semua desain mengikuti skala yang sudah diatur.
3.  **Ringan**: Dengan fitur purge/JIT, hanya CSS yang digunakan yang akan dibundel.
4.  **Mudah diatur**: Bisa dikustomisasi lewat config sesuai brand atau design system.
5.  **Komunitas besar**: Banyak plugin, template, dan dokumentasi.

## Kekurangan Tailwind CSS

1.  **Markup lebih ramai**: Banyak kelas di satu elemen.
2.  **Perlu adaptasi**: Awal belajar mungkin terasa aneh, karena harus hafal utilitas.
3.  **Butuh build process**: Harus pakai tool seperti Vite/Webpack/PostCSS.

## Struktur Dasar Tailwind

Tailwind menyediakan beberbagia kategori utility class, misalnya:

1.  Layout dan Display
    - `flex`, `grid`, `block`, dll.
2.  Spacing (Margin dan Padding)
    - `m-4` (margin 1rem), `mt-2` (margin-top 0.5rem), `px-6` (padding kiri-kanan 1.5rem)
3.  Typography
    - `text-lg`, `font-bold`
4.  Colors dan Background
    - `text-gray-700`, `bg-red-500`
5.  Border dan Radius
    - `border`, `border-2`, `rounded-lg`, `rounded-full`
6.  Effects
    - `shadow-lg`, `opacity-75`, `hover:shadow-xl`
7.  Responsive dan State Variants
    - `sm:`, `md:`, `lg:`, `hover:`, `focus:`, `dark:`

---
