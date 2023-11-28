# Kisi Kisi UASP
- Pindah ke direktori home anda
```bash
cd ~
```
- Buat satu folder kosong `test`
```bash
mkdir test
```
- Masuk ke direktori `test`
```bash
cd test
```
- Tampilkan path direktori saat ini
```bash
pwd
```
- Buat file kosong bernama `empty.txt`
```bash
touch empty.txt
```
- Copy file `/etc/timezone` ke direktori
```bash
cp /etc/timezone timezone
```
- Ubah nama file `timezone` menjadi `tz.txt`
```bash
mv timezone tz.txt
```
- List isi direktori ini
```bash
ls
```
- Pindah ke direktori parent
```bash
cd ..
```
- Hapus direktori `test` dan seisinya
```bash
rm -rf test
```
- Temukan file dengan nama `fdisk` memakai `locate`
```bash
locate –i fdisk
```
- Temukan file dengan nama `fdisk` memakai `find`
```bash
find -name fdisk
```
- Temukan file pada home anda yang ukurannya > 200 MB
```bash
find ~ -size +200M
```
- Temukan file pada home anda yang diubah < 3 hari
```bash
find ~ -mtime -3
```
- Temukan file pada home anda yang diakses > 30 hari
```bash
find ~ -atime +30
```
- Tampilkan 5 baris pertama keluaran perintah `last`
```bash
last | head -n 5
```
- Tampilkan dua baris terakhir file `etc/passwd`
```bash
cat /etc/passwd | tail -n 2
```
- cari file di `/usr/include` yang memuat kata `sem_post`
```bash
grep -rnw '/usr/include/' -e 'sem_post'
```
- Tampilkan kolom 1 dan 5 dari file `/etc/passwd`
```bash
cut -f 1,5 /etc/passwd -d ':'
```
- Tampilkan isi file `/etc/motd` dalam huruf kapital
```bash
cat /etc/motd | tr a-z A-Z
```
- Jalankan cat /dev/random > rand.txt di background
```bash
cat /dev/random > rand.txt &
```
- Tampilkan daftar job
```bash
jobs
jobs -p # Untuk menampilkan sesuai PID
```
- Kirim sinyal STOP ke job tersebut
```bash
kill -STOP 25384 # (Angka sesuai PID output di jobs)
```
- Lanjutkan job tersebut di background
```bash
kill -CONT 25384 # (Angka sesuai PID output di jobs)
```
- Kirim sinyal TERM ke job tersebut
```bash
kill -TERM 25384 # (Angka sesuai PID output di jobs)
```
