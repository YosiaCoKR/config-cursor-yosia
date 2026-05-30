# 🚀 Dokumentasi Konfigurasi Cursor (VS Code) Yosia

Repositori ini berisi file konfigurasi (`setting.json`) untuk IDE Cursor / Visual Studio Code. Konfigurasi ini dirancang untuk memberikan pengalaman coding yang **fokus (minim gangguan)**, **estetik (tema SynthWave)**, dan **produktif (didukung AI & Intellisense penuh)**.

Berikut adalah ringkasan dari fitur-fitur yang ada di dalam konfigurasi ini:

## 🤖 1. Cursor AI & Alur Kerja
- **Partial Accepts:** Menerima sebagian saran dari AI secara bertahap (`enablePartialAccepts`).
- **Terminal AI (Cmd+K):** Mendukung prompt AI langsung di dalam terminal.
- **Konteks Proyek:** Obrolan AI (Chat) disetel untuk selalu memahami konteks proyek secara keseluruhan.

## 🌌 2. Visual Core (Estetika & UI)
- **Tema Warna:** Menggunakan **SynthWave '84** dengan tambahan efek *Glow/Neon* manual pada kursor, *highlight* baris, dan *border* tab.
- **Tema Ikon:** Menggunakan **simple-icons**.
- **Immersive UI (Zero Distraction):** Menyembunyikan elemen yang mengganggu seperti *minimap*, *breadcrumbs*, dan *scrollbar* agar ruang kode lebih luas.
- **Posisi Sidebar:** Diposisikan di sebelah **Kanan** agar kode tidak bergeser saat membuka/menutup sidebar explorer.

## ⌨️ 3. Tipografi & Kenyamanan Visual
- **Font Utama:** `JetBrains Mono`, dipadukan dengan `FiraCode Nerd Font` untuk ikon terminal/ligatures.
- **Kenyamanan Baca:** Ukuran font `15`, tinggi baris `29`, spasi antar huruf `0.6`, dengan *font smoothing antialiased*.
- **Ligatures:** Diaktifkan (`fontLigatures: true`) untuk simbol kode yang lebih cantik (seperti `=>`, `!=`, `===`).
- **Animasi:** Cursor dibuat berkedip perlahan (*phase*) dengan animasi pergerakan yang halus (*smooth scrolling* & *smooth caret animation*).

## ⚡ 4. Formatter & Linter (Per-Bahasa)
Kode akan selalu otomatis diformat saat disimpan (`Format On Save`) maupun saat di-*paste*.
- **Web (JS, TS, React, HTML, CSS, JSON):** Menggunakan `Prettier`.
- **Python:** Menggunakan `Black Formatter` dipadukan dengan **Ruff** sebagai linter (pengganti Flake8+Isort) yang juga akan otomatis merapikan *imports*.
- **Go:** Menggunakan `goimports` dan `golangci-lint`.
- **PHP / Laravel:** Menggunakan `Intelephense` dan `Blade Formatter` (dari `shufo`).
- **Java:** Menggunakan `Oracle Java`.

## 🔍 5. Intellisense & Bantuan Kode (Inlay Hints)
Saran kode dimunculkan secara instan (tanpa *delay*). Konfigurasi ini sangat memanfaatkan **Inlay Hints** (teks samar yang menunjukkan tipe data / nama parameter tanpa harus disorot):
- **Python (cursorpyright):** Menampilkan *return types*, tipe variabel, dan nama argumen pemanggilan fungsi.
- **Go (gopls):** Dokumentasi penuh saat *hover*, *placeholders* saat *autocomplete*, dan petunjuk variabel.
- **JavaScript & TypeScript:** Auto-import dari `package.json`, auto-complete pemanggilan fungsi, dan hints untuk nilai Enum, *return types*, serta tipe parameter.

## 🖥️ 6. Terminal & Sistem
- **Profil Terminal (Windows):** Menggunakan **PowerShell** sebagai default.
- Font terminal disetel menggunakan `FiraCode Nerd Font` agar kompatibel dengan berbagai *tools* command-line masa kini (seperti *Starship prompt* atau *Oh My Posh*).
- Akselerasi GPU terminal diaktifkan.

## 🚀 7. Produktivitas & Fitur Ekstra
- **File Nesting (Explorer):** Mengelompokkan file konfigurasi yang menumpuk. Contoh: `package-lock.json` akan disembunyikan di dalam `package.json`. `.env.local` disembunyikan di dalam `.env`.
- **Auto Close Tag:** Tag HTML/XML/Komponen React akan otomatis ditutup. Aktif juga untuk Blade, Vue, Markdown, dll.
- **Sticky Scroll:** Nama fungsi, *class*, atau struktur bersarang akan tetap "menempel" di atas editor maksimal 5 baris, sehingga Anda tidak tersesat saat men-*scroll* fungsi yang sangat panjang.
- **Penerjemah Komentar:** Komentar kode berbahasa asing dapat diterjemahkan ke Bahasa Indonesia (`id`) saat disorot (*hover*).

---

### 📦 Prasyarat / Ekstensi yang Dibutuhkan
Agar konfigurasi ini berjalan dengan baik, pastikan Anda telah menginstal font dan beberapa ekstensi VS Code / Cursor berikut:
1. **Font:** `JetBrains Mono` & `FiraCode Nerd Font`
2. **Tema:** `SynthWave '84`
3. **Ekstensi Penting:** Prettier, Black Formatter, Ruff, Go, PHP Intelephense, Laravel Blade Snippets, Comment Translate.
