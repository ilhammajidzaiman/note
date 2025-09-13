# git / github

`cek` username dan email yang sedang digunakan.

```bash
git config --global user.name
git config --global user.email
```

`set` username dan email

```bash
git config --global user.name "username"
git config --global user.email "email@example.com"
```

menyimpan `github token`

```bash
git config --global credential.helper store
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
# how to

### update semua branch remote ke lokal

```bash
git fetch --all
```