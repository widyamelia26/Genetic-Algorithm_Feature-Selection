# _Penerapan Genetic Algorithms untuk Seleksi Fitur pada Pemodelan Support Vector Machine (Studi Kasus: Faktor Risiko Diabetes)_

## Deskripsi
Pemodelan yang akurat untuk memprediksi risiko diabetes sangat penting dalam upaya pencegahan dan penanganannya. Namun, tingginya jumlah fitur atau variabel yang terlibat seringkali menyebabkan model menjadi kurang efisien dan rentan terhadap overfitting, sehingga seleksi fitur menjadi langkah krusial dalam proses pemodelan. Meskipun Support Vector Machine (SVM) telah terbukti efektif dalam klasifikasi penyakit, pemilihan fitur yang optimal masih menjadi tantangan.

## Dataset
Data diabetes dari Rumah Sakit di Sylhet, Bangladesh yang terdiri dari 16 fitur dan 1 keluaran. Seluruh fitur kecuali Age mempunyai output biner (1 atau 0).


## Metodologi 
1. Mengambil dataset diabetes dari UCI Machine Learning.
2. Melakukan preprocessing data untuk memastikan kualitas data sebelum digunakan dalam pemodelan.
3. Melakukan pemodelan awal dengan Support Vector Machine (SVM) menggunakan berbagai kernel (Linear, RBF, Sigmoid, Polynomial) tanpa seleksi fitur.
4. Melakukan proses seleksi fitur menggunakan Algoritma Genetika (GA):
   - **Inisialisasi Populasi**: Membuat populasi awal dengan representasi kromosom yang mewakili fitur.
   - **Evaluasi Fungsi Fitness**: Mengevaluasi setiap individu dalam populasi berdasarkan akurasi model SVM.
   - **Cek Kriteria Berhenti**: Mengecek apakah kriteria penghentian terpenuhi (misalnya, mencapai jumlah iterasi maksimum atau perubahan fitness yang kecil).
      - Jika *Ya*, lanjut ke pemodelan SVM dengan fitur terpilih.
      - Jika *Tidak*, lanjut ke langkah berikutnya.
   - **Seleksi Individu**: Memilih individu terbaik untuk generasi selanjutnya.
   - **Crossover**: Melakukan crossover pada individu terpilih untuk menghasilkan solusi baru.
   - **Mutasi**: Melakukan mutasi untuk meningkatkan keragaman populasi.
   - **Generasi Baru**: Menghasilkan populasi generasi baru dan kembali ke evaluasi fitness.
5. Melakukan pemodelan SVM dengan fitur-fitur yang telah dipilih melalui proses GA.
6. Penelitian selesai dengan pemodelan akhir yang optimal.


