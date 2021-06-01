---
layout: post
title: "Quantum & Superposition"
author: "1kb"
categories: journal
tags: [documentation,sample]
image: forest.jpg
---

Banyak orang yang menyalahpahami bahwa ilmu berkaitan dengan Komputasi Quantum terdengar seperti *lo-fi hip-hop* dari Mamang Kesbor, mengawang-awang. Ditambah lagi bahwa terkadang saya kurang puas dengan penjelasan dari buku-buku pop-science yang mencoba menjelaskan *Superposition*. Padahal sejatinya Komputasi Quantum adalah ilmu yang aksesibel dan dapat dipelajari dimana pun selama anda mampu menggunakan Google-Fu dengan baik.

Tulisan ini akan mencoba menjelaskan secara singkat bahwa bagian mendasar dari Komputasi Quantum (setidaknya *Superposition*) dapat mudah dimengerti, dengan catatan anda mengerti sedikit tentang bilangan biner, geometri, probabilitas dan menghitung matrix.

Langsung saja kita mulai penjelasan awamnya.

Setiap yang mempelajari tentang Komputasi Quantum tentunya pernah mendengar tentang Qubit. Namun apa itu Qubit?
Komputasi Digital mengenal istilah Bit, dimana direpresantasikan dengan 0 dan 1. 0 sebagai *Off*. 1 sebagai *On*.
Begitu juga dengan Qubit. Qubit, yang kependekan dari Quantum Bit, juga serupa dengan Bit yang ada di dunia Digital. Hanya saja, Qubit memiliki fitur yang dinamakan sebagai *superposition*, dimana sebuah Qubit bisa berada di dalam kondisi antara 0 dan 1. Atau bisa dituliskan sebagai:

<script type="math/tex; mode=display">
  |\psi \rangle = \alpha |0 \rangle + \beta |1 \rangle
</script>

$$|\psi \rangle$$ adalah yang tadi kita sebut sebagai *superposition*. Namun di ruas kanan dari persamaan di atas, kita bisa melihat angka 0 dan 1 dituliskan di antara notasi yang sama dengan yang digunakan oleh $$\psi$$ pada ruas kanan.
Notasi ini dikenal sebagai Notasi Dirac. Notasi ini menggambarkan keadaan 1 Qubit yang bisa saja bernilai 0 ataupun 1.

Sementara untuk memahami $$\alpha$$ dan $$\beta$$, kita perlu mengingat kembali Teorema Pythagoras.

<script type="math/tex; mode=display">
  a^2 + b^2 = c^2
</script>

Nah, $$\alpha$$ dan $$\beta$$ ini adalah bilangan kompleks, yang mana bisa kita gantikan posisinya daripada variabel a dan b pada teorema di atas. Namun, $$c^2$$ haruslah bernilai 1.

<script type="math/tex; mode=display">
  |\alpha|^2 + |\beta|^2 = 1
</script>

Sebagai contoh, bagaimana cara menggambarkan bahwa sebuah Qubit memiliki probabilitas $$\vert \alpha \vert^2 = 50\%$$ untuk keadaan $$\vert 0 \rangle$$ dan $$\vert \beta \vert^2 = 50\%$$ untuk keadaan $$\vert 1 \rangle$$ ?

Seperti yang kita tahu. Bahwa,
<script type="math/tex; mode=display">
  50\% + 50\% = 1
</script>

Karena itu, kita mulai menuliskannya dengan cara seperti berikut.
<script type="math/tex; mode=display">
  50\%|0\rangle + 50\%|1\rangle
</script>

Cara menulis kita di atas merupakan cara yang tidak konvensional untuk digunakan dalam menggambarkan kondisi superposisi. Oleh karenanya, mesti kita ubah lagi bentuknya.

Kita bisa menukar $$50\%$$ ke dalam bentuk lain agar bentuknya menjadi $$\alpha^2$$.
Tentunya kita bisa menuliskan menjadi,

<script type="math/tex; mode=display">
  \alpha ^2 = 50\% = \left(\sqrt \frac{1}{2}\right) ^2
</script>

Maka,
<script type="math/tex; mode=display">
  \alpha = \sqrt \frac{1}{2}
</script>

Dan ini pun berlaku pula pada $$\beta$$.

Oleh karenanya, kita bisa menuliskan contoh kasus di atas menjadi seperti berikut.

<script type="math/tex; mode=display">
  |\psi \rangle = \frac{1}{\sqrt 2} |0 \rangle + \frac{1}{\sqrt 2} |1 \rangle
</script>

Jadinya, kita baru saja merubahnya menjadi seperti berikut.

<script type="math/tex; mode=display">
    50\%|0\rangle + 50\%|1\rangle \xrightharpoonup{transformed} \frac{1}{\sqrt 2} |0 \rangle + \frac{1}{\sqrt 2} |1 \rangle
</script>

Komposisi dari *superposition* bisa saja bermacam-macam. Jika pada contoh di atas kita menggunakan komposisi $$50\%\vert 0\rangle + 50\%\vert 1\rangle$$ pada 1 Qubit, pada kasus lain komposisinya seperti berikut.

<script type="math/tex; mode=display">
    75\%|0\rangle + 25\%|1\rangle \xrightharpoonup{transformed} \frac{\sqrt 3}{2} |0 \rangle + \frac{1}{2} |1 \rangle
</script>

<script type="math/tex; mode=display">
    20\%|0\rangle + 80\%|1\rangle \xrightharpoonup{transformed} \sqrt\frac{1}{5} |0 \rangle + \frac{2}{\sqrt 5} |1 \rangle
</script>

<script type="math/tex; mode=display">
    60\%|0\rangle + 40\%|1\rangle \xrightharpoonup{transformed} \sqrt\frac{6}{10} |0 \rangle + \sqrt\frac{2}{5} |1 \rangle
</script>

<script type="math/tex; mode=display">
,etc.
</script>

Masih bingung dengan konsep di atas?

Jika masih di rasa sulit, karena konsep di atas berkaitan dengan Teorema Pythagoras, cukup bayangkan saja segitiga siku-siku yang sisi miringnya (*hypotenuse*) bernilai 1. Tugas kalian adalah mencari nilai sisi samping (*adjacent*) dan sisi depannya (*opposite*).
Nilai dari *adjacent* dan *opposite* itulah yang merupakan nilai dari $$\alpha$$ dan $$\beta$$.  

Saya yakin apabila pemahaman tentang geometri dasar dan probabilitas dasar kita cukup baik, sampai tahap ini tentunya tidak ada kesulitan berarti untuk memahami konsep ini.

Okay, pada 1 Qubit terdapat kondisi $$\vert 0\rangle$$ dan $$\vert 1\rangle$$. Bagaimana dengan jumlah Qubit yang lebih dari 1?

Pada bagian ini, setidaknya kita perlu memahami tentang konsep bilangan biner. Berikut adalah tablenya.

|Banyak Qubit|Banyak kondisi | Kondisi|
|---|---|---|
|1   |1|$$\vert 0\rangle , \vert 1\rangle$$   |
|2   |4|$$\vert 00\rangle , \vert 01\rangle , \vert 10\rangle , \vert 11\rangle$$|
|3   |8|$$\vert 000\rangle , \vert 001\rangle , \vert 010\rangle , \vert 011\rangle , \vert 100\rangle , \vert 101\rangle , \vert 110\rangle , \vert 111\rangle$$   |
|...   |...   |...   |
|x   |$$2^x$$   | etc.|

Meningkatnya jumlah Qubit membuat banyak kemungkinan kondisi juga ikut bertambah secara exponensial $$(2^x)$$. Jika kita telah memahami konsep bilangan biner, ini pun tidaklah terlalu sulit.

Kita akan masuk ke bagian yang agak *tricky*. Yaitu Matrix, sub-bagian dari Aljabar Linear.

Sedari tadi kita hanya menyebut kondisi dari 1 Qubit dengan $$\vert 0\rangle$$ dan $$\vert 1\rangle$$. Sejatinya Notasi Dirac tersebut bisa digambarkan dengan matrix seperti berikut.

<script type="math/tex; mode=display">
    |0\rangle \xrightharpoonup{equal} \begin{bmatrix} 1 \\ 0 \end{bmatrix}
</script>

<script type="math/tex; mode=display">
    |1\rangle \xrightharpoonup{equal} \begin{bmatrix} 0 \\ 1 \end{bmatrix}
</script>

Untuk 2 Qubit, maka seperti berikut.

<script type="math/tex; mode=display">
    |00\rangle \xrightharpoonup{equal} \begin{bmatrix} 1\\0\\0\\0 \end{bmatrix}
</script>

<script type="math/tex; mode=display">
    |01\rangle \xrightharpoonup{equal} \begin{bmatrix} 0\\1\\0\\0 \end{bmatrix}
</script>

<script type="math/tex; mode=display">
    |10\rangle \xrightharpoonup{equal} \begin{bmatrix} 0\\0\\1\\0 \end{bmatrix}
</script>

<script type="math/tex; mode=display">
    |11\rangle \xrightharpoonup{equal} \begin{bmatrix} 0\\0\\0\\1 \end{bmatrix}
</script>

Dengan contoh di atas, setidaknya kita bisa membayangkan bentuk matrixnya apabila Qubitnya berjumlah 3, 4, 5, dst.

Sekarang tugas kita adalah bagaimana caranya untuk membuat $$\vert 00 \rangle$$ menjadi ke kondisi superposisi $$\frac{1}{\sqrt 2}\vert 01 \rangle + \frac{1}{\sqrt 2}\vert 10 \rangle$$. Untuk mengubahnya kita memerlukan gerbang Quantum. Jadi, bisa digambarkan seperti ini.

<script type="math/tex; mode=display">
    |00\rangle \xrightharpoonup{quantum gate} \frac{1}{\sqrt 2}|01\rangle + \frac{1}{\sqrt 2}|10\rangle
</script>

Atau dalam bentuk matrix

<script type="math/tex; mode=display">
    \begin{bmatrix} 1\\0\\0\\0 \end{bmatrix} \xrightharpoonup{quantum gate} \begin{bmatrix} 0\\ \sqrt{1/2} \\ \sqrt{1/2} \\0 \end{bmatrix}
</script>

Gerbang Quantum yang dibutuhkan adalah matrix seperti berikut.

<script type="math/tex; mode=display">
    \begin{bmatrix} 0 & 1 & 0 & 0\\
    \sqrt{1/2} & 0 & \sqrt{1/2} & 0\\
    \sqrt{1/2} & 0 & -\sqrt{1/2} & 0\\
    0&0&0&1 \end{bmatrix}
</script>

Dengan mengalikan $$\vert 00\rangle$$ dengan matrix di atas, maka kita dapat membuat kondisi superposisi.

<script type="math/tex; mode=display">
    \begin{bmatrix} 0 & 1 & 0 & 0\\
    \sqrt{1/2} & 0 & \sqrt{1/2} & 0\\
    \sqrt{1/2} & 0 & -\sqrt{1/2} & 0\\
    0&0&0&1 \end{bmatrix} \times \begin{bmatrix} 1\\0\\0\\0 \end{bmatrix} = \begin{bmatrix} 0\\ \sqrt{1/2} \\ \sqrt{1/2} \\0 \end{bmatrix}
</script>

Begitulah sekiranya cara membuat membuat Qubit ke kondisi superposisi.
