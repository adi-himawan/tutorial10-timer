## Tutorial 10 - Timer

#### Commit 2 
![Commit 2](/img/commit2.png)

Berdasarkan lampiran di atas, dapat dilihat bahwa pesan pertama yang ditampilkan adalah "Awan's Komputer: hey hey!". Hal ini bisa terjadi karena baris kode untuk mencetak pesan tersebut dieksekusi sebelum `drop(spawner)` dan `executor.run()`. 

Ketika executor mulai berjalan, task yang telah di-spawn sebelumnya akan mulai dieksekusi. Oleh karena itu, program menampilkan pesan "Awan's Komputer: howdy!" dan setelah jeda 2 detik, program juga menampilkan pesan "Awan's Komputer: done!". Sebagai kesimpulan, program mencetak pesan "Awan's Komputer: hey hey!" terlebih dahulu karena `println!("Awan's Komputer: hey hey!")` berada di luar eksekusi baris kode untuk spawner dan executor yang bersifat asynchronous.