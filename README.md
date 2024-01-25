# Linux-Gerekli-Bilgiler

Blockchain Node Kurulumunda Linux'un Önemi

Node kurulumu sürecinde, Linux işletim sistemi sıklıkla tercih edilir. Güvenlik, esneklik ve stabilite gibi özellikleriyle öne çıkan Linux, blockchain node'larını desteklemek için ideal bir ortam sunar. Ancak, Linux ile çalışabilmek için temel komut satırı bilgisi gerekmektedir. Bu yazıda, blockchain node kurulumu için gerekli olan sudo, apt-get, curl, wget, nano/vi, mkdir, cd, ls, chmod,vs. gibi temel Linux komutlarını ve bu komutların nasıl kullanılacağını ele alacağım.

Blockchain dünyasında etkin bir katılımcı olmak istiyorsanız, bu temel Linux komutlarını öğrenmek ve uygulamak, yolculuğunuzun ilk adımı olacaktır. Şimdi, bu alanda kendinizi geliştirmek için gerekli Linux komutlarına daha yakından bakalım.


Linux Dosya Sistemi: Temel Dizinler ve İşlevleri

Linux işletim sistemi, dosyaları ve dizinleri organize etmek için hiyerarşik bir yapı kullanır. Bu yapı, dosya sistemi içindeki her şeyin bir yerde düzenli bir şekilde saklanmasını sağlar. İşte Linux'taki bazı temel dizinler ve bu dizinlerin işlevleri:
/: Kök Dizini

Tüm dosya ve dizinlerin başlangıç noktasıdır. Sistem üzerindeki her şey bu dizin altında yer alır.
/bin: Temel Komut Dosyaları

Esas kullanıcı komutlarını içerir (örn: ls, cp, mv). Bu komutlar, sistemin başlangıç aşamasında ve tek kullanıcı modunda gereklidir.
/boot: Önyükleme Dosyaları

Sistemin başlangıcında (boot) kullanılan dosyalar ve Linux çekirdeği (kernel) burada saklanır.
/dev: Aygıt Dosyaları

Linux'ta her şey bir dosya olarak ele alınır, bu kapsamda donanım bile. /dev, çeşitli donanım aygıtları (örn: disk sürücüleri, USB cihazları) için özel dosyaları içerir.
/etc: Yapılandırma Dosyaları

Sistem genelindeki yapılandırma dosyaları burada bulunur. Bu dosyalar, sistem ayarları ve başlangıç script'leri gibi çok çeşitli konfigürasyonları içerir.
/home: Kullanıcı Dizinleri

Sistem kullanıcılarının kişisel dosyaları için ayrılan dizindir. Genellikle her kullanıcının kendi adıyla bir alt dizini vardır.
/lib: Sistem Kütüphaneleri ve Modülleri

Sistem çalıştırılabilir dosyaları tarafından kullanılan paylaşılan kütüphane dosyalarını ve çekirdek modüllerini içerir.
/media ve /mnt: Çıkarılabilir Ortamlar

/media genellikle çıkarılabilir ortamlar için kullanılır (USB sürücüler, CD-ROM'lar). /mnt ise geçici olarak bağlanan dosya sistemleri için kullanılır.
/opt: İsteğe Bağlı Uygulamalar

Üçüncü parti yazılımların ve bazı büyük paketlerin yüklendiği dizindir.
/proc: Sistem ve İşlem Bilgileri

Çalışan işlemler ve sistem bilgileri hakkında bilgi içerir. Bu dizin, gerçek bir dosya sistemi değil, bir sanal dosya sistemi olarak işlev görür.
/sbin: Sistem Yönetimi İçin Özel Komutlar

Sistem yönetimi ve bakımı için kullanılan komutları içerir (örn: fdisk, ifconfig, shutdown).
/tmp: Geçici Dosyalar

Uygulamaların geçici dosyaları için kullanılan dizindir. İçeriği genellikle yeniden başlatma işlemlerinde silinir.
/usr: Kullanıcı Programları ve Verileri

Kullanıcı uygulamaları, kütüphaneleri, belgeleri ve sistemin büyük bir bölümünü içerir. Alt dizinleri (/usr/bin, /usr/lib, /usr/local vb.) çeşitli kullanıcı düzeyi uygulamalarını ve verilerini barındırır.
/var: Değişken Veriler

Log dosyaları ve diğer sürekli değişen veriler bu dizinde yer alır.



![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/a8616561-2219-4be8-84f9-369ff8a47c72)


Şekil 1. Kök dizinde "ls -la" komutuyla listelenmiş dizinler





Sık Kullanılan Bazı Linux Komutları
cd (Change Directory)
Tanım: Kullanıcıyı bir dizinden diğerine geçirmek için kullanılır.

Örnek Kullanım: cd /home/kullanici/dokumanlarBu komut, kullanıcıyı /home/kullanici/dokumanlar dizinine taşır.
"cd" komutu tek başına kullanıldığı zaman kullanıcı dizinine götürür. "cd .." yazılırsa bir alt dizine geri döner.




![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/56a4d57d-d5e6-44b8-9862-7688727e84ac)


Şekil 2. cd komutu kullanımı. Gidilen dizin pwd ile gösterilmiştir.



ls (List)
Tanım: Mevcut dizindeki dosya ve dizinleri listelemek için kullanılır.

Yaygın Parametreler:-l: Detaylı listeleme yapar, dosya/dizin izinleri, sahibi, boyutu gibi bilgileri gösterir.
-a: Gizli dosya ve dizinleri de listeler.
-la: Hem detaylı hem de gizli dosya ve dizinleri listeler.
Örnek Kullanım: ls -laBu komut, mevcut dizindeki tüm dosya ve dizinleri, detaylı ve gizli dosyalar dahil listeler.



![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/7b3a6a5b-bc1a-4c1a-a5bb-c5125db90ef8)


Şekil 3. ls -la kullanımı




pwd (Print Working Directory)
Tanım: Kullanıcının şu anda bulunduğu dizinin tam yolunu gösterir.

Örnek Kullanım: pwdBu komut, kullanıcının şu anda hangi dizinde olduğunu gösterir.



![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/2cf5d56d-0460-4dba-83a4-fef0c16211de)


Şekil 4. pwd kullanımı




rm (Remove)
Tanım: Dosya veya dizin silmek için kullanılır.

Yaygın Parametreler:-r: Bir dizin ve içindekileri rekursif olarak siler.
-f: Zorla silme, onay istemez.
Örnek Kullanım: rm -rf /tmp/gecici-dosyalarBu komut, /tmp/gecici-dosyalar dizinini ve içindekileri zorla ve alt klasörler/dosyalar dahil olarak siler.

mkdir (Make directory)
Tanım: Klasör oluşturmak için kullanılır.

touch 
Tanım: Boş bir dosya oluşturmak için kullanılır.

mv (Move)
Tanım: Dosya veya dizinleri taşımak veya yeniden adlandırmak için kullanılır.

Örnek Kullanım: mv eski_dosya.txt yeni_dosya.txtBu komut, eski_dosya.txt'yi yeni_dosya.txt olarak yeniden adlandırır.
cp (Copy)
Tanım: Dosya veya dizinleri kopyalamak için kullanılır.

Yaygın Parametreler:-r: Bir dizini ve içindekileri (alt klasör ve dosyaları)  kopyalar.
Örnek Kullanım: cp -r /kaynak/dizin /hedef/dizinBu komut, /kaynak/dizin'i ve içindekileri /hedef/dizin'e kopyalar.



![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/78fbb9a8-0e04-47de-ac2c-2fccf34c4fe6)


Şekil 5. mkdir, touch, mv, cp ve rm komutlarının kullanımı




sudo (Super User Do)
Tanım: Başka kullanıcıların (genellikle root) ayrıcalıklarıyla komut çalıştırmayı sağlar. Root, Linux'ta en yüksek yetkilere sahip kullanıcıdır ve genellikle sistem yönetimi işlemleri için kullanılır.

Örnek Kullanım: sudo apt-get updateBu komut, root kullanıcısının yetkileriyle paket listelerini günceller.

 wget
Tanım: Web sunucularından dosya indirmek için kullanılır.

Örnek Kullanım: wget https://ornek.com/dosya.tar.gzBu komut, belirtilen URL'den dosya.tar.gz adlı dosyayı indirir.
curl
Tanım: İnternet üzerinden veri alışverişi yapmak için kullanılır. Web sunucularından veri indirme işini wget gibi gerçekleştirebilir ek olarak, API istekleri gönderme gibi işlemlerde kullanılır (GET, POST, vs.).

systemctl
Tanım: systemd sistemi ve servis yöneticisi için kullanılır. Servisleri başlatma, durdurma, yeniden başlatma ve durumlarını kontrol etme gibi işlevleri vardır.

Örnek Kullanım: systemctl start nginxBu komut, nginx servisini başlatır.




![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/fe428737-9ce9-4a9a-8a7f-548375de16b2)


Şekil 6. systemctl ve ilgili parametrelerini kullanarak çalışan tüm servisleri listeledik





![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/bc1cf926-f774-4b35-846b-db56b9e9da3e)


Şekil 7. Voi isimli servisin durumunu "systemctl status voi.service" komutu ile sorguladık





grep
Tanım: Metin içerisinde desen ve kelime arama yapmak için kullanılır. Dosyalar içinde veya diğer komutların çıktılarında arama yapmak için oldukça yararlıdır.

Örnek Kullanım: grep "aranan_kelime" dosya.txtBu komut, dosya.txt içinde "aranan_kelime"yi arar ve eşleşen satırları gösterir.





![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/1638003d-c87b-4b2f-a4aa-38e11aa97cd9)


Şekil 8. Önceki adımda ekrana bastırdığımız tüm servisleri içerisinde "voi" geçenler ile sınırlandırdık





htop
Tanım: Sistem kaynaklarının kullanımını görsel olarak gösteren interaktif bir izleme aracıdır.

Örnek Kullanım: htopBu komut, sistemde çalışan süreçleri ve kaynak kullanımını gösterir.

nano / vi

Metin editörleri. Dosyaları düzenlemek için kullanılır.
Örnek: nano dosya.txt veya vi dosya.txt ile dosya.txt dosyasını düzenleyebilirsiniz.
tar

Dosya arşivleme ve sıkıştırma işlemleri için kullanılır.
Örnek: tar -czvf arsiv.tar.gz /dizin ile /dizin'i arsiv.tar.gz olarak sıkıştırır ve arşivler.
chmod

Dosya ve dizinlerin erişim izinlerini değiştirir.
Örnek: chmod 755 script.sh ile script.sh dosyasına çalıştırma izni verir.






![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/d5b36845-5013-4177-8f5d-9e8f832b19c5)


Şekil 9. Çalıştırma izni vermeden önce dosyayı çalıştırmamıza izin vermedi. chmod +x ile çalıştırma izni verdik, chmod 755 de olurdu.





NOT: Tek parça olarak yapıştırılması istenilen bazı kodları Github'dan kopyalayıp terminal ekranına yapıştırıken kodlar, tek parça halinde değil de yarım yarım yapıştırılabiliyor. Bu durum da hataya sebebiyet verebiliyor. Böyle durumlar için bir .sh dosyası oluşturup içerisine tüm kod yapıştırılıp +x çalıştırma izni verilip "./dosyaadi.sh" komutu ile çalıştırılırsa komutlar tek seferde çalışacaktır. 

chown

Dosya veya dizinin sahipliğini değiştirmek için kullanılır.
Örnek: chown kullanici:dizin dosya.txt ile dosya.txt'nin sahipliğini kullaniciya verir.
df

Disk alanı kullanımını gösterir.
Örnek: df -h ile insan okunabilir formatta disk kullanım bilgilerini gösterir.
du

Dizinlerdeki dosya kullanım alanını gösterir.
Örnek: du -sh /dizin ile /dizin altındaki dosyaların toplam boyutunu gösterir.

cat, less, more

Dosyanın içine editör ile girmeden, içerisinde ne olduğunu terminal ekranına bastırarak görmemizi sağlarlar. Küçük dosyalar için "cat" kullanımı yeterlidir. Büyük dosyalar içinse "less" kullanarak içerikleri sayfa sayfa görebiliriz, böylece terminali boşuna doldurmamış oluruz.



![image](https://github.com/geocmsk/Linux-Gerekli-Bilgiler/assets/90604931/42e5c2d0-2f7f-4e3e-b11d-53175a0f3546)


Şekil 10. "cat" kullanımı



Derleme için @lilium hocama teşekkür ederim..


