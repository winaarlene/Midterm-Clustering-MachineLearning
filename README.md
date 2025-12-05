# Credit Card Customer Clustering

## 📋 Deskripsi Proyek

Proyek ini bertujuan untuk melakukan segmentasi pelanggan kartu kredit menggunakan teknik Machine Learning clustering. Dengan menganalisis perilaku transaksi pelanggan, kita dapat mengelompokkan pelanggan ke dalam beberapa segmen untuk strategi marketing yang lebih efektif.

## 👤 Identitas

- **Nama**: Wilhelmina Arlene S
- **NIM**: 1103223046

## 🎯 Tujuan

- Melakukan eksplorasi dan preprocessing data pelanggan kartu kredit
- Menentukan jumlah cluster optimal menggunakan metode Elbow dan Silhouette Score
- Membangun model K-Means Clustering untuk segmentasi pelanggan
- Mengevaluasi performa model dengan berbagai metrics
- Menganalisis karakteristik setiap cluster pelanggan

## 📊 Dataset

**File**: `clusteringmidterm.csv`

Dataset berisi informasi perilaku transaksi pelanggan kartu kredit dengan fitur-fitur:

- `CUST_ID`: ID pelanggan
- `BALANCE`: Saldo kartu kredit
- `PURCHASES`: Total pembelian
- `CREDIT_LIMIT`: Limit kredit
- `PAYMENTS`: Total pembayaran
- Dan fitur-fitur lainnya terkait transaksi

## 🛠️ Teknologi & Library

- **Python 3.x**
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing
- **Scikit-learn** - Machine learning algorithms
- **Matplotlib & Seaborn** - Data visualization

## 📁 Struktur Proyek

```
uts-midterm-clustering/
│
├── clusteringmidterm.csv           # Dataset
├── uts_midterm_clustering.ipynb    # Jupyter Notebook utama
└── README.md                        # Dokumentasi proyek
```

## 🚀 Cara Menjalankan

### 1. Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

### 2. Jalankan Notebook

- Buka `uts_midterm_clustering.ipynb` di Jupyter Notebook atau VS Code
- Jalankan cell secara berurutan dari atas ke bawah
- Pastikan file `clusteringmidterm.csv` berada di direktori yang sama

## 📈 Alur Kerja (Pipeline)

### 1. **Data Loading & Exploration**

- Memuat dataset dari file CSV
- Eksplorasi statistik deskriptif
- Identifikasi missing values

### 2. **Data Preprocessing**

- Menghapus kolom yang tidak relevan (CUST_ID)
- Handling missing values dengan median
- Menghapus data duplikat

### 3. **Feature Scaling**

- Standardisasi fitur menggunakan StandardScaler
- Memastikan semua fitur memiliki skala yang sama

### 4. **Penentuan Optimal Clusters**

- Metode Elbow (Inertia)
- Silhouette Score Analysis
- Visualisasi untuk menentukan k optimal

### 5. **Model Training**

- Algoritma: K-Means Clustering
- Training dengan k optimal
- Assignment cluster untuk setiap pelanggan

### 6. **Model Evaluation**

- **Silhouette Score**: Mengukur kualitas cluster
- **Davies-Bouldin Index**: Mengukur separasi antar cluster
- **Inertia**: Mengukur kompaksi cluster

### 7. **Visualization**

- PCA untuk reduksi dimensi ke 2D
- Scatter plot untuk visualisasi cluster
- Bar chart untuk karakteristik cluster

### 8. **Cluster Analysis**

- Analisis karakteristik setiap cluster
- Profiling pelanggan per segmen
- Business insights & recommendations

## 📊 Model & Metrics

### Model: K-Means Clustering

- **Init**: k-means++
- **Max Iterations**: 300
- **Random State**: 42 (reproducibility)

### Evaluation Metrics:

- **Silhouette Score**: Range [-1, 1], semakin tinggi semakin baik
- **Davies-Bouldin Index**: Semakin rendah semakin baik
- **Inertia**: Within-cluster sum of squares

## 🎯 Hasil & Kesimpulan

Setelah menjalankan model clustering, diperoleh beberapa segmen pelanggan dengan karakteristik berbeda:

- Setiap cluster memiliki pola spending dan payment yang unik
- Model dapat digunakan untuk targeted marketing strategy
- Segmentasi membantu dalam personalisasi layanan pelanggan

## 📝 Catatan

- Model ini menggunakan unsupervised learning (tidak ada label)
- Jumlah cluster optimal ditentukan secara otomatis
- Hasil clustering dapat bervariasi tergantung random initialization
