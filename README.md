# LabPy07
# Tugas Pemrograman P10
![Screenshot 2024-11-27 193547](https://github.com/user-attachments/assets/d062a42f-891e-4dd5-8170-2d1ed2f2a1a8)
![Screenshot 2024-11-27 194124](https://github.com/user-attachments/assets/c55d6d8c-e288-4e1b-b3eb-2b452b56c723)
![Screenshot 2024-11-27 194220](https://github.com/user-attachments/assets/e734a66c-98b0-4df0-8424-cd4f74db11e2)

# Penjelasan
Berikut adalah penjelasan mengenai kode yang Anda berikan, yang merupakan program sederhana untuk mengelola data mahasiswa. Program ini memungkinkan pengguna untuk menambah, menampilkan, menghapus, dan mengubah data mahasiswa. Mari kita bahas setiap bagian dari kode tersebut:

# 1. Daftar Mahasiswa
    - mahasiswa = []
  - Ini adalah daftar (list) kosong yang digunakan untuk menyimpan data mahasiswa. Setiap mahasiswa akan disimpan sebagai dictionary (kamus) yang berisi nama dan nilai.

# 2. Fungsi `tambah(nama, nilai)`
    - def tambah(nama, nilai):
          """Menambahkan data mahasiswa ke dalam daftar."""
          mahasiswa.append({"nama": nama, "nilai": nilai})
          print(f"Data {nama} berhasil ditambahkan.")
  - Fungsi ini menerima dua parameter, `nama`dan `nilai`, dan menambahkan data siswa baru ke dalam daftar `mahasiswa`. Setelah menambahkan data, fungsi ini akan mencetak 
    konfirmasi pesan.

# 3. Fungsi `tampilkan()`
     - def tampilkan():
           """Menampilkan semua data mahasiswa."""
           if not mahasiswa:
               print("Tidak ada data mahasiswa.")
               return
           print("Daftar Nilai Mahasiswa:")
           for index, mhs in enumerate(mahasiswa, start=1):
               print(f"{index}. Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")

  - Fungsi ini digunakan untuk menampilkan semua data siswa yang tersimpan. Jika tidak ada data, akan dicetak pesan bahwa tidak ada data siswa. Jika ada, akan mencetak 
    daftar pelajar beserta nilainya.

# 4. Fungsi `hapus(nama)`
     -def hapus(nama):
          """Menghapus data mahasiswa berdasarkan nama."""
          global mahasiswa
          _mhs = [mhs for mhs in mahasiswa if mhs["nama"] != nama]
          if len(_mhs) < len(mahasiswa):
              mahasiswa = _mhs
              print(f"Data {nama} berhasil dihapus.")
         else:
             print(f"Data {nama} tidak ditemukan.")
  - Fungsi ini menghapus data siswa berdasarkan nama. Jika nama siswa ditemukan dalam daftar, data tersebut akan dihapus dan pesan konfirmasi akan ditampilkan. Jika tidak 
    ditemukan, akan tercetak pesan bahwa data tidak ada.

# 5. Fungsiubah `(nama, nilai_baru)`
     - def ubah(nama, nilai_baru):
           """Mengubah data mahasiswa berdasarkan nama."""
           for mhs in mahasiswa:
                if mhs["nama"] == nama:
                    mhs["nilai"] = nilai_baru
                    print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
                    return
            print(f"Data {nama} tidak ditemukan.")

  - Fungsi ini digunakan untuk mengubah nilai siswa berdasarkan nama. Jika nama siswa ditemukan, nilai tersebut akan diperbarui dan konfirmasi pesan akan ditampilkan. Jika 
    tidak ditemukan, akan tercetak pesan bahwa data tidak ada.

# 6. Fungsi `menu()`
     - def menu():
           """Menampilkan menu utama."""
           while True:
               print("\nMenu:")
               print("1. Tambah Data")
               print("2. Tampilkan Data")
               print("3. Hapus Data")
               print("4. Ubah Data")
               print("5. Keluar")
               pilihan = input("Pilih opsi (1-5): ")

               if pilihan == '1':
                   nama = input("Masukkan nama mahasiswa: ")
                   nilai = input("Masukkan nilai mahasiswa: ")
                   tambah(nama, nilai)
              elif pilihan == '2':
                   tampilkan()
              elif pilihan == '3':
                   nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
                   hapus(nama)
              elif pilihan == '4':
                   nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
                   nilai_baru = input("Masukkan nilai baru: ")
                   ubah(nama, nilai_baru)
              elif pilihan == '5':
                   print("Terima kasih!")
                   break
              else:
                   print("Pilihan tidak valid. Silakan coba lagi.")

  - Fungsi ini menampilkan menu utama yang memungkinkan pengguna untuk memilih tindakan yang ingin dilakukan. Program akan terus berjalan dalam loop hingga pengguna memilih 
    untuk keluar.

# 7. Menjalankan Program
     - if __name__ == "__main__":
       menu()
  - Bagian ini memastikan bahwa fungsi `menu()` hanya dijalankan jika file ini dieksekusi sebagai program utama, bukan diimpor sebagai modul.

# Hasil Dari Run (Output)

# Tambah Data

# Tampilkan Data
![Screenshot 2024-11-27 192747](https://github.com/user-attachments/assets/83f03c82-88a0-44e3-ad06-e011daa461ab)
# Hapus Data
![Screenshot 2024-11-27 192825](https://github.com/user-attachments/assets/8a6c9d57-a3b4-4739-b2b7-19c356d75728)
# Ubah Data 
![Screenshot 2024-11-27 192804](https://github.com/user-attachments/assets/879506a9-24f3-45ad-a2b9-b62552cb7c99)
# Keluar
![Screenshot 2024-11-27 192839](https://github.com/user-attachments/assets/24a1b19e-1442-4080-950f-33aba9a01159)

# Komponen Flowchart
![WhatsApp Image 2024-11-27 at 00 37 56](https://github.com/user-attachments/assets/244ef38e-a3c0-4c70-a927-0693a2d69638)

# 1. Start: Titik awal dari program.
# 2. Menu: Tampilkan menu utama dengan pilihan:
  - Tambah Data
  - Tampilkan Data
  - Hapus Data
  - Ubah Data
  - Keluar
# 3. Input Pilihan: Menerima input dari pengguna untuk memilih opsi menu.
# 4. Proses Berdasarkan Pilihan:
  - Jika Pilihan 1 (Tambah Data):
     - Input nama dan nilai mahasiswa.
     - Panggil fungsi `tambah(nama, nilai)` untuk menambahkan data.
     - Kembali ke menu.
  - Jika Pilihan 2 (Tampilkan Data):
     - Panggil fungsi `tampilkan()` untuk menampilkan semua data mahasiswa.
     - Kembali ke menu.
     - Jika Pilihan 3 (Hapus Data):
     - Input nama mahasiswa yang ingin dihapus.
     - Panggil fungsi `hapus(nama)` untuk menghapus data.
     - Kembali ke menu.
  - Jika Pilihan 4 (Ubah Data):
     - Input nama mahasiswa yang ingin diubah dan nilai baru.
     - Panggil fungsi `ubah(nama, nilai_baru)` untuk mengubah data.
     - Kembali ke menu.
     - Jika Pilihan 5 (Keluar):
     - Tampilkan pesan "Terima kasih!" dan akhiri program.
# 5. Error Handling: Jika pilihan tidak valid, tampilkan pesan kesalahan dan kembali ke menu.
# 6. nd: Titik akhir dari program ketika pengguna memilih untuk keluar.

# Penjelasan Flowchart
 - Start: Program dimulai.
 - Tampilkan Menu: Menu ditampilkan kepada pengguna.
 - Input Pilihan: Pengguna memilih opsi dari menu.
 - Proses Berdasarkan Pilihan: Bergantung pada pilihan, program akan melakukan tindakan yang sesuai (menambah,
