# Project N8N - Google Drive dan Sheet

Project untuk membantu industri menggunakan AI workflow dengan n8n, terintegrasi dengan Google Drive dan Google Sheet.

## 📋 Deskripsi Project

Project ini merupakan solusi workflow automation yang dirancang untuk membantu industri dalam:

- **Otomatisasi Proses Bisnis**: Menggunakan n8n untuk mengotomatisasi tugas-tugas repetitif
- **Integrasi Google Drive**: Mengelola file dan dokumen secara otomatis
- **Integrasi Google Sheet**: Memproses dan mengelola data spreadsheet secara efisien
- **AI Workflow**: Memanfaatkan kecerdasan buatan untuk meningkatkan produktivitas

## 🎯 Manfaat untuk Industri

1. **Efisiensi Waktu**: Menghemat waktu dengan mengotomatisasi tugas manual
2. **Pengurangan Human Error**: Meminimalkan kesalahan manusia dalam proses bisnis
3. **Skalabilitas**: Mudah dikembangkan sesuai kebutuhan bisnis
4. **Integrasi Mudah**: Dapat terhubung dengan berbagai aplikasi dan layanan
5. **Cost-Effective**: Solusi open-source yang hemat biaya

## 🛠️ Cara Instalasi n8n

### Metode 1: Menggunakan NPM

```bash
# Instalasi global menggunakan npm
npm install n8n -g

# Jalankan n8n
n8n start
```

### Metode 2: Menggunakan Docker

```bash
# Pull image n8n dari Docker Hub
docker pull n8nio/n8n

# Jalankan n8n dengan Docker
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
```

### Metode 3: Menggunakan Docker Compose

Buat file `docker-compose.yml`:

```yaml
version: "3.8"

services:
  n8n:
    image: n8nio/n8n
    restart: always
    ports:
      - "5678:5678"
    volumes:
      - ~/.n8n:/home/node/.n8n
    environment:
      - N8N_BASIC_AUTH_ACTIVE=true
      - N8N_BASIC_AUTH_USER=admin
      - N8N_BASIC_AUTH_PASSWORD=your_secure_password_here  # Ganti dengan password yang kuat
```

> ⚠️ **Penting**: Pastikan untuk mengganti `your_secure_password_here` dengan password yang kuat dan aman sebelum menjalankan di environment production.

Jalankan dengan:

```bash
docker-compose up -d
```

### Akses n8n

Setelah instalasi, buka browser dan akses:

```
http://localhost:5678
```

## 🔧 Konfigurasi Integrasi

### Google Drive

1. Buka Google Cloud Console
2. Buat project baru atau pilih project yang ada
3. Aktifkan Google Drive API
4. Buat OAuth 2.0 credentials
5. Masukkan credentials di n8n

### Google Sheet

1. Aktifkan Google Sheets API di Google Cloud Console
2. Gunakan credentials yang sama dengan Google Drive
3. Konfigurasikan node Google Sheets di n8n

## 📚 Dokumentasi Tambahan

- [Dokumentasi Resmi n8n](https://docs.n8n.io/)
- [Google Drive API](https://developers.google.com/drive)
- [Google Sheets API](https://developers.google.com/sheets)

## 🤝 Kontribusi

Kontribusi sangat diterima! Silakan buat pull request atau buka issue untuk diskusi.

## 📄 Lisensi

Project ini bersifat open-source.
