# SAMPAI
Sistem AMan Password Anda Instan

<img width="448" alt="Screenshot 2024-07-01 at 09 56 23" src="https://github.com/it-t4mpan/SAMPAI/assets/168879273/b0a70337-7377-4d67-b5f0-06f143da2874">

# Ringkasan Fungsi dan Fitur Unggulan pada Script Password Generator
Fungsi:
- Inisialisasi Sesi dan Perlindungan CSRF:
- Script menginisialisasi sesi PHP dengan session_start().
Menghasilkan token CSRF dan menyimpannya di sesi untuk melindungi dari serangan cross-site request forgery.

- Fungsi Pembuatan Password:
  - generatePasswords($keyword, $count, $strength): Fungsi ini menghasilkan array password berdasarkan keyword yang diberikan. Setiap password:
    - Dibuat dengan menambahkan karakter acak (angka dan simbol khusus) ke keyword.
    - Memiliki panjang total antara 8 hingga 32 karakter tergantung pada tingkat kekuatan yang dipilih.
    - Mengandung setidaknya satu karakter khusus atau simbol.

- Penanganan Form dan Validasi:

- Script menangani pengiriman form melalui permintaan POST.
  - Memvalidasi input keyword untuk memastikan panjangnya antara 4 hingga 12 karakter.
  - Menghasilkan 10 rekomendasi password jika input valid.

- Penilaian Kekuatan Password:
  - Menggunakan library zxcvbn untuk menilai kekuatan password dan memberikan umpan balik langsung.

- Riwayat Password:
  - Menampilkan 10 password yang dihasilkan sekaligus.

- Export Password:
  - Fitur untuk mengekspor password yang dihasilkan ke dalam file teks dengan ekstensi .txt.
  - Menyertakan timestamp pengunduhan password dalam nama file.

- Fitur Unggulan:  
  - Desain Responsif dengan Tailwind CSS:
    -  Script menggunakan Tailwind CSS untuk styling, memastikan desain yang modern dan responsif.
    - CSS kustom ditambahkan untuk mengatur lebar maksimum container utama.
      
- Input Form dan Tombol:
  - Form mencakup field input untuk keyword dengan batas karakter 4 hingga 12.
  - Atribut maxlength dan minlength pada field input memastikan batas ini di sisi klien.
  - Ada dua tombol: "Generate" untuk mengirim form dan "Reset" untuk mengosongkan form tanpa me-refresh halaman.

- Rekomendasi Password:
    - Setelah pengiriman form, script menampilkan daftar 10 rekomendasi password.
    - Setiap password adalah kombinasi dari keyword, angka, dan karakter khusus.

- Fungsi Salin ke Clipboard:
  - Setiap rekomendasi password memiliki tombol "Copy" yang memungkinkan pengguna untuk menyalin password ke clipboard dengan satu klik.

- Error Handling dan Pesan:
     - Jika keyword kurang dari 4 karakter atau lebih dari 12 karakter, pesan kesalahan akan ditampilkan.

- Export Password ke File Teks:
  - Menambahkan tombol untuk meng-export password yang dihasilkan ke file teks dengan nama yang mencakup timestamp, contoh: R4hasia_2024-07-01_12-30-45.txt.
