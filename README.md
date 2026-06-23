# Viola Kasir - Sistem Kasir Web

Sistem kasir modern untuk restoran dan cafe yang dapat digunakan sebagai Progressive Web App (PWA) tanpa perlu server lokal seperti XAMPP.

## 🚀 Cara Menggunakan Tanpa XAMPP

### Opsi 1: Deploy ke Hosting Gratis (Rekomendasi)

#### 1. GitHub Pages (Gratis & Mudah)

**Langkah-langkah:**
1. Buat akun GitHub di https://github.com
2. Buat repository baru dengan nama `viola-kasir`
3. Upload semua file dari folder `Viola_kasir` ke repository
4. Masuk ke Settings → Pages
5. Pilih branch `main` dan folder `root`
6. Klik Save
7. Tunggu beberapa menit, aplikasi akan tersedia di `https://username.github.io/viola-kasir`

#### 2. Netlify Drop (Gratis & Sangat Mudah)

**Langkah-langkah:**
1. Buka https://app.netlify.com/drop
2. Drag & drop folder `Viola_kasir` ke area upload
3. Tunggu proses upload selesai
4. Aplikasi akan langsung tersedia dengan URL random
5. Bisa rename URL menjadi custom di dashboard Netlify

#### 3. Vercel (Gratis & Profesional)

**Langkah-langkah:**
1. Install Vercel CLI: `npm i -g vercel`
2. Buka terminal di folder `Viola_kasir`
3. Jalankan: `vercel`
4. Ikuti instruksi di terminal
5. Aplikasi akan deploy ke Vercel dengan URL gratis

### Opsi 2: Install sebagai PWA di Mobile

**Android:**
1. Buka aplikasi di browser (Chrome)
2. Tunggu prompt "Add to Home Screen"
3. Klik "Add"
4. Aplikasi akan muncul di home screen seperti native app

**iOS:**
1. Buka aplikasi di browser (Safari)
2. Tap tombol Share
3. Pilih "Add to Home Screen"
4. Tap "Add"
5. Aplikasi akan muncul di home screen

### Opsi 3: Convert ke APK (Advanced)

**Menggunakan Capacitor:**

```bash
# Install Capacitor
npm install @capacitor/core @capacitor/cli @capacitor/android

# Initialize
npx cap init ViolaKasir com.viola.kasir

# Build web app
npx cap add android

# Copy web assets
npx cap sync

# Open Android Studio
npx cap open android
```

**Menggunakan Cordova:**

```bash
# Install Cordova
npm install -g cordova

# Create project
cordova create viola-kasir com.viola.kasir ViolaKasir

# Add platform
cd viola-kasir
cordova platform add android

# Copy web files to www folder
# Build
cordova build android
```

## 📱 Fitur PWA

- ✅ Install ke home screen seperti native app
- ✅ Offline capability (bisa digunakan tanpa internet)
- ✅ Push notifications (opsional)
- ✅ Full screen mode
- ✅ Auto-update
- ✅ Data tersimpan di localStorage

## 🌐 Hosting Gratis yang Direkomendasikan

1. **GitHub Pages** - Gratis, unlimited bandwidth, GitHub integration
2. **Netlify** - Gratis, drag & drop deployment, custom domain
3. **Vercel** - Gratis, fast CDN, automatic SSL
4. **Firebase Hosting** - Gratis 10GB transfer, fast performance
5. **Cloudflare Pages** - Gratis, unlimited bandwidth, global CDN

## 🔧 Konfigurasi

### Manifest.json
File ini mengatur tampilan app saat diinstall:
- Icon app
- Warna tema
- Orientation (portrait/landscape)
- Start URL

### Service Worker
Mengaktifkan offline capability dan caching:
- Cache semua file statis
- Serve dari cache saat offline
- Auto-update cache saat ada perubahan

## 📦 Struktur File

```
Viola_kasir/
├── index.html          # Halaman utama
├── style.css           # Styling
├── script.js           # Logic aplikasi
├── manifest.json       # PWA manifest
├── service-worker.js   # Service worker untuk offline
└── README.md          # Panduan ini
```

## 💾 Data Storage

Semua data tersimpan di localStorage browser:
- Keranjang belanja
- Daftar produk
- Data pelanggan
- Riwayat penjualan
- Pengaturan

Data akan tetap tersimpan meskipun browser ditutup atau device restart.

## 🎯 Keuntungan PWA vs Native App

| PWA | Native App |
|-----|------------|
| Gratis deploy | Perlu bayar developer account |
| Cross-platform | Perlu develop per platform |
| Auto-update | Perlu update manual |
| Ukuran kecil | Ukuran besar |
| Instant loading | Perlu install |

## 📞 Support

Jika mengalami masalah:
1. Pastikan browser mendukung PWA (Chrome, Safari, Edge)
2. Clear cache browser jika ada masalah loading
3. Pastikan semua file sudah terupload dengan benar
4. Cek console browser untuk error message

## 🔐 Keamanan

- Data tersimpan lokal di device user
- Tidak ada koneksi ke server eksternal
- Tidak perlu database server
- 100% client-side application

## 📝 Catatan Penting

1. **Backup Data**: Data di localStorage bisa hilang jika browser cache dihapus
2. **Export/Import**: Gunakan fitur export CSV untuk backup data
3. **Testing**: Test di multiple device sebelum production
4. **Browser Support**: Gunakan browser modern (Chrome, Safari, Edge)

## 🎉 Selamat Menggunakan!

Sistem kasir Viola siap digunakan tanpa XAMPP. Deploy ke hosting gratis dan install sebagai PWA di mobile device Anda.
