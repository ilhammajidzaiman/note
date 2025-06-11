# instalasi

1. install paket.

```bash
sudo apt-get install Postgresql Postgresql-contrib
```

2. cek versi.

```bash
psql --version
```

3. command.

```bash
sudo systemctl status Postgresql
sudo systemctl start Postgresql
sudo systemctl stop Postgresql
sudo systemctl enable Postgresql
sudo systemctl restart Postgresql
```

# setting user

1. akses user postgres.

```bash
sudo -i -u postgres
psql
```

2. setelah masuk ke PostgreSQL, masukkan password baru untuk user postgres.

```bash
\password postgres
```

3. buat user baru.

```bash
CREATE USER postgres WITH PASSWORD 'postgres';
```

4. hati-hati, Kalau ingin memberi hak superuser (opsional).

```bash
ALTER USER postgres WITH SUPERUSER;
```

# reset password

1. login sebagai user sistem postgres.

```bash
sudo -i -u postgres
```

2. masuk ke PostgreSQL.

```bash
psql
```

3. Jalankan perintah untuk mengubah password.

```bash
ALTER USER postgres WITH PASSWORD 'password_baru';
```

4. keluar dari PostgreSQL.

```bash
\q
```

5.  `restart` PostgreSQL

# remote

1. edit file `postgresql.conf`

```bash
Linux: /etc/Postgresql/<versi>/main/Postgresql.conf

Windows: C:\Program Files\PostgreSQL\<versi>\data\Postgresql.conf
```

2. ubah atau tambahkan baris berikut.

```bash
listen_addresses = '*'
```

3. edit file `pg_hba.conf`

```bash

Linux: /etc/Postgresql/<versi>/main/pg_hba.conf

Windows: C:\Program Files\PostgreSQL\<versi>\data\pg_hba.conf
```

4. tambahkan di akhir file.

```bash
host        all     all     0.0.0.0/0       md5
```

5. `restart` PostgreSQL.

6. buka port firewall.

```bash
sudo ufw allow 5432/tcp
```

7. tes koneksi dari client.

```bash
psql -h <ip_server> -U <username> -d <nama_database>
```

atau gunakan tool GUI seperti `pgAdmin`, `DBeaver`, atau lainnya dengan IP server.

# hapus instalasi

1. `hentikan` layanan PostgreSQL

2. hapus paket PostgreSQL dan dependensinya.

```bash
sudo apt-get --purge remove postgresql*
```

3. hapus direktori data dan konfigurasi (opsional).

```bash
sudo rm -rf /etc/Postgresql
sudo rm -rf /etc/Postgresql-common
sudo rm -rf /var/lib/Postgresql
sudo rm -rf /var/log/Postgresql
sudo rm -rf /var/run/Postgresql
```

4. hapus user dan grup postgres (jika tidak digunakan aplikasi lain).

```bash
sudo deluser postgres
sudo delgroup postgres
```

5. bersihkan paket-paket yang tidak dibutuhkan (opsional).

```bash
sudo apt-get autoremove --purge
```

6. cek apakah PostgreSQL benar-benar sudah hilang. Jika tidak ada output atau psql not found, maka PostgreSQL sudah berhasil dihapus sepenuhnya.

```bash
which psql
```
