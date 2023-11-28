## Pindah ke direktori home anda
Recall that ~ stands for your home directory
```bash
cd ~
```
## Buat satu folder kosong 'test'
```bash
mkdir test
```
## Masuk ke direktori 'test'
```bash
cd test
```
## Tampilkan path direktori saat ini
```bash
pwd
```
pwd command, tells you what your current directory is

## Buat file kosong bernama 'empty.txt'
```bash
touch empty.txt
```

## Copy file '/etc/timezone' ke direktori ini
-> cp [source] [destination]
```bash
cp /etc/timezone test
```

## Ubah nama file 'timezone' menjadi 'tz.txt'
[You can move or rename a file with the mv command]
-> mv [source] [destination]
```bash
mv timezone tz.txt
```

## List isi direktori ini
```bash
ls test
```

## Pindah ke direktori parent
menggunakan perintah .. untuk merujuk ke direktori parent dari direktori saat ini
kalau mau pindah ke direktori satu tingkat di atas cuup cd ..
kalau mau ke dir /home ketik d $HOME atau cd~
```bash
cd ..
```
## Hapus direktori 'test' seisinya
To remove a folder and all its contents, you need to specify the -r (recursive) option
```bash
rm -r test
```

## Temukan file dengan nama 'fdisk' memakai `locate`
locate [OPTION] 'PATTERN
```bash
locate fdisk
```
## Temukan file dengan nama 'fdisk' memakai `find`
```bash
find -name fdisk
```

## Temukan file pada home anda yang ukurannya > 200 MB
```bash
find -size +200M
```

## Temukan file pada home anda yang diubah < 3 hari
atime: access time; mtime: modify time; ctime: change time
```bash
find -mtime -3
```

## Temukan file pada home anda yang diakses > 30 hari
```bash
find -atime +30
```

## Tampilkan 5 baris pertama keluaran perintah `last`
```bash
head -5 last
```
atau 
```bash
head -n 5 last
```
[ini kalau last -> file]
```bash
last | head -n 5 
```
[ini kalau last -> perintah]

## Tampilkan dua baris terakhir file '/etc/passwd'
```bash
tail -2 /etc/passwsd
```
atau 
```bash
tail -n 2 /etc/passwd
```

## Cari file di '/usr/include' yang memuat kata 'sem_post'
find itu buat nyari file dsb
grep buat nyari teks atau kata di dalem file; Mencetak baris teks yang cocok dengan suatu pola
-> grep [OPTION] 'PATTERN' FILE
```bash
grep -r 'sem_post' /usr/include
```
## Tampilkan kolom 1 dan 5 dari file '/etc/passwd'
```bash
awk '{print $1, $5}' /etc/passwd 
```

## Tampilkan isi file '/etc/motd' dalam huruf kapital
```bash
awk '{print toupper($0)}' [/etc/motd]
```
-----
