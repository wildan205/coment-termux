# Install Termux Pemula
- apt update 
- apt upgrade
- apt install git
- apt install pythone 
- apt install wget
- apt install curl
- termux-setup-storage 
- apt install php
- apt install pip2

# Cara Menghilangkan Tampilan Home Termux
- apt update
- apt upgrade
- tuch .hushlogin
- Enter Lalu Exit

# cara mengunakan github
- apt update
- apt upgrade
- apt install git
- Lalu Enter
- Baru masukan clone nya atau url

# cara install ubuntu mengunakan handphone
# bahan yang di butuhkan 
- install  Andronix
- install VNC viewer
# tata cara install
- buka apk andronix
- cari logo ubuntu lalu klik
- pilih ubuntu 9
- ketika sudah muncul pilih desktop environment kita,saya sarankan xfce,klik disitu
- otomatis akan ada tulisan "command copied",untuk dijalankan pada termux
- setelah itu lalu buka termux kalian
- paste/tempelkan "command" tadi,tekan enter
- tunggu prosesnya,ditengah proses kita disuruh memasukkan password vncserver
- setelah proses selesai,tulisan "$" pada termux akan berubah menjadi "root@localhost:~#"
- Selamat,anda telah masuk pada os Ubuntu 19 secara CLI (Command line interface)
- untuk masuk desktop GUI (graphical user interface)
- ketikkan "vncserver",nanti akan keluar port untuk vncserver desktop kita (disini :5)
- masuk ke VNC viewer dan klik (+)
- lalu masukkan address dan nama,hostname ubuntu kita otomatis adalah "localhost" dan port saya adalah :5,Klik save
- terus untuk langkah selanjutnya  klik connect
- jika ada peringatan tentang "encryption" kita terjang aja lah
- masukkan password anda,Klik continue
- ubuntu sudh terinstall 100% silahkan eksploitasi sesuai kebutuhan anda
# tata cara keluar dari ubuntu dam termux yang kita install tadi 
- untuk keluar dari remote desktop klik tombol X diatas
- Untuk shutdown,masuk ke cli Termux
Ketikkan "exit" Dan enter,sampai tulisan "root@localhost:~" berubah jadi "$"
- untuk keluar dari Termux ketik exit Dan tekan enter sekali lagi
   
