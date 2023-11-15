# mind_archives_mobile

## Tugas 8

### Jelaskan perbedaan antara Navigator.push() dan Navigator.pushReplacement(), disertai dengan contoh mengenai penggunaan kedua metode tersebut yang tepat!
Method Navigator.push() menambahkan suatu rute ke dalam stack route yang dikelola oleh Navigator. Method ini mmenyebabkan route yang ditambahkan akan berada di bagian paling atas dari stack, sehingga route yang baru ditambahkan dapat ditampilkan kepada pengguna. Method ini biasanya digunakan ketika diperlukan adanya navigasi ke halaman baru yang memungkinkan pengguna untuk kembali ke halaman sebelumnya.

Sedangkan Navigator.pushReplacement() akan membuat rute baru ke dalam stack route yang dikelola oleh navigator dan akan menggantikan rute sebelumnya dengan yang baru. Dengan adanya hal ini, pengguna tidak bisa kembali ke rute sebelumnya dan rute yang baru dibuat akan menjadi rute paling atas dari stack. Salah satu contoh implementasi dari Navigator.pushReplacement() adalah halaman login.

### Jelaskan masing-masing layout widget pada Flutter dan konteks penggunaannya masing-masing!
Rows & Colums: digunakan untuk melakukan penyusunan terhadap widget lain secara horizontal (row) maupun secara vertikal (kolom)

Container: container digunakan sebagai building block yang berisi widget lainnya. Selain itu, container juga dapat melakukan setting terhadap constraints di dalam child widget, seperti width, height, margin, dan padding.

Stack: stack digunakan agar widget dapat dijadikan overlay dari widget lainnya. Selain itu, widget yang ada di dalam stack juga dapat diposisikan di atas, bawah, kanan, ataupun kiri dari stack tersebut.

ListView & GridView: kedua hal ini digunakan untuk menampilkan display dari sebuah list atau grid widget dalam jumlah yang besar.

Expanded &  Flexible: digunakan di layout baris dan kolom untuk mendistribusikan ruang kosong yang ada di dalam child widget. Selain itu, kedua hal ini juga dapat diterapkan untuk membuat layout yang responsif.


### Sebutkan apa saja elemen input pada form yang kamu pakai pada tugas kali ini dan jelaskan mengapa kamu menggunakan elemen input tersebut!
Untuk mengambil input dari user mengenai nama, jumlah, dan deskripsi, maka digunakan 3 buah TextFormField yang masing-masing memiliki controllernya sendiri, yaitu _name, _amount, dan juga _description. TextFormField digunakan untuk menerima input dari pengguna untuk nama, jumlah, dan deskripsi dan masing-masing barang agar nantinya hasil input dapat ditampilkan melalui pop-up.


### Bagaimana penerapan clean architecture pada aplikasi Flutter?
Di dalam Flutter, terdapat sebuah design principle yang disebut dengan separation of concern ke dalam beberapa layer. Dengan hal ini, maka sebuah sistem di mana setiap bagian memiliki peran dan tujuannya masing-masing dengan meningkatkan kemampuan untuk beradaptasi dengan perubahan merupakan hal yang penting.

Terdapat beberapa layer yang dapat digunakan untuk mengaplikasikan prinsip separation of concern, di antaranya sebagai berikut:
1. Feature layer: merupakan presentation layer dari aplikasi yang menampilkan UI dan juga event handler dari UI tersebut.
2. Domain layer: merupakan layer paling dalam yang tidak memiliki dependensi dengan layer yang lain dan memiliki entities, use cases, dan juga repositories.
3. Data layer: merupakan layer data dari aplikasi yang berperan di dalam pengambilan data, seperti API atau dari database lokal.
4. Resources & shared library: merupakan layer yang dapat diakses oleh layer lainnya,  seperti assets(images, fonts, colors, etc) dan juga reusable components, functionalities, dan library dari pihak ketiga.

### Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial)
Pertama-tama, directory baru bernama widgets dibuat. Setelah itu, tambahkan berkas baru bernama left_drawer dan lakukan import untuk halaman-halaman yang ingin dimasukkan ke dalam menu left_drawer. Setelah import selesai dilakukan, lakukan routing untuk halaman yang sudah diimport. Lakukan modifikasi terhadap elemen desain sesuai dengan ketentuan dan juga tampilan yang diinginkan. Setelah left_drawer.dart selesai dibuat, masukkan drawer ke dalam halaman menu.dart. 

Untuk membuat sebuah form sederhana agar nantinya program dapat menampilkan data barang yang telah diinput user, pertama-tama, buat berkas baru dalam direktori lib dengan nama shoplist_form.dart dan implementasikan hal-hal yang dibutuhkan ke dalam file tersebut, seperti membuat variabel baru, column, TextFormField, dan lain sebagainya. Untuk memunculkan dialog, fungsi showDialog() ditambahkan di bagian onPressed dan AlertDialog dimunculkan pada fungsi tersebut. Untuk menambahkan fitur navigasi pada tombol,  maka tambahkan onTap() dan lakukan navigasi ke route add product.

Setelah semua hal di atas dijalankan, pindahkan file sehingga menu.dart dan shoplist_form.dart berada di dalam direktori screens, left_drawer.dart dan shop_card.dart berada di dalam direktori widgets, dan main.dart berada di dalam direktori lib. Perlu diingat bahwa direktori screens dan widgets berada di dalam direktori lib. Program pun selesai!

## Tugas 7

### Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?
Stateless widget adalah widget yang mana properti dan penampilannya tidak akan berubah selama widget tersebut ada. Stateless widget tidak bisa merubah state selama runtime aplikasi yang berarti widget tidak bisa di-redraw selama aplikasi berjalan. Contoh dari stateless widget adalah Icon, IconButton, dan Text.
Stateful widget adalah widget yang bisa mengganti propertinya selama runtime. Karena sifatnya yang dinamis dan mutable, maka stateful widget dapat didraw berkali-kali selama aplikasi berjalan. Stateful widget juga dapat merubah penampilannya untuk merespon event yang telah di-trigger oleh interaksi pengguna atau untuk menerima data. Contoh dari Stateful Widget adalah Checkbox, RadioButton, Form, dan lain lain.

### Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.
- MyApp: Merupakan widget utama yang mewakili aplikasi
- MyHomePage: Merupakan widget utama di mana seluruh widget yang digunakan untuk homepage aplikasi ditampilkan.
- Scaffold: Merupakan struktur dasar aplikasi Flutter yang berfungsi untuk menyediakan kerangka kerja untuk tampilan aplikasi.
- AppBar: Merupakan bar yang digunakan sebagai header dari aplikasi tersebut.
- ShopCard: Merupakan widget yang digunakan untuk menampilkan elemen-elemen yang terdapat di dalam grid, seperti icon dan teks. Respon event pengguna juga dapat direspon melalui widget ini ketika diklik
- SnackBar: Merupakan widget yang berfungsi untuk menampilkan suatu pesan setelah widget diklik.
- Inkwell: Merupakan widget yang berfungsi untuk membuat suatu area responsif terhadap sentuhan pengguna.
- Padding: Layout widget yang digunakan untuk mengatur jarak dalam widget
- Column: Layout widget yang digunakan untuk mengatur widget secara vertikal
- Center: Layout widget yang digunakan untuk membuat suatu elemen berada di tengah-tengah layar.
- Material: Widget yang digunakan untuk mengatur warna latar belakang.

### Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
Pertama-tama, project flutter baru bernama mind_archives_mobile dibuat. Setelah itu, dilakukan modifikasi di dalam file main.dart dengan cara memindahkan 2 class, yaitu MyHomepage dan _MyHomePageState ke dalam file menu.dart yang baru saja dibuat. Setelah itu, dilakukan import di dalam menu.dart dengan import 'package:mind_archives_mobile/menu.dart';

Untuk membuat widget sederhana di dalam aplikasi ini, dilakukan beberapa perubahan dalam file menu.dart. Pertama-tama, buat MyHomepage menjadi stateless, kemudian ubah ({super.key, required this.title}) menjadi ({Key? key}) : super(key: key);. Setelah itu, final String title; akan dihapus dan digantikan dengan method widget build yang baru. Setelah hal tersebut dijalankan, buat class baru bernama ShopItem yang berisi name, icon, dan juga color. Setelah itu, tambahkan item di bawah MyHomePage({Key? key}) : super(key: key);yang bertujuan untuk menampilkan widget dan juga menginisialisasi warna sesuai dengan widget yang ada. Setelah itu, tambahkan method Scaffold dan buat Stateless Widget baru untuk menampilkan card. Di dalam ShopCard, ubah color menjadi item.color agar dapat menggunakan warna yang telah diassign di dalam ShopItem. Setelah melakukan beberapa langkah di atas, aplikasi akan bisa dijalankan :3