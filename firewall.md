# firewall

### Cek status firewall aktif

```bash
sudo ufw status
sudo ufw status numbered
```

```bash
sudo ufw enable
sudo ufw reload
sudo ufw app list
sudo ufw allow 'nginx http'
```

### Tambahkan port

```bash
sudo ufw allow 8025
sudo ufw allow 8025/tcp
sudo ufw allow 8000:9000/tcp
```

### Hapus port

```bash
sudo ufw delete allow 8025
sudo ufw delete allow 8025/tcp
sudo ufw delete allow 8000:9000/tcp
```
