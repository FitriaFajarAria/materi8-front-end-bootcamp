# materi8-front-end-bootcamp

# React-Testing

Adalah seperangkat helpers yang memungkinkan kita untuk mengetes komponen pada React tanpa bergantung pada detail implementasinya. Testing adalah praktik penting dalam rekayasa perangkat lunak yang membantu membangun perangkat lunak yang tangguh dan berkualitas tinggi serta meningkatkan kepercayaan tim terhadap kode, menjadikan aplikasi lebih fleksibel dan rentan terhadap lebih sedikit kesalahan saat memperkenalkan atau memodifikasi fitur. Beberapa pengembang bahkan menulis pengujian sebelum menulis fitur, mengikuti proses yang disebut pengembangan berbasis pengujian TDD (Test-driven development), TDD adalah pengembangan yang mengacu pada testing sebelum melakukan proses coding.Ada banyak jenis testing yang terbagi dalam tiga kategori utama yaitu :

1. unit testing, menguji apakah fungsi atau class dalam code berjalan dengan baik.
2. integration testing, menguji suatu fitur apakah berjalan dengan baik jika digabungkan dengan bagian lain dari aplikasi / website.
3. UI testing, menguji apakah aplikasi / website dapat dipakai user tanpa mengalami bug atau error.

Berikut adalah tampilan alur pengujian/testing :

1. impor fungsi untuk menguji
2. berikan masukan ke fungsi
3. tentukan apa yang diharapkan sebagai output
4. periksa apakah fungsi menghasilkan output yang diharapkan

 Alasan unit testing itu penting :
 
1. Membantu memperbaiki bug di awal pada siklus software development dan menghemat biaya
2. Membantu developer untuk memahami basis kode dan memungkinkan mereka membuat perubahan dengan cepat
3. Berfungsi sebagai dokumentasi proyek
4. Membantu reusability code pada projek baru

Unit testing memiliki tiga teknik yang disebut black box testing, white box testing dan gray box testing.

Black box testing adalah sebuah pengujian yang tidak perlu melihat dan memahami suatu software lebih dalam, pengujiannya melalui user interface, input dan output

2. White Box Testing

White box testing bersifat transparan jadi kita bisa melihat suatu sistem dari awal sampai akhir untuk dilakukan testing. Untuk testingnya dilakukan untuk menguji struktur internal, desain, fungsi dan detail implementasi dari sebuah aplikasi

3. Grey Box Testing

Grey box testing ini merupakan sebuah perpaduan antara black box testing dan white box testing. Pengujiannya ini digunakan untuk eksekusi test, resiko dan metode penilaian

Jest adalah test runner pada JavaScript yang memungkinkan untuk mengakses DOM melalui jsdom. Untuk setiap pengujian, Umumnya kita me-render ke sebuah elemen DOM yang terhubung dengan document, agar pengujian dapat menerima event DOM. Setelah pengujian selesai, kita harus melakukan "pembersihan". Cara yang umum dilakukan adalah menggunakan pasangan blok beforeEach dan afterEach agar mereka terus berjalan dan memisahkan efek-efek dari sebuah pengujian hanya kepada pengujian tersebut. Jest adalah kerangka pengujian JavaScript yang memungkinkan pengembang menjalankan pengujian pada kode JavaScript dan TypeScript dan terintegrasi dengan baik dengan React. Install Jest:


                npm i jest --save-dev

Untuk menjalankan tes, tambahkan ini ke package.json:


                "scripts": {
                 "test": "jest"
                }                
 
 menjalankan semua pengujian dengan menggunakan perintah npm sederhana:
 
       
                 npm run test
 
 
 ### Menggunakan Test Coverage
 
Pada sebuah proyek, ada baiknya kita melakukan sebuah testing terhadap semua komponen yang kita buat. Hal ini bertujuan untuk memastikan bahwa setiap komponen berfungsi semestinya. Namun terkadang kita lupa untuk membuat test untuk suatu komponen. Disinilah peran Test Coverage sangat berarti. Test Coverage berfungsi untuk melihat komponen mana saja yang sudah memiliki test dan komponen yang belum memiliki test. Untuk menjalankan test ini kita hanya perlu mengetikan perintah npm test — -coverage pada terminal, dan akan muncul daftar komponen mana saja yang sudah dan belum memiliki test. Berikut contoh hasil dari perintah npm test — -coverage.

### Fungsi Mock Dengan Menggunakan Jest

Seperti artinya kita akan membuat tiruan/mock dari suatu fungsi dan membuat balikannya secara manual, sehingga tidak peduli apakah fungsi tersebut bekerja, fungsi akan mengembalikan nilai sesuai yang kita definisikan. Kita akan mencoba membuat mock dari fungsi fungsiTambah yang kita buat sebelumnya. 

### Snapshot Testing

Snapshot testing merupakan fitur pada Jest yang memungkinkan kita membandingkan hasil render dari suatu komponen. Hasil render ini akan dibaca dalam bentuk JSON kedalam suatu file tersendiri yang secara otomatis akan terbentuk saat kita menjalankan snapshot testing. 
