# Tugas 7
### Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget, dan jelaskan perbedaan dari keduanya.
Stateless Widget adalah widget yang tidak memiliki state alias tidak dapat berubah. Stateless Widget hanya memiliki satu build method yang digunakan untuk mengembalikan widget yang akan ditampilkan sehingga ketika ada data yang berubah, widget ini tidak akan berubah. Sedangkan, Stateful Widget adalah widget yang memiliki state alias dapat berubah. Hal ini karena Stateful Widget memiliki dua class, yaitu StatefulWidget untuk membuat widget dan State sebagai tempat untuk menyimpan data yang dapat berubah. Ketika ada data yang berubah, widget ini akan di rebuild sehingga data yang ditampilkan akan berubah.

### Sebutkan widget apa saja yang kamu gunakan pada proyek ini dan jelaskan fungsinya.
1. Scaffold
    Menyediakan struktur dasar untuk halaman, termasuk area untuk AppBar dan body. Digunakan sebagai wadah utama untuk tampilan halaman ini.
2. AppBar 
    Bagian atas halaman yang biasanya digunakan untuk menampilkan judul atau navigasi. Di sini, digunakan untuk menampilkan judul aplikasi, yaitu "Luveina's Store".
3. Padding
    Menambahkan ruang di sekitar elemen. Digunakan di dalam body halaman untuk memberi jarak di sekeliling konten halaman.
4. Column
    Menyusun widget secara vertikal. Digunakan untuk menyusun elemen-elemen dalam satu kolom di dalam body.
5. Row
    Menyusun widget secara horizontal. Digunakan untuk menampilkan tiga kartu informasi (InfoCard) secara horizontal.
6. InfoCard
    Merupakan StatelessWidget kustom yang menampilkan judul dan isi dalam bentuk kartu. Menggunakan widget dasar Card, Container, dan Text untuk menampilkan konten statis.
7. Center
    Menempatkan elemen di tengah layar. Digunakan untuk mengatur konten utama agar berada di tengah halaman.
8. GridView.count
    Menyusun elemen dalam bentuk grid dengan jumlah kolom tertentu. Di sini digunakan untuk menampilkan daftar ItemCard dalam bentuk grid dengan 3 kolom.
9. ItemCard
    Merupakan StatelessWidget kustom yang menampilkan kartu dengan ikon dan teks. Menggunakan Material, InkWell, dan Container untuk membuat efek tombol dengan animasi klik.
10. Material
    Memberikan desain material pada widget. Digunakan di dalam ItemCard untuk memberikan warna latar dan border melengkung.
11. InkWell
    Memberikan efek klik (ripple effect) pada widget yang bisa ditekan. Di sini, digunakan pada ItemCard agar bisa merespons ketika kartu ditekan.
12. Container
    Wadah yang bisa digunakan untuk mengatur ukuran, padding, dan warna. Digunakan di berbagai tempat untuk mengatur tata letak dan ukuran widget.
13. Icon
    Menampilkan ikon berdasarkan tipe data IconData. Digunakan di dalam ItemCard untuk menampilkan ikon sesuai dengan data pada ItemHomepage.
14. Text
    Menampilkan teks. Digunakan di berbagai tempat seperti di AppBar, InfoCard, dan ItemCard untuk menampilkan judul, konten, dan nama item.
15. SnackBar
    Menampilkan pesan notifikasi singkat di bagian bawah layar. Digunakan dalam ItemCard untuk menampilkan pesan saat tombol ditekan.

### Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
`setState()` berfungsi untuk memberitahu framework bahwa ada perubahan pada data atau variabel yang berdampak pada tampilan. Ketika `setState()` dipanggil, method `build()` dari widget terkait akan dijalankan sehingga tampilan akan diperbarui untuk mencerminkan perubahan data terbaru. Variabel yang dapat terdampak oleh `setState()` adalah variabel yang digunakan dalam widget yang di-rebuild, baik langsung maupun tidak langsung. Variabel ini bisa berupa variabel lokal di dalam method `build()` atau variabel di luar method `build()` yang digunakan dalam membangun tampilan widget.

### Jelaskan perbedaan antara const dengan final.
Perbedaan antara `const` dan `final` adalah `const` harus diinisialisasi dengan nilai konstan pada saat deklarasi. Sedangkan, `final` dapat diinisialisasi dengan nilai yang dihitung pada saat runtime.

### Jelaskan bagaimana cara kamu mengimplementasikan checklist-checklist di atas.
1. Membuat repository baru di GitHub dengan nama "luveinastore-mobile".
2. Membuat proyek Flutter baru dengan nama "luveina_store"
3. Membuat `menu.dart` dan memindahkan MyHomePage _MyHomePageState dari `main.dart` ke dalam `menu.dart` sebagai file utama yang berisi daftar item yang akan ditampilkan.
4. Mengubah MyHomePage menjadi StatelessWidget dan Membuat class `ItemHomepage` untuk menyimpan data item dan menambahkan variabel `item` untuk menyimpan daftar item yang akan ditampilkan.
5. Membuat class `ItemCard` sebagai StatelessWidget kustom untuk menampilkan kartu item dengan ikon dan teks.
6. Membuat Card yang Berisi NPM, Nama, dan Kelas dalam class InfoCard.
7. Membuat 3 button yang berisi icon dan text "Lihat Daftar Produk", "Tambah Produk", dan "Logout".

# Tugas 8
### Apa kegunaan const di Flutter? Jelaskan apa keuntungan ketika menggunakan const pada kode Flutter. Kapan sebaiknya kita menggunakan const, dan kapan sebaiknya tidak digunakan?
`const` digunakan untuk membuat variabel yang nilainya konstan pada saat kompilasi. Keuntungan menggunakan `const` adalah mempercepat proses kompilasi dan mengurangi penggunaan memori karena nilai variabel yang sama hanya disimpan sekali. Sebaiknya menggunakan `const` ketika nilai variabel tidak berubah sepanjang aplikasi dan digunakan secara berulang. Sebaliknya, sebaiknya tidak menggunakan `const` ketika nilai variabel dapat berubah atau hanya digunakan sekali.

### Jelaskan dan bandingkan penggunaan Column dan Row pada Flutter. Berikan contoh implementasi dari masing-masing layout widget ini!
`Column` digunakan untuk menyusun widget secara vertikal alias dari atas ke bawah, sedangkan `Row` digunakan untuk menyusun widget secara horizontal alias dari kiri ke kanan. 

Contoh implementasi `Column`:
```dart
content: SingleChildScrollView(
    child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
            children: [
                Text('Product Name: $_name'),
                Text('Description: $_description'),
                Text('Amount: $_amount'),
            ],
        ),
),
```
Contoh implementasi `Row`:
```dart
content: SingleChildScrollView(
    child: Row(
        mainAxisAlignment: MainAxisAlignment.spaceEvenly,
        children: [
            Text('Product Name: $_name'),
            Text('Description: $_description'),
            Text('Amount: $_amount'),
        ],
    ),
),
```

### Sebutkan apa saja elemen input yang kamu gunakan pada halaman form yang kamu buat pada tugas kali ini. Apakah terdapat elemen input Flutter lain yang tidak kamu gunakan pada tugas ini? Jelaskan!
Elemen input yang digunakan pada halaman form adalah `TextFormField` untuk memasukkan name, description, dan amount. Elemen input Flutter lain yang tidak digunakan pada tugas ini adalah `CupertinoTextField` yang memiliki desain khas iOS.

### Bagaimana cara kamu mengatur tema (theme) dalam aplikasi Flutter agar aplikasi yang dibuat konsisten? Apakah kamu mengimplementasikan tema pada aplikasi yang kamu buat?
Cara mengatur tema dalam aplikasi Flutter adalah dengan menggunakan `ThemeData` dan `Theme` di dalam `MaterialApp`. Dengan menggunakan `ThemeData`, kita dapat mengatur warna, font, dan gaya widget secara konsisten di seluruh aplikasi. Pengimplementasian tema pada aplikasi agar konsisten dilakukan dengan menambahkan `ThemeData` di dalam `MaterialApp` dan mengatur warna primer dan sekunder serta font default.

### Bagaimana cara kamu menangani navigasi dalam aplikasi dengan banyak halaman pada Flutter?
Navigasi dalam aplikasi dengan banyak halaman pada Flutter dapat ditangani dengan menggunakan `Navigator` dan `MaterialPageRoute`. Dengan `Navigator`, kita dapat melakukan navigasi antar halaman dengan push dan pop. Untuk melakukan navigasi, kita dapat menggunakan `Navigator.push()` untuk menambahkan halaman baru dan `Navigator.pop()` untuk kembali ke halaman sebelumnya. Selain itu, kita juga dapat menggunakan `MaterialPageRoute` untuk mengatur transisi antar halaman.

# Tugas 9
### Jelaskan mengapa kita perlu membuat model untuk melakukan pengambilan ataupun pengiriman data JSON? Apakah akan terjadi error jika kita tidak membuat model terlebih dahulu?
Model digunakan untuk mengonversi data JSON menjadi objek yang dapat diakses dan diubah dengan mudah. Dengan model, kita dapat mengatur struktur data yang akan diambil atau dikirim sehingga memudahkan proses pengambilan dan pengiriman data. Jika tidak membuat model terlebih dahulu, maka akan sulit untuk mengakses data JSON karena data tersebut hanya berupa string dan tidak memiliki struktur yang jelas.

### Jelaskan fungsi dari library http yang sudah kamu implementasikan pada tugas ini
Library http digunakan untuk melakukan permintaan HTTP ke server dan menerima respon dari server. Dengan library http, kita dapat melakukan berbagai metode HTTP seperti GET, POST, PUT, DELETE, dll. Library http juga menyediakan berbagai fitur seperti header, body, dan parameter untuk mengirim data ke server dan menerima respon dari server.

### Jelaskan fungsi dari CookieRequest dan jelaskan mengapa instance CookieRequest perlu untuk dibagikan ke semua komponen di aplikasi Flutter.
CookieRequest adalah class yang digunakan untuk membuat permintaan HTTP dengan cookie. CookieRequest perlu dibagikan ke semua komponen di aplikasi Flutter agar cookie yang diterima dari server dapat disimpan dan digunakan di seluruh aplikasi. Dengan menggunakan CookieRequest, kita dapat menyimpan cookie yang diterima dari server dan mengirim cookie saat melakukan permintaan HTTP ke server.

### Jelaskan mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter.
Mekanisme pengiriman data mulai dari input hingga dapat ditampilkan pada Flutter adalah sebagai berikut:
1. Membuat form input dengan TextFormField untuk memasukkan data.
2. Menyimpan data yang dimasukkan oleh pengguna ke dalam variabel.
3. Mengirim data ke server dengan menggunakan library http dan CookieRequest.
4. Menerima respon dari server dan mengonversi respon menjadi objek yang dapat diakses.
5. Menampilkan data yang diterima dari server ke dalam widget seperti Text atau ListView.

### Jelaskan mekanisme autentikasi dari login, register, hingga logout. Mulai dari input data akun pada Flutter ke Django hingga selesainya proses autentikasi oleh Django dan tampilnya menu pada Flutter.
Mekanisme autentikasi dari login, register, hingga logout adalah sebagai berikut:
1. Pengguna memasukkan data akun seperti username dan password pada form login atau register di Flutter.
2. Data akun yang dimasukkan oleh pengguna dikirim ke server Django dengan menggunakan library http dan CookieRequest.
3. Server Django melakukan autentikasi data akun yang diterima dari Flutter.
4. Jika autentikasi berhasil, server Django mengirim respon berupa token atau cookie ke Flutter.
5. Flutter menyimpan token atau cookie yang diterima dari server Django dan menampilkan menu atau halaman utama aplikasi.

### Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step! (bukan hanya sekadar mengikuti tutorial).
1. Membuat app baru dengan nama "authentication" di project Django sebelumnya dan membuat fungsi-fungsi untuk login, logout, dan register pada `views.py` yang terdapat di dalamnya.
2. Menginstall package yang telah disediakan oleh tim asisten dosen dengan cara menjalankan:
```dart
flutter pub add provider
flutter pub add pbp_django_auth
```
3. Memodifikasi root widget agar menyediakan CookieRequest library ke semua child widgets dengan menggunakan Provider.
4. Membuat berkas `login.dart` dan `register.dart` yang akan memanfaatkan CookieRequest untuk melakukan autentikasi.
5. Membuat model pada flutter untuk menyimpan data user yang diterima dari server Django dengan menggunakan Quicktype.
6. Menerapkan fetch data dari Django untuk ditampilkan ke Flutter.
7. Mengintegrasikan form pada Flutter dengan layanan Django.
