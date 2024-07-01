# Predict Loan Default Customers

## Problem Statement

Perusahaan multifinance perlu meningkatkan keakuratan penilaian risiko kredit untuk mengoptimalkan keputusan bisnis dan mengurangi kerugian. Kami mengembangkan model machine learning menggunakan data pinjaman dari Lending Club (2007-2014) untuk memprediksi risiko kredit, dengan fokus pada metrik bisnis seperti kerugian dan margin keuntungan bersih. Analisis data ini bertujuan untuk mengidentifikasi pola yang mengindikasikan pinjaman berpotensi buruk atau berisiko, tanpa asumsi yang kuat, untuk mendukung pengambilan keputusan investasi.

**Deskripsi Kolom-Kolom Dari Dataset Pinjaman:**
    
`loan_amnt`: Jumlah total pinjaman yang diminta oleh peminjam.

`funded_amnt`: Jumlah total pinjaman yang didanai oleh investor.

`funded_amnt_inv`: Jumlah pinjaman yang didanai oleh investor individual.

`term`: Jangka waktu pelunasan pinjaman dalam bulan (contoh: 36 atau 60 bulan).

`int_rate`: Suku bunga pinjaman dalam persentase.

`installment`: Jumlah cicilan bulanan yang harus dibayar oleh peminjam.

`grade`: Peringkat kredit yang diberikan kepada peminjam oleh platform pinjaman.

`sub_grade`: Sub-peringkat kredit yang lebih rinci.

`emp_title`: Judul pekerjaan peminjam.

`emp_length`: Lama bekerja peminjam dalam tahun.

`home_ownership`: Status kepemilikan rumah peminjam (contoh: Rent, Own, Mortgage).

`annual_inc`: Penghasilan tahunan peminjam.

`verification_status`: Status verifikasi penghasilan peminjam.

`issue_d`: Tanggal penerbitan pinjaman.

`loan_status`: Status pinjaman (contoh: Fully Paid, Charged Off, Current).

`pymnt_plan`: Apakah ada rencana pembayaran (biasanya 'n' untuk tidak).

`url`: URL untuk detail pinjaman.

`desc`: Deskripsi pinjaman yang diberikan oleh peminjam.

`purpose`: Tujuan pinjaman (contoh: debt consolidation, home improvement).

`title`: Judul pinjaman yang diberikan oleh peminjam.

`zip_code`: Kode pos tempat tinggal peminjam.

`addr_state`: Negara bagian tempat tinggal peminjam.

`dti`: Debt-to-income ratio, rasio antara total utang dengan penghasilan peminjam.

`delinq_2yrs`: Jumlah kejadian gagal bayar dalam 2 tahun terakhir.

`earliest_cr_line`: Tanggal pembukaan rekening kredit pertama peminjam.

`inq_last_6mths`: Jumlah permintaan kredit dalam 6 bulan terakhir.

`mths_since_last_delinq`: Jumlah bulan sejak kejadian gagal bayar terakhir.

`mths_since_last_record`: Jumlah bulan sejak catatan kredit buruk terakhir.

`open_acc`: Jumlah akun kredit terbuka.

`pub_rec`: Jumlah catatan publik negatif (contoh: kebangkrutan, lien).

`revol_bal`: Saldo kredit bergulir (revolving balance).

`revol_util`: Persentase penggunaan kredit bergulir.

`total_acc`: Jumlah total akun kredit.

`initial_list_status`: Status daftar awal pinjaman (contoh: f untuk whole loan, w untuk fractional).

`out_prncp`: Prinsipal yang tersisa dari pinjaman.

`out_prncp_inv`: Prinsipal yang tersisa dari pinjaman bagi investor.

`total_pymnt`: Jumlah total pembayaran yang telah dilakukan.

`total_pymnt_inv`: Jumlah total pembayaran yang telah dilakukan oleh investor.

`total_rec_prncp`: Jumlah total prinsipal yang telah diterima kembali.

`total_rec_int`: Jumlah total bunga yang telah diterima kembali.

`total_rec_late_fee`: Jumlah total denda keterlambatan yang telah diterima.

`recoveries`: Jumlah yang telah dipulihkan dari pinjaman yang gagal bayar.

`collection_recovery_fee`: Biaya pemulihan dari koleksi pinjaman yang gagal bayar.

`last_pymnt_d`: Tanggal pembayaran terakhir.

`last_pymnt_amnt`: Jumlah pembayaran terakhir.

`next_pymnt_d`: Tanggal pembayaran berikutnya (jika ada).

`last_credit_pull_d`: Tanggal penarikan laporan kredit terakhir.

`collections_12_mths_ex_med`: Jumlah koleksi dalam 12 bulan terakhir, kecuali koleksi medis.

`mths_since_last_major_derog`: Jumlah bulan sejak kejadian kredit buruk besar terakhir.

`policy_code`: Kode kebijakan pinjaman.

`application_type`: Tipe aplikasi (contoh: Individual, Joint).

`acc_now_delinq`: Jumlah akun yang sedang gagal bayar.

`tot_coll_amt`: Jumlah total koleksi.

`tot_cur_bal`: Jumlah total saldo saat ini.

`total_rev_hi_lim`: Batas kredit bergulir tertinggi.

## Goals

- Loss Reduction, mengurangi dampak kerugian yang ditimbulkan oleh "Bad Customer" yang memiliki potensi gagal bayar.
- Memutuskan bahwa pengajuan pinjaman dapat diterima atau ditolak.

## Objectivness

- Membuat prediktif model untuk memprediksi dan mengklasifikasikan nasabah berpotensi gagal bayar atau tidak
- Mengidentifikasi karakteristik nasabah yang berpotensi gagal bayar.

## Insights

- Pengaruh Jangka Waktu Pinjaman: Pinjaman dengan jangka waktu lebih lama cenderung memiliki profil risiko yang lebih tinggi.
- Pengaruh Kepemilikan Rumah: Jenis kepemilikan rumah tertentu berkaitan dengan tingkat risiko pinjaman yang berbeda.
- Importansi Fitur: Variabel seperti total pembayaran yang diterima, pemulihan, dan tingkat bunga sangat mempengaruhi hasil pinjaman.

## Pemodelan & Evaluasi

- Regresi Logistik: Mencapai akurasi tinggi (97.99%) dan AUC (99.29%), dengan presisi dan recall seimbang.
- SVM (Kernel Linear): Akurasi sedikit lebih rendah dibandingkan Regresi Logistik tetapi AUC tinggi (99.34%) dan recall yang kuat.
- Naive Bayes: Akurasi lebih rendah (91.97%) tetapi presisi sangat tinggi (97.31%) dan recall yang masuk akal.
- K Neighbors Classifier: Akurasi terendah di antara model (85.48%) dengan AUC sedang (86.24%) dan recall moderat.


