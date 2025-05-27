# Install banyak versi

```bash
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:ondrej/php
```

### install versi 8.3 dengan paket

```bash
sudo apt-get install php8.3 php8.3-fpm php8.3-cli php8.3-mysql php8.3-xml php8.3-curl php8.3-mbstring
```

### jalankan php-fpm 8.3

```bash
sudo systemctl start php8.3-fpm
sudo systemctl enable php8.3-fpm
sudo systemctl status php8.3-fpm
```

### restart nginx

```bash
sudo systemctl reload nginx
```

### cek versi php

```bash
php -v
```

### ubah versi php-cli

```bash
sudo update-alternatives --install /usr/bin/php php /usr/bin/php8.3 83
sudo update-alternatives --config php
```

# PHP extensions

```bash
sudo apt-get install php-ctype
```

```bash
sudo apt-get install php-curl
```

```bash
sudo apt-get install php-xml
```

```bash
sudo apt-get install php-fileinfo
```

```bash
sudo apt-get install php-filter
```

```bash
sudo apt-get install php-mbstring
```

```bash
sudo apt-get install php-tokenizer
```

```bash
sudo apt-get install php-intl
```

```bash
sudo apt-get install php-xml
```

```bash
sudo apt-get install php-gd
```

```bash
# untuk mysql
sudo apt-get install php-mysql

# untuk postgres
sudo apt-get install php-pgsql

# untuk sqlite
sudo apt-get install php-sqlite3
```

### remove all package and config

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
