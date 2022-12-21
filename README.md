# Praktikum11

## Handling
-Penanganan file adalah bagian penting dari aplikasi apapun.

## Exception Handling
-Exception (eksepsi) merupakan suatu kesalahan(error) yang terjadi saat proses eksekusi program sedang berjalan
-Kesalahan ini akan menyebabkan program berakhir dengan tidak normal.

## Assertion
-Saat menemukan pernyataan, Python mengevaluasi eskpresi yang menyertainya, yang mana semoga benar. Jika ekspresi salah, Python memunculkan pengecualian AssertionError.

Sintaks untuk pernyataan yaitu: assert Expression[, Arguments] Jika pernyataan gagal, Python menggunakan ArgumentExpression. ArgumentExpression sebagai argumen-argumen untuk AssertionError. Pengecualian AssertionError dapat ditangkap dan ditangani seperti pengecualian lainnya menggunakan try kecuali pernyataan, tetapi jika dibiarkan mereka akan menghentikan program dan menghasilkan backtrace.


## Menangani Pengecualian
Jika Anda memiliki beberapa kode mencurigakan yang mungkin mengeluarkan pengecualian, Anda dapat mempertahankan program Anda letakkan kode yang mencurigakan di *try: blok. Setelah coba: blok, sertakan pernyataan sertakan *except: statement, diikuti oleh blok kode yang menangani masalah seanggun mungkin.

Contoh :

-Contoh-contoh ini membuka file, menulis konten file, dan keluar dengan aman karena ada tidak masalah
-Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![gambar 1](ss/1.png)

## Fasal kecuali Tanpa Pengecualian
Anda juga dapat menggunakan pernyataan exception tanpa exception yang didefinisikan sebagai berikut: try: You do your operations here; ...................... except: If there is any exception, then execute this block. ...................... else: If there is no exception then execute this block. Pernyataan coba-kecuali jenis ini menangkap semua pengecualian pengecualian yang terjadi. Menggunakan percobaan seperti try-expect pernyataan tidak dianggap sebagai praktik pemrograman yang baik, karena mereka menangkap semuanya pengecualian tetapi tidak membuat programmer mengidentifikasi kemungkinan penyebab masalah terjadi.

## Klausa Kecuali dengan Berbagi Pengecualian
-Anda juga dapat menggunakan pernyataan exception yang sama untuk menangani beberapa exception sebagai berikut: try: You do your operations here; ...................... except(Exception1[, Exception2[,...ExceptionN]]]): If there is any exception from the given exception list, then execute this block. ...................... else: If there is no exception then execute this block.

# Klausa coba-akhirnya
Contoh :

-Jika anda tidak memiliki izin untuk membukafile dalam mode tulis yang dapat ditulis, maka ini akan menghasilkan hasil berikut:

![gambar 2](ss/2.png)

-Ketika exception dilempar ke dalam blok try, eksekusi segera dilanjutkan ke akhir memblok. Setelah semua pernyataan di blok akhirnya dieksekusi, pengecualian dimunculkan lagi dan ditangani dalam pernyataan kecuali jika ada di lapisan berikutnya yang lebih tinggi dari percobaan-kecuali penyataan.

## Argumen Pengecualian
Contoh :

-Berikut adalah contoh untuk satu pengecualian
-Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![gambar 3](ss/3.png)

## Melempar Pengecualian
Contoh :

-Pengecualian dapat berupa string, kelas, atau objek. Sebagian besar pengecualian adalah pengecualian dari inti Python menimbulkan adalah kelas dengan argumen=argumen yang merupakan turunan dari kelas. Mendefinisikan pengecualian baru cukup mudah dan dapat dilakukan sebagai berikut:

![gambar 4](ss/4.png)

## Pengecualian yang Ditetapkan Pengguna
-Python juga memungkinkan Anda membuat pengecualian sendiri dengan menurunkan kelas-kelas dari yang standar pengecualian bawaan.
-Berikut adalah contoh-contoh yang terkait dengan RuntimeError. Di sini, kelas dibuat yang merupakan subkelas dari subkelas RuntimeError. Ini berguna saat anda perlu menampilkan tampilan informasi yang lebih spesifik saat e pengecualian tertangkap.
-Di blok try, pengecualian yang ditentukan pengguna dimunculkan dan ditangkap di blok except. Itu variabel e digunakan untuk membuat instance dari kelas Networkerror.

![gambar 5](ss/5.png)
