# Sintak Git

Panduan singkat perintah Git yang umum digunakan sehari-hari.

------------------------------------------------------------------------

## 1. Konfigurasi

### Fungsi

Mengatur identitas pengguna.

**Sintaks**

``` bash
git config --global user.name "Nama"
git config --global user.email "email@example.com"
```

**Contoh**

``` bash
git config --global user.name "Arip"
git config --global user.email "arip@example.com"
```

------------------------------------------------------------------------

## 2. Membuat Repository

### Fungsi

Membuat repository Git baru.

``` bash
git init
```

Contoh:

``` bash
mkdir project
cd project
git init
```

------------------------------------------------------------------------

## 3. Clone Repository

### Fungsi

Mengunduh repository.

``` bash
git clone <url>
```

Contoh:

``` bash
git clone https://github.com/user/project.git
```

------------------------------------------------------------------------

## 4. Melihat Status

``` bash
git status
```

Menampilkan perubahan file.

------------------------------------------------------------------------

## 5. Menambahkan File

Semua file:

``` bash
git add .
```

Satu file:

``` bash
git add app.js
```

------------------------------------------------------------------------

## 6. Commit

``` bash
git commit -m "Pesan commit"
```

Contoh:

``` bash
git commit -m "Add login feature"
```

------------------------------------------------------------------------

## 7. Riwayat Commit

``` bash
git log
git log --oneline
```

------------------------------------------------------------------------

## 8. Melihat Perubahan

``` bash
git diff
git diff --staged
```

------------------------------------------------------------------------

## 9. Branch

Lihat branch:

``` bash
git branch
```

Buat branch:

``` bash
git branch feature-login
```

Hapus:

``` bash
git branch -d feature-login
```

------------------------------------------------------------------------

## 10. Pindah Branch

``` bash
git switch main
git switch -c feature-api
```

Alternatif lama:

``` bash
git checkout main
```

------------------------------------------------------------------------

## 11. Merge

``` bash
git merge feature-login
```

------------------------------------------------------------------------

## 12. Remote

Lihat remote:

``` bash
git remote -v
```

Tambah remote:

``` bash
git remote add origin https://github.com/user/project.git
```

------------------------------------------------------------------------

## 13. Push

Push pertama:

``` bash
git push -u origin main
```

Push berikutnya:

``` bash
git push
```

------------------------------------------------------------------------

## 14. Pull

``` bash
git pull
```

------------------------------------------------------------------------

## 15. Fetch

``` bash
git fetch
```

------------------------------------------------------------------------

## 16. Restore

Batalkan perubahan file:

``` bash
git restore app.js
```

Unstage:

``` bash
git restore --staged app.js
```

------------------------------------------------------------------------

## 17. Reset

Batalkan commit terakhir tetapi simpan perubahan:

``` bash
git reset --soft HEAD~1
```

Hapus commit dan perubahan:

``` bash
git reset --hard HEAD~1
```

------------------------------------------------------------------------

## 18. Stash

Simpan sementara:

``` bash
git stash
```

Lihat daftar:

``` bash
git stash list
```

Kembalikan:

``` bash
git stash pop
```

------------------------------------------------------------------------

## 19. Tag

Buat tag:

``` bash
git tag v1.0.0
```

Push tag:

``` bash
git push origin v1.0.0
```

------------------------------------------------------------------------

# Workflow Harian

``` text
git clone
↓
git switch -c feature
↓
Edit file
↓
git status
↓
git add .
↓
git commit -m "Message"
↓
git push
↓
Pull Request / Merge
```

# Cheatsheet

  Perintah      Fungsi
  ------------- -------------------------------
  git init      Membuat repository
  git clone     Mengunduh repository
  git status    Melihat status
  git add       Menambahkan file ke staging
  git commit    Menyimpan perubahan
  git log       Riwayat commit
  git diff      Melihat perubahan
  git branch    Mengelola branch
  git switch    Pindah branch
  git merge     Menggabungkan branch
  git remote    Mengelola remote
  git push      Mengirim commit
  git pull      Mengambil perubahan terbaru
  git fetch     Mengambil update tanpa merge
  git restore   Membatalkan perubahan
  git reset     Reset commit
  git stash     Menyimpan perubahan sementara
  git tag       Memberi versi rilis
