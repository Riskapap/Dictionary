# Dictionary

Source Code dan Penjelasan
```
dataMhs = {}                                                                                     ## Membuat Dictionary kosong
print("==================================================================")
print("|      PROGRAM INPUT NILAI MAHASISWA MENGGUNAKAN DICTIONARY      |")
print("==================================================================")

while True:                                                                                      ## LOOPING AKTIF
    c = input("\nA)dd, E)dit, S)earch, D)elete L)ist, Q)uit: ")                                  ## Membuat Menu

    ## MENU ADD
    if (c.lower() == 'a'):                                                                       ## MENU ADD
        print("\n=========================")
        print("| TAMBAH DATA MAHASISWA |")
        print("=========================")
        nama          = input("Masukkan Nama        : ")                                         ## Menginput Nama
        nim           = input("Masukkan NIM         : ")                                         ## Menginput NIM
        nilaiTugas    = int(input("Masukkan Nilai Tugas : "))                                    ## Menginput Nilai Tugas
        nilaiUts      = int(input("Masukkan Nilai UTS   : "))                                    ## Menginput Nilai UTS
        nilaiUas      = int(input("Masukkan Nilai UAS   : "))                                    ## Menginput Nilai UAS
        nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)              ## Menghitung Nilai Akhir
        dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir                          ## Menambahkan data yang sudah diinput ke Dictionary
        print("\nData Berhasil Ditambahkan!")

    ## MENU EDIT
    elif (c.lower() == 'e'):                                                                     ## Menu EDIT
        print("\n=======================")
        print("| EDIT DATA MAHASISWA |")
        print("=======================")
        nama = input("Masukkan Nama: ")                                                          ## Cari nama yang akan diedit
        if nama in dataMhs.keys():                                                               ## Mengambil key dari Dictionary
            nim           = input("Masukkan NIM Baru         : ")                                ## Menginput NIM baru
            nilaiTugas    = int(input("Masukkan Nilai Tugas Baru : "))                           ## Menginput Nilai Tugas Baru
            nilaiUts      = int(input("Masukkan Nilai UTS Baru   : "))                           ## Menginput Nilai UTS Baru
            nilaiUas      = int(input("Masukkan Nilai UAS Baru   : "))                           ## Menginput Nilai UAS Baru
            nilaiAkhir    = (0.30 * nilaiTugas) + (0.35 * nilaiUts) + (0.35 * nilaiUas)          ## Menghitung Nilai Akhir Baru
            dataMhs[nama] = nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir                      ## Mengupdate data ke Dictionary
            print("\nData Berhasil Di Update!")
        else:                                                                                    
            print("Data tidak ditemukan!")                                                       ## Jika nama tidak ditemukan maka muncul perintah tsb.

    ## MENU SEARCH
    elif (c.lower() == 's'):                                                                     ## Menu SEARCH
        print("\n=======================")
        print("| CARI DATA MAHASISWA |")
        print("=======================")
        nama = input("Masukan Nama:  ")                                                          ## Masukkan nama yang akan dicari
        if nama in dataMhs.keys():                                                               ## Mengambil keys dari Dictionary
            print("\n                   DAFTAR NILAI MAHASISWA                   ")
            print("==============================================================")
            print("|     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==============================================================")
            print("| {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(nama, nim, nilaiTugas, nilaiUts, nilaiUas, nilaiAkhir)) ## Format tabel
            print("==============================================================")
        else:
            print("Datanya {0} Tidak Ada ".format(nama))                                        ## Jika data tidak ditemukan, akan muncul perintah tsb.

    ## MENU DELETE
    elif (c.lower() == 'd'):                                                                    ## Menu DELETE
        nama = input("Masukkan Nama:  ")                                                        ## Masukkan nama yang akan didelete
        if nama in dataMhs.keys():                                                              ## Mengambil keys dari Dictionary
            del dataMhs[nama]                                                                   ## Menghapus data yang dipilih
            print("Data Telah dihapus!")
        else:
            print("Data Mahasiswa Tidak Ada".format(nama))                                      ## Jika data tidak ditemukan, akan muncul perintah tsb.

    ## MENU LIST
    elif (c.lower() == 'l'):                                                                    ## Menu LIST
        if dataMhs.items():                                                                     ## Mengambil items dari Dictionary
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            i = 0
            for x in dataMhs.items():
                i += 1
                print("| {6:2} | {0:12s} | {1:9s} | {2:5} | {3:5} | {4:5} | {5:6} |".format(x[0], x[1][0], x[1][1], x[1][2], x[1][3], x[1][4], i))  ## Format tabel
            print("==================================================================")
        else:
            print("\n                      DAFTAR NILAI MAHASISWA                    ")
            print("==================================================================")
            print("| No |     Nama     |    NIM    | Tugas |  UTS  |  UAS  |  Akhir |")
            print("==================================================================")
            print("|                          TIDAK ADA DATA!                       |")
            print("==================================================================")        ## Jika data masih kosong, akan muncul pesan tsb.

    ## MENU KELUAR PROGRAM
    elif (c.lower() == 'q'):                                                                   ## Menu QUIT
        print("\n Veno Setyoaji Wiratama \n 311910363 \n TI.19.A.2")
        break                                                                                  ## Mengakhiri LOOPING

    else:
        print("Pilih menu yang tersedia: ")                                                    ## Jika menu yang dipilih tidak valid, akan muncul pesan tsb.
```

# Flowchart
![Flowchart](https://user-images.githubusercontent.com/56241285/72215973-3b305a80-354d-11ea-931c-e56f86b25f4f.png)

# Screenshot Input
![Input (1)](https://user-images.githubusercontent.com/56241285/72216033-0ec90e00-354e-11ea-966a-9216a8dbdfe6.png)
![Input (2)](https://user-images.githubusercontent.com/56241285/72216034-0ec90e00-354e-11ea-9da0-f21247244858.png)
![Input (3)](https://user-images.githubusercontent.com/56241285/72216035-0ec90e00-354e-11ea-85e0-13946d323fc5.png)

# Screenshot Ouput
![Output (1)](https://user-images.githubusercontent.com/56241285/72216036-0f61a480-354e-11ea-9f67-ccdb1b9e7fcc.png)
![Output (2)](https://user-images.githubusercontent.com/56241285/72216037-0f61a480-354e-11ea-94a3-355b3ae2de76.png)
