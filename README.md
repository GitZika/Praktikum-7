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

### T)ambah

Pertama tama kalian bisa menambahkan data sesuai keinginan kalian

<img width="347" alt="tambah" src="https://user-images.githubusercontent.com/118233561/206830511-7ce3f5a1-a48d-42b3-99a5-4b3af6f615d5.png">
    
### L)ihat
    
Lalu kalian bisa melihat data yang baru saja kalian masukan
    
<img width="497" alt="lihat" src="https://user-images.githubusercontent.com/118233561/206830695-de18a55a-7e9f-48ce-bdf5-a7ad4c4692ff.png">
    
### H)apus
    
kalian juga bisa menghapus data yang anda inginkan
    
<img width="359" alt="hapus 1" src="https://user-images.githubusercontent.com/118233561/206830751-494e38f7-c471-4669-9a6f-62f0d844cfa5.png">
    
lalu data yang kalian hapus akan terhapus
    
<img width="502" alt="hapus 2" src="https://user-images.githubusercontent.com/118233561/206830770-d7de0090-cc8c-40c3-bba1-ca4a42363297.png">
    
### U)bah 
    
atau kalian bisa mengubah data tersebut bila ada kesalahan input pada data
    
<img width="350" alt="ubah 1" src="https://user-images.githubusercontent.com/118233561/206830837-705d99b9-a560-480c-9c99-2cec70200a63.png">
    
lalu data yang kalian ubah akan berubah
    
<img width="502" alt="ubah 2" src="https://user-images.githubusercontent.com/118233561/206830849-55c0ccb9-10a9-4663-a628-a27e90883838.png">
    
### C)ari
    
kalian bisa menggunakan "cari" untuk mencari data apabila data yang tersimpan banyak
    
<img width="463" alt="cari" src="https://user-images.githubusercontent.com/118233561/206830893-c7aad19c-517b-4f1a-8204-9a7e107232fd.png">
    
### K)eluar
    
kalian bisa keluar dari program untuk menyudahi program
    
<img width="466" alt="Keluar" src="https://user-images.githubusercontent.com/118233561/206830930-b4637e78-c2e1-4b89-9c33-ae60643f9ba4.png">



## Flowchart

<img width="543" alt="flow" src="https://user-images.githubusercontent.com/118233561/206831289-10c4b936-b823-495b-a30e-019438272b56.png">

    
    
# SEKIAN TERIMAKASIH MOHON MAAF BILA ADA KESALAHAN




    
    





    
    









