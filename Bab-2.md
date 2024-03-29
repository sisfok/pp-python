---
title: Conditional Statement
layout: default
author: "@BobChrismansyah dan @deovaliandro"
---

- [If-else Statement](#if-else-statement)
  - [If statement](#if-statement)
  - [If-else statement](#if-else-statement-1)
  - [If-elif-else statement](#if-elif-else-statement)
  - [Nested if Statement](#nested-if-statement)
  - [Shorthand if statement](#shorthand-if-statement)
  - [ShortHand if-else statement](#shorthand-if-else-statement)
- [Match Case](#match-case)

_Conditional statement_ adalah sebuah statement yang mengandung sebuah kondisi.
Jika kondisi tersebut bernilai benar, maka statement akan dijalankan. Jika
kondisi tersebut bernilai salah, maka statement tidak akan dijalankan.
Pengkondisian biasanya dalam bentuk if statement, yaitu salah satu fitur utama
dari bahasa pemrograman, tidak terkecuali Python. Hampir tidak ada bahasa
pemrograman yang tidak memiliki if statement dan hampir tidak ada cara untuk
memprogram tanpa cabang dalam aliran kode (setidaknya jika kode tersebut perlu
memecahkan masalah yang kompleks).Pengkondisian dapat digunakan untuk mengontrol
jalannya program. Contoh penggunaan pengkondisian adalah untuk menentukan apakah
suatu bilangan merupakan bilangan ganjil atau genap.

Bahasa pemrograman seperti C, C++, dan Java setidaknya memiliki fitur
conditional statement seperti if statement dan switch case, namun dalam bahasa
Python switch case baru di adaptasi pada versi 3.10 keatas yang dikenal sebagai
"structural pattern matching" atau "match case". Artinya, pada versi sebelumnya
pengkondisian hanya dapat dilakukan menggunakan if statement. Ekspresi terdiri
dari satu atau beberapa operator perbandingan dan operator logika yang akan
menghasilkan nilai True (benar) atau False (salah).

Pengkondisian biasanya dalam bentuk if statement, yaitu salah satu fitur utama
dari bahasa pemrograman, tidak terkecuali Python. Hampir tidak ada bahasa
pemrograman yang tidak memiliki if statement dan hampir tidak ada cara untuk
memprogram tanpa cabang dalam aliran kode (setidaknya jika kode tersebut perlu
memecahkan masalah yang kompleks).

Bahasa pemrograman seperti C, C++, dan Java setidaknya memiliki fitur
conditional statement seperti if statement dan switch case, namun dalam bahasa
python switch case baru di adaptasi pada versi 3.10 keatas yang dikenal sebagai
"structural pattern matching" atau "match case". Artinya, pada versi sebelumnya
pengkondisian hanya dapat dilakukan menggunakan if statement. Ekspresi terdiri
dari satu atau beberapa operator perbandingan dan operator logika yang akan
menghasilkan nilai True (benar) atau False (salah).

Tabel Operator Perbandingan

| Opertor | Arti                         | Contoh | Hasil |
|:-------:|:----------------------------:|:------:|:-----:|
| ==      | Sama dengan                  | a == b | False |
| !=      | Tidak sama dengan            | a != b | True  |
| >       | Lebih besar dari             | a > b  | False |
| <       | Lebih kecil dari             | a < b  | True  |
| >=      | Lebih besar atau sama dengan | a >= b | False |
| <=      | Lebih kecil atau sama dengan | a <= b | True  |

Tabel Operator Logika

| Operator | Arti                  | Contoh                | Hasil |
|:--------:|:---------------------:|:---------------------:|:-----:|
| and      | Jika keduanya benar   | a < 5 and b < 10      | True  |
| or       | Jika salah satu benar | a < 5 or b < 4        | True  |
| not      | Jika salah satu benar | not(a < 5 and b < 10) | False |

## If-else Statement

### If statement

_If statement_ adalah jenis pengkondisian di mana kode dieksekusi apabila
ekspresi terpenuhi atau bernilai True (benar). Pernyataan dari if statement
harus memiliki indent minimal sepanjang satu spasi di awal tiap baris kode.
Suatu pernyataan dapat berupa satu baris atau satu blok kode.

Alur Program

```mermaid
flowchart LR
A([Start]) --> B{Ekspresi <br> <strong>if</strong>}
B -->|True| C[<strong>perintah</strong> <br> di dalam blok <strong>IF</strong>]
C --> E([End])
B ---->|False| E([End])
```

Contoh 1:

```python
angka = 5

if angka > 0:
    print(angka,"adalah bilangan positif")
    print("pernyataan ini benar")
```

Output:

```bash
5 adalah bilangan positif
pernyataan ini benar
```

Contoh 2:

```python
angka = 5

if angka < 0:
    print(angka,"adalah bilangan negatif")
    print("pernyataan ini False!")
```

Output:

```bash
pernyataan ini False!
```

Contoh 3:

```python
angka = -2

if angka > 0:
    print(angka, "adalah bilangan positif")

if angka < 0:
    print(angka, "adalah bilangan negatif")
    print("Pernyataan ini bernilai benar")
```

Output:

```bash
-2 adalah bilangan negatif
pernyataan ini bernilai benar
```

### If-else statement

Pernyataan "else" digunakan ketika bagian benar dan salah dari kondisi tertentu
ditentukan untuk dieksekusi. Ketika kondisinya benar, pernyataan di dalam blok
if dieksekusi; jika kondisinya salah, program pada blok else akan dieksekusi.

Pernyataan if-else dalam Python memiliki sintaks berikut:

```python
if ekspresi:
    #Pernyataan/stastement (dieksekusi jika ekspresi bernilai True)
else:
    #pernyataan/statement (dieksekusi jika ekspresi bernilai False)
```

Alur Program

```mermaid
flowchart LR
A([Start]) --> B{Ekspresi <br> <strong>if</strong>}
B -->|True| C[<strong>perintah</strong> <br> di dalam blok <strong>IF</strong>]
C --> E([Stop])
D --> E([Stop])
B -->|False| D[<strong>perintah</strong> <br> di dalam blok <strong>ELSE</strong>]
```

Contoh 1

```python
angka = 5

if angka >= 0:
    print("bilangan positif atau nol")
else:
    print(angka, "adalah bilangan negatif")
```

Output

```bash
bilangan positif atau nol
```

Contoh 2

```python
x = 5
y = 20

if x == y:
    print("x dan y bernilai sama")
else:
    print("x tidak sama dengan y")
```

Output:

```bash
x tidak sama dengan y
```

### If-elif-else statement

Pernyataan elif memungkinkan Anda untuk memeriksa beberapa ekspresi dan
mengeksekusi blok kode segera setelah salah satu kondisi mengevaluasi ke True.
Dalam hal ini, kondisi if dievaluasi terlebih dahulu. Jika salah, pernyataan
elif akan dieksekusi, jika itu juga salah, pernyataan else akan dieksekusi.

Pernyataan If..Elif..else dalam Python memiliki sintaks berikut:

```python
if ekspresi:
    #dieksekusi jika ekspresi bernilai True
elif ekspresi:
    #dieksekusi jika ekspresi (elif) bernilai True
else:
    #dieksekusi jika ekspresi bernilai False

Alur program

```mermaid
flowchart LR
A([Start]) --> B{Ekspresi <br> <strong>if</strong>}
B -->|True| C[<strong>perintah</strong> <br> di dalam blok <strong>IF</strong>]
B ---->|False| D{Ekspresi <br> <strong>elif</strong>}
D --->|True| F[<strong>perintah</strong> <br> di dalam blok <strong>ELIF</strong>]
D ---->|False| G[<strong>perintah</strong> <br> di dalam blok <strong>ELSE</strong>]

F --> E([Stop])
C --> E{ Stop}
G --> E([Stop])
```

Contoh 1

```python
angka = 1

if angka > 0:
    print(angka, "adalah bilangan positif")
elif angka == 0:
    print(angka, "adalah bilangan nol")
else:
    print(angka, "adalah bilangan negatif")
```

Outuput:

```bash
1 adalah bilangan positif
```

Contoh 2

```python
angka = -1

if angka > 0:
    print(angka, "adalah bilangan positif")
elif angka == 0:
    print(angka, "adalah bilangan nol")
else:
    print(angka, "adalah bilangan negatif")
```

Outputnya:

```bash
-1 adalah bilangan negatif
```

### Nested if Statement

Pernyataan IF bersarang adalah pernyataan di mana pernyataan If terletak di
dalam pernyataan If lainnya. Ini digunakan ketika variabel harus diproses lebih
dari sekali. Pernyataan if, if-else, dan if-elif-else dapat digunakan dalam
program.

Pernyataan if bersarang dalam Python memiliki sintaks berikut:

```python
if ekspresi:
    #dieksekusi jika ekspresi bernilai True
    if ekspresi:
        # dieksekusi jika ekspresi if (luar) dan if (dalam) bernilai True
```

Alur program

```mermaid
flowchart LR
A([Start]) --> B{Ekspresi <br> <strong>if</strong> 'luar'}
B -->|False| E
B ---->|True| D[<strong>perintah</strong> <br> di dalam blok <strong>IF</strong> 'luar']
D --->F{Ekspresi <br> <strong>if</strong> 'dalam'}
F --->|False| E
F --->|True| H[<strong>perintah</strong> <br> di dalam blok <strong>IF</strong> 'dalam']
H --> E([Stop])
E([Stop])
```

Contoh 1

```python
angka = -1

if angka >= 0:
    if angka == 0:
        print(angka,"adalah bilangan nol")
    else:
        print(angka,"adalah bilangan positif")
else:
    print(angka,"adalah bilangan negatif")
```

Outputnya:

```bash
-1 adalah bilangan negatif
```

### Shorthand if statement

Shorthand if statement digunakan ketika hanya satu statement yang perlu
dieksekusi di dalam blok if. Pernyataan ini dapat disertakan di baris yang sama
dengan pernyataan If.

Pernyataan Short Hand if dalam Python memiliki sintaks berikut:

```python
if kondisi: statement
```

Contoh Program:

```python
a = 123

if a > 100: print(a, "lebih besar dari seratus")
```

Output:

```bash
123 lebih besar dari seratus
```

### ShortHand if-else statement

Shorthand if-else digunakan untuk menyebutkan pernyataan If-else dalam satu
baris di mana hanya ada satu pernyataan untuk dieksekusi di blok if dan else.

Short Hand if-else dalam Python memiliki sintaks berikut:

```python
statement (True) if kondisi else statement (False)
```

Contoh Program:

```python
a = 123
print(a, "lebih besar dari 100") if a > 100 else print(a, "lebih kecil dari 100")
```

Output:

```bash
123 lebih besar dari 100
```

## Match Case

Pernyataan switch mengevaluasi ekspresi, mencocokkan nilai ekspresi terhadap
serangkaian klausa kasus, dan mengeksekusi pernyataan setelah klausa kasus
pertama dengan nilai yang cocok, hingga pernyataan break ditemukan. Klausa
default dari pernyataan switch akan dilompati jika tidak ada kasus yang cocok
dengan nilai ekspresi.

Short Hand if dalam Python memiliki sintaks berikut:

```python
match variabel:
    case nilai-1:
        statement-1
    case nilai-2:
        statement-2
    case nilai-…:
        statement-…
    case _:
        statement-default (jika tidak ada case yang sesuai)
```

Alur Program

```mermaid
flowchart LR
B[Match Variabel]
B ----> D{Case <br> Nilai-1}
D ---> |True| F[Statement-1]
F ---> E

D --->|False| H{Case <br> Nilai-2}
H --->|True| J[Statement-2]
J ---> E

H --->|False| L{Case <br> Nilai-3}
L --->|True| N[Statement-3]
N ---> E 

L --->|False| P{Case <br> 'default'}
P ---> R[Statement default]
R ---> E

E([Stop])
```

Contoh program:

```python
bahasa = "Python"

match bahasa:
    case "JavaScript":
        print("kamu akan menjadi web developer.")
    case "Python":
        print("kamu akan menjadi Data Scientist")
    case "PHP":
        print("kamu akan menjadi backend developer")
    case "Solidity":
        print("kamu akan menjadi Blockchain developer")
    case "Java":
        print("kamu akan menjadi mobile app developer")
    case _:
        print("bahasa tidak penting, yang penting adalah mampu untuk menyelesaikan masalah.")
```

Output:

```bash
kamu akan menjadi Data Scientist
```
