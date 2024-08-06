# Submission 2: Machine Learning Pipeline - Hotel Cancellation Prediction
Nama: Hanny

Username dicoding: hanhanhanny

![hotel booking](https://www.hotellinksolutions.com/images/blog/indirect-booking-or-direct-booking.jpg)

| | Deskripsi |
| ----------- | ----------- |
| Dataset | [Hotel Reservation Dataset](https://www.kaggle.com/datasets/ahsan81/hotel-reservations-classification-dataset) |
| Masalah | Di era digital saat ini, kemudahan memesan hotel secara online menjadi sangat populer. Namun, tingkat pembatalan pemesanan yang tinggi dapat merugikan pihak hotel karena berpotensi kehilangan pendapatan dan mengganggu perencanaan kapasitas. Selain itu, calon pelanggan lain yang ingin menginap bisa merasa dirugikan karena mengira hotel telah penuh. |
| Solusi machine learning | Untuk mengatasi masalah ini, saya mengembangkan model prediksi menggunakan machine learning yang dapat memprediksi apakah pelanggan akan membatalkan pemesanan atau tidak. Model ini membantu hotel untuk mengambil tindakan preventif dan mengoptimalkan manajemen reservasi mereka. |
| Metode pengolahan | Dataset yang digunakan memiliki 19 fitur, di mana fitur Booking_ID dihapus karena tidak relevan. Fitur target yaitu booking_status ditransformasi menjadi integer, dengan nilai 1 untuk pesanan yang tidak dibatalkan dan 0 untuk yang dibatalkan. Data kemudian dibagi menjadi set training dan testing dengan rasio 80:20, dan fitur-fitur dikategorikan menggunakan one-hot encoding untuk fitur kategorikal, normalisasi untuk fitur numerik, dan fitur tanggal dibiarkan tetap. |
| Arsitektur model | Arsitektur model yang digunakan adalah input layer dengan shape (17,), diikuti dengan beberapa Dense layer yang jumlah dan unitnya diacak menggunakan Tuner. Output dari model ini memiliki shape (1,) dengan fungsi aktivasi sigmoid, karena masalah ini merupakan Binary Classification. |
| Metrik evaluasi | Metrik evaluasi mencakup ExampleCount, AUC, FalsePositives, TruePositives, FalseNegatives, TrueNegatives, dan BinaryAccuracy. Metrik ini memberikan gambaran menyeluruh tentang kinerja model. |
| Performa model | Model ini mencapai val_binary_accuracy sebesar 0.7859 dan loss sebesar 0.4406. Hasil ini menunjukkan bahwa model memiliki tingkat akurasi yang cukup baik dalam memprediksi apakah pelanggan akan membatalkan pemesanan mereka. |
| Opsi Deployment | Model ini dideploy menggunakan platform Railway, yang memungkinkan model untuk diakses secara online dan diterapkan pada sistem reservasi hotel secara real-time. |
| Web App | https://hotel-cancellation-prediction-production.up.railway.app/v1/models/hr-model/metadata |
| Monitoring | Monitoring model ini dilakukan menggunakan Prometheus. Proses monitoring mencakup pemantauan jumlah permintaan (request) yang diterima oleh model, sehingga performa model dapat dievaluasi dan dioptimalkan secara berkelanjutan. |
