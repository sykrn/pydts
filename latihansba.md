# Instruksi
1. Buka editor kesukaan Anda masing-masing. Kemudian buatlah file script `.py` untuk diupload sebagai jawaban setiap soal.
2. Format soal:
  * Anda akan diberikan suatu text atau soal dengan tugas tertentu.
  * Dalam soal akan diberika suatu case input/output yang diperlukan.

### contoh: 
---    
    input:    
    1

    output:    
    365
yang artinya user memberikan input `1`, dan program mengeluarkan `365`.

---
    input:    
    1 2

    output:    
    hallo 12
  yang artinya user memberikan input `1 2`, dan program mengeluarkan `hallo 12`.

  * Setiap output diwajibkan untuk sama dengan definisi soal tanpa diimprovisasi. Sebagai contoh, jika soal meminta Anda untuk mengeluarkan tulisan `hello world` jangan pernah memodifikasi seperti `hello world!` (perhatikan tanda seru). Samakanlan logika input output yang diberikan.

Selamat mengerjakan

---

## Soal 1

Buatlah suatu program python untuk menghitung luas lingkaran. Program Anda akan meminta masukan/input dari user berupa nilai diameter `d`, dan mengeluarkan tulisan berupa nilai luasan dari lingkaran tersebut. Gunakan nilai π = 3.1416. 

contoh case Input/Ouput:

### case 1:
    input:
    1

    output:
    0.7854

### case 2:
    input:
    3

    output:
    7.0686
---
## Pembahasan

Jawaban yang dianggap benar oleh system (Grader). Fokus pada nilai kesamaan output (baik format ataupun nilai) terhadap instruksi soal beradasarkan contoh/case (input case pengujian bisa jadi berbeda dengan yang ada di soal).


contoh script `latihansba.py` yang **BENAR**:

```
d = float(input())
L = 3.1416 * d**2 / 4
print(L)
```
atau 
```
d = input()
d = float(d)
L = 3.1416 * d**2 / 4
print(L)
```

Anda boleh untuk melakukan apapun sesuai logika anda **KECUALI** baris input/output yang harus sama sesuai deskripsi soal dan contoh testcase.

contoh script `latihansba.py` yang **SALAH**:

```
d = float(input())
L = 3.1416 * d**2 / 4
print('Luas lingkaran adalah ',L)
```

Hal ini akan disalahkan oleh sistem grader. karna output yang di keluarkan dianggap berbeda meski secara logika hal tersebut adalah benar. 
