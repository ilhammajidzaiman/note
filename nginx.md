# instalasi

```bash
sudo apt-get install nginx
```

# firewall

```bash
sudo ufw status
sudo ufw enable
sudo ufw app list
sudo ufw allow 'nginx http'
```

# command

```bash
sudo systemctl status nginx
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl reload nginx
sudo systemctl enable nginx
sudo systemctl disable nginx
```

# server blocks

1. masuk kedirektori.

```bash
cd /etc/nginx/sites-available/your_domain
```

2. buat symbolic link.

```bash
sudo ln -s /etc/nginx/sites-available/your_domain /etc/nginx/sites-enabled/
```

3. cek status.

```bash
sudo nginx -t
```

4. `restart` nginx.

# project

directori project nginx di ubuntu `/var/www/`.

1. cek izin.

```bash
ls -la
```

2. ubah kepemilikan.

```bash
# cara 1
sudo chown -R $(whoami):$(whoami) /var/www/project

# cara 2
sudo chown -R $USER:$USER /var/www/project

# cara 3
chown -R www-data:www-data /var/www/project
```

3. ubah izin direktori.

```bash
# bisa semua path
sudo chmod -R 775 /var/www/project

# atau khusus storage
sudo chmod -R 775 /var/www/project/storage
```

# memberikan akses ke git terhadap direktori

1. hapus files `lock`.

```bash
rm -f .git/index.lock
```

2. `reset` commit terakhir.

```bash
git reset --hard HEAD
```

3. `restart` nginx.
