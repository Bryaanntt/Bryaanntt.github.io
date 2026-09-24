---
title: "Week 2 — Limit Fungsi: Konsep, Limit Kiri-Kanan, dan Limit Aljabar"
date: 2026-09-23 09:00:00 +0700
categories: [Kalkulus, Jurnal Mingguan]
tags: [limit, limit-kiri-kanan, faktorisasi, merasionalkan, limit-aljabar, matematika]
pin: false
math: true
---

## Awal Cerita

Minggu kedua kalkulus, lanjut dari Fungsi ke Limit Fungsi. Kalau minggu lalu fokusnya "apa itu fungsi", minggu ini fokusnya "apa yang terjadi kalau $x$ mendekati suatu titik". Ternyata ini yang jadi dasar buat turunan nanti, jadi harus paham konsepnya, bukan cuma hafal langkah-langkahnya.

Di jurnal ini saya rangkum materinya, sekalian bahas latihan soal 15 nomor yang dikasih kemarin.

---

## 1. Limit Itu Apa

Limit itu menjelaskan nilai yang **didekati** suatu fungsi ketika variabel mendekati suatu titik tertentu, tanpa harus tepat berada di titik itu.

$$
\lim_{x \to a} f(x) = L
$$

Artinya, ketika nilai $x$ semakin mendekati $a$, maka nilai fungsi $f(x)$ semakin mendekati $L$.

> Yang penting: limit itu soal "mendekati", bukan soal "sama dengan". Fungsinya bisa saja tidak terdefinisi tepat di $x=a$, tapi limitnya tetap bisa ada.

---

## 2. Empat Jenis Limit

1. **Limit biasa** — substitusi langsung
2. **Limit kiri** ($x \to a^-$) — dari arah kiri
3. **Limit kanan** ($x \to a^+$) — dari arah kanan
4. **Limit aljabar** — perlu faktorisasi atau merasionalkan

### Limit Biasa

Kalau fungsinya polinom atau fungsi kontinu, limit bisa langsung dihitung pakai substitusi.

**Contoh**: $\displaystyle\lim_{x \to 2}(3x^2-5x+1) = 3(2)^2-5(2)+1 = 12-10+1 = 3$

---

## 3. Limit Kiri dan Limit Kanan

Dipakai kalau fungsinya berupa fungsi potongan (piecewise). Caranya: hitung limit dari masing-masing sisi, lalu bandingkan.

$$
\lim_{x \to a} f(x) \text{ ada} \iff \lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x)
$$

Kalau kedua sisi hasilnya beda, berarti limitnya **tidak ada** di titik itu.

**Contoh**: $f(x) = \begin{cases} x+2, & x<1 \\ 3x-1, & x \geq 1 \end{cases}$

- Limit kiri: $\lim_{x \to 1^-} f(x) = 1+2 = 3$
- Limit kanan: $\lim_{x \to 1^+} f(x) = 3(1)-1 = 2$
- Karena $3 \neq 2$, maka $\lim_{x \to 1} f(x)$ **tidak ada**.

---

## 4. Limit Aljabar dengan Faktorisasi

Kalau substitusi langsung menghasilkan bentuk $\frac{0}{0}$ (indeterminate), fungsinya harus disederhanakan dulu pakai faktorisasi, baru disubstitusi.

**Rumus penting**:
$$
a^2-b^2=(a-b)(a+b) \qquad a^3-b^3=(a-b)(a^2+ab+b^2)
$$

**Contoh**: $\displaystyle\lim_{x \to 3}\frac{x^2-9}{x-3} = \lim_{x \to 3}\frac{(x-3)(x+3)}{x-3} = \lim_{x \to 3}(x+3) = 6$

---

## 5. Limit Aljabar dengan Merasionalkan

Kalau ada bentuk akar yang menghasilkan $\frac{0}{0}$, dikalikan dengan sekawannya dulu.

**Rumus sekawan**:
$$
(\sqrt{A}-\sqrt{B})(\sqrt{A}+\sqrt{B}) = A-B
$$

**Contoh**: $\displaystyle\lim_{x \to 4}\frac{\sqrt{x}-2}{x-4} = \lim_{x \to 4}\frac{1}{\sqrt{x}+2} = \frac{1}{4}$

---

## 6. Strategi Menentukan Metode

| Bentuk fungsi | Metode |
|---|---|
| Fungsi kontinu (polinom) | Substitusi langsung |
| Fungsi potongan | Limit kiri dan kanan |
| Bentuk $\frac{0}{0}$ (polinom) | Faktorisasi |
| Bentuk $\frac{0}{0}$ (ada akar) | Merasionalkan |

**Checklist sebelum menjawab soal limit:**
- Sudah coba substitusi langsung?
- Apakah hasilnya bentuk $\frac{0}{0}$?
- Kalau fungsi potongan, sudah hitung limit kiri dan kanan?
- Kalau polinom, sudah difaktorkan?
- Kalau ada akar, sudah pakai sekawan?
- Substitusi baru dilakukan setelah bentuk disederhanakan.

**Kesalahan yang sering terjadi:**
1. Menganggap bentuk $\frac{0}{0}$ sama dengan nol.
2. Salah memilih rumus pada fungsi potongan.
3. Lupa menyederhanakan setelah faktorisasi.

---

## 7. Latihan Soal (15 Soal) — Sekalian Dibahas

**1.** $\displaystyle\lim_{x \to 2}(3x^2-5x+1)$
A. 1 B. 2 C. 3 D. 5 E. 7
> $3(2)^2-5(2)+1 = 12-10+1=3$. **Jawaban: C**

**2.** $\displaystyle\lim_{x \to -1}(2x^3+x^2-4)$
A. -3 B. -5 C. -6 D. -7 E. 5
> $2(-1)^3+(-1)^2-4 = -2+1-4=-5$. **Jawaban: B**

**3.** $\displaystyle\lim_{x \to 3}(x^3-2x^2+x-6)$
A. 8 B. 10 C. 11 D. 12 E. 15
> $3^3-2(3)^2+3-6 = 27-18+3-6=6$. Hasil substitusi langsungnya 6 — sepertinya ada salah ketik di pilihan jawaban aslinya karena tidak ada opsi yang cocok. Jawaban benarnya tetap **6**.

**4.** $f(x) = \begin{cases} x+2, & x<1 \\ 3x-1, & x \geq 1 \end{cases}$. Nilai $\displaystyle\lim_{x \to 1^-} f(x)$?
A. 1 B. 2 C. 3 D. 4 E. 5
> Dari kiri pakai $x+2$: $1+2=3$. **Jawaban: C**

**5.** Dengan fungsi pada soal nomor 4, tentukan $\displaystyle\lim_{x \to 1^+} f(x)$.
A. 1 B. 2 C. 3 D. 4 E. 5
> Dari kanan pakai $3x-1$: $3(1)-1=2$. **Jawaban: B**

**6.** $g(x) = \begin{cases} x^2, & x<2 \\ x+2, & x \geq 2 \end{cases}$. Nilai limit kiri dan kanan saat $x \to 2$ berturut-turut?
A. (2,4) B. (4,2) C. (4,4) D. (6,4) E. (4,6)
> Kiri: $2^2=4$. Kanan: $2+2=4$. **Jawaban: C**

**7.** $p(x) = \begin{cases} x^2-1, & x<2 \\ 5-x, & x \geq 2 \end{cases}$. Pernyataan yang benar mengenai limit saat $x \to 2$?
A. Kiri=3, kanan=3, limit ada B. Kiri=3, kanan=4, tidak ada C. Kiri=4, kanan=3, tidak ada D. Kiri=4, kanan=4, ada E. Kiri=5, kanan=3, tidak ada
> Kiri: $2^2-1=3$. Kanan: $5-2=3$. Sama, jadi limitnya ada. **Jawaban: A**

**8.** $\displaystyle\lim_{x \to 3}\frac{x^2-9}{x-3}$
A. 3 B. 5 C. 6 D. 8 E. 9
> $\frac{(x-3)(x+3)}{x-3}=x+3 \to 3+3=6$. **Jawaban: C**

**9.** $\displaystyle\lim_{x \to 2}\frac{x^2-4}{x-2}$
A. 2 B. 3 C. 4 D. 5
> $\frac{(x-2)(x+2)}{x-2}=x+2 \to 2+2=4$. **Jawaban: C**

**10.** $\displaystyle\lim_{x \to 1}\frac{x^3-1}{x-1}$
A. 1 B. 2 C. 3 D. 4 E. 5
> $\frac{(x-1)(x^2+x+1)}{x-1}=x^2+x+1 \to 1+1+1=3$. **Jawaban: C**

**11.** $\displaystyle\lim_{x \to -2}\frac{x^2+x-2}{x+2}$
A. -5 B. -4 C. -3 D. -2 E. -1
> $x^2+x-2=(x+2)(x-1)$, jadi $\frac{(x+2)(x-1)}{x+2}=x-1 \to -2-1=-3$. **Jawaban: C**

**12.** $\displaystyle\lim_{x \to 4}\frac{x^2-5x+4}{x-4}$
A. 1 B. 2 C. 3 D. 4 E. 5
> $x^2-5x+4=(x-4)(x-1)$, jadi $x-1 \to 4-1=3$. **Jawaban: C**

**13.** $\displaystyle\lim_{x \to 4}\frac{\sqrt{x}-2}{x-4}$
A. 1/8 B. 1/6 C. 1/4 D. 1/2 E. 1
> Kalikan sekawan: $\frac{1}{\sqrt{x}+2} \to \frac{1}{2+2}=\frac{1}{4}$. **Jawaban: C**

**14.** $\displaystyle\lim_{x \to 9}\frac{3-\sqrt{x}}{9-x}$
A. 1/3 B. 1/6 C. 1/9 D. 1/12 E. 1/18
> Kalikan sekawan: $\frac{1}{3+\sqrt{x}} \to \frac{1}{3+3}=\frac{1}{6}$. **Jawaban: B**

**15.** $\displaystyle\lim_{x \to 1}\frac{\sqrt{2x+7}-3}{x-1}$
A. 1/6 B. 1/3 C. 1/2 D. 2/3 E. 1
> Kalikan sekawan: $\frac{2(x-1)}{(x-1)(\sqrt{2x+7}+3)} = \frac{2}{\sqrt{2x+7}+3} \to \frac{2}{3+3}=\frac{1}{3}$. **Jawaban: B**

---

## 8. Dokumentasi

Beberapa foto pendukung selama belajar minggu ini:

![Materi di Papan](/assets/img/journal/week2/foto1week2.jpeg){: width="350" }

![Materi di Papan](/assets/img/journal/week2/foto2week2.jpeg){: width="350" }


---

## 9. Refleksi

Beberapa hal yang saya sadari minggu ini:

- Limit itu intinya soal mendekati, bukan soal harus terdefinisi tepat di titik itu — konsep ini penting supaya tidak asal substitusi.
- Untuk fungsi potongan, paling gampang salah kalau lupa cek dulu limit kiri dan kanannya sama atau tidak sebelum menyimpulkan limitnya ada.
- Faktorisasi dan merasionalkan itu intinya sama-sama cara menghindari bentuk $\frac{0}{0}$ — tinggal lihat bentuknya: polinom pakai faktorisasi, ada akar pakai sekawan.
- Dari 15 soal latihan kemarin, yang paling sering salah itu kalau terburu-buru substitusi tanpa cek dulu apakah hasilnya $\frac{0}{0}$.

**Yang masih agak susah**: soal nomor 3 sempat bikin bingung karena hasil hitungan saya tidak cocok sama pilihan jawaban yang ada — jadi belajar juga buat tetap percaya proses hitungnya sendiri daripada maksa nyocokin ke opsi.

**Target minggu depan**: mulai masuk ke turunan fungsi, dan lebih banyak latihan soal limit fungsi trigonometri kalau ada.

---

## 10. Referensi
- Materi kuliah: *Limit Fungsi* (Modul Teori Limit Fungsi, Week 2 — Kalkulus A)
- Latihan Soal Week 2 — Limit Fungsi (15 soal pilihan ganda)
- Diskusi kelas dan latihan mandiri

---

*Jurnal ini bagian dari tugas mingguan mata kuliah Kalkulus.*