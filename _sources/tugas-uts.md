# TUGAS UTS DETERMINAN

## 1. Matriks A

$$A=\begin{bmatrix}a&b&c&d&e\\f&g&h&i&j\\k&l&m&n&o\\p&q&r&s&t\\u&v&w&x&y\end{bmatrix}$$

## 2. Determinan Matriks 5x5

Menggunakan ekspansi kofaktor pada baris pertama:


$$\text{det}(A)=aC_{11}-bC_{12}+cC_{13}-dC_{14}+eC_{15}$$


dengan:


$$C_{ij}=(-1)^{i+j}M_{ij}$$

## 3. Matriks Adjoin ($\text{adj } A$)

$\text{adj}(A)$ = transpose dari matriks kofaktor. Bentuk matriksnya:


$$\text{adj}(A)=\begin{bmatrix}C_{11}&C_{21}&C_{31}&C_{41}&C_{51}\\C_{12}&C_{22}&C_{32}&C_{42}&C_{52}\\C_{13}&C_{23}&C_{33}&C_{43}&C_{53}\\C_{14}&C_{24}&C_{34}&C_{44}&C_{54}\\C_{15}&C_{25}&C_{35}&C_{45}&C_{55}\end{bmatrix}$$

## 4. Invers Matriks

$$A^{-1}=\frac{1}{\text{det}(A)}\text{adj}(A)$$

## 5. Syarat Invers

$$\text{det}(A)\neq0$$


Jika $\text{det}(A) = 0 \rightarrow A$ tidak memiliki invers.

## 6. Bentuk Perhitungan Determinannya dari Eliminasi Gauss

### 1. Matriks A

Diketahui matriks:


$$A=\begin{bmatrix}1&0&0&0&0\\2&1&0&0&0\\0&3&1&0&0\\0&0&4&1&0\\0&0&0&5&1\end{bmatrix}$$


Matriks di atas merupakan matriks segitiga bawah (*lower triangular*), karena semua elemen di atas diagonal utama bernilai nol.

### 2. Determinan Matriks (dengan penjelasan)

Karena matriks merupakan matriks segitiga bawah, maka determinannya adalah hasil kali elemen diagonal utama:


$$\text{det}(A) = 1 \times 1 \times 1 \times 1 \times 1 = 1$$

### 3. Mencari Invers dengan Eliminasi Gauss-Jordan

Matriks augmentasi awal $[A \mid I]$:


$$\begin{bmatrix}1&0&0&0&0 &\mid& 1&0&0&0&0\\2&1&0&0&0 &\mid& 0&1&0&0&0\\0&3&1&0&0 &\mid& 0&0&1&0&0\\0&0&4&1&0 &\mid& 0&0&0&1&0\\0&0&0&5&1 &\mid& 0&0&0&0&1\end{bmatrix}$$

* **Langkah 1:** Hilangkan elemen di bawah pivot kolom 1 ($R_2 \leftarrow R_2-2R_1$)

$$\begin{bmatrix}1&0&0&0&0 &\mid& 1&0&0&0&0\\0&1&0&0&0 &\mid& -2&1&0&0&0\\0&3&1&0&0 &\mid& 0&0&1&0&0\\0&0&4&1&0 &\mid& 0&0&0&1&0\\0&0&0&5&1 &\mid& 0&0&0&0&1\end{bmatrix}$$


* **Langkah 2:** Hilangkan elemen di bawah pivot kolom 2 ($R_3 \leftarrow R_3-3R_2$)

$$\begin{bmatrix}1&0&0&0&0 &\mid& 1&0&0&0&0\\0&1&0&0&0 &\mid& -2&1&0&0&0\\0&0&1&0&0 &\mid& 6&-3&1&0&0\\0&0&4&1&0 &\mid& 0&0&0&1&0\\0&0&0&5&1 &\mid& 0&0&0&0&1\end{bmatrix}$$


* **Langkah 3:** Hilangkan elemen di bawah pivot kolom 3 ($R_4 \leftarrow R_4-4R_3$)

$$\begin{bmatrix}1&0&0&0&0 &\mid& 1&0&0&0&0\\0&1&0&0&0 &\mid& -2&1&0&0&0\\0&0&1&0&0 &\mid& 6&-3&1&0&0\\0&0&0&1&0 &\mid& -24&12&4&1&0\\0&0&0&5&1 &\mid& 0&0&0&0&1\end{bmatrix}$$


* **Langkah 4:** Hilangkan elemen di bawah pivot kolom 4 ($R_5 \leftarrow R_5-5R_4$)

$$\begin{bmatrix}1&0&0&0&0 &\mid& 1&0&0&0&0\\0&1&0&0&0 &\mid& -2&1&0&0&0\\0&0&1&0&0 &\mid& 6&-3&1&0&0\\0&0&0&1&0 &\mid& -24&12&4&1&0\\0&0&0&0&1 &\mid& 120&-60&20&-5&1\end{bmatrix}$$



### 4. Hasil Invers

Karena sisi kiri sudah menjadi matriks identitas, maka diperoleh $A^{-1}$ pada sisi kanan:


$$A^{-1}=\begin{bmatrix}1&0&0&0&0\\-2&1&0&0&0\\6&-3&1&0&0\\-24&12&4&1&0\\120&-60&20&-5&1\end{bmatrix}$$

### 5. Matriks Adjoin

Gunakan hubungan: $\text{adj}(A) = \text{det}(A) \cdot A^{-1}$
Karena $\text{det}(A) = 1$, maka $\text{adj}(A) = A^{-1}$.

### 6. Jawaban Akhir (Ringkas)

1. **Determinan:** $\text{det}(A) = 1$
2. **Adjoin:** 
$$\text{adj}(A) = \begin{bmatrix}1&0&0&0&0\\-2&1&0&0&0\\6&-3&1&0&0\\-24&12&4&1&0\\120&-60&20&-5&1\end{bmatrix}$$


3. **Invers:** $A^{-1} = \text{adj}(A)$