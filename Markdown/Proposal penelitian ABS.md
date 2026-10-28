# **PROPOSAL PENELITIAN**

## Artificialobacterium syntheticum (ABS)



Pengembangan Platform Simulasi Biologis Multi-Spesies Berbasis Data Penelitian dan Pemodelan Komputasional



Bidang: Biologi Komputasional, Bioinformatika, dan Rekayasa Perangkat Lunak



Jenis Penelitian: Penelitian pengembangan (Research and Development) dengan pendekatan simulasi in silico.



##### 1\. Latar Belakang



Bakteri merupakan organisme uniseluler yang memiliki berbagai mekanisme biologis, seperti metabolisme, pertumbuhan, pembelahan sel, dan respons terhadap perubahan lingkungan. Mekanisme tersebut saling berkaitan dan memengaruhi kelangsungan hidup bakteri.



Kemajuan teknologi komputasi memungkinkan berbagai proses biologis direpresentasikan melalui model matematika dan simulasi komputer. Pendekatan ini memungkinkan peneliti mempelajari perilaku sistem biologis secara virtual tanpa harus selalu melakukan eksperimen langsung.



Berdasarkan hal tersebut, dirancang Artificialobacterium syntheticum (ABS), yaitu platform simulasi biologis multi-spesies yang bertujuan merepresentasikan mekanisme kehidupan bakteri menggunakan data penelitian ilmiah.



ABS direncanakan menggunakan Escherichia coli K-12 MG1655 dan Bacillus subtilis 168 sebagai model referensi awal. Melalui pendekatan modular, ABS diharapkan mampu menjalankan simulasi berbagai spesies bakteri tanpa perlu membangun ulang keseluruhan mesin simulasi.



##### 2\. Rumusan Masalah



Bagaimana merancang sistem simulasi komputer yang mampu merepresentasikan mekanisme biologis beberapa spesies bakteri secara modular?



Bagaimana hubungan antara ketersediaan nutrien, proses metabolisme, pertumbuhan biomassa, dan pembelahan sel dapat direpresentasikan secara matematis?



Bagaimana perbedaan karakteristik biologis antarspesies memengaruhi hasil simulasi pertumbuhan dan perubahan populasi?



Seberapa akurat hasil simulasi ABS apabila dibandingkan dengan data eksperimen dan model biologis dari penelitian ilmiah yang telah dipublikasikan?



Bagaimana pengaruh kompleksitas model dan jumlah sel terhadap efisiensi komputasi serta performa simulasi?



##### 3\. Tujuan Penelitian



###### 3.1 Tujuan Umum



Mengembangkan platform simulasi biologis multi-spesies berbasis komputer yang mampu merepresentasikan, mengamati, dan menganalisis perilaku bakteri melalui model matematika serta data penelitian ilmiah.



###### 3.2 Tujuan Khusus



Merancang arsitektur simulasi modular yang memungkinkan penggunaan beberapa model spesies bakteri dalam satu sistem.



Mengembangkan model komputasional yang menghubungkan penyerapan nutrien, metabolisme, pertumbuhan, dan pembelahan sel.



Menganalisis pengaruh perubahan kondisi lingkungan terhadap pertumbuhan dan dinamika populasi bakteri virtual.



Mengevaluasi kesesuaian hasil simulasi dengan data biologis yang tersedia melalui metode validasi kuantitatif.



Mengukur efisiensi pemrosesan, penggunaan memori, dan kemampuan sistem dalam mensimulasikan sejumlah besar sel.



##### 4\. Manfaat Penelitian

###### 

###### 4.1 Manfaat Teoretis



Memberikan kontribusi pada pemahaman mengenai penerapan model matematika dan sistem komputasional dalam merepresentasikan proses biologis mikroorganisme.



###### 4.2 Manfaat Praktis



Menghasilkan prototipe perangkat lunak yang dapat digunakan untuk melakukan eksperimen virtual, mengamati perubahan kondisi lingkungan, serta menganalisis dinamika pertumbuhan bakteri.



###### 4.3 Manfaat Pendidikan



Menyediakan media pembelajaran interaktif untuk memahami proses metabolisme, pertumbuhan, pembelahan sel, serta hubungan antara organisme dan lingkungannya.



###### 4.4 Manfaat Teknologi



Mengeksplorasi penggunaan Rust, pemrosesan numerik, dan arsitektur perangkat lunak modular dalam pengembangan mesin simulasi ilmiah yang efisien dan dapat dikembangkan.



##### 5\. Hipotesis Penelitian



Hipotesis awal yang akan diuji adalah:



H1: Arsitektur simulasi modular memungkinkan beberapa spesies bakteri direpresentasikan menggunakan mesin simulasi yang sama dengan parameter biologis berbeda.



H2: Perubahan ketersediaan nutrien menghasilkan perbedaan pola pertumbuhan dan dinamika populasi sesuai karakteristik model masing-masing spesies.



H3: Model yang dikalibrasi menggunakan data penelitian mampu menghasilkan prediksi pertumbuhan yang mendekati data eksperimen dalam kondisi yang sebanding.



Hipotesis tersebut belum dianggap terbukti sebelum pengujian dan validasi dilakukan.



##### 6\. Metode Penelitian



Penelitian dilaksanakan secara komputasional melalui tahapan berikut.



Studi literatur: Mengumpulkan informasi dan parameter biologis dari publikasi ilmiah, basis data metabolik, dan penelitian pemodelan sel.



Perancangan model: Menentukan representasi sel, kondisi lingkungan, variabel biologis, persamaan pertumbuhan, dan mekanisme pembelahan.



Pengembangan sistem: Mengimplementasikan mesin simulasi menggunakan Rust, dengan Python sebagai alat pendukung analisis ilmiah.



Eksperimen virtual: Menjalankan simulasi terhadap dua spesies referensi menggunakan variasi kondisi lingkungan yang telah ditentukan.



Validasi: Membandingkan hasil simulasi dengan data penelitian pada kondisi yang sesuai, menggunakan metrik kesalahan seperti RMSE, serta memeriksa konsistensi numerik dan keseimbangan massa.



Evaluasi: Menganalisis akurasi model, performa perangkat lunak, keterbatasan, dan kemungkinan pengembangan selanjutnya.



##### 7\. Batasan Penelitian



Penelitian dilakukan sepenuhnya melalui simulasi komputer tanpa eksperimen laboratorium biologis.



Spesies referensi awal dibatasi pada E. coli K-12 MG1655 dan B. subtilis 168.



Model awal berfokus pada metabolisme sederhana, penyerapan nutrien, pertumbuhan, dan pembelahan sel.



Pemodelan genom lengkap, seluruh reaksi molekuler, dan evolusi biologis belum termasuk cakupan awal.



Keakuratan hasil bergantung pada kualitas data, asumsi matematis, dan kondisi validasi.



Visualisasi digunakan sebagai alat pengamatan, bukan sebagai bukti keakuratan biologis.



##### 8\. Hasil yang Diharapkan



Penelitian diharapkan menghasilkan prototipe ABS yang mampu menjalankan simulasi sel individual dari beberapa spesies, menampilkan dinamika pertumbuhan dan populasi, serta menghasilkan data yang dapat dibandingkan dengan penelitian ilmiah.



Selain itu, penelitian diharapkan memberikan informasi mengenai kemampuan dan keterbatasan pendekatan komputasional dalam merepresentasikan sistem biologis sederhana.



##### 9\. Referensi Awal



Karr, J. R., dkk. (2012). A Whole-Cell Computational Model Predicts Phenotype from Genotype. Cell, 150(2), 389–401. https://doi.org/10.1016/j.cell.2012.05.044



BiGG Models. Escherichia coli K-12 MG1655: iML1515. https://bigg.ucsd.edu/models/iML1515



BiGG Models. Bacillus subtilis 168: iYO844. https://bigg.ucsd.edu/models/iYO844



SBML Community. Systems Biology Markup Language. https://sbml.org/

