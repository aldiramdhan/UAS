# Dokumentasi Dashboard Analisis Kerentanan Sosial Ekonomi (KSE)

## Gambaran Umum

Dashboard ini dirancang untuk memberikan visualisasi yang komprehensif mengenai data bantuan sosial berdasarkan analisis Kerentanan Sosial Ekonomi (KSE). Dashboard menampilkan berbagai jenis visualisasi yang disesuaikan dengan kebutuhan analisis, mulai dari distribusi data, ranking, hingga komposisi faktor-faktor yang mempengaruhi kerentanan sosial ekonomi.

## Proses Pembuatan Dashboard

### 1. Arsitektur Dashboard

Dashboard dibangun dengan struktur berikut:
- **Frontend**: HTML5, CSS3, dan JavaScript
- **Framework CSS**: Tailwind CSS untuk styling responsif
- **Library Visualisasi**: Chart.js untuk pembuatan grafik interaktif
- **Data Source**: File JSON yang berisi data hasil pembersihan
- **Layout**: Responsive grid system untuk berbagai ukuran layar

### 2. Struktur Data dan KPI

#### Key Performance Indicators (KPI)
Dashboard menampilkan 4 KPI utama:
- **Total Responden**: Jumlah keseluruhan data yang dianalisis
- **Calon Penerima Bansos**: Jumlah individu dengan skor KSE ≥ 3
- **Rata-rata Skor KSE**: Nilai rata-rata kerentanan sosial ekonomi
- **Pengangguran Produktif**: Jumlah pengangguran usia 18-60 tahun

### 3. Jenis Visualisasi dan Penerapannya

#### 3.1 Diagram Batang (Bar Chart)
**Implementasi:**
- **Chart 1**: Penerima Bansos per Provinsi
- **Chart 2**: Peringkat Provinsi berdasarkan Total Skor KSE
- **Chart 4**: Pengangguran Usia Produktif per Provinsi

**Alasan Penggunaan:**
Diagram batang dipilih untuk visualisasi distribusi dan ranking karena:
- Memudahkan perbandingan nilai antar kategori (provinsi)
- Efektif untuk menampilkan data numerik yang dapat diurutkan
- Memberikan gambaran jelas tentang proporsi relatif antar wilayah
- Mudah diinterpretasi untuk identifikasi provinsi dengan kebutuhan bantuan tertinggi

**Contoh:**
```
Diagram batang horizontal menampilkan:
- Sumbu X: Jumlah penerima bansos
- Sumbu Y: Nama provinsi
- Warna: Biru konsisten untuk keterbacaan
- Sorting: Dari nilai tertinggi ke terendah
```

#### 3.2 Diagram Lingkaran (Pie Chart)
**Implementasi:**
- **Chart 3**: Distribusi Pekerjaan Penerima Bansos

**Alasan Penggunaan:**
Diagram lingkaran dipilih untuk menampilkan proporsi karena:
- Menunjukkan komposisi bagian dari keseluruhan
- Memvisualisasikan persentase setiap kategori pekerjaan
- Mudah mengidentifikasi kategori dominan
- Efektif untuk data kategorikal dengan jumlah kategori terbatas

**Contoh:**
```
Diagram lingkaran menampilkan:
- Sektor: Jenis pekerjaan (Petani, Buruh, Tidak Bekerja, dll.)
- Ukuran: Proporsi dari total penerima bansos
- Warna: Pallet warna yang berbeda untuk setiap kategori
- Label: Persentase dan nama kategori
```

#### 3.3 Histogram/Diagram Batang Distribusi
**Implementasi:**
- **Chart 5**: Distribusi Skor KSE Keseluruhan

**Alasan Penggunaan:**
Histogram dipilih untuk menampilkan distribusi frekuensi karena:
- Menunjukkan pola distribusi data kontinyu
- Membantu identifikasi nilai yang paling sering muncul
- Memberikan gambaran tentang spread data
- Useful untuk analisis statistik lebih lanjut

**Contoh:**
```
Histogram menampilkan:
- Sumbu X: Rentang skor KSE (0-6)
- Sumbu Y: Frekuensi kemunculan
- Bins: Interval skor untuk pengelompokan
- Warna: Gradasi untuk menunjukkan intensitas
```

#### 3.4 Diagram Donat (Doughnut Chart)
**Implementasi:**
- **Chart 6**: Komposisi Faktor Penyebab Kerentanan

**Alasan Penggunaan:**
Diagram donat dipilih untuk analisis komposisi faktor karena:
- Memberikan fokus pada proporsi setiap faktor kerentanan
- Ruang tengah dapat digunakan untuk informasi tambahan
- Lebih modern dan clean dibanding pie chart biasa
- Efektif untuk menampilkan 6 faktor KSE (P1-P6)

**Contoh:**
```
Diagram donat menampilkan:
- P1: Pendapatan < UMR (Merah)
- P2: Keluarga < 4 anggota (Biru)
- P3: Balita > 1 (Hijau)
- P4: Lansia > 1 (Kuning)
- P5: Disabilitas (Ungu)
- P6: Anak Putus Sekolah (Pink)
```

### 4. Sistem Warna dan Tema

#### 4.1 Pallet Warna
Dashboard menggunakan sistem warna yang konsisten:
- **Primary Colors**: Biru untuk data utama
- **Secondary Colors**: Hijau untuk data positif, Merah untuk data kritis
- **Accent Colors**: Kuning, Ungu, Pink untuk kategori tambahan
- **Background**: Dark theme (Gray-900) untuk mengurangi eye strain

#### 4.2 Aksesibilitas
- Kontras tinggi antara teks dan background
- Ukuran font yang dapat dibaca
- Responsive design untuk berbagai perangkat
- Color-blind friendly palette

### 5. Interaktivitas dan Responsivitas

#### 5.1 Fitur Interaktif
- **Hover Effects**: Menampilkan detail nilai saat kursor di atas elemen
- **Legend**: Keterangan yang dapat diklik untuk toggle visibility
- **Tooltip**: Informasi detail yang muncul saat hover
- **Responsive Charts**: Menyesuaikan ukuran sesuai container

#### 5.2 Layout Responsif
- **Desktop**: Grid 2 kolom untuk charts utama
- **Tablet**: Grid 1 kolom dengan ukuran optimal
- **Mobile**: Stacked layout dengan scroll vertikal
- **KPI Cards**: Flexible grid yang menyesuaikan layar

### 6. Optimasi Performa

#### 6.1 Data Loading
- Asynchronous data loading untuk menghindari blocking
- Error handling untuk kasus file tidak ditemukan
- Data preprocessing untuk optimasi rendering

#### 6.2 Rendering
- Chart.js dengan konfigurasi responsive
- Lazy loading untuk charts yang tidak terlihat
- Efficient DOM manipulation

### 7. Keunggulan Dashboard

#### 7.1 Insight yang Diberikan
- **Distribusi Geografis**: Identifikasi provinsi dengan kebutuhan tertinggi
- **Profil Penerima**: Analisis demografis dan pekerjaan
- **Faktor Kerentanan**: Komposisi masalah sosial ekonomi
- **Trend Analysis**: Pola distribusi skor KSE

#### 7.2 Kegunaan untuk Pengambilan Keputusan
- **Alokasi Anggaran**: Berdasarkan distribusi geografis
- **Program Targeted**: Sesuai profil pekerjaan penerima
- **Prioritas Intervensi**: Berdasarkan faktor kerentanan dominan
- **Monitoring**: Tracking progress program bantuan sosial

### 8. Panduan Penggunaan

#### 8.1 Cara Membaca Dashboard
1. **Mulai dari KPI Cards** untuk mendapat gambaran umum
2. **Analisis Distribusi Geografis** melalui charts provinsi
3. **Pahami Profil Penerima** melalui distribusi pekerjaan
4. **Identifikasi Faktor Kritis** melalui komposisi kerentanan

#### 8.2 Interpretasi Data
- Skor KSE ≥ 3 menunjukkan kelayakan menerima bansos
- Provinsi dengan jumlah penerima tinggi perlu prioritas
- Faktor kerentanan dominan menentukan jenis intervensi
- Distribusi skor KSE menunjukkan heterogenitas populasi

### 9. Pengembangan Lanjutan

#### 9.1 Fitur Tambahan yang Dapat Dikembangkan
- **Filter Dinamis**: Berdasarkan provinsi, pekerjaan, atau skor
- **Time Series**: Analisis trend temporal
- **Drill-down**: Detail tingkat kabupaten/kota
- **Export Data**: Kemampuan unduh data dan visualisasi

#### 9.2 Integrasi Sistem
- **API Integration**: Koneksi dengan database real-time
- **User Authentication**: System login untuk akses terbatas
- **Dashboard Personalization**: Kustomisasi tampilan per user
- **Alert System**: Notifikasi untuk anomali data

## Kesimpulan

Dashboard ini dirancang dengan pendekatan user-centric yang mempertimbangkan kebutuhan analisis data bantuan sosial. Setiap jenis visualisasi dipilih berdasarkan karakteristik data dan tujuan analisis spesifik. Kombinasi antara estetika modern, fungsionalitas yang baik, dan insight yang actionable menjadikan dashboard ini sebagai tools yang efektif untuk mendukung pengambilan keputusan dalam program bantuan sosial.

Penggunaan teknologi web modern memastikan dashboard dapat diakses dari berbagai perangkat, sementara desain yang intuitif memudahkan pengguna dari berbagai latar belakang teknis untuk memahami dan menggunakan informasi yang disajikan.
