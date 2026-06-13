# Tugas Determinan & Invers Matriks

## BAGIAN A: Menghitung Determinan Matriks (Ekspansi Baris)

### 1. Matriks $2 \times 2$

$$A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}$$

**Penyelesaian:**
Menggunakan ekspansi baris pertama ($i = 1$):

* $a_{11} = -7 \implies M_{11} = 4$
* $a_{12} = -5 \implies M_{12} = 1$

$$\det(A) = (-1)^{1+1}(-7)(4) + (-1)^{1+2}(-5)(1)$$

$$\det(A) = 1(-28) + (-1)(-5)$$

$$\det(A) = -28 + 5 = -23$$

---

### 2. Matriks $3 \times 3$

$$A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}$$

**Penyelesaian:**
Menggunakan ekspansi baris ketiga ($i = 3$) karena memiliki elemen nol terbanyak:

* $a_{31} = 0, \quad a_{32} = 0, \quad a_{33} = 1$
* Minor $M_{33}$:

$$M_{33} = \det\begin{bmatrix} 0 & 2 \\ 1 & -2 \end{bmatrix} = (0)(-2) - (2)(1) = -2$$



$$\det(A) = (-1)^{3+3} \cdot a_{33} \cdot M_{33}$$

$$\det(A) = (1)(1)(-2) = -2$$

---

### 3. Matriks $4 \times 4$

$$A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}$$

**Penyelesaian:**


$$\det(A) = -128$$

---

---

## BAGIAN B: Menghitung Invers Matriks (Metode Adjoint)

Rumus utama: $A^{-1} = \frac{1}{\det(A)} \text{adj}(A)$

### 1. Matriks $2 \times 2$

$$A = \begin{bmatrix} -7 & -5 \\ 1 & 4 \end{bmatrix}$$

**Penyelesaian:**

* Dari soal A.1, didapatkan $\det(A) = -23$
* Kofaktor:

$$C_{11} = 4, \quad C_{12} = -1, \quad C_{21} = 5, \quad C_{22} = -7$$


* Matriks Adjoint:

$$\text{adj}(A) = \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix}$$


* Invers Matriks:

$$A^{-1} = \frac{1}{-23} \begin{bmatrix} 4 & 5 \\ -1 & -7 \end{bmatrix} = \begin{bmatrix} -\frac{4}{23} & -\frac{5}{23} \\ \frac{1}{23} & \frac{7}{23} \end{bmatrix}$$



---

### 2. Matriks $3 \times 3$

$$A = \begin{bmatrix} 0 & 2 & -3 \\ 1 & -2 & -1 \\ 0 & 0 & 1 \end{bmatrix}$$

**Penyelesaian:**

* Dari soal A.2, didapatkan $\det(A) = -2$
* Nilai Kofaktor $C_{ij}$:
* $C_{11} = +((-2)(1) - (0)(-1)) = -2$
* $C_{12} = -((1)(1) - (0)(-1)) = -1$
* $C_{13} = +((1)(0) - (0)(-2)) = 0$
* $C_{21} = -((2)(1) - (0)(-3)) = -2$
* $C_{22} = +((0)(1) - (0)(-3)) = 0$
* $C_{23} = -((0)(0) - (0)(2)) = 0$
* $C_{31} = +((2)(-1) - (-2)(-3)) = -8$
* $C_{32} = -((0)(-1) - (1)(-3)) = -3$
* $C_{33} = +((0)(-2) - (1)(2)) = -2$


* Matriks Adjoint ($\text{adj}(A) = C^T$):

$$\text{adj}(A) = \begin{bmatrix} -2 & -2 & -8 \\ -1 & 0 & -3 \\ 0 & 0 & -2 \end{bmatrix}$$


* Invers Matriks:

$$A^{-1} = \frac{1}{-2} \begin{bmatrix} -2 & -2 & -8 \\ -1 & 0 & -3 \\ 0 & 0 & -2 \end{bmatrix} = \begin{bmatrix} 1 & 1 & 4 \\ 0.5 & 0 & 1.5 \\ 0 & 0 & 1 \end{bmatrix}$$



---

### 3. Matriks $4 \times 4$

$$A = \begin{bmatrix} 1 & -3 & 1 & 1 \\ -3 & 1 & 1 & 1 \\ 1 & 1 & -3 & 1 \\ 1 & 1 & 1 & -3 \end{bmatrix}$$

**Penyelesaian:**


$$A^{-1} = -\frac{1}{128} \text{adj}(A)$$