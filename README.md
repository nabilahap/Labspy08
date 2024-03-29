# Labspy08

### Profil
```py
Nama  : Nabilah Ananda Putri

Nim   : 312110263

Kelas : TI.21.A.1
```

## Tugas Praktikum
- Buatlah program sederhana dengan mengaplikasikan penggunaan class. Buatlah class untuk menampilkan daftar nilai mahasiswa, dengan ketentuan;
> - Method *tambah()* untuk menambahkan data
> - Method *tampilkan()* untuk menampilkan data
> - Method *hapus(nama)* untuk menghapus data berdasarkan nama
> - Method *ubah(nama)* untuk mengubah data berdasarkan nama
> - Buatlah diagram class, flowchart dan penjelasan program pada README.md

### Penjelasan
- Untuk mengimport dan mendapatkan clear system pada os
```py
import os
```

- Untuk membuat class beserta untuk menampung data mahasiswa dan atributnya
```py
class data_mhsw:
    nama=""
    nim=""
    tugas=""
    uts=""
    uas=""
```

- Untuk membuat class `data_mhsw` dengan atributnya, yaitu nama, nim, tugas, uts dan uas.

    ```python
    class data_mhsw:
        nama=""
        nim=""
        tugas=""
        uts=""
        uas=""
    ```

- Untuk membuat variable `data = []` untuk menampung list dari `data_mhsw`.

    ```python
    data = []
    ```

- Untuk membuat fungsi tambahan, jika diperlukan fungsi tersebut akan dipanggil oleh program.

    ```python
    def no_data():
        print("DAFTAR NILAI MAHASISWA")
        print("----------------------")
        print()
        print(" - TIDAK ADA DATA - ")
        print()
    ```

- Untuk menampilkan data ( **lihat()** )
    - Jika belum menginput data, maka akan memanggil fungsi `no_data()`.
    - Jika sebelumnya sudah menginput data, maka data yang sudah diinput akan ditampilkan oleh program.

        ```python
        def lihat():
            os.system("cls")
            if len(data) <=0:
                no_data()     
            else:
                for a in data:
                    print("DAFTAR NILAI MAHASISWA")
                    print("-----------------------")
                    print("Nama Mahasiswa\t: "+a.nama)
                    print("NIM Mahasiswa\t: "+str(a.nim))
                    print("Nilai Tugas\t: "+str(a.tugas))
                    print("Nilai UTS\t: "+str(a.uts))
                    print("Nilai UAS\t: "+str(a.uas))
                    print("Nilai Akhir\t: "+str(a.akhir))
                    print()
        ```

- Untuk menambah data ( **tambah()** )
    - Menginput nim, nama, nilai tugas, nilai uts dan nilai uas.
    - Data yang telah diinput akan ditambahkan ke dalam variable `data`.

        ```python
        def tambah():
            os.system("cls")
            b = data_mhsw()
            print("TAMBAH DATA")
            print("------------")
            b.nama = (input("Nama Mahasiswa\t: "))
            b.nim = (int(input("NIM Mahasiswa\t: ")))
            b.tugas = (int(input("Nilai Tugas\t: ")))
            b.uts = (int(input("Nilai UTS\t: ")))
            b.uas = (int(input("Nilai UAS\t: ")))
            b.akhir = (b.tugas*30/100) + (b.uts*35/100) + (b.uas*35/100) 
            data.append(b)
            print()
        ```

- Untuk mengubah data ( **ubah()** )
    Menginput nama, kemudian input data yang ingin diubah. 

        ```python
        def ubah():
            os.system("cls")
            if len(data) <=0:
                no_data()
            else:
                nama = data_mhsw()
                print("UBAH DATA")
                print("---------")
                nama = (input("Nama Mahasiswa\t: "))
                for nama in data:
                    nama.tugas = (int(input("Nilai Tugas\t: ")))
                    nama.uts = (int(input("Nilai UTS\t: ")))
                    nama.uas = (int(input("Nilai UAS\t: ")))
                    akhir = (nama.tugas*30/100) + (nama.uts*35/100) + (nama.uas*35/100)
                print()
        ```

- Untuk enghapus data ( **hapus()** )
    Menginput nama, setelah nama diinput maka data yang lainnya akan ikut terhapus sesuai dengan nama yang diinputkan.

        ```python
        def hapus():
            os.system("cls")
            if len(data) <=0:
                no_data()
            else:
                nama = data_mhsw()
                print("HAPUS DATA")
                print("----------")
                nama = (input("Nama Mahasiswa\t: "))
                for nama in data:
                    data.remove(nama)
                print()
        ```

- Untuk enggunakan perulangan uncountable, yang artinya selama statement bernilai "True" maka program akan terus berjalan. Jika statementnya "False" maka program terhenti.

    ```python
    Loop = True
    while Loop:
        print("Pilih Menu")
        print("----------")
        tanya = input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar] : ")
        print()

        if tanya=="l" or tanya=="L":
            lihat()
        
        elif tanya=="t" or tanya=="T":
            tambah()
        
        elif tanya=="u" or tanya=="U":
            ubah()
        
        elif tanya=="h" or tanya=="H":
            hapus()
        
        elif tanya=="k" or tanya=="K":
            print("Program Selesai")
            Loop = False
    ```

### Output 
* ![Gambar1](Screenshots/s1.png)

* ![Gambar2](Screenshots/s2.png)

* ![Gambar3](Screenshots/s3.png)

* ![Gambar4](Screenshots/s4.png)


### Sekian dan Terimakasih