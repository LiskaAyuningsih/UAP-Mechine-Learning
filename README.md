# UAP-Mechine-Learning



<h1 align="center">Tomato leaf disease classification using mobileNet and resnet models</h1>


# Deskripsi Proyek

klasifikasi penyakit daun tomat dikembangkan untuk mengatasi tantangan dalam mengidentifikasi dan mengelola penyakit tanaman secara manual. Dengan meningkatnya kebutuhan akan metode yang cepat dan akurat, pendekatan ini memanfaatkan dua model deep learning populer, MobileNet dan ResNet. MobileNet dikenal dengan efisiensinya, sementara ResNet unggul dalam performa klasifikasi yang andal. Dataset yang digunakan berasal dari platform Kaggle, yang menyediakan koleksi gambar daun tomat dengan berbagai jenis penyakit, memungkinkan analisis dan pelatihan model secara mendalam.

# Tujuan

1. Membandingkan performa dua model deep learning (MobileNet dan ResNet) dalam klasifikasi penyakit daun tomat.
2. Menghasilkan aplikasi web yang dapat digunakan untuk mendeteksi penyakit daun tomat secara langsung dari gambar.

# Sumber dataset 

dataset yang digunakan berasal dari kaggle dapat diakses melalui link berikut ini: https://www.kaggle.com/datasets/ashishmotwani/tomato



# Deskripsi Model

Model yang digunakan dalam proyek ini adalah mobileNet dan Resnet berikut penjelasan dari model tersebut:
1. MobileNetV2
   MobileNetV2 adalah model deep learning yang dirancang untuk efisiensi tinggi dengan mempertimbangkan perangkat yang memiliki keterbatasan sumber daya, seperti perangkat seluler. Model ini menggunakan inovasi berupa inverted residual blocks dan linear bottleneck yang memungkinkannya mempertahankan akurasi tinggi meskipun memiliki ukuran yang kecil dan komputasi yang ringan. Dalam proyek ini, MobileNetV2 digunakan dengan bobot awal yang dilatih pada dataset ImageNet. Bagian dasar model dibekukan untuk menjaga bobot pretrained, sedangkan lapisan tambahan di atasnya dilatih untuk menyesuaikan dengan dataset yang terdiri dari berbagai kategori gambar. Pendekatan ini memastikan bahwa MobileNetV2 dapat memberikan hasil yang optimal dalam waktu pelatihan yang lebih singkat dan penggunaan memori yang efisien.

   2. ResNet50
      ResNet50 adalah model deep learning yang populer untuk tugas klasifikasi gambar karena kemampuannya menangani jaringan yang sangat dalam tanpa menghadapi masalah vanishing gradient. Model ini memanfaatkan residual blocks dengan koneksi pintas (skip connections), yang memungkinkan pelatihan arsitektur lebih dalam dengan lebih stabil. Dalam proyek ini, ResNet50 digunakan dengan bobot pretrained dari ImageNet, di mana lapisan dasar dibekukan untuk mempertahankan fitur generik yang telah dipelajari, sementara lapisan tambahan dilatih untuk mendukung klasifikasi dataset spesifik. Dengan kemampuannya menangkap fitur kompleks, ResNet50 menjadi pilihan tepat untuk dataset yang membutuhkan model yang lebih kuat dalam menganalisis pola visual tingkat tinggi.
