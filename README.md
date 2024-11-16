# praktikum
## Deskripsi tugas
buat program sederhana untuk menambahkan data kedalam sebuah list dengan rincian sebagai berikut:
- Program meminta memasukan data sebanyak banyaknya (gunakan perulangan)
- Tampilkan pertanyaan untuk menambah data (y/t?), apabila jawaban t (Tidak), maka program akan menampilkan daftar datanya
- Nilai akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%)

## Kode python
```python
# Inisialisasi list kosong untuk menyimpan data
data_list = []

# Perulangan untuk menambah data
while True:
    # Meminta pengguna memasukkan data
    nama = input("Masukkan nama: ")
    tugas = float(input("Masukkan nilai tugas (0-100): "))
    uts = float(input("Masukkan nilai UTS (0-100): "))
    uas = float(input("Masukkan nilai UAS (0-100): "))
    
    # Menghitung nilai akhir
    nilai_akhir = (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
    
    # Menyimpan data ke dalam list
    data_list.append({
        "Nama": nama,
        "Tugas": tugas,
        "UTS": uts,
        "UAS": uas,
        "Nilai Akhir": nilai_akhir
    })
    
    # Menanyakan apakah ingin menambah data lagi
    lanjut = input("Tambah data lagi? (y/t): ").lower()
    if lanjut == 't':
        break

# Menampilkan daftar data
print("\nDaftar Data:")
print(f"{'Nama':<15} {'Tugas':<10} {'UTS':<10} {'UAS':<10} {'Nilai Akhir':<10}")
for data in data_list:
    print(f"{data['Nama']:<15} {data['Tugas']:<10} {data['UTS']:<10} {data['UAS']:<10} {data['Nilai Akhir']:<10.2f}")
```

## Ouput
![Screenshot 2024-11-16 164734](https://github.com/user-attachments/assets/ae52d239-0c10-4391-b928-8feaa678ab63)

## Penjelasan program
1. Memasukkan Data:
  - Menggunakan perulangan while True agar pengguna bisa memasukkan data sebanyak-banyaknya.
  - Meminta input untuk nama, nilai tugas, UTS, dan UAS.
2. Menghitung Nilai Akhir:
- Nilai akhir dihitung dengan bobot:
  - Tugas: 30%
  - UTS: 35%
  - UAS: 35%.
3. Menyimpan Data:
  - Data disimpan dalam list sebagai dictionary untuk memudahkan pengelolaan.
4. Menambah Data Lagi:
  - Program menanyakan apakah ingin menambah data lagi (y untuk ya, t untuk tidak).
5. Menampilkan Data:
  - Data ditampilkan dalam format tabel.

## Flowchart
![Screenshot 2024-11-16 170731](https://github.com/user-attachments/assets/929ca22c-6796-4ec0-843d-8f3d1d110d2f)
