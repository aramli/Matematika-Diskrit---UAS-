# Praktikum Ujian Akhir Semester
Tugas Project Ujian Akhir Semester Mata Kuliah Matematika Diskrit<br>

NAMA    : Andi Ramli Hidayat <br>
NIM     : 312510385 <br>
KELAS   : TI.25 C.5

# Penjelasan Program Graf (DFS & BFS)
<ul>
  <li>Tujuan Program</li>
  Program ini dibuat untuk mempelajari dan mendemonstrasikan algoritma traversal pada graf. Traversal berarti menelusuri simpul-simpul (vertex) dalam sebuah graf sesuai aturan tertentu.
Tujuan utamanya:
  <ul>
    <li> Menunjukkan cara kerja DFS (Depth First Search) baik secara rekursif maupun iteratif.</li>
    <li> Menunjukkan cara kerja BFS (Breadth First Search).</li>
    <li> Memberikan contoh implementasi graf sederhana menggunakan Python dengan adjacency list.</li>
</ul>
    Program ini diperuntukkan untuk pembelajaran Matematika Diskrit atau struktur data, khususnya pada materi Graf dan Algoritma Traversal.<br><br>

  
  <li>Konsep Dasar</li>
  <ul>
    <li>DFS (Depth First Search): algoritma penelusuran graf dengan cara masuk sedalam mungkin ke simpul berikutnya sebelum kembali.</li>
    <li>BFS (Breadth First Search): algoritma penelusuran graf dengan cara melebar atau level per level, menelusuri simpul yang berdekatan terlebih dahulu.</li>
    <li>Iteratif vs Rekursif: DFS bisa ditulis dengan cara rekursif (fungsi memanggil dirinya sendiri) atau iteratif (menggunakan stack).</li>
  </ul>
  
  <li>Penjelasan Kode</li>
  <img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/1.png" width="850"/><br>
  1. Pertama-tama, Bagian ini hanya menampilkan identitas mahasiswa dan mata kuliah. Tidak ada logika program di sini, hanya informasi awal ketika program dijalankan.
<br><br>

 <img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/2.png" width="850"/><br>
  2. Selanjutnya, Di sini kita membuat kelas Graph untuk merepresentasikan graf. Konstruktor __init__ menerima jumlah simpul (vertices) dan menyimpannya dalam variabel self.V. Selain itu, dibuat juga self.graph berupa adjacency list, yaitu daftar yang berisi list kosong untuk setiap simpul. Struktur ini digunakan untuk menyimpan hubungan antar simpul sehingga graf dapat direpresentasikan dengan efisien

<br><br>

<img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/3.png" width="850"/><br>
  3. Kemudian, Fungsi add_edge digunakan untuk menambahkan sisi (edge) antara simpul u dan v. Karena graf ini tak berarah (undirected), maka setiap kali kita menambahkan hubungan dari u ke v, kita juga menambahkan hubungan dari v ke u. Dengan cara ini, hubungan antar simpul berlaku dua arah.
<br><br>

<img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/4.png" width="850"/><br>
  4. Lalu, Fungsi dfs adalah implementasi Depth First Search secara rekursif. Algoritma ini bekerja dengan menandai simpul yang sedang dikunjungi, mencetak simpul tersebut, lalu memanggil dirinya sendiri untuk menelusuri simpul tetangga yang belum dikunjungi. Dengan cara ini, DFS akan masuk sedalam mungkin ke dalam graf sebelum kembali ke simpul sebelumnya.
<br><br>

<img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/5.png" width="850"/><br>
  5. Selanjutnya, Fungsi dfs_iterative adalah versi iteratif dari DFS. Prinsipnya sama dengan DFS rekursif, tetapi menggunakan struktur data stack untuk mengatur simpul yang akan dikunjungi. Cara ini menghindari penggunaan rekursi dan lebih cocok untuk graf yang besar.
<br><br>

<img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/6.png" width="850"/><br>
  6. Kemudian, Fungsi bfs adalah implementasi Breadth First Search. Berbeda dengan DFS, BFS menggunakan struktur data queue untuk menelusuri graf secara melebar. BFS akan mengunjungi semua simpul tetangga terlebih dahulu sebelum pindah ke level berikutnya.
<br><br>

<img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/7.png" width="850"/><br>
  7. Terakhir, Pada bagian main program, dibuat sebuah graf dengan empat simpul, yaitu 0, 1, 2, dan 3. Kemudian ditambahkan beberapa sisi: simpul 0 terhubung ke simpul 1 dan 2, simpul 1 terhubung ke simpul 2, dan simpul 2 terhubung ke simpul 3. Setelah graf terbentuk, program menjalankan DFS mulai dari simpul 0, lalu menjalankan BFS juga mulai dari simpul 0.
<br><br>

  <li>Hasil Output</li>
  <img src="https://github.com/aramli/Matematika-Diskrit---UAS-/raw/main/img/8.png" width="850"/><br>
  1. DFS<br><br>
  Ketika program menjalankan DFS mulai dari simpul 0, urutan simpul yang dikunjungi adalah 0 → 1 → 2 → 3. Hal ini terjadi karena DFS selalu masuk sedalam mungkin. Dari simpul 0, algoritma langsung masuk ke simpul 1. Dari 1, ia menemukan tetangga 2, lalu masuk ke 2. Dari 2, ia menemukan simpul 3 dan masuk ke sana. Setelah semua simpul dikunjungi, traversal selesai. Jadi, hasil DFS menunjukkan pola penelusuran yang fokus ke kedalaman graf terlebih dahulu.
 2. BFS <br><br>
 Ketika program menjalankan BFS mulai dari simpul 0, urutan simpul yang dikunjungi adalah 0 → 1 → 2 → 3. Bedanya dengan DFS, BFS menelusuri simpul secara melebar.    Dari simpul 0, algoritma mengunjungi semua tetangga langsung yaitu 1 dan 2. Setelah itu, BFS melanjutkan ke simpul berikutnya dalam antrian, yaitu 3 yang merupakan  tetangga dari 2. Traversal selesai setelah semua simpul dikunjungi. Jadi, hasil BFS menunjukkan pola penelusuran yang fokus ke simpul-simpul yang berdekatan terlebih dahulu sebelum pindah ke level berikutnya.

</ul>
