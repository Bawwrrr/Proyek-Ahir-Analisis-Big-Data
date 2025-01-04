
# Analisis Dataset Spotify

Oleh : 
Nurvianto Akbar Ikhsani (202110370311123)
Pramestya Hilal Syahfigral Adzani (202110370311129)
Mohamad Ferdyansyah (202110370311137)

## Pendahuluan

### Pengantar

Dataset Spotify menyajikan informasi yang luas terkait lagu, termasuk fitur musikal, genre, dan tingkat popularitas. Kajian ini bertujuan untuk menggali wawasan berbasis data dengan mendalam, guna mengidentifikasi pola dan tren yang signifikan dalam dataset. Kami juga mengevaluasi apakah fitur-fitur tertentu memiliki potensi menjadi elemen unggulan dalam dunia musik, baik dari sisi industri maupun dari perspektif konsumen.

Musik telah menjadi bagian integral dari kehidupan manusia, dan dengan berkembangnya teknologi, analisis data dalam dunia musik membuka peluang baru untuk memahami preferensi audiens. Dataset Spotify menyediakan berbagai fitur seperti danceability, energy, loudness, valence, dan lain-lain, yang memungkinkan kita untuk mengevaluasi elemen-elemen kunci yang memengaruhi popularitas dan daya tarik sebuah lagu.

### Rencana

Studi ini mengadopsi pendekatan "teardown" yang terfokus pada hubungan antar fitur dalam dataset. Dengan mengeksplorasi korelasi, distribusi, dan pola temporal, kami berusaha memahami keterkaitan kompleks antara dimensi musikal dan popularitas. Proses analisis ini dilakukan secara bertahap, dimulai dari eksplorasi awal, pembersihan data, hingga tahap visualisasi mendalam untuk mengungkap hubungan tersembunyi.

Analisis ini juga memprioritaskan interpretasi hasil dengan mengaitkannya pada konteks industri musik. Dengan demikian, temuan-temuan dapat langsung diterapkan untuk pengembangan strategi pemasaran, produksi musik, atau bahkan penelitian akademik lebih lanjut.

### Teknik Analisis

Kami memanfaatkan metode analisis statistik dan visualisasi data untuk mengevaluasi hubungan antar fitur dalam dataset. Teknik ini meliputi:

-   Penghitungan korelasi untuk menilai kekuatan hubungan antar variabel.
-   Visualisasi dengan grafik untuk mengidentifikasi pola distribusi dan tren temporal.
-   Eksplorasi distribusi fitur dengan histogram dan kurva kepadatan.
-   Analisis scatter plot untuk mengevaluasi hubungan langsung antara dua variabel.

### Tujuan Analisis

Penelitian ini bertujuan memberikan wawasan yang bernilai bagi peneliti dan konsumen yang berminat pada analisis data musik. Kami berupaya mempermudah proses identifikasi elemen-elemen kunci yang menentukan daya tarik lagu berdasarkan data empiris. Selain itu, hasil analisis ini diharapkan dapat menjadi referensi bagi pengembangan algoritma rekomendasi musik atau strategi komersialisasi yang lebih efektif.

----------

## Perangkat Lunak yang Digunakan

Analisis ini melibatkan penggunaan pustaka Python berikut:

-   **pandas**: untuk manipulasi dan analisis data.
-   **numpy**: untuk komputasi numerik.
-   **matplotlib**: untuk pembuatan grafik.
-   **seaborn**: untuk visualisasi data yang lebih informatif.

Perangkat lunak ini dipilih karena keunggulannya dalam memproses data skala besar dan kemampuannya menghasilkan visualisasi yang jelas serta interpretatif. Kombinasi keempat pustaka ini memungkinkan analisis yang efisien dan mendalam.

----------

## Temuan Utama

### Analisis Genre dan Popularitas

-   Genre _pop_ secara konsisten menunjukkan tingkat popularitas tertinggi di antara genre lain. Popularitas genre ini mencerminkan daya tariknya yang universal, yang dapat diatribusikan pada elemen-elemen seperti kesederhanaan melodi, daya tarik emosional, dan kampanye pemasaran yang agresif.

### Korelasi Antar Fitur Musikal

1.  **Energy dan Loudness**: Korelasi positif kuat (0.68), menunjukkan bahwa lagu dengan tingkat energi tinggi cenderung lebih keras. Hal ini mencerminkan preferensi audiens terhadap musik dengan karakteristik yang menggugah semangat.
2.  **Valence dan Danceability**: Korelasi positif sedang (0.33), menunjukkan bahwa lagu yang lebih ceria memiliki kecenderungan lebih mudah untuk menari. Temuan ini relevan dalam memahami elemen-elemen yang mendorong audiens untuk terlibat secara fisik dengan musik.
3.  **Tempo**: Korelasi dengan fitur lain sangat lemah, mengindikasikan bahwa tempo tidak secara signifikan memengaruhi _danceability_, _energy_, atau _valence_. Hal ini menunjukkan bahwa tempo lebih bersifat independen sebagai elemen musikal.

### Popularitas Lagu dan Hubungan Fitur

-   Popularitas lagu tidak menunjukkan korelasi signifikan dengan fitur musikal tertentu:
    -   _Danceability_: 0.06 (lemah).
    -   _Energy_: -0.11 (lemah negatif).
    -   _Valence_: 0.03 (lemah).
-   Popularitas lagu kemungkinan lebih dipengaruhi oleh faktor non-musikal seperti lirik, artis, dan strategi promosi. Hal ini menunjukkan perlunya analisis holistik yang melibatkan faktor di luar dimensi musikal.

### Tren Temporal (1959–2009)

1.  **Danceability**: Nilai bervariasi dari 0.2 (tahun 1960-an) hingga mencapai 0.8 pada era modern. Tren ini mencerminkan peningkatan preferensi terhadap musik yang mendukung aktivitas fisik seperti menari.
2.  **Energy**: Meningkat secara progresif dari 0.4 hingga hampir menyentuh 1, menunjukkan transisi ke musik dengan intensitas tinggi.
3.  **Valence**: Mencapai nilai 0.2 hingga hampir 1, menunjukkan pergeseran dari lagu dengan emosi ekstrem ke emosi yang lebih netral. Tren ini relevan untuk memahami perubahan selera audiens terhadap lagu-lagu dengan nada emosional yang lebih moderat.

----------

## Visualisasi Data

### 1. Perbandingan Lagu Akustik dan Non-Akustik

Grafik batang menunjukkan:

-   Lagu akustik memiliki popularitas rata-rata sekitar 45.
-   Lagu non-akustik memiliki popularitas rata-rata lebih rendah, sekitar 40.

Hasil ini menunjukkan bahwa lagu akustik memiliki daya tarik yang sedikit lebih besar dibandingkan lagu non-akustik, yang mungkin disebabkan oleh persepsi audiens terhadap keaslian dan emosi yang disampaikan melalui elemen akustik.

### 2. Histogram Distribusi Durasi Lagu

Distribusi durasi lagu menunjukkan:

-   Mayoritas lagu berdurasi 3-4 menit, mencerminkan standar industri.
-   Lagu dengan durasi sangat pendek atau panjang merupakan _outlier_.

Histogram ini memberikan wawasan tentang pola durasi yang diterima secara luas di industri musik dan bagaimana outlier dapat menciptakan variasi yang menarik.

### 3. Scatter Plot Hubungan Durasi dan Popularitas

Scatter plot menunjukkan:

-   Tidak terdapat hubungan linear yang jelas antara durasi dan popularitas lagu.
-   Lagu berdurasi pendek (<4 menit) lebih banyak ditemukan, dengan popularitas bervariasi.
-   Lagu berdurasi panjang (>6 menit) jumlahnya lebih sedikit, tetapi popularitasnya tetap beragam.

Interpretasi ini menunjukkan bahwa durasi lagu bukanlah faktor penentu utama popularitas, dan elemen-elemen lain perlu dieksplorasi lebih lanjut.

----------

## Kesimpulan

### Wawasan Utama

1.  Genre _pop_ memiliki tingkat popularitas tertinggi, mencerminkan daya tariknya yang universal dan kemampuan untuk menarik perhatian audiens secara luas.
2.  Hubungan antar fitur musikal mengungkapkan bahwa _energy_ dan _loudness_ sangat berkaitan, sementara fitur lain memiliki hubungan yang lebih lemah, yang memberikan wawasan tentang elemen-elemen yang memengaruhi pengalaman mendengarkan.
3.  Popularitas lagu tidak dapat dijelaskan hanya berdasarkan fitur musikal; faktor lain seperti lirik, artis, dan promosi memainkan peran penting.
4.  Tren temporal menunjukkan bahwa musik modern cenderung lebih energik, ceria, dan _danceable_, mencerminkan evolusi selera audiens.

### Implikasi

Temuan ini memberikan pandangan yang komprehensif bagi industri musik dan konsumen yang ingin memahami pola dalam musik populer. Penelitian lanjutan dapat difokuskan pada pengaruh faktor non-musikal seperti lirik, strategi pemasaran, atau inovasi teknologi dalam menciptakan musik yang lebih menarik dan beresonansi dengan audiens global.
