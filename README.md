# Employee Attrition
## Dataset

- WA*Fn-UseC*-HR-Employee-Attrition

### Deskripsi

- Dataset ini digunakan untuk menganalisis faktor-faktor yang menyebabkan pergantian karyawan (attrition) di suatu perusahaan. Tujuan analisis ini adalah untuk menentukan faktor-faktor yang dapat diubah guna mencegah kehilangan karyawan yang berpotensi baik. Watson Analytics digunakan sebagai alat analisis. yang baik.

### Data

- Dataset ini berisi informasi tentang karyawan yang bekerja atau telah bekerja di perusahaan tersebut. Setiap baris dalam dataset ini mewakili satu karyawan, sementara setiap kolom mewakili atribut yang menggambarkan karyawan tersebut.

## Atribut Dalam Dataset

### A. Tipe Data yang Tidak Sesuai

Berdasarkan pengamatan di samping, dapat kita ketahui dari perbandingan "column" dengan "Dtype" dataset yang dimiliki ada kolom yang memiliki jenis data yang tidak sesuai, yaitu:

- Education
- EviromentSatisfication
- JobInvloment
- JobLevel
- Jobsatisfaction
- PerformanceRating
- RelationshipSatisfaction
- StockOptionLevel
- WorkLifeBalance

### B. Kolom Kosong

Data yang memiliki kolom kosong dapat dilihat dari perbandingan jumlah data (RangeIndex = 1470) dengan Non-Null Count untuk masing-masing kolom, sehingga didapatkan informasi berupa tidak adanya nilai kosong (null) pada setiap kolom di dataset yang kita miliki.

### C. Nilai Summary Aneh

Dari informasi di samping diketahui bahwa:
Beberapa kolom numerik pada dataset yang dimiliki skew (dilihat dari perbedaan yang cukup besar antara mean dan median), yaitu kolom.

- DistanceFromeHome
- MonthlyIncome
- PercentSalaryHike
- TotalWorkingYears
- YearsAtCompany
- YearsinCurrentRole
- YearsSinceLastPromotion
- YearsWithCurrManager
  Ada kolom numerik dan kategorik yang perlu di drop karena hanya memiliki 1 nilai unique yaitu kolom StandarHours, EmployeeCount, EmployeeNumber, dan Over18

## Univariate Analysis

Hasil Observasi Univariate Analysis Kolom Numerik:

- Fitur-fitur yang memiliki outlier dan memiliki distribusi skewed, seperti : (Age, MonthlyIncome, NumCompaniesWorked, PercentSalaryHike, TrainingTimeLastYears, YearsAtCompany, TotalWorkingYears, YearsCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager).
- Ada juga fitur-fitur numerik yang berdistribusi multimodal/bimodal seperti: TrainingTimesLastYear, YearsCurrentRole, and YearsWithCurrManager.
- Ada juga yang berdistribusi seragam seperti : DailyRate, EmployeeNumber, HourlyRate dengan MonthlyRate.
- Terdapat juga yang distribusinya mirip, seperti:
  YearsWithCurrRole dengan YearsWithCurrManager
  YearsSinceLastPromotion dengan YearsAtCompany

Hasil Observasi Univariate Analysis Kolom Kategorik:
Untuk fitur kategorik tidak ada fitur dengan nilai yang mendominasi dan kategori yang terlalu banyak. Untuk Target, jumlah yang tidak attrition mendominasi variabel target (Class Imbalance).
Pada saat Pre-Processing sebaiknya fitur-fitur yang berdistribusi skew di transformasi menjadi mendekati normal terlebih dahulu sebelum melakukan step-step berikutnya. Kemudian, fitur-fitur seperti EmployeeCount, StandardHours, dan Over18 sebaiknya di drop karena nilainya konstanta dan tidak berubah.
Untuk fitur EmployeeNumber juga sebaiknya di drop karena fitur ini merupakan fitur identifikasi untuk setiap employee dan nilai nya unik untuk setiap row di dataset. Selanjutnya, pada saat pre-processing harus juga dilakukan handling untuk class imbalance nya pada variabel target.

## Multivariate Analysis

Hasil Observasi Multivariate Analysis:

- Terdapat beberapa feature yang memiliki korelasi yang cukup kuat dengan tarfet feature dengan nilai di atas 0,10 seperti feature age, jobinvolvemen, joblevel, monthlyincome, stokoptionlevel, totalworkingyears, yeasratcompany, dan yearsincurrentrole
- korelasi paling tinggi terletak pada nilai 0,17 pada feature totalworkingyears dan joblevel menandakan bahwa 2 faktor tersebut yang paling tinggi mempengaruhi Attrition
- Terdapat kekosongan nilai korelasi di kolom EmployeeCount dan StandardHours, dikarena nilai dalam kolom tersebut konstan.

## Business Insight

