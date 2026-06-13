# Tugas: OBE_5variabel_dan_5persamaan (Eliminasi Gauss)

**Sistem Persamaan Linear 5 Variabel dan 5 Persamaan**

## 1. Sistem Persamaan Linear

$$x + y + w + v + z = 5$$

$$2x + 3y + w + v + z = 8$$

$$x + y + 2w + v + z = 7$$

$$x + y + w + 3v + z = 9$$

$$x + y + w + v + 2z = 8$$

---

## 2. Bentuk Matriks Augmented

$$\left[ \begin{array}{ccccc|c} 
1 & 1 & 1 & 1 & 1 & 5 \\ 
2 & 3 & 1 & 1 & 1 & 8 \\ 
1 & 1 & 2 & 1 & 1 & 7 \\ 
1 & 1 & 1 & 3 & 1 & 9 \\ 
1 & 1 & 1 & 1 & 2 & 8 
\end{array} \right]$$

---

## 3. Penyelesaian Menggunakan OBE

### Langkah 1: Eliminasi Elemen di Bawah Pivot Pertama

Lakukan operasi pada baris kedua hingga kelima menggunakan baris pertama sebagai acuan:

* $R_2 = R_2 - 2R_1$
* $R_3 = R_3 - R_1$
* $R_4 = R_4 - R_1$
* $R_5 = R_5 - R_1$

Hasil matriks:


$$\left[ \begin{array}{ccccc|c} 
1 & 1 & 1 & 1 & 1 & 5 \\ 
0 & 1 & -1 & -1 & -1 & -2 \\ 
0 & 0 & 1 & 0 & 0 & 2 \\ 
0 & 0 & 0 & 2 & 0 & 4 \\ 
0 & 0 & 0 & 0 & 1 & 3 
\end{array} \right]$$

### Langkah 2: Mengubah Nilai Pivot Menjadi 1

Ubah elemen diagonal pada baris keempat agar bernilai 1:

* $R_4 = \frac{1}{2} R_4$

Hasil matriks akhir (Bentuk Eselon Baris):


$$\left[ \begin{array}{ccccc|c} 
1 & 1 & 1 & 1 & 1 & 5 \\ 
0 & 1 & -1 & -1 & -1 & -2 \\ 
0 & 0 & 1 & 0 & 0 & 2 \\ 
0 & 0 & 0 & 1 & 0 & 2 \\ 
0 & 0 & 0 & 0 & 1 & 3 
\end{array} \right]$$

---

## 4. Substitusi Balik (Back-Substitution)

Dari bentuk matriks eselon baris di atas, kita dapat langsung menentukan nilai variabel dari baris bawah ke atas:

* **Baris 5:** 
$$z = 3$$


* **Baris 4:** 
$$v = 2$$


* **Baris 3:** 
$$w = 2$$


* **Baris 2:** Masukkan nilai $w, v,$ dan $z$:

$$y - w - v - z = -2$$


$$y - 2 - 2 - 3 = -2$$


$$y - 7 = -2 \implies y = 5$$


* **Baris 1:** Masukkan nilai $y, w, v,$ dan $z$:

$$x + y + w + v + z = 5$$


$$x + 5 + 2 + 2 + 3 = 5$$


$$x + 12 = 5 \implies x = -7$$



---

## 5. Hasil Akhir

$$x = -7, \quad y = 5, \quad w = 2, \quad v = 2, \quad z = 3$$