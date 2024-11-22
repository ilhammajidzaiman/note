# Nginx Revese

### Cek Permissions

```bash
ls -la
```

### Ubah Permissions

```bash
sudo chown -R $(whoami):$(whoami) .
```

```bash
sudo chown -R $USER:$USER /var/www/project
```

```bash
sudo chmod -R 775 /var/www/project
```

```bash
sudo chmod -R 777 /var/www/project
```

```bash
sudo chown -R www-data:www-data /var/www/project
```

```bash
sudo chown -R username:username /var/www/project
```

### Hapus files `.lock`.

```bash
rm -f .git/index.lock
```

### Reset commit `terakhir`.

```bash
git reset --hard HEAD
```

### Use git stash

If you have uncommitted changes that you want to keep, you can stash them before pulling:

```bash
sudo git stash
sudo git pull
sudo git stash pop
```

### Restart Your Machine

```bash
sudo nginx -t
sudo service nginx restart
```
