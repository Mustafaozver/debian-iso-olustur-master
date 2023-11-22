Debian (Unstable/Sid) ISO oluşturma rehberi
--------------------------------------------------------------------------------------------

İlk Önce scpritlerin program olarak çalışmalarına izin verelim:

chmod +x isoyap isoolustur

Bu komutları girdikten sonra sudo ./isoyap komutu ile isoyap dosyasını çalıştırın.


Masaüstü ve kurulum komutları
----------------------------------------------------------------------------------------------

Xfce       : apt-get install xfce4 xfce4-goodies network-manager-gnome

Lxde       : apt-get install lxde network-manager-gnome

Cinnamon   : apt-get install cinnamon

KDE plasma : apt-get install kde-standard

Gnome      : apt-get install gnome-core

Mate       : apt-get install lightdm mate-desktop-environment-extras network-manager-gnome

Budgie     : apt-get install budgie-desktop

----------------------------------------------------------------------------------------------

Son olarak da isteğe bağlı olarak kurulu gelmesini istediğimiz paketleri yazmamız yeterli.
----------------------------------------------------------------------------------------------

apt-get install mugshot blueman gvfs-backends synaptic firefox-esr firefox-esr-l10n-tr neofetch htop gnome-calculator vs kurabilirsiniz..

Yazıcı ve tarayıcı için: apt-get install printer-driver-all system-config-printer simple-scan xsane paketleri kurabilirsiniz

en son update-grub komutu ile grubu güncelleyelim ve exit komutu ile çıkış yapalım 

sudo ./isoolustur dosyasını çalıştırıyoruz işlem tamamlanıyor.


https://youtu.be/2B687KPefTw 

Unuttuğumuz sonradan eklemek yada silmek istediğimiz paket/paketler varsa aşağıda yazılı komutlar ile chroot içine girip ekleyelim. 
-------------------------------------------------------------------------------------------------------------------------------------------------

for i in dev dev/pts proc sys; do mount -o bind /$i debian-chroot/$i; done

chroot debian-chroot /bin/bash

apt update 

işimiz bitince de exit komutu ile çıkıp ./isoolustur çalıştıralım.

Yaptığımız iso canlı olduğu için kurulumu aracına ihtiyacınız olacak  
--------------------------------------------------------------------------------------------------------------------------------
https://github.com/17g-installer
