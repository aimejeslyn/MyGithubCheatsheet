# Github

Tiga kondisi utama dalam Git: "modified", "staged", dan "committed"

### 1. Modified 
Kondisi "modified" terjadi ketika terdapat perubahan pada file dalam working directory yang belum ditambahkan ke dalam staging area. Ini berarti file telah mengalami modifikasi tetapi belum disimpan ke dalam Git.

Langkah untuk memindahkan file dari kondisi "modified" ke "staged" adalah dengan menambahkan file tersebut ke dalam staging area menggunakan perintah `git add`.

### 2. Staged 
Kondisi "staged" adalah ketika perubahan pada file sudah ditambahkan ke dalam staging area. File-file yang berada di staging area siap untuk dikommit ke dalam repositori.
Langkah untuk memindahkan file dari kondisi "staged" ke "committed" adalah dengan melakukan commit menggunakan perintah `git commit`.

### 3. Committed 
Kondisi "committed" terjadi ketika perubahan pada file telah dicommit ke dalam repositori Git. File-file yang telah dicommit menjadi bagian dari riwayat versi.

![image](https://github.com/aimejeslyn/msib6/assets/91269730/0b21b1db-8714-4bce-8fe7-187d4ede8022)

source: 
https://medium.com/@lucasmaurer/git-gud-the-working-tree-staging-area-and-local-repo-a1f0f4822018 

Dengan demikian, perubahan pada file melewati tiga tahapan utama dalam siklus Git: dari "modified" ke "staged" dengan perintah `git add`, dan dari "staged" ke "committed" dengan perintah `git commit`.




### Konfigurasi Awal
Setelah menginstal Git, langkah pertama adalah mengonfigurasi informasi pengguna:
```bash
git config --global user.name "aime jeslyn"
git config --global user.email jeslyns62@gmail.com
git config --list
git config --global init.defaultBranch main
```

### Membuat Repository
Untuk membuat repositori baru:
```bash
git init nama-directory  # Inisialisasi repositori di dalam direktori
git init .               # Inisialisasi repositori di direktori saat ini
```

### Pengaturan `.gitignore`
File `.gitignore` digunakan untuk mengabaikan file atau direktori tertentu dalam Git.

### Melihat Status dan Riwayat
Periksa status dan riwayat perubahan:
```bash
git status           # Melihat status file dalam repositori
git log              # Melihat riwayat commit
git log --oneline    # Melihat riwayat commit dalam format satu baris
git log index.html   # Melihat riwayat commit untuk file tertentu
git log --author='aime jeslyn'  # Melihat riwayat commit oleh penulis tertentu
```

### Perbandingan Kode
Melihat perbedaan antara kode saat ini dan yang sudah dikommit:
```bash
git diff index.html          # Perbedaan antara working directory dan staging area
git diff <commit1> <commit2> # Perbedaan antara dua commit
```

### Menambahkan Perubahan ke Staging Area
Menambahkan perubahan ke staging area sebelum melakukan commit:
```bash
git add .            # Menambahkan semua file yang berubah
git add index.html   # Menambahkan file tertentu
git add index.html style.css app.js  # Menambahkan beberapa file
```

### Membatalkan Perubahan Sebelum Stage
Membatalkan perubahan sebelum ditambahkan ke staging area:
```bash
git checkout <file>    # Mengembalikan file dari working directory ke kondisi terakhir di staging area
git reset              # Membatalkan perubahan di staging area
git revert -n <commit> # Membuat revert untuk commit tertentu
```

### Penggunaan Branch
Mengelola branch untuk pengembangan yang terpisah:
```bash
git branch <nama branch>      # Membuat branch baru
git checkout <nama branch>    # Pindah ke branch lain
git branch -d <nama branch>   # Menghapus branch
```

### Langkah-langkah Umum
Langkah-langkah umum dalam menggunakan Git:
```bash
git init .                           # Inisialisasi repositori dalam direktori saat ini
git add .                            # Menambahkan semua perubahan ke staging area
git commit -m "comment"              # Melakukan commit dengan pesan komit
git push origin main / <branch-name> # Mengunggah Perubahan ke Remote Repository (GitHub)
```

