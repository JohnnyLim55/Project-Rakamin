# Project-Rakamin
 Rakamin Project is a project-based internship program that provides students with the opportunity to work on real-world projects with leading companies in the technology industry. The program is designed to help students develop their skills and experience in a practical setting.

# Project-Rakamin
 Rakamin Project is a project-based internship program that provides students with the opportunity to work on real-world projects with leading companies in the technology industry. The program is designed to help students develop their skills and experience in a practical setting.
# INSIGHT

* Kebanyakan perusahaan dapat membayar penih pinjamannya, hanya 32,3% yang tidak dapat membayar secara lunas MIS Status by Industry
* Selain unknown insudtri, industri retail trade dan manufacturing memiliki jumlah pinjaman cair yang besar dibandingkan industri lainnya.
* Untuk rata-rata, industri Mgmt_comp, manufacturing, oil_gas, dan Agro Fishery memiliki rata-rata pinjaman yang besar, meskipun total jumlah pinjaman di grafik sebelumnya termasuk kecil. Hal ini mengindikasikan bahwa jumlah peminjam di sektor ini masih sedikit.
* Terdapat 3 Industri yang memiliki tingkat gagal bayar paling tinggi yaitu RE/Rental/Lease (48%), Finance/Insurance (47%), dan Trans/Ware (43%)
* Sedangkan untuk Industri dengan tingkat gagal bayar terendah ada pada Healthcare/Social_assist(20%), Ag/For/Fish/Hunt (16 %), dan Min/Quar/Oil_Gas_ext (14%) MIS Status by State
* 3 Wilayah yang memiliki jumlah pinjaman terbanyak ada pada California, New York, dan Texas. Meskupin begitu tingkat gagal bayar pada wilayah tersebut juga cukup tinggi. CA ada di angka 37%, NY(33%), dan TX(32%).
* Florida (46%),Georgia(43%), dan Nevada(42%) merupakan 3 wilayah dengan tingkat gagal bayar tertinggi pada periode waktu data.
* Sedangkan 3 wilayah dengan tingkat gagal bayar terendah ada pada ND(15%), WY(14%), dan VT(14%)

# Business Recommendation:
* Target peminjam bisa dipromosikan lebih pada perusahaan berbasis management company, Min/Quar/Oil_Gas_ext, dan Ag/For/Fish/Hunt karena memiliki **rata-rata pinjaman yang besar, jumlah peminjam yang belum begitu banyak, dan paling penting memiliki tingkat gagal bayar yang rendah**. Salah satu hal yang dapat dilakukan untuk mempromosikan pinjaman yaitu memberikan jalur khusus dan potongan bunga pada peminjam dengan sektor perusahaan tersebut.
* Peningkatan Manajemen Risiko di Industri dengan Tingkat Gagal Bayar Tinggi. Untuk industri seperti Real Estate/Rental/Lease, Finance/Insurance, Transportation/Warehousing dll yang memiliki tingkat gagal bayar tinggi, perusahaan harus lebih berhati-hati dalam manajemen risiko dan penilaian kredit. Ini dapat mencakup peningkatan proses verifikasi, pengembangan strategi pengambilan keputusan yang lebih baik, dan pemantauan aktif pelanggan dalam sektor tersebut.
* Evaluasi Strategi Pemasaran di Wilayah Dengan Tingkat Gagal Bayar Tinggi. Untuk wilayah seperti Florida, Georgia, Nevada dll yang memiliki tingkat gagal bayar tinggi, perusahaan harus memeriksa strategi pemasaran dan penilaian risiko di wilayah tersebut. Mungkin dapat dilakukan dengan peningkatan dalam penilaian kredit atau pengurangan eksposur risiko di wilayah ini.

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
