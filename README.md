# Cijo Jidan Riady - DataScience Portfolio
<div class='tableauPlaceholder' id='viz1699817299753' style='position: relative'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Su&#47;SupermarketSalesDashboard_16998170443410&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='SupermarketSalesDashboard_16998170443410&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Su&#47;SupermarketSalesDashboard_16998170443410&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1699817299753');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='100%';vizElement.style.height=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.height='1577px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>

## Personal Project: Prediksi persetujuan kartu kredit menggunakan Python
#### Link Kaggle:
<a>https://www.kaggle.com/code/cijojidanriady/case-study-credit-card-approval-classification/notebook</a>
#### Deskripsi project:
+ Mengimport package python yang akan digunakan dalam project:
  - NumPy
  - Pandas
  - Matplotlib.pyplot
  - Seaborn
  - Sklearn
+ Menggunakan Pandas untuk mengimport [file csv dari Kaggle](https://www.kaggle.com/datasets/jorgemacosmartos/crx-uci-ml-repository/) ke dalam bentuk DataFrame (nama fitur tidak diketahui untuk menjaga kerahasiaan data)
+ Memeriksa data untuk nilai hilang, row duplikat, dan unique value setiap row
  - Tidak ada missing value
  - Terdapat value berbentuk '?' yang perlu diproses pada beberapa fitur
+ Melakukan data cleaning
  - Mengubah value '?' menjadi bentuk NumPy NaN
  - Terdapat missing value pada fitur 0, 1, 3, 4, 5, 6, dan 13<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/42bfd1c9-386d-4771-8857-b07385d5d6e6)
  - Semua missing value terdapat pada fitur dengan datatype object
  - Berdasarkan informasi dataset, fitur 1 merupakan nilai numeric continous sehingga perlu diubah menjadi data type yang sesuai
  - Setelah dicek, fitur 1 memiliki distribusi yang miring ke kanan sehingga missing value perlu diisi dengan median fitur tersebut<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/06948b04-0928-47ae-893f-dcb3353b70cf)
  - Kemudian fitur dengan tipe data object diisi dengan mode dari fitur masing-masing
+ Preprocessing and splitting data
  - Target variabel (fitur 15) akan dimap menjadi 1 dan 0
  - Fitur dengan tipe data objek akan diubah menjadi value numerik menggunakan LabelEncoder dari sklearn
  - Data dibagi menjadi train dan test set (1/3 digunakan untuk test set)
  - Data train dan test akan melalui proses scaling menggunakan MinMaxScaler dari sklearn (scaling dilakukan setelah test agar menghindari terjadinya bocornya data)
+ Fit model Logistic Regression dan cek performa model
  - Model dilatih dengan data yang sudah diproses
  - Model mendapatkan akurasi sebesar 87.7% dengan data yang belum pernah dilihat
  - Confusion matrix dari model dapat dilihat sebagai berikut:<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/12f3460a-8a63-4795-95c7-4c9cbda44ab5)
  - Fitur yang paling digunakan dalam prediksi apakah lamaran kartu kredit akan disetujukan adalah sebagai berikut:<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/cfda6dac-b465-4dc3-b835-455290fbe452)
+ Mencari hyperparameter model yang paling sesuai dengan tuning
  - Menggunakan GridSearchCV, model mendapatkan skor yang sama dengan parameter optimal: {'C': 1.623776739188721, 'max_iter': 150, 'penalty': 'l2', 'tol': 0.01}<br>
    ![download](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/ae9d13b0-d4a8-499b-871b-84846b63b284)
  - Berdasarkan classification report, kedua model memiliki hasil yang sama maka dapat diasumsikan model awal sudah teroptimisasi<br>
    ![image](https://github.com/CijoJR/DataScience_Portfolio/assets/80349832/683d36e1-a55b-4967-bbbf-01851b2be397)

## Personal Project: Spotify Top Songs 2023 - EDA and Visualizations
#### Link Kaggle:
<a>https://www.kaggle.com/code/cijojidanriady/spotify-data-2023-eda-and-visualizations</a>
#### Deskripsi project:
+ Mengimport package python yang akan digunakan dalam project:
  - NumPy
  - Pandas
  - Matplotlib.pyplot
  - seaborn
+ Menggunakan Pandas untuk mengimport [file csv dari Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023) ke dalam bentuk DataFrame.
+ Memeriksa data untuk nilai hilang atau duplikat
  - Terdapat nilai hilang dalam fitur 'streams', 'in_deezer_playlists', 'in_shazam_charts', 'key'
  - Tidak ada row duplikat dari dataset
+ Melakukan data cleaning dengan mengubah tipe data dan mengisi data kosong
  - Mengubah tipe data fitur 'streams' dari object menjadi numeric
  - Nilai 'in_deezer_playlists' dan 'in_shazam_charts' yang hilang diisi dengan 0 karena fitur berupa ranking dan dapat dianggap suatu lagi yang tidak memiliki nilai berarti tidak termasuk dalam ranking tersebut
  - Nilai 'stream' yang hilang dihapus karena merupakan <1% dari dataset
  - Nilai 'key' yang hilang diisi dengan '-'
+ Melakukan feature engineering
  - Menambahkan kolom jumlah putaran per juta
  - Menambahkan kolom kategori artis dengan mengkategorikan jumlah artis menjadi 'solo' dan 'multiple' 
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

## Project Tugas Kuliah: Visualisasi bencana alam di Jawa Barat menggunakan Google Data Studio
#### Tugas 
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
