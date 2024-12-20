# <u>Revese Nginx</u>

Konfigurasi webserver nginx di `ubuntu`

### Cek izin:

```bash
ls -la
```

### Ubah kepemilikan:

##### cara 1

```bash
sudo chown -R $(whoami):$(whoami) /var/www/project
```

##### cara 2
```bash
sudo chown -R $USER:$USER /var/www/project
```

### Ubah izin:

```bash
sudo chmod -R 775 /var/www/project
```

# <u>Memberikan akses ke git terhadap direktori</u>

### Hapus files `lock`:

```bash
rm -f .git/index.lock
```

### Reset commit `terakhir`:

```bash
git reset --hard HEAD
```

### Restart servis:

```bash
sudo nginx -t
sudo service nginx restart
```
