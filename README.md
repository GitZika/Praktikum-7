# Praktikum-7

<p> Nama    :   Azhyka Rizki Ramadhan <p>
<p> NIM     :   312210287 <p>
<p> Kelas   :   TI.22.A3 <p>

<img width="607" alt="1" src="https://user-images.githubusercontent.com/118233561/206141265-b297cf00-9094-44c4-bbb7-81a059e7894c.png">


<p> berikut code nya <p>

```python
mahasiswa = {}

def show():
    if mahasiswa.items():
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        i = 0
        for a in mahasiswa.items():
            i += 1
            print("| {no:2d} | {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |      {5:6.2f} |"
                  .format(a[0][: 14], a[1][0], a[1][1], a[1][2], a[1][3], a[1][4], no=i))
        print("=================================================================================")

    else:
        print("Daftar Nilai")
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                                TIDAK ADA DATA                                 |")
        print("=================================================================================")


def add():
    print("Tambah Data")
    nama = input("Nama\t         : ")
    nim = input("NIM\t         : ")
    uts = int(input("Nilai UTS\t : "))
    uas = int(input("Nilai UAS\t : "))
    tugas = int(input("Nilai Tugas\t : "))
    akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
    mahasiswa[nama] = nim, tugas, uts, uas, akhir


def delete():
    print("Hapus Data")
    nama = input("Masukkan Nama : ")

    if nama in mahasiswa.keys():
        del mahasiswa[nama]

    else:
        print("Nama tidak ditemukan")


def update():
    print("Ubah Data")
    nama = input("Masukkan Nama : ")
    if nama in mahasiswa.keys():
        nim = input("NIM\t : ")
        uts = int(input("Nilai UTS\t : "))
        uas = int(input("Nilai UAS\t : "))
        tugas = int(input("Nilai Tugas\t : "))
        akhir = (tugas * 30 / 100) + (uts * 35 / 100) + (uas * 35 / 100)
        mahasiswa[nama] = nim, tugas, uts, uas, akhir

    else:
        print("Nama tidak ditemukan ")


def search():
    print("Cari Data")
    a = input("Masukkan Nama : ")
    if a in mahasiswa.keys():
        print("===========================================================================")
        print("|      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir   |")
        print("===========================================================================")
        print("| {0:14s} | {1:11s} | {2:7d} | {3:7d} | {4:7d} |     {5:6.2f} |"
              .format(a, mahasiswa[a][0], mahasiswa[a][1], mahasiswa[a][2], mahasiswa[a][3], mahasiswa[a][4]))
        print("===========================================================================")

    else:
        print("=================================================================================")
        print("| No |      Nama      |     NIM     |  Tugas  |   UTS   |   UAS   |    Akhir    |")
        print("=================================================================================")
        print("|                          DATA TIDAK DITEMUKAN                                 |")
        print("=================================================================================")


def menu():
    print("\n")
    print("====================================================")
    print("      \t\t Program input nilai       ")
    print("====================================================\n")

    x = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar]: ")
    print("\n")

    if x == 'L':
        show()
    elif x == 'T':
        add()
    elif x == 'U':
        update()
    elif x == 'H':
        delete()
    elif x == 'C':
        search()
    elif x == 'K':
        print("==========================================================================")
        print('\n')
        print("> You exit the code                        ")
        print("\n")
        print("==========================================================================")

        exit()

    else:
        print("            KODE YANG ANDA MASUKKAN TIDAK VALID !!!!!!!!!!!")


while True:
    menu()

```

<p> output awal akan berupa seperti ini <p>

<img width="341" alt="satu" src="https://user-images.githubusercontent.com/118233561/206829823-3ca0f2a5-c2d8-4c59-b41f-15189f2a0cea.png">

## Panduan 
<p> L = untuk melihat data <p>
<p> T = untuk menambahkan data <p>
<p> U = untuk mengubah data <p>
<p> H = untuk menghapus data <p>
<p> C = untuk mencari data <p>
<p> K = untuk keluar dari program <p>

## T)ambah

Pertama tama kalian bisa menambahkan data sesuai keinginan kalian

<img width="347" alt="tambah" src="https://user-images.githubusercontent.com/118233561/206830511-7ce3f5a1-a48d-42b3-99a5-4b3af6f615d5.png">










