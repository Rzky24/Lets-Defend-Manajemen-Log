# Lets-Defend-Manajemen-Log
Sebagai Analis SOC, Anda akan melakukan banyak analisis log. Karena alasan ini, penting untuk memahami sistem/solusi "Manajemen Log". Tidak masalah produk apa yang Anda gunakan, yang penting adalah mengetahui apa yang harus dicari dan di mana mencarinya.



Bagian selanjutnya dari pelajaran ini membahas bagaimana solusi "Manajemen Log" dapat digunakan secara efektif oleh analis SOC.



Apa itu Manajemen Log?
Sesuai namanya, Manajemen Log menyediakan akses ke semua log dalam suatu lingkungan (log web, log OS, firewall, proxy, EDR, dll.) dan memungkinkan Anda untuk mengelolanya di satu tempat. Hal ini meningkatkan efisiensi dan menghemat waktu.



Jika Anda tidak dapat mengakses log dari satu tempat, maka permintaan yang sama (misalnya, tujuannya adalah untuk menentukan semua pengguna di letsdefend.io) harus dikirim ke perangkat yang berbeda. Hal ini akan meningkatkan kemungkinan kesalahan dan jumlah waktu yang perlu Anda habiskan.



Jika Anda membuka halaman “Manajemen Log” di LetsDefend, Anda akan melihat berbagai sumber log seperti Proxy, Exchange, dan Firewall yang terdaftar sebagai “Tipe”. Ini berarti bahwa semua sumber log ini telah dikumpulkan di satu tempat dan output log dari sumber seperti Proxy, FW, dll. dapat dilihat hanya dengan satu kueri.

<img width="1563" height="525" alt="image" src="https://github.com/user-attachments/assets/a7737ea9-3bc4-4b93-949c-b9558941f246" />
Tujuan Manajemen Log
Analis SOC biasanya mengandalkan Manajemen Log untuk menentukan apakah ada komunikasi dengan alamat tertentu dan untuk melihat detail komunikasi tersebut. Misalnya, Anda menemukan sebuah malware dan setelah menjalankannya, Anda menemukan bahwa malware tersebut berkomunikasi dengan dan mengeksekusi perintah dari alamat "letsdefend.io". Dalam situasi ini, pusat komando & kontrol adalah "letsdefend.io", Anda dapat mencari "letsdefend.io" di manajemen log perusahaan Anda untuk melihat apakah ada perangkat yang mencoba berkomunikasi dengan pusat komando & kontrol tersebut.



Hal ini membawa kita pada situasi kedua: Anda melihat peringatan SIEM yang menunjukkan bahwa perangkat LetsDefendHost di jaringan Anda membocorkan data ke alamat IP 122[.]194[.]229[.]59. Anda telah melakukan investigasi, mengisolasi perangkat dari jaringan, melakukan proses yang diperlukan, dan sekarang Anda memegang kendali. Tetapi masih ada sesuatu yang belum Anda tangani: apakah ada perangkat lain yang mengirim data ke alamat IP yang mencurigakan (122[.]194[.]229[.]59)? Peringatan tersebut mungkin hanya mencakup LetsDefendHost, tetapi Anda tetap harus mencari alamat yang mencurigakan di Manajemen Log untuk melihat apakah ada sesuatu yang mungkin belum terdeteksi oleh sistem dan mencoba menemukan koneksi apa pun.



Lakukan pencarian log dasar:

Pertanyaan

Alamat IP sumber mana yang memasukkan URL 'https://github.com/apache/flink/compare'? 172.16.17.54
Jawaban: Buka halaman Manajemen Log, di sisi kanan Anda akan melihat bilah pencarian, tempel tautan tersebut dan lihat alamat IP-nya.
<img width="1400" height="468" alt="image" src="https://github.com/user-attachments/assets/695202ef-8bd6-40ae-9bce-3ce0b1923ac8" />
172.16.17.54



Apa tipe log yang memiliki nomor port tujuan 52567 dan alamat IP sumber 8.8.8.8? DNS
Format Jawaban: logtype
Jawaban: Buka halaman Manajemen Log, di sisi kanan Anda akan melihat bilah pencarian, tempelkan alamat IP, lalu cari nomor port tujuan yang diberikan, dan Anda akan mendapatkan jenis lognya.
<img width="1400" height="470" alt="image" src="https://github.com/user-attachments/assets/896146d6-5607-4be3-88ff-159d6f189d52" />

