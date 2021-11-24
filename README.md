# Cara konfigurasi VPN

1. Install Debian di VirtualBox, atau pakai Debian yang dipakai untuk praktek FTP. Intinya sudah ada FTP dan berfungsi
2. Sambungkan Server Debian ke internet dengan cara
    - Change Adapter Settings
    - Pilih Wifi atau jaringan OC
    - Klik Properties
    - Masuk Tab Sharing
    - Centang dan Pilih Virtual Box Host Only Adapter

3. Ganti jaringan Virtual Box ke Brindged Network, BUKAN HOST ONLY
4. DI debian tambahkan DNS Google dengan cara
    - ```nano /etc/resolv.conf```
    - lalu tambahkan ```nameserver 8.8.8.8```
    - Simpan file
5. lalu masukan command
    - ```ip addr```
    - Ingat IP Tersebut
    - ```wget https://git.io/vpn -O openvpn-install.sh```
    - ```bash openvpn-install.sh```
    - Untuk bagian IP masukan IP Server dari ip addr
    - Untuk protocol biarkan kosong atau ketik 1 untuk UDP
    - Untuk Port kosongkan lagi
    - Untuk DNS pilih no 2 untuk DNS Google
    - Lalu mas=ukan nama client
    - Tekan tombol apa saja
    - sampai selesai
    - Jika sudah masukan command ```cat /root/NAMA_CLIENT.ovpn > /home/USER_FTP/NAMA_CLIENT.ovpn```
6. Lalu buka FTP dengan FileZilla, lalu download file NAMA_CLIENT.ovpn ke PC anda
7. Download OpenVPN Connect [disini](https://openvpn.net/downloads/openvpn-connect-v3-windows.msi) lalu install
8. Setel;ah di install, klik dua kali Pada file ovpn tadi
9. Done



Wak ngantuak jan tanyo2 lai kawan
