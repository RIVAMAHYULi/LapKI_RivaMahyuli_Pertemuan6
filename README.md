# LapKI_RivaMahyuli_Pertemuan6

PEMBAHASAN
Firewall dan Intrusion Detection Systems (IDS) sering digunakan untuk mengotomatisasi sebagian tugas pemantauan lalu lintas. Baik firewall dan IDS mencocokkan lalu lintas masuk dengan aturan administratif. Firewall biasanya membandingkan header paket dengan kumpulan aturan sementara IDS sering menggunakan muatan paket untuk perbandingan kumpulan aturan. Karena firewall dan IDS menerapkan aturan yang telah ditentukan sebelumnya ke bagian yang berbeda dari paket IP, IDS dan aturan firewall memiliki struktur yang berbeda.

PERTANYAAN 1
Pada VM CyberOps Workstation ketika kita menjalankan mininet dan menuliskan perintah xterm R1 di prompt maka Shell R1 terbuka di jendela terminal dengan teks hitam dan latar belakang putih.Pengguna apa yang masuk ke shell itu? Ini indikatornya apa??

--> pengguna yang masuk ke shell R1 adalah pengguna yang sedang menjalankan perintah "xterm R1" di prompt Mininet. Jadi, pengguna tersebut memiliki akses ke shell virtual R1 pada jaringan simulasi Mininet yang sedang berjalan.

Indikator yang terlihat adalah tampilan jendela terminal yang muncul setelah perintah "xterm R1" dijalankan, dengan teks hitam dan latar belakang putih, menunjukkan bahwa shell R1 sudah aktif dan siap digunakan.

PERTANYAAN 2
Port apa yang digunakan saat berkomunikasi dengan server web malware? Apa indikatornya?

-->Port yang umumnya digunakan saat berkomunikasi dengan server web malware adalah port 80 (HTTP) atau port 443 (HTTPS). Kedua port ini merupakan port standar untuk protokol web, sehingga seringkali tidak terdeteksi oleh firewall atau sistem keamanan.

Beberapa indikator yang dapat menunjukkan komunikasi dengan server web malware antara lain:
1. Aktivitas koneksi jaringan yang tidak biasa atau tidak diharapkan pada port 80 atau 443.
2. Koneksi ke alamat IP atau nama domain yang tidak dikenal atau mencurigakan.
3. Aktivitas HTTP yang tidak biasa, seperti penggunaan header HTTP yang tidak standar, atau pengiriman permintaan HTTP yang aneh atau terenkripsi.
4. Adanya file-file dengan ekstensi yang mencurigakan atau tidak umum, yang mungkin merupakan bagian dari malware yang diunduh atau diinstal melalui koneksi web yang tidak aman.

PERTANYAAN 3
Entri peringatan
ditunjukkan di bawah ini. Stempel waktu Anda akan berbeda:
04/28-17:00:04.092153 [**] [1:1000003:0] Malicious Server Hit! [**]
[Priority: 0] {TCP} 209.165.200.235:34484 -> 209.165.202.133:6666

* Berdasarkan peringatan yang ditunjukkan di atas, apa alamat IPv4 sumber dan tujuan yang digunakan dalam transaksi?
> Alamat IPv4 sumber adalah 209.165.200.235 dan alamat IPv4 tujuan adalah 209.165.202.133. Hal ini dapat diketahui dari informasi pada bagian akhir peringatan yang menunjukkan port sumber dan tujuan. Simbol "->" menunjukkan arah koneksi, di mana alamat IP sumber adalah 209.165.200.235 dan port sumber adalah 34484, sedangkan alamat IP tujuan adalah 209.165.202.133 dan port tujuan adalah 6666. Selain itu, peringatan tersebut juga menunjukkan bahwa transaksi menggunakan protokol TCP.

* Berdasarkan alert di atas, port sumber dan tujuan apa yang digunakan dalam transaksi?
> Port sumber yang digunakan dalam transaksi adalah 34484, dan port tujuan yang digunakan adalah 6666.Hal ini dapat dilihat dari informasi pada bagian akhir peringatan, yang menunjukkan port sumber dan tujuan yang digunakan dalam transaksi. Simbol "->" menunjukkan arah koneksi, di mana port sumber adalah 34484 dan alamat IP sumber adalah 209.165.200.235, sedangkan port tujuan adalah 6666 dan alamat IP tujuan adalah 209.165.202.133. Selain itu, peringatan tersebut juga menunjukkan bahwa transaksi menggunakan protokol TCP.

* Berdasarkan peringatan yang ditunjukkan di atas, kapan pengunduhan dilakukan? 
> Pengunduhan dilakukan pada 04/28 17:00:04

* Berdasarkan peringatan yang ditunjukkan di atas, apa pesan yang direkam IDS signature?

> IDS signature yang direkam dalam peringatan di atas adalah "Malicious Server Hit!". Nomor ID aturan signature adalah 1:1000003 dan prioritasnya adalah 0. Signature atau aturan IDS (Intrusion Detection System) digunakan untuk mendeteksi pola atau tanda-tanda dari serangan atau aktivitas yang mencurigakan pada jaringan. Dalam peringatan di atas, IDS signature digunakan untuk mendeteksi adanya serangan atau aktivitas mencurigakan yang terdeteksi pada jaringan, yang kemudian menghasilkan peringatan untuk memperingatkan administrator jaringan.

PERTANYAAN 4
Bagaimana file PCAP ini berguna bagi analis keamanan?
File PCAP adalah file yang merekam lalu lintas jaringan yang diambil dari sebuah interface jaringan. File PCAP dapat sangat berguna bagi analis keamanan untuk menganalisis dan memeriksa aktivitas jaringan dan mencari tahu apakah ada aktivitas mencurigakan atau ancaman keamanan yang terjadi pada jaringan tersebut.

Berikut adalah beberapa cara file PCAP dapat berguna bagi analis keamanan:

- Menganalisis lalu lintas jaringan: File PCAP dapat digunakan untuk menganalisis lalu lintas jaringan dan mengidentifikasi protokol dan aplikasi yang digunakan, sumber dan tujuan koneksi, dan data yang ditransfer.
- Mendeteksi serangan jaringan: File PCAP dapat digunakan untuk mendeteksi serangan jaringan seperti Denial of Service (DoS), malware, atau serangan phishing.
- Investigasi insiden keamanan: File PCAP dapat membantu dalam investigasi insiden keamanan dengan memberikan bukti elektronik dan memperlihatkan aktivitas yang terjadi pada jaringan pada saat insiden terjadi.
- Monitoring jaringan: File PCAP dapat digunakan untuk monitoring jaringan dan mendeteksi aktivitas mencurigakan pada jaringan dalam waktu nyata atau ketika sedang menganalisis lalu lintas yang telah direkam sebelumnya.
- Dengan menggunakan alat analisis lalu lintas jaringan seperti Wireshark, analis keamanan dapat memeriksa file PCAP dan menganalisis lalu lintas jaringan untuk mendeteksi ancaman keamanan atau masalah jaringan.

PERTANYAAN 5
Rantai apa yang saat ini digunakan oleh R1?
Berdasarkan output perintah iptables -L -v yang diberikan, saat ini R1 menggunakan tiga rantai, yaitu:

INPUT
FORWARD
OUTPUT
Setiap rantai memiliki kebijakan default ACCEPT, yang berarti setiap paket yang masuk, diteruskan atau keluar diizinkan oleh R1. Saat ini, belum ada aturan tambahan yang ditambahkan ke dalam rantai-rantai tersebut.

PERTANYAAN 6
Apakah unduhan berhasil kali ini? jelaskan
> Berdasarkan output yang diberikan, unduhan gagal dilakukan. Hal ini dapat dilihat dari pesan "Connecting to 209.165.202.133:6666... failed: Connection timed out." yang muncul pada kedua percobaan unduhan. Pesan tersebut menunjukkan bahwa tidak terdapat koneksi yang berhasil terjalin antara H5 dan server yang diminta untuk mengunduh file tersebut. Oleh karena itu, dapat disimpulkan bahwa unduhan tidak berhasil dilakukan.

Apa pendekatan yang lebih agresif tetapi juga valid saat memblokir server yang melanggar?

> Pendekatan yang lebih agresif tetapi juga valid untuk memblokir server yang melanggar adalah dengan menggunakan tindakan penangkapan atau pemblokiran secara langsung di firewall, IPS, atau perangkat keamanan jaringan lainnya.

Tindakan ini dapat dilakukan dengan menambahkan aturan pada firewall atau IPS yang memblokir semua koneksi yang berasal dari atau menuju ke server yang melanggar. Selain itu, tindakan penangkapan dapat dilakukan dengan mengisolasi server yang melanggar dari jaringan atau memblokir port yang digunakan oleh server tersebut.

Namun, sebelum melakukan tindakan yang agresif tersebut, sebaiknya dianalisis terlebih dahulu dampak yang mungkin ditimbulkan oleh tindakan tersebut terhadap jaringan dan sistem yang terhubung. Tindakan yang terlalu agresif dapat mempengaruhi operasi jaringan atau sistem yang tidak berkaitan dengan server yang melanggar. Oleh karena itu, sebaiknya tindakan yang dilakukan harus dipertimbangkan secara matang dan dilakukan dengan hati-hati.
