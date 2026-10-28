
# PROTOKOL EKSPERIMEN ABS-EXP-001

**Judul:** Analisis Pertumbuhan _Escherichia coli_ K-12 MG1655 pada Kondisi Nutrien Sedang Menggunakan Model Biologis Komputasional

**Platform:** Artificialobacterium syntheticum (ABS)  
**Versi:** Research Protocol 0.1  
**Metode:** Simulasi _in silico_  
**Status:** Perencanaan, belum implementasi

## 1. Pertanyaan Penelitian

Bagaimana perubahan biomassa, ketersediaan nutrien, dan laju pertumbuhan _E. coli_ K-12 MG1655 selama 12 jam simulasi ketika ditempatkan dalam lingkungan virtual dengan konsentrasi glukosa awal 2,0 g/L?

## 2. Tujuan Eksperimen

1.  Memodelkan pertumbuhan biomassa bakteri berdasarkan ketersediaan glukosa.
    
2.  Mensimulasikan konsumsi nutrien secara dinamis.
    
3.  Menghitung laju pertumbuhan spesifik dan waktu penggandaan biomassa.
    
4.  Membandingkan pertumbuhan yang diprediksi dengan data pengamatan biologis.
    
5.  Menguji kestabilan numerik dan konsistensi neraca substrat-biomassa.
    

## 3. Hipotesis

**H1:** Biomassa meningkat selama nutrien tersedia dan kondisi model mendukung pertumbuhan.

**H2:** Penurunan konsentrasi glukosa menuju nol menyebabkan laju pertumbuhan menurun.

**H3:** Setelah parameter model dikalibrasi, laju pertumbuhan selama fase eksponensial dapat mendekati pengamatan yang dipublikasikan untuk strain dan kondisi nutrisi yang sebanding.

Hipotesis ini akan dievaluasi, bukan diasumsikan benar.

## 4. Desain Lingkungan Virtual

Parameter

Kondisi awal

Organisme

E. coli K-12 MG1655

Medium referensi

Minimal M9

Sumber karbon

Glukosa

Glukosa awal

2,0 g/L

Temperatur

37°C, konstan

pH

7,0, konstan

Oksigen

Diasumsikan tidak membatasi

Nutrien lain

Diasumsikan mencukupi

Sistem

Batch tertutup untuk glukosa

Lama simulasi

12 jam

Interval output

10 menit

**Catatan:** Nilai temperatur, pH, dan asumsi oksigen merupakan kondisi desain simulasi. Kecocokannya dengan setiap dataset referensi harus diperiksa sebelum validasi kuantitatif.

## 5. Variabel Penelitian

**Variabel bebas:**

-   Konsentrasi glukosa awal, ditetapkan sebesar 2,0 g/L.
    

**Variabel terikat:**

-   Biomassa bakteri (gDW/L).
    
-   Konsentrasi glukosa tersisa (g/L).
    
-   Laju pertumbuhan spesifik (jam⁻¹).
    
-   Waktu penggandaan biomassa (menit).
    
-   Jumlah sel virtual, apabila model pembelahan individual telah terkalibrasi.
    

**Variabel terkendali:**

-   Strain bakteri.
    
-   Temperatur dan pH.
    
-   Kondisi ketersediaan oksigen.
    
-   Komposisi lingkungan selain glukosa.
    
-   Model matematika dan aturan integrasi numerik.
    

## 6. Model Matematika

Model awal menggunakan kinetika Monod, yang menghubungkan laju pertumbuhan mikroorganisme dengan konsentrasi substrat pembatas.

**Persamaan 1. Laju pertumbuhan spesifik**

μ(S) = μmax × S / (Ks + S)

**Persamaan 2. Perubahan biomassa**

dX/dt = μ(S) × X

**Persamaan 3. Konsumsi glukosa**

dS/dt = −μ(S) × X / Y

Dengan:

Simbol

Definisi

X

Konsentrasi biomassa (gDW/L)

S

Konsentrasi glukosa (g/L)

μ

Laju pertumbuhan spesifik (jam⁻¹)

μmax

Parameter maksimum laju pertumbuhan

Ks

Konstanta setengah saturasi glukosa

Y

Hasil biomassa per massa glukosa yang dikonsumsi

Model ini merupakan penyederhanaan tingkat populasi. Ia belum menjelaskan replikasi DNA, ATP individual, biosintesis protein, atau setiap reaksi metabolik.

Untuk versi sel individual, pertambahan biomassa total akan dihubungkan dengan pertumbuhan massa sel. Pembelahan hanya membagi biomassa sel induk kepada sel anak, tanpa menciptakan biomassa baru.

## 7. Parameter Referensi Awal

Parameter

Nilai atau status

Glukosa awal

2,0 g/L

Biomassa awal

0,002 gDW/L, asumsi sementara

Waktu penggandaan acuan

Sekitar 67,7 menit

Laju pertumbuhan acuan

Sekitar 0,614 jam⁻¹

μmax

Perlu kalibrasi

Ks

Memerlukan rujukan atau analisis sensitivitas

Y

Perkiraan awal 0,44 gDW/g glukosa dari studi berbeda

Nilai Y berasal dari penelitian pada kondisi glukosa yang tidak identik, sehingga hanya digunakan sebagai parameter eksploratif awal.

Parameter yang belum diketahui tidak boleh disamarkan menjadi angka biologis yang sudah terverifikasi.

## 8. Prosedur Simulasi

**Tahap A. Persiapan data**

1.  Menentukan identitas strain dan profil biologis.
    
2.  Mengumpulkan parameter pertumbuhan beserta referensinya.
    
3.  Menetapkan nilai awal dan satuan setiap variabel.
    
4.  Memisahkan parameter hasil pengamatan, asumsi desain, dan parameter yang dikalibrasi.
    

**Tahap B. Inisialisasi lingkungan**

1.  Membuat lingkungan virtual homogen.
    
2.  Menetapkan kondisi glukosa awal sebesar 2,0 g/L.
    
3.  Menginisialisasi biomassa bakteri.
    
4.  Memastikan seluruh parameter memiliki nilai dan satuan yang konsisten.
    

**Tahap C. Simulasi pertumbuhan**

1.  Menghitung laju pertumbuhan berdasarkan kondisi glukosa saat itu.
    
2.  Menghitung perubahan biomassa selama interval waktu simulasi.
    
3.  Mengurangi glukosa berdasarkan konsumsi model.
    
4.  Memperbarui keadaan lingkungan dan populasi.
    
5.  Mencatat hasil setiap 10 menit waktu biologis.
    
6.  Melanjutkan hingga 12 jam atau terjadi kegagalan numerik.
    

**Tahap D. Pengolahan hasil**

Menghasilkan tabel dan grafik pertumbuhan, konsumsi glukosa, laju pertumbuhan, dan perubahan populasi.

**Tahap E. Evaluasi**

Membandingkan hasil dengan data penelitian yang sesuai serta mengukur penyimpangan model.

## 9. Data Validasi

Dataset pertumbuhan MG1655 dari University of Wisconsin digunakan sebagai referensi awal.

Salah satu pengamatan pada glukosa 0,2% mencatat:

Waktu (jam)

OD600

0

0,005

2

0,012

3,25

0,026

4,5

0,054

5,5

0,103

7

0,211

9

0,493

**Sumber:** University of Wisconsin, E. coli Genome Project, MG1655 Growth Curve.

OD600 merupakan pengukuran kekeruhan optik, bukan jumlah sel atau massa kering secara langsung. Perbandingan biomassa hasil simulasi dengan OD600 memerlukan model observasi atau faktor konversi yang relevan.

Data ini dapat dipisahkan menjadi bagian kalibrasi dan pengujian pada waktu yang tidak digunakan untuk kalibrasi. Kurva lain dalam sumber yang sama dapat digunakan untuk menguji konsistensi tambahan, tetapi bukan dianggap sebagai validasi dari laboratorium independen.

## 10. Metode Evaluasi

**A. Validasi pertumbuhan**

Menghitung laju pertumbuhan dari kemiringan grafik logaritma biomassa selama fase eksponensial.

Waktu penggandaan:

t_d = ln(2) / μ

Nilai ini kemudian dibandingkan dengan referensi biologis.

**B. Validasi numerik**

Model harus memenuhi:

-   Konsentrasi glukosa tidak negatif.
    
-   Biomassa tidak negatif.
    
-   Tidak ada pertumbuhan baru dari model Monod ketika substrat awal nol.
    
-   Perubahan biomassa mengikuti hubungan hasil konversi substrat yang digunakan model.
    
-   Perubahan ukuran langkah numerik tidak menyebabkan perbedaan hasil yang tidak terkendali.
    

**C. Analisis sensitivitas**

Mengubah parameter μmax, Ks, dan Y secara terpisah, misalnya ±10%, untuk memahami seberapa besar pengaruh ketidakpastian parameter.

**D. Reproduksibilitas**

Simulasi deterministik dengan input dan konfigurasi sama harus memberikan hasil sama dalam toleransi numerik yang ditetapkan.

Jika model stokastik digunakan kemudian, percobaan dengan seed acak tetap dan pengulangan beberapa seed akan dianalisis secara terpisah.

## 11. Kriteria Keberhasilan

**Keberhasilan perangkat lunak:**

-   Seluruh simulasi selesai tanpa kesalahan numerik.
    
-   Variabel tidak menghasilkan NaN atau nilai negatif yang tidak valid.
    
-   Output dapat direproduksi.
    
-   Neraca substrat-biomassa sederhana dipenuhi dalam toleransi yang ditetapkan.
    

**Keberhasilan model biologis:**

-   Model menghasilkan fase pertumbuhan yang dapat dianalisis.
    
-   Waktu penggandaan hasil prediksi dibandingkan dengan referensi sekitar 67,7 menit.
    
-   Kesalahan prediksi pada data yang tidak digunakan untuk kalibrasi dilaporkan.
    
-   Ketidakpastian dan keterbatasan model dijelaskan.
    

Sebagai target kerja awal, selisih waktu penggandaan sampai ±15% dapat digunakan sebagai ambang evaluasi sementara. Ambang ini adalah keputusan metodologis, bukan standar universal akurasi biologi.

## 12. Keterbatasan

Model belum memperhitungkan:

-   Perubahan pH akibat metabolisme.
    
-   Akumulasi produk samping seperti asetat.
    
-   Pembatasan oksigen yang berubah sepanjang waktu.
    
-   Fase lag secara eksplisit.
    
-   Kematian dan dormansi.
    
-   Regulasi gen dan reaksi metabolik lengkap.
    
-   Variasi fisiologis antarindividu.
    

Karena itu, kecocokan model pada fase eksponensial belum membuktikan kemampuan model mereproduksi seluruh siklus pertumbuhan bakteri.

## 13. Hasil yang Diharapkan

Eksperimen ini diharapkan menghasilkan:

1.  Kurva pertumbuhan biomassa selama 12 jam.
    
2.  Kurva perubahan konsentrasi glukosa.
    
3.  Estimasi laju pertumbuhan dan waktu penggandaan.
    
4.  Evaluasi kesesuaian model dengan data penelitian.
    
5.  Laporan kesalahan numerik, sensitivitas parameter, serta keterbatasan biologis.
    
6.  Fondasi ilmiah untuk pengembangan ABS menuju simulasi sel individual dan multi-spesies.
    

Hasil tersebut merupakan target penelitian, bukan hasil eksperimen yang telah diperoleh.

## 14. Referensi Utama

1.  University of Wisconsin E. coli Genome Project. _Growth of E. coli Strain MG1655._  [https://www.genome.wisc.edu/resources/k12growth/mg1655growthcurve.htm](https://www.genome.wisc.edu/resources/k12growth/mg1655growthcurve.htm)
    
2.  LaCroix, R. A., dkk. (2015). _Use of Adaptive Laboratory Evolution To Discover Key Mutations Enabling Rapid Growth of Escherichia coli K-12 MG1655 on Glucose Minimal Medium._  [https://doi.org/10.1128/AEM.02246-14](https://doi.org/10.1128/AEM.02246-14)
    
3.  _Microbial Primer: Bacterial Growth Kinetics._  [https://pmc.ncbi.nlm.nih.gov/articles/PMC10924458/](https://pmc.ncbi.nlm.nih.gov/articles/PMC10924458/)
    
4.  BiGG Models. _Escherichia coli Core Metabolic Model._  [https://bigg.bio/models/e_coli_core/](https://bigg.bio/models/e_coli_core/)
    

----------

**Status akhir:** Protokol siap untuk peninjauan ilmiah dan penyempurnaan parameter. Belum ada eksperimen dijalankan maupun kode diimplementasikan.
