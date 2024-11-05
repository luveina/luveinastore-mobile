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

