# 413 Request Entity Too Large

```base
413 Request Entity Too Large
nginx/1.24.0 (Ubuntu)
```

Terjadi ketika server menolak permintaan karena ukuran konten upload melebihi batas yang telah ditentukan. Biasanya disebabkan oleh:

- `Konfigurasi Nginx`: Parameter client_max_body_size terlalu kecil.

- `Konfigurasi PHP`: Parameter upload_max_filesize atau post_max_size di file php.ini terlalu kecil.

# <u>Konfigurasi Nginx</u>

Tambahkan atau sesuaikan parameter jika konfigurasi secara `Global` atau hanya untuk `Per-situs`.

### Global: `/etc/nginx/nginx.conf`

```base
http {
    client_max_body_size 20M;
}
```

### Per-situs: `/etc/nginx/sites-available/<nama_situs>`

```base
server {
    client_max_body_size 20M;
}
```

### Restart Nginx

Simpan perubahan, `restart` Nginx.

```base
sudo systemctl restart nginx
#atau
sudo service nginx restart
```

# <u>Konfigurasi PHP</u>

PHP memiliki batasan bawaan untuk ukuran file upload. Suaikan parameter `upload_max_filesize` dan `post_max_size`.

### Konfigurasi File `php.ini`

sesuaikan dengan versi PHP Anda

- `/etc/php/8.3/fpm/php.ini`

- `/etc/php/8.3/cli/php.ini`

Edit file `php.ini` dan sesuaikan nilainya:

```base
upload_max_filesize = 20M
post_max_size = 20M
```

<u>Catatan</u>: Nilai `post_max_size` harus sama atau lebih besar dari `upload_max_filesize`.

### Restart PHP-FPM

Simpan perubahan, `restart` php-fpm.

```base
sudo systemctl restart php8.3-fpm
```
