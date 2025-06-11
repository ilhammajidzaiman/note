# tambahkan repository

```bash
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:ondrej/php
```

# install php

1. install.

```bash
sudo apt-get install php8.4
sudo apt-get install php8.4-fpm
sudo apt-get install php8.4-cli
```

2. jalankan php-fpm.

```bash
sudo systemctl start php8.4-fpm
sudo systemctl enable php8.4-fpm
sudo systemctl status php8.4-fpm
```

3. `restart` nginx.

4. cek versi php

```bash
php -v
```

5. `ubah versi` php-cli

```bash
sudo update-alternatives --config php
```

# extensions

```bash
sudo apt-get install php8.4-fpm
sudo apt-get install php8.4-cli
sudo apt-get install php8.4-xml
sudo apt-get install php8.4-curl
sudo apt-get install php8.4-mbstring
sudo apt-get install php8.4-mysql
sudo apt-get install php8.4-pgsql
sudo apt-get install php8.4-sqlite3
sudo apt-get install php8.4-tokenizer
sudo apt-get install php8.4-zip
sudo apt-get install php8.4-intl
sudo apt-get install php8.4-ctype
sudo apt-get install php8.4-fileinfo
sudo apt-get install php8.4-filter
```

# install dengan paket extensions

```bash
sudo apt-get install php8.4 php8.4-fpm php8.4-cli php8.4-xml php8.4-curl php8.4-mbstring php8.4-mysql php8.4-pgsql php8.4-sqlite3 php8.4-tokenizer php8.4-zip php8.4-intl php8.4-ctype php8.4-fileinfo php8.4-filter
```

# remove semua paket dan pengaturan

```bash
sudo systemctl stop php*-fpm
sudo apt-get remove --purge 'php*'
sudo apt-get autoremove --purge
sudo rm -rf /etc/php
sudo rm -rf /var/lib/php
sudo rm -rf /var/run/php
sudo rm -rf /usr/lib/php
sudo rm -rf /usr/include/php
sudo rm -rf /usr/share/php
sudo nano /etc/nginx/sites-available/default
sudo systemctl restart nginx
```
