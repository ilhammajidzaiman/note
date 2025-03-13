# Instalation

```bash
sudo apt update
sudo apt install nginx
```

# Setting Firewall

```bash
sudo ufw app list

sudo ufw enable
```

# Checking Web Server

```bash
systemctl status nginx
```

# Managing the Nginx Process

```bash
sudo systemctl stop nginx
sudo systemctl start nginx
sudo systemctl restart nginx
sudo systemctl reload nginx
sudo systemctl disable nginx
sudo systemctl enable nginx
```

# Setting Up Server Blocks

```bash
sudo mkdir -p /var/www/your_domain/html
```

```bash
sudo chown -R $USER:$USER /var/www/your_domain/html
```

```bash
sudo chmod -R 755 /var/www/your_domain
```

```bash
nano /var/www/your_domain/html/index.html
```

```bash
sudo nano /etc/nginx/sites-available/your_domain
```

```bash
sudo ln -s /etc/nginx/sites-available/your_domain /etc/nginx/sites-enabled/
```

```bash
sudo nginx -t

sudo systemctl restart nginx
```
