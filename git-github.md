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

## 1. remote

#### update semua branch remote ke lokal

```bash
git fetch --all
```

#### tambahkan branch remote ke branch lokal

```bash
git fetch origin branch_1:branch_1
git checkout branch_1
```

## 2. local

#### lihat branch

```bash
git branch
```

#### buat branch baru

```bash
git branch branch_1
```

#### hapus branch

```bash
git branch -d branch_1
```

`-d` = hanya bisa dihapus kalau sudah merge ke branch lain.

`-D` = paksa hapus walaupun belum merge.

#### pindah ke branch lain

```bash
git checkout branch_1
```

#### merg dari `branch_1` ke `branch_2`

```bash
# pindah ke branch_2
git checkout branch_2

# merge branch yang akan di gabungkan
git merge branch_1
```

#### push `branch_1` ke remote

```bash
git push origin branch_1
```
