## TUGAS PRAKTIKUM 4
Nama : Rafli Dhiya Fadhaly

Nim : 312410251

Kelas : TI 24 A2
## Input dan output dari Praktikum 4
## Input
![carbon](https://github.com/user-attachments/assets/0727f850-06fc-4a1f-9b4b-82771e275f46)
## Output
![Screenshot (67)](https://github.com/user-attachments/assets/af293320-646f-4485-8074-52ed69d33c2f)
## Flowchart
![WhatsApp Image 2024-11-14 at 17 16 46_9337b041](https://github.com/user-attachments/assets/ab9031bd-70b2-4855-a0e1-a10468c63004)
## 1. Fungsi hitung_nilai_akhir(tugas, uts, uas):
```python
def hitung_nilai_akhir(tugas, uts, uas):
    return (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
```
Fungsi ini menerima 3 parameter: nilai tugas, UTS, dan UAS
Menghitung nilai akhir dengan bobot:
Tugas: 30% (0.30)
UTS: 35% (0.35)
UAS: 35% (0.35)
Mengembalikan hasil perhitungan nilai akhir
## 2. Fungsi tampilkan_daftar(daftar_mahasiswa):
```python
def tampilkan_daftar(daftar_mahasiswa):
    print("=" * 70)  # Membuat garis pembatas
    print("| No |     Nama      |    NIM    | Tugas | UTS | UAS | Akhir |")
    print("=" * 70)  # Membuat garis pembatas
```
Menerima parameter berupa list yang berisi data mahasiswa
Membuat tampilan tabel dengan header
Menggunakan perulangan untuk menampilkan setiap data mahasiswa
Format output menggunakan string formatting untuk merapikan tampilan
enumerate(daftar_mahasiswa, 1) digunakan untuk membuat penomoran mulai dari 1
## 3. Fungsi main():
```python
def main():
    daftar_mahasiswa = []  # Inisialisasi list kosong
```
Fungsi utama program
Membuat list kosong untuk menyimpan data mahasiswa
## 4. Input Data dan Validasi:
```python
while True:
    print("\nMasukkan data mahasiswa")
    nama = input("Nama : ")
    nim = input("NIM : ")
    
    while True:
        try:
            tugas = float(input("Nilai Tugas : "))
            if 0 <= tugas <= 100:
                break
            print("Nilai harus antara 0-100!")
        except ValueError:
            print("Masukkan nilai yang valid!")
```
Menggunakan nested while loop untuk input dan validasi
Try-except untuk menangani input nilai yang tidak valid
Validasi rentang nilai (0-100)
Proses yang sama dilakukan untuk nilai UTS dan UAS
## 5. Menyimpan Data:
```python
# Hitung nilai akhir
nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)

# Tambahkan ke daftar
mahasiswa = {
    'nama': nama,
    'nim': nim,
    'tugas': tugas,
    'uts': uts,
    'uas': uas,
    'nilai_akhir': nilai_akhir
}
daftar_mahasiswa.append(mahasiswa)
```
Memanggil fungsi hitung_nilai_akhir
Membuat dictionary untuk menyimpan data satu mahasiswa
Menambahkan dictionary ke dalam list daftar_mahasiswa
## 6. Konfirmasi Tambah Data:
```python
tambah = input("\nTambah data (y/t)? ")
if tambah.lower() != 'y':
    break
```
Meminta konfirmasi untuk menambah data lagi
Jika input bukan 'y', keluar dari loop
## 7. Menampilkan Hasil:
```python
print("\nDaftar Nilai Mahasiswa:")
tampilkan_daftar(daftar_mahasiswa)
```
Memanggil fungsi tampilkan_daftar untuk menampilkan semua data
## 8. Entry Point Program:
```python
if __name__ == "__main__":
    main()
```
Memastikan fungsi main() hanya dijalankan jika file dijalankan langsung
Tidak akan dijalankan jika file di-import sebagai modul
Fitur-fitur Program:

Dapat menambahkan data mahasiswa secara dinamis
Validasi input untuk nilai (harus numerik dan 0-100)
Perhitungan nilai akhir otomatis dengan bobot yang ditentukan
Tampilan output dalam bentuk tabel yang rapi
Penanganan error untuk input yang tidak valid
Konfirmasi untuk menambah data baru
Program ini dibuat untuk memudahkan pengelolaan data nilai mahasiswa dengan interface yang user-friendly dan penanganan error yang baik.
