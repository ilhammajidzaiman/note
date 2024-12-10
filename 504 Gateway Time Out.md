# 504 Gateway Time Out

Konfigurasi pada virtual host/Server block

### Path Virtual host/Server block:

```bash
/etc/nginx/sites-available/
```

### Kode konfigurasi:

```bash
server {
    ...
    #504 gateway timeout
    proxy_connect_timeout 3000;
    proxy_read_timeout 3000;
    proxy_send_timeout 3000;
    fastcgi_read_timeout 3000;
    ...

    location ~ \.php$ {
        ...
        # timeout php-fpm
        fastcgi_connect_timeout 3000;
        fastcgi_send_timeout 3000;
        fastcgi_read_timeout 3000;
        ...
    }
}
```

### Restart servis:

```bash
sudo nginx -t
sudo service nginx restart
```
