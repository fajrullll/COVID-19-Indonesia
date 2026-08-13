# COVID-19 Indonesia — K-Means Clustering

Proyek sederhana ini mengelompokkan provinsi di Indonesia berdasarkan **total kasus COVID-19** dan **total kematian** menggunakan algoritma **K-Means Clustering**.

## Proses Analisis

1. Membaca dataset COVID-19 Indonesia dengan Pandas.
2. Mengambil total kasus dan total kematian tertinggi setiap provinsi.
3. Menormalisasi data ke rentang 0–1 menggunakan `MinMaxScaler`.
4. Membagi provinsi menjadi tiga kelompok menggunakan K-Means.
5. Menampilkan kelompok dalam grafik sebaran dengan warna berbeda.
6. Membandingkan hasil clustering untuk jumlah cluster 2–10.
7. Mengevaluasi dan menjelaskan hasil menggunakan tiga metode.

## Evaluasi Clustering

- **Inertia** mengukur total jarak data terhadap pusat cluster. Nilai lebih kecil menunjukkan anggota cluster lebih rapat, tetapi nilainya selalu menurun ketika jumlah cluster bertambah.
- **Silhouette Score** mengukur kekompakan dan pemisahan cluster. Nilai yang semakin mendekati `1` menunjukkan hasil semakin baik.
- **Davies-Bouldin Index** mengukur kemiripan antar-cluster. Nilai yang semakin kecil menunjukkan cluster semakin terpisah.

Model menggunakan **3 cluster** karena memperoleh Silhouette Score tertinggi dan Davies-Bouldin Index terendah pada data yang dianalisis. Inertia digunakan sebagai informasi tambahan mengenai kerapatan cluster.

## Teknologi

- Python
- Pandas dan NumPy
- Matplotlib dan Seaborn
- Scikit-learn
- Jupyter Notebook

## Struktur File

- `data_mining_k_means (3).ipynb` — notebook analisis dan clustering.
- `dataset/covid_19_indonesia_time_series_all.csv` — dataset yang digunakan.

## Menjalankan Proyek

Instal pustaka yang diperlukan:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

Buka notebook, pilih kernel Python yang sesuai, lalu jalankan seluruh cell secara berurutan.
