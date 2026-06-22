Struktur Data: Array dan Linked List
1. Karakteristik Memori dan Akses Data

Array dapat mengakses elemen secara langsung menggunakan indeks karena data disimpan secara berurutan (kontinu) di memori. Oleh karena itu alamat elemen dapat dihitung dengan cepat sehingga kompleksitas aksesnya O(1).

Sedangkan pada Singly Linked List, node disimpan secara tidak berurutan (non-kontinu) dan setiap node hanya menyimpan alamat node berikutnya. Untuk mengakses elemen tertentu, pencarian harus dimulai dari node pertama hingga node yang dicari ditemukan. Karena itu kompleksitas aksesnya O(n).

Kesimpulan:

Array → memori kontinu → akses O(1)
Linked List → memori non-kontinu → akses O(n)
2. Analisis Efisiensi Operasi Manipulasi

Linked List lebih unggul dibandingkan Array untuk operasi penyisipan (insertion) dan penghapusan (deletion).

Pada Array, ketika menyisipkan atau menghapus data di tengah, elemen-elemen lain harus digeser sehingga membutuhkan waktu O(n).

Pada Linked List, cukup mengubah pointer antar node tanpa perlu menggeser data sehingga membutuhkan waktu O(1) apabila posisi node sudah diketahui.

Alasan Teoritis:

Array menggunakan lokasi memori berurutan sehingga perubahan ukuran memerlukan pergeseran elemen.
Linked List menggunakan hubungan antar pointer sehingga lebih fleksibel dalam manipulasi data.
3. Konsep Doubly Linked List

Doubly Linked List adalah struktur data yang setiap node memiliki dua pointer:

Pointer ke node berikutnya (next)
Pointer ke node sebelumnya (prev)

Struktur node:

[Prev | Data | Next]
Dampak Pointer Tambahan

Kelebihan:

Dapat ditelusuri maju dan mundur.
Penghapusan node lebih mudah.
Navigasi data lebih fleksibel.

Kekurangan:

Membutuhkan memori lebih besar karena ada pointer tambahan.
Implementasi lebih kompleks dibandingkan Singly Linked List.
4. Mekanisme Circular Linked List

Circular Linked List adalah Linked List yang node terakhirnya menunjuk kembali ke node pertama.

Perbedaannya dengan Linked List biasa:

Linked List biasa: node terakhir menunjuk ke NULL.
Circular Linked List: node terakhir menunjuk ke head (node pertama).
Use Case

Contoh penggunaan Circular Linked List:

Sistem Round Robin pada CPU Scheduling.
Playlist musik yang diputar berulang.
Permainan berbasis giliran pemain.

Struktur ini efektif karena proses dapat berulang tanpa harus kembali ke awal secara manual.

5. Array Dinamis di Python

Python List diimplementasikan sebagai Dynamic Array.

Ketika kapasitas array penuh dan dilakukan operasi append(), Python akan:

Mengalokasikan memori baru yang lebih besar.
Menyalin seluruh elemen lama ke memori baru.
Menambahkan elemen baru.
Membebaskan memori lama.

Meskipun proses resize membutuhkan waktu O(n), operasi append() secara rata-rata (amortized) tetap memiliki kompleksitas O(1) karena resize tidak terjadi setiap saat.

Contoh:

data = [1, 2, 3]
data.append(4)

Jika kapasitas masih tersedia, elemen langsung ditambahkan. Jika kapasitas penuh, Python melakukan resize terlebih dahulu.

