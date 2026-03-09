# Update depedency

### composer

all dependency:

```bash
composer audit
composer update
```

specific dependency:

```bash
composer audit --format=table
composer update --with-all-dependencies
composer show spatie/browsershot
composer require spatie/browsershot:^5.0.5
```

### npm

all dependency:

```bash
npm audit
npm audit fix
# or
npm update
```

specific dependency:

```bash
npm install tar@latest
```

# Fix hdd partition system format

for NTFS:

```bash
sudo ntfsfix -d /dev/sda1
```

for FAT32/exFAT:

```bash
sudo fsck.vfat -a /dev/sda1
```
