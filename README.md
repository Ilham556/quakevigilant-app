# 🌍 QuakeVigilant: Sistem Monitoring & Edukasi Gempa Bumi

![Banner Project](https://via.placeholder.com/1000x300?text=QuakeVigilant+Dashboard)

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Framework-Streamlit-red?logo=streamlit)](https://streamlit.io/)
[![Database](https://img.shields.io/badge/Database-MySQL-orange?logo=mysql)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

> **QuakeVigilant** adalah aplikasi berbasis web yang dirancang untuk memantau aktivitas seismik secara *real-time* menggunakan data USGS, menganalisis pola gempa melalui visualisasi data interaktif, dan menyediakan platform edukasi kebencanaan.

---

## 📑 Daftar Isi
- [📖 Tentang Proyek](#-tentang-proyek)
- [✨ Fitur Utama](#-fitur-utama)
- [🏗️ Arsitektur Sistem](#️-arsitektur-sistem)
- [🛠️ Teknologi yang Digunakan](#️-teknologi-yang-digunakan)
- [🚀 Instalasi & Konfigurasi](#-instalasi--konfigurasi)
- [📂 Konfigurasi Database](#-konfigurasi-database)
- [📱 Penggunaan](#-penggunaan)

---

## 📖 Tentang Proyek

Indonesia berada di kawasan *Ring of Fire* yang rawan gempa. **QuakeVigilant** hadir sebagai solusi pemantauan yang mengintegrasikan:
1.  **Data Real-time**: Mengambil data gempa bumi terkini langsung dari API USGS (United States Geological Survey).
2.  **Analisis Visual**: Menampilkan sebaran gempa dalam bentuk Peta Interaktif, Heatmap, dan Grafik Statistik.
3.  **Manajemen Informasi**: Sistem admin untuk mengelola artikel edukasi dan data pengguna.

Aplikasi ini dibangun menggunakan pola desain **MVC (Model-View-Controller)** untuk memastikan kode yang bersih, terstruktur, dan mudah dikembangkan.

---

## ✨ Fitur Utama

### 1. 🌏 Monitoring Seismik (USGS Integration)
* **Real-time Feed**: Mengambil data gempa mingguan terbaru secara otomatis dari API USGS.
* **Filter Cerdas**: Memfilter data berdasarkan magnitudo, kedalaman, dan lokasi (fokus wilayah Indonesia).
* **Interaktif Map**: Visualisasi titik gempa dengan detail kedalaman dan kekuatan.

### 2. 📊 Analisis Data & Heatmap
* **Heatmap Visualization**: Memetakan densitas kejadian gempa untuk mengidentifikasi zona rawan.
* **Statistik Temporal**: Grafik tren kejadian gempa berdasarkan waktu (Pagi, Siang, Malam), musim, dan kategori kekuatan.
* **Klasifikasi Otomatis**: Pengelompokan gempa (Micro, Minor, Light, s.d. Major) dan kedalaman (Shallow, Intermediate, Deep).

### 3. 📝 Manajemen Artikel & Edukasi
* **CRUD System**: Admin dapat Membuat, Membaca, Memperbarui, dan Menghapus artikel edukasi gempa.
* **Integrasi Multimedia**: Mendukung link gambar dan video untuk konten edukasi.

### 4. 🔐 Sistem Autentikasi & User
* **Multi-Role Access**: Login aman untuk Admin dan User biasa.
* **Manajemen Profil**: Pengguna dapat memperbarui data profil mereka sendiri.

---

## 🏗️ Arsitektur Sistem

Proyek ini menerapkan **Design Pattern MVC**:

* **Model (`model.py`)**: Menangani logika bisnis, koneksi database MySQL, pengambilan data API USGS, dan pemrosesan data (Pandas).
* **View (`view.py`)**: Menangani antarmuka pengguna (UI) menggunakan Streamlit (File View dipanggil oleh Controller).
* **Controller (`controller.py`)**: Menghubungkan Model dan View, menangani input pengguna, dan logika navigasi.
* **Main (`main.py`)**: Titik masuk aplikasi yang menginisialisasi seluruh komponen.

---

## 🛠️ Teknologi yang Digunakan

* **Bahasa**: Python
* **Framework Web**: Streamlit
* **Data Processing**: Pandas, NumPy
* **Database**: MySQL (dengan konektor `mysql-connector-python`)
* **API Eksternal**: USGS Earthquake API
* **Visualisasi**: Plotly (via Streamlit), Folium (opsional/inferred)

---

## 🚀 Instalasi & Konfigurasi

Ikuti langkah berikut untuk menjalankan aplikasi di lokal komputer Anda:

### 1. Clone Repositori
```bash
git clone [https://github.com/Ilham556/quakevigilant-app.git](https://github.com/Ilham556/quakevigilant-app.git)
cd quakevigilant-app
