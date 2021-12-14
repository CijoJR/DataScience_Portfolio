# Cijo Jidan Riady
## DataScience Portfolio

### Personal Project: Prediksi persetujuan kartu kredit menggunakan Python
#### Deskripsi project:
+ Menggunakan Pandas untuk mengimport data persetujuan kartu kredit dari UCI Machine Learning Repository berbentuk csv ke dalam bentuk DataFrame.
+ Mengubah dan mengisi missing values pada DataFrame berdasarkan mean.
+ Membelah data menjadi data training dan testing. 
+ Melakukan exploratory data analisis korelasi antara feature. Kemudian visualisasi pencarian menggunakan Seaborn heatmap.
![image](https://user-images.githubusercontent.com/80349832/146022628-cbd9583d-34cf-478c-b040-d2fb13a7cc51.png)
+ Melakukan scaling pada data dengan min-max scaler pada range 0-1 dengan cara fit ke data training kemudian transform ke seluruh data.
+ Membuat model logistic regression dan melatihnya menggunakan data training yang telah di-scaling.
+ Melakukan evaluasi performa dari model yang dibuat. Model yang dibuat memiliki akurasi sekitar 84% dan confusion matrix sebagai berikut:
 ![image](https://user-images.githubusercontent.com/80349832/146025386-dae389e6-1882-43dd-ba96-bf0a87519bc5.png)
  dan classification report sebagai berikut:
 ![image](https://user-images.githubusercontent.com/80349832/146033377-6d6cc52a-7107-4049-9c66-82ac9f946c08.png)
+ Melakukan optimisasi pada model yang telah dibuat dengan cara mencari value hyperparameter yang sesuai menggunakan GridSearchCV. Hyperparameter yang dipilih adalah tol (0.01, 0.001, 0.0001) dan max_iter(100, 150, 200) dengan cross validation sebanyak 5 fold.
+ Setelah optimisasi, model memiliki akurasi sekitar 85.5% menggunakan hyperparameter {'max_iter': 100, 'tol': 0.01}.

### Personal Project: Visualisasi rating dan viewership TV series *'The Office'* menggunakan Python
#### Deskripsi project:
+ Menggunakan Pandas untuk mengimport data csv dari Kaggle ke dalam bentuk DataFrame.
+ Mengolah data rating episode menjadi 4 kategori dan membagi DataFrame menjadi 2 berdasarkan adanya bintang tamu atau tidak.
+ Menggunakan Matplotlib untuk membuat visualisasi scatterplot dengan 4 dimensi (episode number, viewership, rating, dan bintang tamu)

#### Hasil Visualisasi:
![image](https://user-images.githubusercontent.com/80349832/138271826-49dfdc95-c309-4771-940f-93f2482ea0fe.png)

  Figure di atas menunjukan viewership, rating, dan adanya bintang tamu pada setiap episode *The office*. Viewership setiap episode dapat dilihat dengan tingginya pada sumbu-y. Rating dapat dilihat melalui warna dimana warna mendekati merah berarti rating rendah dan semakin hijau berarti semakin tinggi. Ada atau tidaknya terindikasi dengan marker berbentuk bintang.


### Personal Project: Visualisasi bencana alam di Jawa Barat menggunakan Google Data Studio
#### Deskripsi project:
+ Mengimport 3 data dari opendata Jawa Barat ke dalam Google Data Studio via csv file, yaitu:
  - Angka korban bencana alam di Jawa Barat pada tahun (2019)
  - Angka terjadinya banjir di Jawa Barat (2012-2020)
  - Angka terjadinya kekeringan di Jawa Barat (2019)
+ Melakukan berbagai macam visualisasi pada data tersebut seperti bar chart, linechart, pie, treemap, dan map visualization.
+ Menambahkan tombol untuk memungkinkan selection data tahun dan kota/kabupaten bagi user.

#### Hasil Dashboard:
##### Halaman #1
![bencana_alam-1](https://user-images.githubusercontent.com/80349832/138287827-f1c164b2-96cf-41f4-aec6-a3c7a058c2b6.jpg)

##### Halaman #2
![bencana_alam-2](https://user-images.githubusercontent.com/80349832/138287850-ec9cb166-351e-4431-9a58-b59cb8ca3f5d.jpg)

##### Halaman #3
![bencana_alam-3](https://user-images.githubusercontent.com/80349832/138287866-c45dc796-6927-40f3-9563-6f126c959cf2.jpg)
