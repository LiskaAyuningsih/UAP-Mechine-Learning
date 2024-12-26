# UAP-Mechine-Learning



<h1 align="center">Tomato leaf disease classification using mobileNet and resnet models</h1>


# Deskripsi Proyek

klasifikasi penyakit daun tomat dikembangkan untuk mengatasi tantangan dalam mengidentifikasi dan mengelola penyakit tanaman secara manual. Dengan meningkatnya kebutuhan akan metode yang cepat dan akurat, pendekatan ini memanfaatkan dua model deep learning populer, MobileNet dan ResNet. MobileNet dikenal dengan efisiensinya, sementara ResNet unggul dalam performa klasifikasi yang andal. Dataset yang digunakan berasal dari platform Kaggle, yang menyediakan koleksi gambar daun tomat dengan berbagai jenis penyakit, memungkinkan analisis dan pelatihan model secara mendalam.

# Tujuan

1. Membandingkan performa dua model deep learning (MobileNet dan ResNet) dalam klasifikasi penyakit daun tomat.
2. Menghasilkan aplikasi web yang dapat digunakan untuk mendeteksi penyakit daun tomat secara langsung dari gambar.

# Sumber dataset 

Dataset "Tomato" yang diambil dari Kaggle berisi koleksi gambar daun tomat yang digunakan untuk mendeteksi dan mengklasifikasikan berbagai jenis penyakit tanaman tomat serta kondisi daunnya yang sehat. Dataset ini terdiri dari beberapa kelas, yaitu: bacterial spot, early blight, healthy, late blight, leaf mold, mosaic virus, septoria leaf spot, dan yellow leaf curl virus. Dengan jumlah total 25851 gambar, dataset ini memiliki resolusi gambar yang seragam, sehingga cocok untuk berbagai aplikasi pembelajaran mesin berbasis visi komputer. Link dataset dapat diakses melalui link berikut ini: https://www.kaggle.com/datasets/ashishmotwani/tomato



# Deskripsi Model

Model yang digunakan dalam proyek ini adalah mobileNet dan Resnet berikut penjelasan dari model tersebut:
1. MobileNetV2
   MobileNetV2 adalah model deep learning yang dirancang untuk efisiensi tinggi dengan mempertimbangkan perangkat yang memiliki keterbatasan sumber daya, seperti perangkat seluler. Model ini menggunakan inovasi berupa inverted residual blocks dan linear bottleneck yang memungkinkannya mempertahankan akurasi tinggi meskipun memiliki ukuran yang kecil dan komputasi yang ringan. Dalam proyek ini, MobileNetV2 digunakan dengan bobot awal yang dilatih pada dataset ImageNet. Bagian dasar model dibekukan untuk menjaga bobot pretrained, sedangkan lapisan tambahan di atasnya dilatih untuk menyesuaikan dengan dataset yang terdiri dari berbagai kategori gambar. Pendekatan ini memastikan bahwa MobileNetV2 dapat memberikan hasil yang optimal dalam waktu pelatihan yang lebih singkat dan penggunaan memori yang efisien.

2. ResNet50
   ResNet50 adalah model deep learning yang populer untuk tugas klasifikasi gambar karena kemampuannya menangani jaringan yang sangat dalam tanpa menghadapi masalah vanishing gradient. Model ini memanfaatkan residual blocks dengan koneksi pintas (skip connections), yang memungkinkan pelatihan arsitektur lebih dalam dengan lebih stabil. Dalam proyek ini, ResNet50 digunakan dengan bobot pretrained dari ImageNet, di mana lapisan dasar dibekukan untuk mempertahankan fitur generik yang telah dipelajari, sementara lapisan tambahan dilatih untuk mendukung klasifikasi dataset spesifik. Dengan kemampuannya menangkap fitur kompleks, ResNet50 menjadi pilihan tepat untuk dataset yang membutuhkan model yang lebih kuat dalam menganalisis pola visual tingkat tinggi.




# Analisis Ferforma Model 

MobileNetV2 dirancang untuk kecepatan dan efisiensi komputasi, yang membuatnya cocok untuk perangkat dengan sumber daya terbatas, seperti ponsel atau perangkat IoT. Dalam penelitian ini, MobileNetV2 menunjukkan performa yang kompetitif dalam mengklasifikasikan dataset daun tomat dengan tingkat akurasi tinggi. Keunggulannya terletak pada arsitektur depthwise separable convolutions, yang mengurangi jumlah parameter dan operasi tanpa mengorbankan akurasi secara signifikan. Meskipun cepat dan ringan, performanya pada dataset yang lebih kompleks mungkin sedikit tertinggal dibandingkan model yang lebih besar, seperti ResNet50.

ResNet50 adalah model berbasis deep residual learning yang dirancang untuk menangani masalah degradasi dalam pelatihan jaringan dalam yang sangat dalam. Dalam analisis dataset daun tomat, ResNet50 sering memberikan hasil yang lebih akurat dibandingkan MobileNetV2 karena kemampuannya untuk menangkap fitur yang lebih kompleks melalui arsitekturnya yang dalam. Namun, model ini membutuhkan sumber daya komputasi lebih besar untuk pelatihan dan inferensi, menjadikannya lebih cocok untuk aplikasi di server atau sistem dengan daya komputasi tinggi.

Dalam eksperimen ini, kedua model dievaluasi berdasarkan akurasi, loss, dan kecepatan pelatihan. ResNet50 menghasilkan akurasi lebih tinggi, khususnya pada dataset validasi, karena kemampuannya menangkap detail gambar yang kompleks. Sementara itu, MobileNetV2 unggul dalam efisiensi waktu pelatihan, membuatnya pilihan ideal untuk aplikasi real-time atau skala besar dengan sumber daya terbatas.
