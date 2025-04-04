# masterplan

A new Flutter project - Managing State in Flutter

## GIF 
PRAKTIKUM 1
https://github.com/user-attachments/assets/39f42d46-ce8b-492e-af7a-1e282d223b16

## Praktikum 1

1.  Tugas Praktikum 1: Dasar State dengan Model-View
Selesaikan langkah-langkah praktikum tersebut, lalu dokumentasikan berupa GIF hasil akhir praktikum beserta penjelasannya di file README.md! Jika Anda menemukan ada yang error atau tidak berjalan dengan baik, silahkan diperbaiki.
2.  Jelaskan maksud dari langkah 4 pada praktikum tersebut! Mengapa dilakukan demikian?
3.  Mengapa perlu variabel plan di langkah 6 pada praktikum tersebut? Mengapa dibuat konstanta ?
4.  Lakukan capture hasil dari Langkah 9 berupa GIF, kemudian jelaskan apa yang telah Anda buat!
5.  Apa kegunaan method pada Langkah 11 dan 13 dalam lifecyle state ?

Jawaban Praktikum 1

1. Telah Terselesaikan Tanpa Error

---


2. Jelaskan maksud dari langkah 4 pada praktikum tersebut! Mengapa dilakukan demikian?

Langkah 4 menjelaskan tentang pembuatan model data dasar yaitu `Task` dan `Plan`. Model ini digunakan untuk memisahkan logika data dari tampilan (UI). 
- `Task` merepresentasikan satu tugas yang memiliki deskripsi dan status selesai (complete).
- `Plan` adalah kumpulan dari beberapa task, yang memiliki nama dan daftar tugas (tasks).

Langkah ini dilakukan agar data lebih terstruktur, mudah digunakan, dan mendukung pengelolaan state yang baik di aplikasi Flutter. Pendekatan ini juga sesuai dengan prinsip pemrograman yang baik yaitu separation of concerns dan memudahkan proses pengujian serta pemeliharaan aplikasi di masa depan.

---

3. Mengapa perlu variabel plan di langkah 6 pada praktikum tersebut? Mengapa dibuat konstanta?

Variabel `plan` digunakan untuk menyimpan data state aplikasi saat ini, yaitu daftar tugas yang ditampilkan dan dimodifikasi pada layar. Saat pengguna menambahkan, mengedit, atau mencentang tugas, semua perubahan akan disimpan dalam variabel `plan`.

Variabel ini dibuat sebagai konstanta (`const`) karena kelas `Plan` dan `Task` bersifat immutable (tidak dapat diubah). Untuk mengubah isinya, kita perlu membuat objek baru. Dengan menggunakan `const`, kita menjamin bahwa objek tersebut tidak akan berubah sembarangan dan mendukung optimalisasi performa oleh Flutter saat membangun ulang UI.

---

4. Lakukan capture hasil dari Langkah 9 berupa GIF, kemudian jelaskan apa yang telah Anda buat!

Pada langkah 9, aplikasi telah dapat menambahkan daftar tugas menggunakan tombol tambah (+). Ketika tombol ditekan, sebuah task kosong ditambahkan ke daftar. Pengguna kemudian dapat mengisi deskripsi tugas dan mencentang kotak untuk menandai tugas tersebut telah selesai.

GIF yang diambil memperlihatkan:
- Pengguna menekan tombol tambah untuk menambahkan task baru.
- Pengguna mengetik deskripsi di setiap task.
- Pengguna mencentang dan menghapus centang dari task sesuai status penyelesaian.

Fitur ini memperlihatkan penerapan konsep state management di Flutter, di mana perubahan data (state) secara otomatis menyebabkan tampilan (UI) diperbarui menggunakan `setState`.

---

5. Apa kegunaan method pada Langkah 11 dan 13 dalam lifecyle state?

Langkah 11 menggunakan method `initState()` yang merupakan bagian dari lifecycle `State` di Flutter. Method ini dipanggil sekali saat state pertama kali dibuat. Dalam praktikum ini, digunakan untuk menginisialisasi `ScrollController` dan menambahkan listener agar keyboard ditutup otomatis saat pengguna melakukan scroll (terutama di perangkat iOS).

Langkah 13 menggunakan method `dispose()` yang juga bagian dari lifecycle `State`. Method ini dipanggil saat state akan dihapus dari widget tree. Fungsinya untuk membersihkan sumber daya yang digunakan, dalam hal ini untuk memanggil `dispose()` pada `ScrollController` agar tidak terjadi memory leak.

Kedua method ini penting untuk pengelolaan resource secara efisien dan memastikan aplikasi tetap stabil dan optimal.




