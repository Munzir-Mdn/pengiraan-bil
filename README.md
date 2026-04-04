📊 Dashboard Pengiraan Bil & Masa Kiraan (3 Fasa)

Web application berasaskan HTML + JavaScript (client-side sahaja) untuk:

Mengira tenaga elektrik dan anggaran bil bulanan bagi sistem 3 fasa (menggunakan jumlah arus).

Mengira masa kiraan (meter constant method) berdasarkan nilai rev/kWh atau imp/kWh.

Aplikasi ini direka untuk kegunaan teknikal, kerja lapangan, dan tujuan akademik.

🔗 Demo Web: [https://munzir-mdn.github.io/Sistem_Pengiraan_Elektrik/  ](https://munzir-mdn.github.io/pengiraan-bil/)
🔗 Repository: [https://github.com/Munzir-Mdn/Sistem_Pengiraan_Elektrik](https://github.com/Munzir-Mdn/pengiraan-bil)  

⚙️ Kaedah Pengiraan
1️⃣ Pengiraan Tenaga & Bil (3 Fasa – Kaedah Jumlah Arus)

Jumlah arus:

I_total = Ir + Iy + Ib

Kuasa aktif:

P = I_total × V × PF

Tenaga sehari:

kWh/day = (P × Jam) / 1000

Tenaga bulanan:

kWh/month = kWh/day × Hari

Anggaran bil:

Bil (RM) = kWh/month × Tarif

Nota: Kaedah ini mengikuti formula spreadsheet asal (jumlah arus × V × PF). Ia bukan formula √3 V_LL I PF standard 3 fasa.

2️⃣ Masa Kiraan (Meter Constant Method)

Digunakan untuk mengira masa berdasarkan:

MASA (ms)

V (Voltage)

I_total (A)

PF

KONSTAN (rev/kWh atau imp/kWh)

Bilangan nadi/pusingan

Formula:

MasaKiraan = (MASA / (V × I_total × PF × K)) × nadi

Dengan:

MASA = 3,600,000 ms (default = 1 jam)

K = 500 rev/kWh atau 500 imp/kWh (contoh)

nadi = 100 (default)

Output dipaparkan dalam:

milisaat (ms)

saat (s)

🖥️ Ciri-Ciri Dashboard

Dua kad besar:

🔵 Kad 1: Pengiraan Bil

🟢 Kad 2: Masa Kiraan

Auto-kira bila input berubah

Validasi asas (PF antara 0–1, tiada nilai negatif)

Ringkasan terperinci boleh disalin

Sync I_total antara dua kad

Paparan unit ms dan saat

Tanpa server (boleh guna terus dalam browser)

📂 Struktur Projek
pengiraan-bil-dashboard/
├── index.html
└── README.md


Tiada dependency tambahan. Semua kod dalam satu fail index.html.

🚀 Cara Guna
Kaedah 1: Jalankan Secara Tempatan

Download atau clone repository.

Buka fail index.html.

Masukkan nilai input.

Keputusan dikira secara automatik.

Kaedah 2: Deploy ke GitHub Pages

Create repository baru di GitHub.

Upload:

index.html

README.md

Pergi ke:

Settings → Pages

Pilih:

Deploy from branch → main

Aplikasi akan tersedia melalui link GitHub Pages.

🧪 Data Ujian (Nilai Spreadsheet)

Untuk pengesahan:

Ir = 45 A
Iy = 45 A
Ib = 45 A
V = 230 V
PF = 0.85
Jam = 16
Hari = 30
Tarif = 0.519 RM/kWh

Expected output:

I_total = 135 A

Tenaga sehari ≈ 422.28 kWh

Bil bulanan ≈ RM 6,574.90

Untuk masa kiraan:

MASA = 3,600,000 ms

K = 500

nadi = 100

Expected:

Masa kiraan ≈ 27.28 ms

📘 Kesesuaian Penggunaan

Sesuai untuk:

Juruteknik elektrik

Pelajar kejuruteraan elektrik

Pengesahan bacaan meter

Analisis penggunaan tenaga

Demonstrasi akademik

⚠️ Had & Penambahbaikan Masa Hadapan

Tidak menggunakan formula √3 sistem 3 fasa standard.

Tiada penyimpanan data (database).

Tiada eksport PDF/CSV (boleh ditambah kemudian).

Boleh ditambah:

Toggle formula 3 fasa standard

Preset tarif

Export CSV

Simpan data menggunakan LocalStorage

📄 Lesen

Projek ini boleh digunakan untuk tujuan pembelajaran dan bukan komersial.
Sila ubah suai mengikut keperluan teknikal anda.
