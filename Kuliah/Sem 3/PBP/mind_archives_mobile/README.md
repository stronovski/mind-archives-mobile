# mind_archives_mobile

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