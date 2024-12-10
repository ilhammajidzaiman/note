# Maximum Execution Time

### Konfigurasi maximum execution time:

```bash
# php-fpm:
/etc/php/8.3/fpm/php.ini

# php-cli:
/etc/php/8.3/cli/php.ini
```

### Ubah nilai konfigurasi:

```bash
max_execution_time = 30
```

### Restart servis:

```bash
sudo systemctl restart php8.3-fpm
sudo systemctl restart nginx
```
