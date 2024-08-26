# Data Analisis dan Data Visualisasi untuk dataset Supermarket Customer
Additional Portofolio Capstone Project Modul 2 Purwadhika Job Connector Data Science Online Batch 15 (JCDSOL-015)
- Mochamad Aditya Putra
- Link Drive untuk penjelasan PPT:
  https://drive.google.com/file/d/1eyMCg-rroNzz1jNIKFkWgkvFrBDgpWgR/view?usp=sharing
- Link untuk google collab notebook:
  https://colab.research.google.com/drive/1OgbmvOuiL5LmcMg4hWDoMyzt5sOUyQW_?usp=sharing
- Link untuk Dashboard Tableau:
  https://public.tableau.com/app/profile/aditya.putra5948/viz/SupermarketCustomerDashboard_17245985050640/Dashboard1?publish=yes
# Data Dictionary
|kolom | Penjelasan |
|----- | ---------- |
| ID | Pengidentifikasi unik pelanggan|
| Year_Birth| Tahun Customer lahir|
| Education| Tingkat Pendidikan Customer|
| Marital_Status | Status Pernikahan customer |
| Income| Pendapatan tahunan rumah tangga pelanggan|
| Kidhome | Jumlah anak di rumah pelanggan|
| Teenhome| Jumlah remaja di rumah pelanggan|
| Dt_Customer | Tanggal pendaftaran pelanggan dengan perusahaan|
| Recency | Jumlah hari sejak pembelian terakhir pelanggan|
| MntWines | Jumlah yang dibelanjakan untuk wine dalam 2 tahun terakhir|
| MntFruits| Jumlah yang dibelanjakan untuk buah-buahan dalam 2 tahun terakhir|
| MntMeatProducts| Jumlah yang dibelanjakan untuk jenis Daging dalam 2 tahun terakhir|
| MntFishProducts | Jumlah yang dibelanjakan untuk jenis Ikan dalam 2 tahun terakhir |
| MntSweetProducts| Jumlah yang dibelanjakan untuk jenis Permen dalam 2 tahun terakhir|
| MntGoldProds | Jumlah yang dibelanjakan untuk produk ber-label emas (produk premium) dalam 2 tahun terakhir|
| NumDealsPurchases| Jumlah pembelian yang dilakukan dengan diskon|
| NumWebPurchases | Jumlah pembelian yang dilakukan melalui situs web Perusahaan|
| NumCatalogPurchases | Jumlah pembelian yang dilakukan menggunakan katalog|
| NumStorePurchases| Jumlah pembelian yang dilakukan langsung di toko|
| NumWebVisitsMonth | Jumlah bulan kunjungan ke situs web perusahaan |
| AcceptedCmp3| 1 jika pelanggan menerima penawaran pada kampanye ke-3, 0 jika pelanggan tidak menerima penawaran|
| AcceptedCmp4 | 1 jika pelanggan menerima penawaran pada kampanye ke-4, 0 jika pelanggan tidak menerima penawaran|
| AcceptedCmp5| 1 jika pelanggan menerima penawaran pada kampanye ke-5, 0 jika pelanggan tidak menerima penawaran|
| AcceptedCmp1 | 1 jika pelanggan menerima penawaran pada kampanye ke-1, 0 jika pelanggan tidak menerima penawaran|
| AcceptedCmp2 | 1 jika pelanggan menerima penawaran pada kampanye ke-2, 0 jika pelanggan tidak menerima penawaran|
| Complain| 1 Jika pelanggan melakukan komplain pada 2 tahun terakhir, 0 jika pelanggan tidak melakukan komplain|
| Z_CostContact | Kolom ini diasumsikan merujuk pada biaya yang dikeluarkan untuk setiap kontak atau interaksi dengan pelanggan. Ini bisa mencakup biaya untuk mengirimkan email, menelepon pelanggan, atau aktivitas pemasaran lainnya. Biasanya, ini adalah biaya rata-rata yang terkait dengan mencapai atau menghubungi pelanggan dalam kampanye pemasaran.|
| Z_Revenue |Kolom ini diasumsikan merujuk pada pendapatan yang dihasilkan dari pelanggan yang dihubungi. Ini bisa mewakili pendapatan rata-rata yang diperoleh dari setiap kontak atau interaksi dengan pelanggan, terutama dalam konteks kampanye pemasaran.|
| Response | apakah pelanggan merespons atau menerima tawaran dalam kampanye pemasaran terakhir.|

# Background
Dalam industri ritel, pemahaman yang mendalam tentang pelanggan adalah kunci keberhasilan untuk meningkatkan penjualan dan mempertahankan loyalitas pelanggan. Supermarket yang beroperasi dalam lingkungan yang sangat kompetitif harus dapat mengenali pola belanja pelanggan mereka, mengidentifikasi segmen pasar yang berbeda, dan merespons kebutuhan dan preferensi pelanggan dengan tepat.

Dataset "Supermarket Customer" mengandung informasi penting mengenai demografi pelanggan, perilaku pembelian, respons terhadap kampanye promosi, dan preferensi produk.

Berikut beberapa fakta mengenai perilaku pembelian pelanggan supermarket di Eropa dan Amerika, yang membandingkan perilaku pembelian melalui Web, Katalog, dan Store (Toko Fisik):

- Eropa:
  - Perubahan Selama Pandemi: Di Eropa, khususnya selama pandemi COVID-19, terjadi lonjakan besar dalam pembelian online, terutama untuk kebutuhan pokok seperti makanan. Di Swedia, misalnya, pembelian online meningkat sebesar 49% pada tahun 2020 dibandingkan dengan tahun sebelumnya. Hal ini juga terlihat di Italia, di mana pembelian online meningkat 56% dari perkiraan awal 26%. Link artikel: [link text](https://link.springer.com/article/10.1007/s10660-024-09879-6)
  - Preferensi Produk Lokal dan Kesadaran Lingkungan: Konsumen di Eropa, terutama yang berbelanja online, cenderung memiliki kesadaran yang lebih tinggi terhadap lingkungan dan lebih memilih produk lokal. Hal ini karena produk lokal sering kali dianggap lebih ramah lingkungan dan mengurangi jejak karbon dibandingkan dengan produk yang diimpor. Link artikel: [link text](https://link.springer.com/article/10.1007/s10660-024-09828-3)

- Amerika Serikat:
  - Dominasi Belanja Online: Di Amerika Serikat, belanja online terus mendominasi terutama dalam kategori non-makanan, dengan Amazon memegang sekitar 40% dari penjualan online pada awal pandemi. Konsumen Amerika lebih sering beralih ke belanja online karena kemudahan dalam membandingkan harga dan ulasan produk dari berbagai sumber, yang jarang ditemukan di toko fisik. Link artikel: [link text](https://link.springer.com/article/10.1007/s10660-024-09879-6)
  - Interaksi Antar Saluran: Banyak konsumen di Amerika menggabungkan belanja online dan offline untuk mendapatkan manfaat maksimal. Misalnya, mereka sering mencari informasi produk secara online tetapi melakukan pembelian di toko fisik jika harga di sana lebih kompetitif atau jika mereka membutuhkan produk segera. Link artikel: [link text](https://link.springer.com/article/10.1007/s11116-020-10163-3)

# Problem Statement
Berdasarkan latar belakang di atas dan data set yang diberikan. Saya akan menganalis **'Apa perbedaan utama dalam perilaku pembelian antara Web vs Catalog vs Store?''**

Perilaku Pembelian pada web, catalog dan store:
* Dengan meningkatnya adopsi teknologi digital, pelanggan sekarang memiliki banyak pilihan untuk berbelanja baik secara online maupun offline. Menganalisis perbedaan perilaku antara pelanggan yang lebih suka berbelanja di web, catalog, dan store dapat membantu supermarket dalam mengoptimalkan strategi pemasaran dan operasi mereka.

Untuk analisis tentang perbedaan perilaku pembelian antara Web, Katalog, dan Toko Fisik, berikut beberapa referensi:

- Perbedaan Pengalaman Berbelanja Online vs Offline: Studi menunjukkan bahwa pengalaman belanja online dan offline memiliki beberapa perbedaan signifikan, terutama dalam hal kemudahan akses informasi, harga, dan kecepatan mendapatkan produk. Misalnya, belanja online menawarkan kemudahan untuk membandingkan produk dan harga, serta menghemat waktu dan biaya transportasi, sementara belanja offline memberikan keuntungan dalam hal segera mendapatkan produk setelah pembelian. Selain itu, harga produk di toko fisik cenderung lebih tinggi dibandingkan dengan harga online. Link artikel:[link text](https://link.springer.com/article/10.1007/s10660-024-09879-6) dan [link text](https://link.springer.com/article/10.1007/s11116-020-10163-3)

- Pilihan Saluran Belanja: Konsumen di negara berkembang menunjukkan preferensi yang bervariasi antara belanja online dan offline tergantung pada faktor-faktor seperti usia, orientasi terhadap kemudahan, dan tanggung jawab lingkungan. Konsumen yang lebih muda dan lebih berorientasi pada kemudahan cenderung lebih sering berbelanja online karena fleksibilitas dan kemudahan yang ditawarkan. Sebaliknya, konsumen yang lebih tradisional mungkin lebih memilih belanja di toko fisik atau melalui katalog. Link artikel:[link text](https://link.springer.com/article/10.1007/s11116-020-10163-3) dan [link text](https://link.springer.com/article/10.1007/s10660-024-09828-3)

- Perilaku Konsumen dalam Belanja Online dan Offline: Perilaku pembelian juga dipengaruhi oleh faktor-faktor seperti kesadaran lingkungan dan preferensi terhadap produk lokal. Konsumen yang berbelanja online sering kali lebih sadar lingkungan dan memiliki preferensi yang lebih kuat terhadap produk lokal dibandingkan dengan mereka yang hanya berbelanja secara offline. Ini bisa menjadi pertimbangan penting dalam analisis perilaku pembelian melalui saluran yang berbeda. Link artikel: [link text](https://link.springer.com/article/10.1007/s10660-024-09828-3)

# Kesimpulan dan Rekomendasi
Berdasarkan analisis yang dilakukan pada dataset "Supermarket Customer", untuk mencari perbedaan utama dalam perilaku pembelian antara Web vs Catalog vs Store. Dapat disimpulkan berdasarkan jawaban dari sub-pertanyaan dibawah bahwa perbedaan utama dalam perilaku pembelian adalah Frekuensi pembelian, Rata-rata pengeluaran per pembelian, Pengaruh Sosial (Complain), dan Kampanye Pemasaran.

Kesimpulan diatas terjawab oleh sub-pertanyaan berikut:

Apakah ada kecenderungan pelanggan untuk lebih sering membeli melalui satu kanal tertentu dibandingkan yang lain? Jika dilihat berdasarkan Histogram, ketika frekuensi pembelian berkisar antara 0 sampai 5 maka pelanggan cenderung melakukan pembelian pada kanal Catalog. Untuk frekuensi pembelian diatas 5 pelanggan cenderung memilih kanal Store. Untuk kanal Web frekuensi pembelian cenderung merata. Kesimpulannya adalah kecenderungan bagi pelanggan untuk lebih sering memilih Catalog ketika pembelian mereka sedikit, dan beralih ke Store ketika mereka melakukan lebih banyak pembelian. Kanal Web digunakan secara merata di berbagai tingkat frekuensi pembelian.

Apakah rata-rata pengeluaran per pembelian berbeda antara pelanggan yang membeli melalui Web, Catalog, dan Store? Jika dilihat berdasarkan Barplot, terdapat perbedaan rata-rata pengeluaran per pembelian dimana Catalog memiliki rata-rata terbesar yaitu 1.103,79, disusul oleh Store sebesar 821,07,dan yang terakhir Web sebesar 811,86

Apakah ada perbedaan dalam jenis produk yang lebih sering dibeli oleh pelanggan di web, catalog dan store? Jika dilihat berdasarkan Pie Chart, Tidak ada perbedaan dalam jenis produk yang dibeli pada kanal pembelian. Dimana Wine tetap mendominasi dengan presentase sekitar 50%, disusul oleh daging dengan presentase sekitar 27%. Untuk produk kualitas tinggi(gold) memiliki presentase sekitar 7%, untuk ikan memiliki presentase sekitar 6%, dan yang terakhir untuk buah dan makanan manis memiliki presentase sekitar 4%.

Bagaimana pengaruh diskon terhadap pilihan kanal pembelian (Web, Catalog, Store)? Jika dilhat berdasarkan Stackked Barchart, Diskon memiliki pengaruh signifikan dalam meningkatkan jumlah pembelian secara keseluruhan. Terlihat jelas bahwa semakin banyak jumlah pembelian dengan diskon, semakin tinggi pula total jumlah pembelian yang terjadi. Tetapi tujuan kita untuk mengetahui perbedaan utama dalam perilaku pembelian antar kanal, maka dari itu Diskon tidak menjadi perbedaan utama dalam perilaku pembelian pelanggan.

Seberapa besar pengaruh Complaints terhadap keputusan pembelian pelanggan? Jika dilihat berdasarkan BoxPlot, pelanggan yang tidak melakukan complain cenderung memiliki rata-rata pengeluaran yang relatif banyak dibandingkan dengan yang melakukan complain. Pada kanal Web rata-rata pengeluaran untuk yang tidak melakukan complain sebesar 2376 lalu yang melakukan complain sebesar 2287 dan pada kanal Catalog dan Store rata-rata pengeluaran untuk yang tidak melakukan complain sebesar 1537 lalu yang melakukan komplain sebesar 1143. Maka dari itu dapat disimpulkan bahwa complain memiliki pengaruh dalam keputusan pembelian pelanggan berdasarkan kanal pembelian.

Apakah ada perbedaan dalam karakteristik demografis pelanggan (misalnya, usia dan pendapatan) yang lebih memilih Web, Catalog, atau Store? Jika dilihat berdarkan Boxplot untuk karakteristik demografis berdasarkan usia, di setiap kanal terdapat pelanggan dengan rentang usia yang cukup luas mulai dari yang muda hingga yang tua. Dan jika dilihat berdasarkan Boxplot untuk karakteristik demografis berdasarkan income, Rentang pendapatan (termasuk outlier) untuk ketiga kanal juga terlihat cukup serupa. Ini menunjukkan bahwa variasi pendapatan pelanggan di antara ketiga kanal tidak terlalu berbeda. Maka dari itu dapat disimpulkan bahwa karakteristik demografis pelanggaan (usia dan pendapatan) tidak memiliki pengaruh terhadap perilaku pembelian pada kanal pembelian.

Bagaimana efektivitas kampanye pemasaran berbeda di antara Web, Catalog, dan Store? Jika dilihat berdasarkan Barplot untuk Efektivitas Kampanye Pemasaran Berdasarkan Kanal Pembelian, Store adalah kanal yang paling dominan dalam hal respons terhadap kampanye pemasaran dengan 3430 jumlah penerimaan kampanye, disusul oleh kanal Web yang memiliki 2590 jumlah penerimaan kampanye. Dan yang terakhir adalah kanal Catalog yang memiliki 2300 jumlah penerimaan kampanye. Maka dari itu dapat disimpulkan kampanye pemasaran merupakan salah satu perbedaan utama dalam perilaku pembelian pada kanal pembelian.

Untuk menetapkan target realistis dalam meningkatkan Frekuensi Pembelian, Rata-rata Pengeluaran, Pengaruh Sosial (Complaints), dan Efektivitas Kampanye Pemasaran dalam konteks supermarket, berikut ini adalah rekomendasinya:

Frekuensi Pembelian
Target: Tingkatkan tingkat pembelian ulang (repeat purchase rate) setidaknya 5-10% per tahun.

Strategi: Terapkan strategi keterlibatan pasca-pembelian yang dipersonalisasi. Ini bisa mencakup pengiriman pengingat yang ditargetkan berdasarkan pola pembelian pelanggan, seperti saran produk terkait. Selain itu, menggunakan otomatisasi pemasaran untuk memicu tindakan secara real-time dapat secara signifikan meningkatkan retensi pelanggan.

Rata-rata Pengeluaran per Pembelian
Target: Tetapkan tujuan untuk meningkatkan ukuran keranjang rata-rata sebesar 10-15%.

Strategi: Strategi cross-sell dan up-sell sangat efektif. Misalnya, memanfaatkan email transaksional untuk merekomendasikan produk pelengkap atau menawarkan paket bundling dan promosi dapat mendorong pengeluaran yang lebih tinggi per transaksi. Rekomendasi yang digerakkan oleh AI berdasarkan minat eksternal pelanggan juga dapat memperluas pengeluaran mereka di berbagai kategori produk.

Pengaruh Sosial (Complaints)
Target: Kurangi penurunan pembelian terkait keluhan sebesar 20%.

Strategi: Kembangkan pendekatan proaktif terhadap manajemen keluhan. Ini mencakup respon yang cepat terhadap keluhan dan menggunakan data dari keluhan untuk meningkatkan produk dan layanan. Pelanggan yang puas, terutama mereka yang masalahnya diselesaikan dengan efisien, lebih mungkin untuk terus berbelanja di Supermarket.

Efektivitas Kampanye Pemasaran
Target: Tingkatkan ROI kampanye sebesar 15-20% dan tingkatkan tingkat konversi dengan fokus pada audiens yang ditargetkan.

Strategi: Untuk mengukur dan meningkatkan efektivitas kampanye, tetapkan tujuan dan metrik yang jelas seperti ROI, tingkat konversi, dan biaya akuisisi pelanggan. Menggunakan kerangka pengukuran kampanye yang terstruktur dengan baik dapat membantu mengidentifikasi tren dan membuat penyesuaian berbasis data untuk mengoptimalkan kampanye yang sedang berjalan.

Link artikel: link text dan link text

Lalu Rekomendasi untuk mempertahankan serta meningkatkan faktor-faktor yang menjadi perbedaan utama dalam perilaku pembelian antara Web, Catalog, dan Store sebagai berikut:

Frekuensi Pembelian:
Catalog:
Target: Meningkatkan frekuensi pembelian menjadi rata-rata 6-8 kali per tahun per pelanggan.
Alasan: Dengan strategi pemasaran yang lebih personal, seperti katalog khusus dan penawaran eksklusif, peningkatan frekuensi ini bisa dicapai, terutama untuk pelanggan yang sudah terbiasa dengan kanal ini.
Store:
Target: Meningkatkan frekuensi pembelian menjadi rata-rata 7-10 kali per tahun per pelanggan.
Alasan: Dengan program loyalitas dan pengalaman berbelanja yang menarik di toko, mendorong pelanggan untuk lebih sering datang ke toko adalah target yang realistis.
Web:
Target: Menjaga dan sedikit meningkatkan frekuensi menjadi 5-7 kali per tahun.
Alasan: Karena frekuensi di Web sudah merata, fokus bisa diarahkan pada menjaga stabilitas ini dengan promosi online yang efektif.
Rata-rata Pengeluaran per Pembelian:
Catalog:
Target: Meningkatkan rata-rata pengeluaran menjadi 1.200 per pembelian.
Alasan: Dengan fokus pada produk premium dan bundling yang menarik, peningkatan ini bisa dicapai. Catalog sering kali menarik pelanggan yang lebih berorientasi pada kualitas dan nilai tinggi.
Store:
Target: Meningkatkan rata-rata pengeluaran menjadi 900 per pembelian.
Alasan: Pengalaman berbelanja fisik yang baik, ditambah dengan strategi cross-selling dan upselling yang efektif, dapat mendorong pelanggan untuk berbelanja lebih banyak.
Web:
Target: Meningkatkan rata-rata pengeluaran menjadi 850 per pembelian.
Alasan: Peningkatan ini bisa dicapai melalui personalisasi penawaran dan rekomendasi produk yang cerdas selama proses checkout.
Pengaruh Sosial (Complaints):
Web:
Target: Mengurangi complain sehingga rata-rata pengeluaran dari pelanggan yang tidak melakukan complain bisa mencapai 2851,2.
Alasan: Dengan peningkatan layanan pelanggan online, mengurangi complain dan menjaga kepuasan pelanggan adalah target yang realistis.
Catalog:
Target: Mengurangi complain sehingga rata-rata pengeluaran dari pelanggan yang tidak melakukan complain bisa mencapai 1844,4.
Alasan: Dengan pengiriman yang tepat waktu dan produk berkualitas, complain bisa dikurangi, dan kepuasan pelanggan akan meningkat.
Store:
Target: Mengurangi complain sehingga rata-rata pengeluaran dari pelanggan yang tidak melakukan complain bisa mencapai 1844,4.
Alasan: Dengan penanganan complain yang cepat dan efisien di toko, target ini bisa dicapai, menjaga pelanggan untuk kembali berbelanja.
Efektivitas Kampanye Pemasaran:
Store:
Target: Meningkatkan penerimaan kampanye pemasaran menjadi 3.800 penerimaan kampanye.
Alasan: Dengan promosi yang lebih intensif dan acara-acara di toko, respons terhadap kampanye dapat meningkat.
Web:
Target: Meningkatkan penerimaan kampanye pemasaran menjadi 2.900 penerimaan kampanye.
Alasan: Dengan strategi retargeting yang lebih baik dan personalisasi penawaran online, peningkatan ini bisa dicapai.
Catalog:
Target: Meningkatkan penerimaan kampanye pemasaran menjadi 2.500 penerimaan kampanye.
Alasan: Mengirim katalog dengan lebih sering dan menyertakan penawaran menarik bisa meningkatkan efektivitas kampanye di kanal ini.
Target-target ini dibuat berdasarkan peningkatan yang realistis dengan mempertimbangkan potensi pasar dan bisnis di industri supermarket. Peningkatan ini diharapkan bisa dicapai dengan implementasi strategi pemasaran yang tepat dan optimalisasi pengalaman pelanggan di masing-masing kanal.
