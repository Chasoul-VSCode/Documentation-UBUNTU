# Setup Lingkungan Pengembangan Ubuntu

Panduan ini menjelaskan langkah-langkah untuk menyiapkan lingkungan pengembangan di Ubuntu, termasuk menginstal Google Chrome, PHP, Node.js, dan Apache.

## Daftar Isi

- [Prasyarat](#prasyarat)
- [Langkah-langkah Instalasi](#langkah-langkah-instalasi)
  - [1. Update dan Upgrade Sistem](#1-update-dan-upgrade-sistem)
  - [2. Install Google Chrome](#2-install-google-chrome)
  - [3. Install PHP](#3-install-php)
  - [4. Install Node.js](#4-install-nodejs)
  - [5. Install Apache2](#5-install-apache2)
  - [6. Install MySQL (Opsional)](#6-install-mysql-opsional)
  - [7. Install Ekstensi PHP Tambahan (Opsional)](#7-install-ekstensi-php-tambahan-opsional)
  - [8. Restart Apache](#8-restart-apache)
  - [9. Periksa Status Apache](#9-periksa-status-apache)
- [Kesimpulan](#kesimpulan)

## Prasyarat

- Ubuntu terinstal (disarankan versi terbaru).
- Akses ke terminal dengan hak akses `sudo`.

## Langkah-langkah Instalasi

### 1. Update dan Upgrade Sistem

Pertama, buka terminal dan jalankan perintah berikut:

```bash
sudo apt update && sudo apt upgrade -y


2. Install Google Chrome
Untuk menginstal Google Chrome, unduh dan instal dengan perintah berikut:
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt install ./google-chrome-stable_current_amd64.deb


3. Install PHP
Instal PHP dan ekstensi Apache:


sudo apt install php libapache2-mod-php php-mysql
4. Install Node.js
Gunakan NodeSource untuk menginstal Node.js:
curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E  -
sudo apt install -y nodejs

5. Install Apache2
Instal server web Apache2:
sudo apt install apache2


6. Install MySQL (Opsional)
Jika diperlukan, instal MySQL:
sudo apt install mysql-server


7. Install Ekstensi PHP Tambahan (Opsional)
Untuk ekstensi PHP tambahan, jalankan:

sudo apt install php-curl php-xml php-mbstring php-zip

8. Restart Apache
Setelah semua terinstal, restart server Apache:


sudo systemctl restart apache2
9. Periksa Status Apache
Pastikan Apache berjalan dengan baik:


sudo systemctl status apache2
