# Data Analisis dan Data Visualisasi untuk dataset Supermarket Customer
Additional Portofolio Capstone Project Modul 2 Purwadhika Job Connector Data Science Online Batch 15 (JCDSOL-015)
- Mochamad Aditya Putra
- Link Drive untuk penjelasan PPT:
  https://drive.google.com/file/d/1eyMCg-rroNzz1jNIKFkWgkvFrBDgpWgR/view?usp=sharing
- Link Drive untuk PPT:
  https://docs.google.com/presentation/d/1yjvG5Rbu35j1LL-Ugk5ycrUMSTz2IccZ/edit?usp=drive_link&ouid=115316219821335212082&rtpof=true&sd=true
- Link untuk google collab notebook:
  https://colab.research.google.com/drive/1OgbmvOuiL5LmcMg4hWDoMyzt5sOUyQW_?usp=sharing
- Link untuk Dashboard Tableau:
  https://public.tableau.com/app/profile/aditya.putra5948/viz/DashboardforSupermarketsManagement/CustomerBehaviorandChannelPerformanceDashboard2?publish=yes
- Link untuk Dashboard Power BI:
  https://drive.google.com/file/d/1eZgWbMMkgVmCsCUI5wN_r0GdooPXBnNX/view?usp=sharing

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
Kesimpulan dan Rekomendasi dapat dilihat pada link google collab.
