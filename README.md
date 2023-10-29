# Data Preprocessing 
## Data Cleansing
* Handle Missing Values
  - Menghapus feature yang memiliki total missing values >60% dari data, feature yang dihapus adalah ChgOffDate.
  - Feature yang memiliki missing values adalah feature yang memiliki tipe data string atau object sehingga data yang kosong diisi dengan modus
* Handle Duplicated Data
  - Tidak ada duplicated data
* Handle Outliers
  - Outliers dideteksi dan dihapus dengan metode Z-Scores. Jumlah baris data setelah dihapus sebanyak 248.928
* Feature Transformation
  - Pada feature yang bertipe numerik, dilakukan feature transformation menggunakan log transformation. 
* Feature Encoding
  - Feature yang bertipe kategorikal diubah menjadi numerik dengan menggukan feature encoding agar dapat menjadi input pada machine learning
## Feature Engineering
* Feature Extraction
  - Mengembangkan feature baru dari feature baseline yang mungkin dapat meningkatkan performa saat membangun permodelan machine learning.
* Feature Scaling
  - Melakukan data scaling agar membuat nilai numerik data memiliki nilai rentan yang sama
* Feature Selection
  - Mengambil feature yang relavan berdasarkan nilai korelasi terhadap feature target (MIS_Status_int)
* Class Imbalance
  - Nilai 0 dan 1 pada feature target masih tidak seimbang sehingga harus dilakukan class imbalance
  - Handle class imbalace menggunakan oversampling SMOTE pada data training
