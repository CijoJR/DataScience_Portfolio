# Cijo Jidan Riady - DataScience Portfolio

## Personal Project: Prediksi persetujuan kartu kredit menggunakan Python
#### Deskripsi project:
+ Menggunakan Pandas untuk mengimport data persetujuan kartu kredit dari UCI Machine Learning Repository  berbentuk csv ke dalam bentuk DataFrame.
+ Mengubah dan mengisi missing values pada DataFrame berdasarkan mean.
+ Membelah data menjadi data training dan testing. 
+ Melakukan exploratory data analisis korelasi antara feature. Kemudian visualisasi pencarian menggunakan Seaborn heatmap.

![image](https://user-images.githubusercontent.com/80349832/146022628-cbd9583d-34cf-478c-b040-d2fb13a7cc51.png)
+ Melakukan scaling pada data dengan min-max scaler pada range 0-1 dengan cara fit ke data training kemudian transform ke seluruh data.
+ Membuat model logistic regression dan melatihnya menggunakan data training yang telah di-scaling.
+ Melakukan evaluasi performa dari model yang dibuat. Model yang dibuat memiliki akurasi sekitar 84% dan confusion matrix sebagai berikut:

![image](https://user-images.githubusercontent.com/80349832/146025386-dae389e6-1882-43dd-ba96-bf0a87519bc5.png)
+ dan classification report sebagai berikut:

![image](https://user-images.githubusercontent.com/80349832/146033377-6d6cc52a-7107-4049-9c66-82ac9f946c08.png)
+ Melakukan optimisasi pada model yang telah dibuat dengan cara mencari value hyperparameter yang sesuai menggunakan GridSearchCV. Hyperparameter yang dipilih adalah tol (0.01, 0.001, 0.0001) dan max_iter(100, 150, 200) dengan cross validation sebanyak 5 fold.
+ Setelah optimisasi, model memiliki akurasi sekitar 85.5% menggunakan hyperparameter {'max_iter': 100, 'tol': 0.01}.

## Personal Project: Spotify Top Songs 2023 - EDA and Visualizations
#### Link Kaggle: https://www.kaggle.com/code/cijojidanriady/spotify-data-2023-eda-and-visualizations
#### Deskripsi project:
+ Menggunakan Pandas untuk mengimport [file csv dari Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023) ke dalam bentuk DataFrame.
+ Memeriksa data untuk nilai hilang atau duplikat
+ Melakukan data cleaning dengan mengubah tipe data dan mengisi data kosong
+ Melakukan feature engineering dengan menambahkan kolom jumlah putaran per juta dan kategori artis dengan mengkategorikan jumlah artis menjadi 'solo' dan 'multiple' 
+ Mengolah dan visualisasi data untuk menjawab pertanyaan-pertanyaan seperti:

  - Siapa saja artis yang paling didengar pada tahun 2023?<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/11ce1f11-f484-40c9-82bf-a4f71e852432)

  - Dari artis-artis tersebut, lagu keluaran tahun kapan yang paling didengar?<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/7676f279-93ff-44a5-ac16-b3644aa66e36)

  - Lagu-lagu apa saja yang paling didengar dari 5 tahun sebelumnya?<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/e33fa5ea-881e-4ae7-a4b8-ad0f96c7d330)

  - Lagu apa yang lebih banyak jumlah dengar? satu atau lebih artis?<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/5ffb517f-5865-4b52-b290-f787aa873e92)

  - Lagu apa saja yang paling didengar berdasarkan jumlah artis?<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/d9ea58a6-9ed8-45fc-9602-909866b2201c)

  - Kunci apa saja yang sering dipakai dalam lagu-lagu terpopuler Spotify?<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/67efd710-7405-4ebe-a631-4e616e6da5c8)

  - Bagaimana penggunaan kunci mayor dan minor dalam lagu-lagu terpopuler spotify?<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/6f8583f2-b949-43f3-819b-e247fc7139cc)

  - Fitur apa saja yang berkolerasi? <br>
![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/1ee5a230-f5d8-48db-91f0-b6459e19b992)
![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/a27d938e-7974-481e-bff0-689ad4190797)
![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/a85b490f-80cd-410a-a52b-a8e8db114a06)
![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/4220773b-b5b9-4e8e-9f5b-966d0e45150d)

## Personal Project: Visualisasi bencana alam di Jawa Barat menggunakan Google Data Studio
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
