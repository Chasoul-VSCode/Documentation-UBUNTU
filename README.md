# Setup Pack Linux by chasoul
installer FLutter - Laravel, xamppp, and connect to database

## List Pack Programming Setup
FUll Setup? instagram : chasoul.uix

- [Prasyarat](#prasyarat)
- [Langkah-langkah Instalasi](#langkah-langkah-instalasi)
  - [1. Update dan Upgrade Sistem](#1-update-dan-upgrade-sistem)
  - [2. Install Google Chrome](#2-install-google-chrome)
  - [3. Install PHP](#3-install-php)
  - [4. Install Node.js](#4-install-nodejs)
  - [5. Install Apache2](#5-install-apache2)
  - [6. Install NPM](#5-install-apache2)
  - [7. Install composer](#5-install-apache2)
  - [8. Install MySQL (Opsional)](#6-install-mysql-opsional)
  - [9. Install SQLITE3](#6-install-mysql-opsional)
  - [10. Install FLutter SDK](#6-install-mysql-opsional)
  - [11. Install Android Studio](#6-install-mysql-opsional)
  - [12. Install Ekstensi PHP Tambahan (Opsional)](#7-install-ekstensi-php-tambahan-opsional)
  - [13. Restart Apache](#8-restart-apache)
  - [14. Periksa Status Apache](#9-periksa-status-apache)
  - [15. Periksa Android Studio Permision](#9-periksa-status-apache)
- [PLaylist Content](#prasyarat)
    - [1. Linux Installation with chasoul.uix ](#9-periksa-status-apache)

## Langkah-langkah Instalasi

Pertama, buka terminal dan jalankan perintah berikut:

```bash
# Upgrade System
sudo apt update && sudo apt upgrade -y
sudo apt update

# Install new PHP 8.3 packages
sudo dpkg -l | grep php | tee packages.txt
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php8.3 php8.3-cli php8.3-{bz2,curl,mbstring,intl}
sudo apt install php8.3-fpm
sudo a2enconf php8.3-fpm
php -v

# Install node js
sudo apt-get install -y curl
curl -fsSL https://deb.nodesource.com/setup_22.x -o nodesource_setup.sh
sudo -E bash nodesource_setup.sh
sudo apt-get install -y nodejs
node -v

# Install Apache2
sudo apt update
sudo apt install apache2
sudo systemctl status apache2

# Install NPM
sudo apt install nodejs npm
ln -s /usr/bin/nodejs /usr/bin/node
node --version
npm --version

# Install composer
sudo apt update
sudo apt install php-cli unzip
cd ~
curl -sS https://getcomposer.org/installer -o /tmp/composer-setup.php
HASH=`curl -sS https://composer.github.io/installer.sig`
echo $HASH
php -r "if (hash_file('SHA384', '/tmp/composer-setup.php') === '$HASH') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
sudo php /tmp/composer-setup.php --install-dir=/usr/local/bin --filename=composer

# Install SQLITE3
sudo apt update
sudo apt install sqlite3
sqlite3 --version

# Laravel INstallation
composer create-project laravel/laravel example-app
