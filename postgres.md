# Instalation

```bash
sudo apt install postgresql postgresql-contrib
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
sudo systemctl start postgresql
```

```bash
sudo -u postgres createuser -P namapengguna
```

```bash
sudo -u postgres createdb -O namapengguna namadatabase
```

```bash
sudo systemctl restart postgresql
```
