Nama: Aminudin Wijaya  
NRP: 5025241242  
Kelas: Pemrograman Berbasis Kerangka Kerja \- C

Soal.

1. Jelaskan perbedaan aplikasi desktop dengan aplikasi lain? Mengapa masih dibutuhkan  
   

| Parameter Evaluasi | Aplikasi Desktop | Aplikasi berbasis Web (PWA) | Aplikasi Mobile (IOS/Android) | Web-Wrapper (Electron/WebView2) |
| :---- | :---- | :---- | :---- | :---- |
| Cara Kerja | Dijalankan langsung sebagai proses *Native* di lingkungan desktop (.net berarti di lingkungan Windows). Memiliki akses penuh terhadap resource seperti Win32 API, DirectX GPU Acceleration, dsj | Dijalankan di atas *Sandbox* Web Browser. Akses ke resource terbatas (dibatasi Browser) | Dijalankan pada OS Perangkat *Mobile*. Seringkali terdampak oleh siklus manajemen baterai pada perangkat *Mobile*, yang menyebabkan ada nya penurunan performa terutama saat berjalan di latar belakang  | Berjalan di atas sebuah browser buatan berbasis Chromium. Membuat konsumsi RAM menjadi besar bahkan untuk aplikasi dengan fitur yang sangat simpel. |
| *Network Dependency* | Sangat mungkin untuk dijalankan secara offline, terlebih jika semua fitur tidak membutuhkan koneksi keluar (internet). | Bergantung pada koneksi terhadap *Server* *Backend*. Dapat dijalankan secara lokal dengan syarat *Server Backend* juga berada di jaringan lokal | Sangat mungkin untuk dijalankan secara offline, terlebih jika semua fitur tidak membutuhkan koneksi keluar (internet). | Tergantung pada konsep yang dibawa, jika bundle Electron/WebView2 juga menyertakan [node.js](http://node.js) sebagai *Backend Server*, maka arsitektur dapat dimungkinkan offline |
| Performa dan Konsumsi RAM | Sangat efisien, cepat dan hemat RAM (memori), karena rendah nya overhead serta kemampuan untuk memaksimalkan *computing power* secara maksimal | Terdapat banyak overhead proses yang memberatkan pada performa serta konsumsi RAM. Salah satu hal yang paling terasa adalah beban konsumsi RAM untuk menjalankan *Browser Engine* bahkan sebelum aplikasi kita dimuat. | Bergantung pada framework dan bahasa yang digunakan, jika rendah dan minim overhead, maka akan cukup cepat dan rendah penggunaan RAM. Akan tetapi, *computing power* yang dimiliki perangkat *Mobile* pada dasarnya cukup rendah jika dibandingkan dengan perangkat desktop | Paling boros sumber daya dikarenakan mekanisme bundling berbasis Chromium nya. Setiap aplikasi menjalankan sebuah browser Chromium independent. Salah satu sumber daya yang paling boros adalah sumber daya dari sisi RAM (memori) |
| Rancangan UX | Dirancang untuk berjalan maksimal dengan menggunakan perangkat HID (*Human Input Device)* berupa *Mouse/Touchpad* dan *Keyboard* | Dirancang untuk berjalan dengan ekosistem inputan browser | Dirancang untuk berjalan maksimal di ekosistem perangkat *Mobile* yang mayoritas menggunakan HID (*Human Input Device)* berupa *touchscreen* | Dirancang untuk berjalan maksimal selayaknya aplikasi desktop native, namun seringkali tetap mengalami keterbatasan terutama untuk berinteraksi dengan sistem kontrol bawaan OS |

   Kesimpulan: Aplikasi Desktop masih diperlukan terutama untuk aplikasi-aplikasi yang mengandalkan performa, atau untuk memaksimalkan *Computing Power* yang dimiliki oleh perangkat desktop. Salah satu contoh penggunaannya adalah aplikasi desktop untuk menampilkan data telemetri penting terkait performa sebuah sistem yang wajib *Realtime*. Sebagai contoh, sistem telemetri untuk performa mobil balap Formula One.

2. Tuliskan problem yang akan diselesaikan oleh aplikasi yang kamu buat? Definisikan fitur aplikasi yang merupakan solusi dari problem tersebut.   
   Problem yang ingin diselesaikan oleh Aplikasi SIHIFA (Sistem Informasi Hiburan dan Media Favorit).  
- Fragmentasi Data terkait Hobi dan hiburan: Setiap segment hobi dan hiburan biasa nya memiliki platform nya masing-masing untuk menyimpan database informasi. Sebagai contoh seperti MAL (MyAnimeList) untuk database Anime, Manga, dan jejepangan lainnya, Letterboxd untuk film, Spotify untuk musik, Notion untuk materi pengetahuan, dan sebagai nya.  
- Ketergantungan terhadap platform pihak ketiga: Karena platform-platform tersebut adalah platform pihak ketiga, tidak ada jaminan untuk di kemudian hari platform tersebut akan tetap exist dan dapat kita gunakan

Solusi yang dibawakan oleh Aplikasi SIHIFA (Sistem Informasi Hiburan dan   
	Media Favorit).

- Manajemen database/koleksi lintas Hobi dan Hiburan: SIHIFA mampu menampung banyak sekali kategori-kategori hobi maupun hiburan seperti Anime, Film, Buku, Musik dan lain sebagainya. Membuatnya menjadi satu platform tersentral untuk tempat kita menyimpan dan mengeksplorasi konten terkait Hobi dan Hiburan.  
- Offline-first dan Open Source: SIHIFA kami bangun dengan prinsip offline-first serta kode nya juga dibuat sebagai *Open Source* yang menghilangkan kekhawatiran atas pembatasan maupun hilangnya akses yang dapat terjadi jika kita menggunakan platform pihak ketiga.

