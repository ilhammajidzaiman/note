# install

1. cari setting `windows feature on or off` kemudian ceklist.

   - ✅ virtual machine platform
   - ✅ windows sub system for linux

2. `restart` pc

3. cek status wsl

```bash
wsl --status
```

4. cek versi wsl

```bash
wsl --version
```

5. update wsl

```bash
wsl --update
```

6. buka `microsoft store`.

7. cari `ubuntu` sesuai dengan versi yang dinginkan kemudian `get`.

# uninstall

1. lihat daftar yang terinstal.

```bash
wsl --list --verbose
```

2. menghapus daftar.

```bash
wsl --unregister Ubuntu-24.04
```

# reset dari settings

1. buka `Settings>Apps>Installed Apps`.

2. cari `Ubuntu` 24.04.

3. klik opsi advanced options.

4. tekan `reset` (akan menghapus semua data WSL Ubuntu dan mengembalikannya ke kondisi awal).

5. `restart` Ubuntu dari start menu.
