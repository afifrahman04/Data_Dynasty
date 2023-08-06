# Employee Attrition
# STAGE 2
## Dataset

- HR-Employee-Attrition

### Deskripsi

- Dataset ini digunakan untuk menganalisis faktor-faktor yang menyebabkan pergantian karyawan (attrition) di suatu perusahaan. Tujuan analisis ini adalah untuk menentukan faktor-faktor yang dapat diubah guna mencegah kehilangan karyawan yang berpotensi baik. Watson Analytics digunakan sebagai alat analisis. yang baik.

### Data

- Dataset ini berisi informasi tentang karyawan yang bekerja atau telah bekerja di perusahaan tersebut. Setiap baris dalam dataset ini mewakili satu karyawan, sementara setiap kolom mewakili atribut yang menggambarkan karyawan tersebut.



### 1. Data Cleansing
A. Handle missing values = tidak ada data kosong
B. Handle duplicated data = tidak ada data duplicate
C. Handle outliers = Handle outlier akan dilakukanpada data training.
D. Handle class imbalance = Handle class imbalance akandilakukan pada data training


### 2. Feature Engineering
A. Feature selection
(membuang feature yang kurang relevan atauredundan)
Membuang feature StandardHours,EmployeeNumber, Over18 karena bernilaikonstan. Membuang EmployeeCount 

B. Feature extraction
(membuat feature baru dari featureyang sudah ada)
  1. Fitur Employment Stability/AvgYears per Company
  2. Fitur Avg Satisfaction
  3. Fitur Income Experience Ratio
  4. Fitur Income Distance Ratio
  5. Fitur Years in Previous Roles

C. 4 feature tambahan
  1. Salary Breakout = Membagi data gaji karyawan menjadi beberapa kategori, sepertigaji pokok, tunjangan, dan bonus.
  2. Transportation = Karyawan memiliki transportasi pribadi atau tidak.
  3. Dependents = Jumlah tanggungan karyawan, seperti anak, pasangan, danorang tua
  4. Number of Training Programs = Jumlah program pelatihan yang telah diikuti karyawan.
 



