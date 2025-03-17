# Instalation

```bash
sudo apt-get install postgresql postgresql-contrib
```

# Cek versi

```bash
psql --version
```

# Setting

```bash
sudo systemctl start postgresql.service
```

```bash
sudo systemctl status postgresql
```

```bash
sudo systemctl enable postgresql
```

```bash
sudo -u postgres createuser -P namapengguna
```

```bash
sudo -u postgres createdb -O namapengguna namadatabase
```

```bash
sudo systemctl start postgresql
sudo systemctl stop postgresql
sudo systemctl restart postgresql
```

# Dokumentasi

```bash
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-22-04
```
