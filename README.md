# Fitri Ramadhani
# 312410085
# TI.24.A.1
# Mata Kuliah: Bahasa Pemrograman
# Dosen Pengampu: Bapak Agung Nugroho, S.Kom., M.Kom

# LATIHAN STRING 1
# INPUT PROGRAM
```python
txt = 'Hello World'
# 1. Hitung jumlah karakternya
jumlah_karakter = len(txt)
print("Jumlah karakter:", jumlah_karakter)
```
# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring.py"
Jumlah karakter: 11
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> 
```

# INPUT PROGRAM
```python
txt = 'Hello World'
# 2. Ambil karakter terakhir
karakter_terakhir = txt[-1]
print("Karakter terakhir:", karakter_terakhir)
```

# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring.py"
Karakter terakhir: d
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14>
```

# INPUT PROGRAM
```python
txt = 'Hello World'

# 3. Ambil karakter index ke-2 sampai index ke-4 (llo)
substring = txt[2:5]
print("Karakter index 2 sampai 4:", substring)
```

# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring.py"
Karakter index 2 sampai 4: llo
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14>
```

# INPUT PROGRAM
```python
txt = 'Hello World'

# 4. Hilangkan spasi (HelloWorld)
tanpa_spasi = txt.replace(" ", "")
print("Tanpa spasi:", tanpa_spasi)
```

# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring.py"
Tanpa spasi: HelloWorld
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> 
```

# INPUT PROGRAM
```python
txt = 'Hello World'

# 5. Ubah text menjadi huruf besar
huruf_besar = txt.upper()
print("Huruf besar:", huruf_besar)
```

# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring.py"
Huruf besar: HELLO WORLD
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14>
```

# INPUT PROGRAM
```python
txt = 'Hello World'

# 6. Ubah text menjadi huruf kecil
huruf_kecil = txt.lower()
print("Huruf kecil:", huruf_kecil)
```

# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring.py"
Huruf kecil: hello world
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14>
```

# INPUT PROGRAM
```python
txt = 'Hello World'

# 7. Ganti karakter H dengan J
ganti_h = txt.replace("H", "J")
print("Ganti H dengan J:", ganti_h)
```

# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring.py"
Ganti H dengan J: Jello World
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> 
```

# LATIHAN STRING 2
```python
umur = 24
txt = 'Hello, nama saya John, dan umur saya adalah {} tahun'

print(txt.format(umur))
```

# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihanstring2.py"
Hello, nama saya John, dan umur saya adalah 24 tahun
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14>
```

# LATIHAN 3 STUDI KASUS VALIDASI FORM INPUT
# Program Validasi Form Input Pendaftaran Online
program ini menjelaskan fungsi utama dari kode yang dibuat, yaitu memvalidasi data input yang diisi dalam formulir pendaftaran online.

# Deskripsi Program
Program ini dirancang untuk memvalidasi data yang dimasukkan oleh pengguna dalam formulir pendaftaran online. Validasi dilakukan pada tiga jenis data:

   1. Nama Lengkap – harus hanya berisi huruf.
   2. Nomor Telepon – harus hanya berisi angka.
   3. Email – harus mengandung karakter '@' dan '.'.

Jika semua input valid, program akan mencetak pesan sukses. Jika ada kesalahan, pesan error spesifik akan ditampilkan untuk memberi tahu pengguna apa yang perlu diperbaiki.

# Kode Program
```python
def validasi_form(nama, telepon, email):
    # Validasi nama (hanya huruf)
    if not nama.replace(" ", "").isalpha():
        print("Error: Nama harus hanya berisi huruf.")
        return

    # Validasi nomor telepon (hanya angka)
    if not telepon.isdigit():
        print("Error: Nomor telepon harus hanya berisi angka.")
        return

    # Validasi email (harus mengandung '@' dan '.')
    if '@' not in email or '.' not in email:
        print("Error: Email harus mengandung karakter '@' dan '.'.")
        return

    # Jika semua validasi berhasil
    print("Data pendaftaran valid.")

# Input dari pengguna
nama = input("Masukkan nama lengkap: ")
telepon = input("Masukkan nomor telepon: ")
email = input("Masukkan email: ")

# Panggil fungsi validasi
validasi_form(nama, telepon, email)
```
# OUTPUT PROGRAM
```
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14> python -u "c:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14\latihan.py"
Masukkan nama lengkap: Fitri Ramadhani
Masukkan nomor telepon: 083807066072
Masukkan email: fitrirmdhni002@gmail.com
Data pendaftaran valid.

Masukkan nama lengkap: Noel G4ntEng 
Masukkan nomor telepon: 0838i07066072
Masukkan email: noellondokgmailcom
Error: Nama harus hanya berisi huruf.
PS C:\Users\AXIOO\Documents\KULIAH\matkul b.pemrograman\latihan pert-14>
```

# CARA KERJA PROGRAM
   1. Pengguna Mengisi Formulir:
       - Program meminta input nama lengkap, nomor telepon, dan email melalui input().

   2.  Validasi Nama:
       - Program memeriksa apakah nama hanya mengandung huruf dengan isalpha().
       - Jika ada angka atau simbol, program akan menampilkan error:

  Error: Nama harus hanya berisi huruf.

   replace(" ", "") memungkinkan spasi dalam nama tanpa menyebabkan error.

3. Validasi Nomor Telepon:

   - isdigit() digunakan untuk memeriksa apakah nomor telepon hanya berisi angka.
   - Jika ada huruf atau simbol, error ditampilkan:

    Error: Nomor telepon harus hanya berisi angka.

4. Validasi Email:
   - Program memeriksa apakah email mengandung @ dan ..
   - Jika tidak, pesan error:
    Error: Email harus mengandung karakter '@' dan '.'.

5. Validasi Berhasil:
   - Jika semua input valid, program akan mencetak:
Data pendaftaran valid.
