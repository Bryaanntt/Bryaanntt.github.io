---
title: "Week 1 — Fungsi: Domain, Kodomain, Range, Komposisi, dan Invers"
date: 2026-09-16 09:00:00 +0700
categories: [Kalkulus, Jurnal Mingguan]
tags: [fungsi, domain, kodomain, range, fungsi-komposisi, fungsi-invers, matematika]
pin: false
math: true
---

## Awal Cerita

Minggu pertama kalkulus, materinya itu adalah Fungsi. Kelihatannya gampang, tapi ini merupakan dasar buat materi selanjutnya — limit, turunan, integral, semua bergantung dari sini. Jadi harus paham betul dari awal, bukan cuma domain-kodomain-range, tapi komposisi sama invers juga.

Di jurnal ini saya rangkum apa yang dipelajari minggu ini, sekalian bahas quiz 20 soal yang dikasih kemarin.

---

## 1. Fungsi Itu Apa

Simplenya, fungsi itu aturan yang memasangkan tiap anggota di satu himpunan (namanya domain) ke satu anggota saja di himpunan lain (namanya kodomain).

Ditulisnya begini:

$$
f: A \rightarrow B, \quad f(x) = y
$$

- $A$ = domain (daerah asal)
- $B$ = kodomain (daerah kawan)
- $y = f(x)$ = hasil dari $x$ tadi

Yang penting diingat: satu $x$ cuma boleh punya satu pasangan $y$. Kalau ada $x$ yang punya dua pasangan atau lebih, berarti bukan fungsi, cuma relasi biasa.

> Ibaratnya kayak mesin. Masukin bahan ($x$), diproses, keluar hasilnya ($y$). Bahan yang sama harus keluar hasil yang sama juga.

---

## 2. Domain, Kodomain, Range — Sering Ketuker

Tiga istilah ini memang sering bikin bingung kalau tidak diingat baik-baik:

| Istilah | Maksudnya | Contoh (untuk $f(x) = x^2$, $x \in \mathbb{R}$) |
|---|---|---|
| **Domain** | Semua $x$ yang boleh dimasukkan | $\mathbb{R}$ |
| **Kodomain** | Himpunan tujuan yang ditetapkan dari awal (belum tentu semua kepakai) | $\mathbb{R}$ |
| **Range** | Nilai $y$ yang betul-betul keluar dari fungsinya | $[0, \infty)$ |

Intinya: range itu bagian dari kodomain, tapi belum tentu sama persis. Range adalah hasil yang betul-betul ada, kodomain adalah target yang sudah ditentukan dari awal.

### Contoh Biar Jelas

$f(x) = \sqrt{x}$
- **Domain**: $x \geq 0$ — karena akar dari angka negatif tidak terdefinisi
- **Kodomain**: misal ditetapkan $\mathbb{R}$
- **Range**: $y \geq 0$ — hasil akar tidak pernah negatif

Makanya cari domain itu harus hati-hati, apalagi kalau fungsinya ada akar, pecahan, atau log — ada nilai $x$ tertentu yang harus dihindari.

---

## 3. Fungsi Komposisi

Fungsi komposisi itu menggabungkan dua fungsi jadi satu fungsi baru, di mana hasil dari fungsi pertama jadi input untuk fungsi kedua.

$$
(g \circ f)(x) = g(f(x))
$$

Cara bacanya "$g$ komposisi $f$" — artinya $f(x)$ dihitung dulu, baru hasilnya dimasukkan ke $g$.

### Contoh

Misal $f(x) = 2x + 1$ dan $g(x) = x^2$:

$$
(g \circ f)(x) = g(2x+1) = (2x+1)^2
$$

Kalau dibalik urutannya:

$$
(f \circ g)(x) = f(x^2) = 2x^2 + 1
$$

Yang harus diingat: $(g \circ f)(x) \neq (f \circ g)(x)$. Urutannya kebalik, hasilnya beda. Jangan sampai ketuker.

---

## 4. Fungsi Invers

Fungsi invers, ditulis $f^{-1}$, itu kebalikan dari $f$. Kalau $f$ memetakan $x \to y$, berarti $f^{-1}$ memetakan $y \to x$.

$$
f(x) = y \quad \Longleftrightarrow \quad f^{-1}(y) = x
$$

### Syaratnya Apa

Supaya fungsi punya invers (yang juga fungsi), harus bijektif:
- **Injektif (satu-satu)**: tidak ada dua $x$ beda yang hasilnya sama
- **Surjektif**: semua elemen kodomain kepakai (range = kodomain)

### Cara Cari Invers

1. Tulis $y = f(x)$
2. Tukar $x$ sama $y$
3. Selesaikan untuk $y$
4. Itu dia $f^{-1}(x)$

**Contoh**: cari invers dari $f(x) = 2x + 3$

$$
y = 2x+3 \;\Rightarrow\; x = 2y+3 \;\Rightarrow\; y = \frac{x-3}{2}
$$

Jadi $f^{-1}(x) = \dfrac{x-3}{2}$.

Cara cek jawabannya gampang, tinggal pastikan $f(f^{-1}(x)) = x$ dan $f^{-1}(f(x)) = x$. Kalau dua-duanya cocok, berarti sudah benar.

---

## 5. Quiz Week 1 (20 Soal) — Sekalian Dibahas

Kemarin juga dikasih quiz 20 soal seputar materi ini. Saya tulis ulang soalnya di sini sekalian jawaban dan alasannya, biar jadi catatan belajar juga.

### A. Domain dan Range

**1.** $f(x) = \dfrac{2}{x-3}$. Domainnya?
A. $x \neq 2$ B. $x \neq 3$ C. $x > 3$ D. $x < 3$ E. $\mathbb{R}$
> Penyebut tidak boleh nol → $x \neq 3$. **Jawaban: B**

**2.** Domain dari $f(x) = \sqrt{5-x}$?
A. $x \geq 5$ B. $x \leq 5$ C. $x < 5$ D. $x \neq 5$ E. $\mathbb{R}$
> Dalam akar harus $\geq 0$ → $5-x \geq 0 \Rightarrow x \leq 5$. **Jawaban: B**

**3.** Range dari $f(x) = x^2+1$, domain $\mathbb{R}$?
A. $y \geq 0$ B. $y < 1$ C. $y \geq 1$ D. $y \leq 1$ E. $\mathbb{R}$
> Minimum $x^2$ itu 0, jadi minimum $f(x)$ adalah 1. **Jawaban: C**

**4.** $f(x) = 2x-5$, domain $-1 \leq x \leq 4$. Range-nya?
A. $-7 \leq y \leq 3$ B. $-3 \leq y \leq 8$ C. $-7 \leq y \leq 3$ D. $-5 \leq y \leq 3$ E. $3 \leq y \leq 8$
> Masukkan batas domainnya: $f(-1)=-7$, $f(4)=3$. **Jawaban: A**

**5.** Domain dari $f(x) = \dfrac{\sqrt{x+2}}{x-1}$?
A. $x \geq -2$ B. $x < -2$ C. $x \geq -2, x \neq 1$ D. $x \neq 1$ E. $\mathbb{R}$
> Ada dua syarat sekaligus: dalam akar $\geq 0$ ($x \geq -2$) dan penyebut $\neq 0$ ($x \neq 1$). **Jawaban: C**

### B. Invers Fungsi

**6.** Invers dari $f(x) = 2x+7$?
A. $\frac{x+7}{2}$ B. $\frac{x-7}{2}$ C. $2x-7$ D. $\frac{7-x}{2}$ E. $2x+7$
> $y=2x+7 \Rightarrow x = \frac{y-7}{2}$. **Jawaban: B**

**7.** $f(x) = \dfrac{x-4}{3}$, berarti $f^{-1}(x)$?
A. $3x-4$ B. $3x+4$ C. $\frac{x+4}{3}$ D. $\frac{x-4}{3}$ E. $4-3x$
> $y=\frac{x-4}{3} \Rightarrow x = 3y+4$. **Jawaban: B**

**8.** $f(x)=5x-2$, nilai $f^{-1}(18)$?
A. 2 B. 3 C. 4 D. 5 E. 6
> $f^{-1}(x)=\frac{x+2}{5}$, jadi $f^{-1}(18) = \frac{20}{5}=4$. **Jawaban: C**

**9.** $f(x)=x^2$ tidak punya invers di domain real karena...
A. tidak punya range B. tidak kontinu C. tidak satu-satu D. tidak terdefinisi E. tidak punya domain
> Contohnya $2$ dan $-2$ sama-sama hasilnya 4, jadi tidak injektif. **Jawaban: C**

**10.** $f(x) = \dfrac{3x+1}{2}$, nilai $f^{-1}(8)$?
A. 3 B. 4 C. 5 D. 6 E. 7
> $f^{-1}(x)=\frac{2x-1}{3}$, jadi $f^{-1}(8)=\frac{15}{3}=5$. **Jawaban: C**

### C. Fungsi Komposisi

**11.** $f(x)=2x+1$, $g(x)=x-3$. $(f \circ g)(x)$?
A. $2x-5$ B. $2x+4$ C. $x-2$ D. $2x-2$ E. $x+1$
> $f(x-3) = 2(x-3)+1 = 2x-5$. **Jawaban: A**

**12.** $f(x)=x^2$, $g(x)=x+2$. Nilai $(g \circ f)(3)$?
A. 9 B. 11 C. 13 D. 25 E. 27
> $f(3)=9$, lanjut $g(9)=11$. **Jawaban: B**

**13.** $f(x)=3x$, $g(x)=x+4$. $(g \circ f)(x)$?
A. $3x$ B. $3x+4$ C. $3x+12$ D. $x+12$ E. $7x$
> $g(3x) = 3x+4$. **Jawaban: B**

**14.** $f(x)=x-1$, $g(x)=2x$. Nilai $(f \circ g)(5)$?
A. 8 B. 9 C. 10 D. 11 E. 12
> $g(5)=10$, lanjut $f(10)=9$. **Jawaban: B**

**15.** $f(x)=x+1$, $g(x)=x^2$. $(f \circ g)(x)$?
A. $x^2$ B. $(x+1)^2$ C. $x^2+1$ D. $2x+1$ E. $x^2+x$
> $f(x^2)=x^2+1$. **Jawaban: C**

### D. Pemahaman Konsep

**16.** Soal pernyataan benar/salah soal domain (ada 4 pernyataan). Yang benar cuma soal domain sama dengan himpunan input, dan domain ditentukan dari syarat fungsi terdefinisi. **Jawaban: B (1 dan 3)**

**17.** Kenapa $f(x)=\sqrt{x-2}$ syaratnya $x \geq 2$?
> Karena nilai dalam akar harus $\geq 0$. **Jawaban: C**

**18.** Fungsi punya invers kalau...
> Setiap output cuma berasal dari satu input (fungsi satu-satu). **Jawaban: D**

**19.** Pernyataan benar soal $(f \circ g)(x)$?
> $g$ dihitung duluan, hasilnya baru jadi input untuk $f$. **Jawaban: B**

**20.** Pernyataan benar soal domain, range, invers, komposisi secara umum?
> Invers diperoleh dengan menukar peran input-output, tapi cuma berlaku untuk fungsi satu-satu. **Jawaban: D**

---

## 6. Dokumentasi

Beberapa foto pendukung selama belajar minggu ini:

![Catatan belajar](/assets/img/journal/week1/foto3w1.jpeg){: width="350" }

![Sesi mengerjakan quiz](/assets/img/journal/week1/foto2w1.jpeg){: width="350" }

![Suasana belajar](/assets/img/journal/week1/foto4w1.jpeg){: width="350" }

---

## 7. Refleksi

Beberapa hal yang saya sadari minggu ini:

- Domain-kodomain-range yang kelihatan sepele ini ternyata kepakai terus di materi limit sama turunan nanti — jadi memang harus paham betul dari sekarang.
- Fungsi komposisi bikin saya harus lebih teliti soal urutan, karena kebiasaan lama sering menyamakan $(f \circ g)$ sama $(g \circ f)$, padahal beda hasilnya.
- Cari invers paling gampang kalau dikerjakan langkah demi langkah (tukar $x$ sama $y$, baru diselesaikan), daripada maksa hafal rumus saja.
- Dari 20 soal quiz kemarin, yang paling bikin mikir itu bagian D (pemahaman konsep) — bukan soal hitungan, tapi memang menguji paham definisi atau tidak.

**Yang masih agak susah**: menentukan domain untuk fungsi gabungan, kayak soal nomor 5 tadi yang ada akar sekaligus pecahan — dua syarat harus digabung, ini yang paling gampang kelewat kalau terburu-buru.

**Target minggu depan**: lebih banyak latihan soal domain-range fungsi majemuk, terus mulai masuk materi limit fungsi.

---

## 8. Referensi
- Materi kuliah: *Fungsi* (Buku Penuntun, Week 1 — Kalkulus A)
- Quiz Week 1 — Fungsi (20 soal pilihan ganda)
- Diskusi kelas dan latihan mandiri

---

*Jurnal ini bagian dari tugas mingguan mata kuliah Kalkulus.*