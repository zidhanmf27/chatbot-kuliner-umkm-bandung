# 🍜 Chatbot Kuliner UMKM Kota Bandung

**Asisten cerdas untuk menemukan rekomendasi kuliner terbaik di Kota Bandung.**

Aplikasi ini adalah chatbot berbasis AI yang menggunakan metode **TF-IDF** dan **Cosine Similarity** untuk memberikan rekomendasi kuliner yang relevan berdasarkan pertanyaan pengguna. Dibangun dengan antarmuka **Streamlit** yang modern, responsif, dan elegan dengan dukungan tema dinamis.

---

## ✨ Fitur Unggulan

### 🤖 Sistem Rekomendasi Cerdas
- **Natural Language Processing (NLP)**: Memahami pertanyaan pengguna dalam bahasa natural.
- **Auto-Correct Typo**: Otomatis mengoreksi kesalahan ketik menggunakan fuzzy matching.
- **Semantic Expansion**: Memperluas konteks pencarian (misal: "nugas" → tambah keyword "wifi", "stopkontak", "nyaman").
- **Synonym Normalization**: Mengenali sinonim dan kata gaul (misal: "cina" → "chinese food", "kafe" → "kafe/kedai kopi").
- **Hybrid Recommendation**: Kombinasi strict mode (kategori spesifik) dan flexible mode (TF-IDF scoring).
- **Match Percentage**: Menampilkan persentase kecocokan untuk setiap rekomendasi.

### 🎨 Antarmuka User-Friendly & Premium
- **Desain Modern**: Font *Plus Jakarta Sans*, glassmorphism effects, dan gradient accent.
- **Tema Dinamis**: 
  - 🌙 **Dark Mode** (default): Elegan dengan gradien biru-ungu
  - ☀️ **Light Mode**: Bersih dengan kontras optimal
  - Toggle instant tanpa reload halaman
- **Fully Responsive**: Tampilan optimal di desktop, tablet, dan mobile
- **Adaptive UI**: Tombol Quick Search otomatis wrapping saat layar sempit
- **Smooth Animations**: Transisi halus dan micro-interactions

### 🚀 Fitur Interaktif

#### Pencarian & Navigasi
- **Pencarian Cepat**: 4 tombol pintas untuk kategori populer (Kopi Murah, Ramen Pedas, Masakan Sunda, Toko Roti)
- **Dual Search Form**: Form pencarian di atas dan bawah untuk kemudahan akses
- **Scroll to Top Button**: Muncul otomatis setelah klik "Lebih Banyak" untuk navigasi cepat ke atas halaman
- **Load More**: Sistem pagination dengan tombol "Lebih Banyak" untuk menampilkan hasil bertahap

#### Sidebar Informatif
- **Statistik Real-time**: Total UMKM dengan status database aktif
- **Filter Preferensi**: Collapsible expander untuk filter harga (Murah/Sedang/Mahal)
- **Filter Kategori**: Pilihan kategori kuliner yang dapat di-collapse
- **Tips Pencarian**: Panduan penggunaan dengan ikon visual

#### Integrasi Eksternal
- **Google Maps Integration**: Setiap rekomendasi dilengkapi tombol "Lihat Lokasi di Google Maps"
- **Direct Navigation**: Klik sekali langsung membuka Google Maps dengan lokasi yang tepat

### 📊 Informasi Lengkap Setiap Rekomendasi
- Nama Rumah Makan dengan ikon kategori
- Badge persentase kecocokan
- Alamat lengkap
- Kategori kuliner
- Range harga dan kategori harga
- Menu unggulan
- Deskripsi tempat
- Tombol aksi Google Maps

---

## 🛠️ Teknologi yang Digunakan

### Backend & Machine Learning
- **Python 3.9+**: Bahasa pemrograman utama
- **Scikit-learn**: TF-IDF Vectorizer & Cosine Similarity
- **Pandas**: Data manipulation dan processing
- **NLTK + Sastrawi**: Text preprocessing dan stemming Bahasa Indonesia
- **Difflib**: Fuzzy matching untuk auto-correct typo

### Frontend & UI/UX
- **Streamlit**: Framework web app interaktif
- **Custom CSS3**: 
  - CSS Variables untuk dynamic theming
  - Flexbox & Grid untuk responsive layout
  - Glassmorphism & gradient effects
  - Smooth transitions & animations
- **Font Awesome 6**: Icon library
- **Google Fonts**: Plus Jakarta Sans typography

### Features & Integrations
- **Session State Management**: Persistent chat history dan preferences
- **Google Maps API**: URL generation untuk location viewing
- **Base64 Encoding**: Local image handling untuk icon display

---

## 📦 Cara Menjalankan Proyek

### 1. Prasyarat
Pastikan Anda sudah menginstal:
- **Python 3.9+** ([Download di python.org](https://www.python.org/))
- **pip** (package manager Python)

### 2. Clone Repository
```bash
git clone <repository-url>
cd chatbot-kuliner
```

### 3. Instal Dependensi
```bash
pip install -r requirements.txt
```

**Dependencies yang dibutuhkan:**
- streamlit
- pandas
- scikit-learn
- nltk
- sastrawi

### 4. Jalankan Aplikasi
```bash
streamlit run app.py
```

Aplikasi akan otomatis terbuka di browser pada `http://localhost:8501`

---

## 📁 Struktur Proyek

```
chatbot-kuliner/
├── app.py                          # File utama aplikasi Streamlit
│                                   # (UI, interaksi user, session management)
│
├── chatbot_engine.py               # Engine chatbot (TF-IDF, Cosine Similarity)
│                                   # (Logika rekomendasi, scoring, filtering)
│
├── preprocessing.py                # Text preprocessing utilities
│                                   # (Stemming, stopword removal, cleaning)
│
├── dataset/
│   └── data-kuliner-umkm-optimized.csv  # Dataset UMKM Kota Bandung
│                                        # (Pre-processed dengan stemming)
│
├── style/
│   ├── app.css                     # Custom styling (Dark/Light mode, responsive)
│   └── icon.png                    # App icon/logo
│
├── requirements.txt                # Python dependencies
└── README.md                       # Dokumentasi proyek (file ini)
```

---

## 🎯 Cara Penggunaan

### Pencarian Dasar
1. Ketik pertanyaan di form pencarian (misal: "kopi murah di dago")
2. Tekan Enter atau klik tombol "Kirim"
3. Lihat rekomendasi yang muncul dengan persentase kecocokan

### Pencarian Cepat
- Klik salah satu dari 4 tombol Quick Search untuk kategori populer
- Sistem otomatis mencari dan menampilkan hasil

### Filter & Preferensi
- Buka sidebar (klik ikon hamburger di kiri atas)
- Pilih filter harga di bagian "PREFERENSI"
- Pilih kategori kuliner di bagian "KATEGORI KULINER"

### Navigasi
- Scroll ke bawah untuk melihat lebih banyak hasil
- Klik "Lebih Banyak" untuk load 5 rekomendasi tambahan
- Tombol "Scroll to Top" akan muncul otomatis untuk kembali ke atas

### Lihat Lokasi
- Klik tombol "Lihat Lokasi di Google Maps" pada setiap kartu rekomendasi
- Browser akan membuka Google Maps dengan lokasi yang tepat

---

## 💡 Tips Pencarian Optimal

- **Spesifik lebih baik**: "kopi murah di dago" > "kopi"
- **Gunakan konteks**: "tempat nugas wifi" akan otomatis mencari cafe dengan WiFi
- **Kombinasi filter**: "chinese food murah romantis"
- **Typo OK**: Sistem akan auto-correct kesalahan ketik
- **Bahasa gaul**: "cina", "kafe", "ngopi" akan dipahami dengan benar

---

## 🔧 Catatan Teknis

### Preprocessing Pipeline
1. **Lowercasing**: Semua teks diubah ke huruf kecil
2. **Punctuation Removal**: Hapus tanda baca
3. **Stemming**: Menggunakan Sastrawi untuk Bahasa Indonesia
4. **Stopword Removal**: Hapus kata-kata umum yang tidak informatif

### Recommendation Algorithm
1. **Query Processing**: Normalisasi, auto-correct, semantic expansion
2. **TF-IDF Vectorization**: Konversi teks ke numerical vectors
3. **Cosine Similarity**: Hitung kemiripan query dengan database
4. **Hybrid Scoring**: 
   - Strict mode untuk kategori spesifik
   - Flexible mode dengan boosting (location, price, etc.)
5. **Ranking & Filtering**: Sort by score, filter by threshold

### Theme Management
- CSS Variables (`--text-primary`, `--bg-primary`, dll) untuk dynamic theming
- JavaScript injection untuk instant theme switching
- Persistent theme preference via session state

### Performance Optimization
- `@st.cache_resource` untuk chatbot engine (load once)
- Pre-processed dataset dengan stemming hasil tersimpan
- Lazy loading untuk rekomendasi (pagination dengan "Lebih Banyak")

---

## 📄 Lisensi & Sumber Data

**Data Source**: [Open Data Bandung - Data Rumah Makan, Restoran, Cafe di Kota Bandung](https://opendata.bandung.go.id/dataset/data-rumah-makan-restoran-cafe-di-kota-bandung)

**Dinas**: Dinas Kebudayaan dan Pariwisata Kota Bandung

---

## 👨‍💻 Pengembang

Dikembangkan sebagai proyek pembelajaran Machine Learning dan Web Development dengan fokus pada:
- Natural Language Processing
- Information Retrieval
- User Experience Design
- Responsive Web Development

---

**Selamat mencoba! 🎉**

*Jika ada pertanyaan atau saran, silakan buat issue atau hubungi pengembang.*
