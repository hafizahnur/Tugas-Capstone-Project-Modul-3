# Tugas-Capstone-Project-Modul-3-ML Travel Insurance

# Latar Belakang

Travel Insurance merupakan perusahaan asuransi perjalanan yang fokusnya adalah menawarkan perlindungan terhadap kejadian tidak terduga seperti kehilangan bagasi, sakit, atau kejadian lainnya saat berpergian. Dalam asuransi perjalanan penilaian klaim menjadi tantangan serius. Penting bagi perusahaan untuk cermat dalam menilai klaim agar dapat mengurangi beban, meningkatkan kinerja, menghemat waktu, dan memberikan layanan terbaik kepada pelanggan. 

# Pernyataan Masalah

Untuk memberikan perlindungan terhadap risiko perjalanan keluar negeri, perusahaan masih sering Kesulitan dalam mengidentifikasi pemegang polis mana yang berhak untuk mengklaim. Diperlukan solusi efisien untuk meningkatkan akurasi penilaian klaim, mengurangi beban keuangan, meningkatkan kinerja, dan kepuasan pelanggan.

# Tujuan

Perusahaan ingin mengembangkan prediksi klaim asuransi dan memahami faktor-faktor yang memotivasi calon pelaku perjalanan dalam mengajukan klaim untuk mengoptimalkan kebijakan premi, strategi pemasaran, dan kepuasan pelanggan.

# Pendekatan Analitik

Kita akan menganalisis data untuk mengidentifikasi pola pemenuhan syarat klaim asuransi pada calon pelaku perjalanan. Selanjutnya, kita akan membuat model klasifikasi untuk memprediksi probabilitas pelaku perjalanan memenuhi syarat klaim atau tidak.

# Metric

- **True Positif**: Calon pelaku perjalanan mengajukan klaim dan berhak menerima klaim, artinya prediksinya sesuai.

- **False Positif**: Calon pelaku perjalanan mengajukan klaim, tetapi model memprediksi bahwa calon pelaku perjalanan tidak berhak menerima klaim. Ini adalah tipe error 1.

- **False Negatif**: Calon pelaku perjalanan tidak mengajukan klaim, tetapi model memprediksi bahwa calon pelaku perjalanan berhak menerima klaim. Ini adalah tipe error 2.

- **True Negatif**: Calon perjalanan perjalanan tidak mengajukan klaim, dan model memprediksi dengan benar bahwa calon pelaku perjalanan tidak menerima klaim.


**Tipe error 1: False Positif**

Dampak: Kesalahan prediksi yang mengakibatkan penggunaan sumber daya yang tidak efisien, beban tambahan, dan potensi kerugian kinerja perusahaan asuransi terjadi karena calon pelaku perjalanan tidak mendapatkan klaim, meskipun telah mengajukannya. Hal ini dapat merugikan efisiensi operasional dan keuangan perusahaan.

**Tipe error 2: False Negative**

Dampak: Kesalahan prediksi yang menyebabkan menurunnya standar kualitas pelayanan asuransi untuk pelaku perjalanan. Calon pelaku perjalanan diharuskan untuk menerima klaim, meskipun sebenarnya tidak mengajukannya. Hal ini dapat merugikan reputasi perusahaan dan mempengaruhi kepercayaan pelanggan.


Dalam konteks ini, `Recall` adalah metrik evaluasi yang lebih relevan karena fokus pada mengurangi False Negatif (FN). Dengan meningkatkan `Recall`dapat membantu meminimalkan risiko kerugian reputasi dan kepercayaan pelaku perjalanan akibat kesalahan prediksi yang mengakibatkan pelaku perjalanan yang seharusnya berhak menerima klaim tidak mendapatkannya.

# Kesimpulan

Setelah dilakukan tuning terlihat skor recall untuk kelas positif kita meningkat sebesar 20%. Sehingga model ini  dapat membantu perusahaan dalam memprediksi pemegang polis yang berhak menerima klaim walaupun hanya sebesar 28

# Rekomendasi

Berdasarkan kesimpulan di atas kita dapat rekomendasi untuk meningkatkan recall prediksi model kita pada kelas positif, maka kita perlu melakukan evaluasi-evaluasi seperti:

- Evaluasi Model Lain:

Mempertimbangkan mencoba model klasifikasi yang berbeda dan kita bisa melihat apakah ada model lain yang memberikan hasil yang lebih baik, terutama dalam hal Recall untuk kelas minoritas.

- Fine-Tuning Model:

Melakukan fine-tuning terhadap hyperparameter model Anda atau eksplorasi lebih lanjut dalam pencarian hyperparameter untuk menemukan kombinasi yang lebih optimal.

- Evaluasi Fitur (Feature Engineering):

Melakukan analisis lebih lanjut terhadap fitur-fitur yang digunakan. Mungkin beberapa fitur tidak memberikan kontribusi signifikan atau ada hubungan non-linear yang tidak tertangkap.

- Pertimbangkan Model Ensemble:

Kita juga dapat mempertimbangkan teknik ensemble seperti penggabungan beberapa model untuk meningkatkan kinerja.
