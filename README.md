# Predict Loan Default Customers

## Problem Statement

Perusahaan multifinance perlu meningkatkan keakuratan penilaian risiko kredit untuk mengoptimalkan keputusan bisnis dan mengurangi kerugian. Kami mengembangkan model machine learning menggunakan data pinjaman dari Lending Club (2007-2014) untuk memprediksi risiko kredit, dengan fokus pada metrik bisnis seperti kerugian dan margin keuntungan bersih. Analisis data ini bertujuan untuk mengidentifikasi pola yang mengindikasikan pinjaman berpotensi buruk atau berisiko, tanpa asumsi yang kuat, untuk mendukung pengambilan keputusan investasi.

## Goals

- Loss Reduction, mengurangi dampak kerugian yang ditimbulkan oleh "Bad Customer" yang memiliki potensi gagal bayar.
- Memutuskan bahwa pengajuan pinjaman dapat diterima atau ditolak.

## Objectivness

- Membuat prediktif model untuk memprediksi dan mengklasifikasikan nasabah berpotensi gagal bayar atau tidak
- Mengidentifikasi karakteristik nasabah yang berpotensi gagal bayar.

## Insights

![Univariate_1](https://github.com/M-Fatoni/IDX_Partners/blob/main/img/LoanAmount.JPG)

![Univariate_2](https://github.com/M-Fatoni/IDX_Partners/blob/main/img/Term.JPG)

![Univariate_3](https://github.com/M-Fatoni/IDX_Partners/blob/main/img/HouseOwnership.JPG)

- Pengaruh Jangka Waktu Pinjaman: Pinjaman dengan jangka waktu lebih lama cenderung memiliki profil risiko yang lebih tinggi.
- Pengaruh Kepemilikan Rumah: Jenis kepemilikan rumah tertentu berkaitan dengan tingkat risiko pinjaman yang berbeda.
- Importansi Fitur: Variabel seperti total pembayaran yang diterima, pemulihan, dan tingkat bunga sangat mempengaruhi hasil pinjaman.

## Pemodelan & Evaluasi

![Univariate_3](https://github.com/M-Fatoni/IDX_Partners/blob/main/img/model_ml.JPG)

- Regresi Logistik: Mencapai akurasi tinggi (97.99%) dan AUC (99.29%), dengan presisi dan recall seimbang.
- SVM (Kernel Linear): Akurasi sedikit lebih rendah dibandingkan Regresi Logistik tetapi AUC tinggi (99.34%) dan recall yang kuat.
- Naive Bayes: Akurasi lebih rendah (91.97%) tetapi presisi sangat tinggi (97.31%) dan recall yang masuk akal.
- K Neighbors Classifier: Akurasi terendah di antara model (85.48%) dengan AUC sedang (86.24%) dan recall moderat.


