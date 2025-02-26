
**VirtualBox Kurulumu:**

**1.VirtualBox Paketinin İndirilmesi**

İlk olarak, VirtualBox'ın uygun sürümünü belirliyoruz. Ubuntu 24.04 sürümüne uygun olan **`.deb`** paketini resmi web sitesinden indiriyoruz. Bu aşamada, sistemle uyumlu sürümün seçilmesine dikkat ediyoruz.

```
bash
wget https://download.virtualbox.org/virtualbox/6.1.34/virtualbox-6.1_6.1.34-149290~Ubuntu~foc
```
![image](https://github.com/user-attachments/assets/b1ec4e09-1c7d-4388-b6dc-a74927559777)


**2.Kurulum İşlemi**

İlk olarak, **VirtualBox** paketinin doğru şekilde indirildiğinden emin olduktan sonra, sistemine yüklemek için aşağıdaki komutu kullanıyoruz:

```
bash
sudo dpkg -i virtualbox-7.1_7.1.4-165100~Ubuntu~noble_amd64.deb
```
![image](https://github.com/user-attachments/assets/322234cc-2d2f-486f-860c-0127221d241f)

**Bağımlılık Sorunlarının Giderilmesi**

Kurulum işlemi sırasında eksik bağımlılıklar nedeniyle hata mesajları alındığında, aşağıdaki komutu kullanarak eksik bağımlılıkları yükleriz:

```
bash
sudo apt --fix-broken install
```


**SANAL MAKİNE YAPILANDIRMASI :**

**Bu bölümde, oluşturacağımız sanal makine için isim ve işletim sistemi tercihlerini belirliyoruz.**

**-Makine Adı**: Sanal makineyi kolayca tanıyabilmek için anlamlı ve uygun bir isim seçin.

**-İşletim Sistemi Türü ve Sürümü**: Sanal makinenin çalıştıracağı işletim sistemi türünü (örneğin, Windows, Linux, macOS) ve sürümünü doğru şekilde seçin. Bu, sanal makinenin performansı ve uyumluluğu açısından kritik bir adımdır.

![image](https://github.com/user-attachments/assets/b3d3e342-6c4a-46bf-a128-e5fde1ff21da)



**Bu bölümde, sanal makine için bellek ve işlemci çekirdeği ayarlarını yapılandırıyoruz.**

**- Bellek (RAM) Ayarı**: Sanal makinenin ihtiyaçlarını karşılayacak uygun bellek miktarını belirliyoruz. Bellek miktarını seçerken, ana sistemin stabil çalışması için yeterli kaynak bulundurmayı göz önünde bulunduruyoruz.

**- Çekirdek Sayısı**: Sanal makinenin kullanacağı işlemci çekirdeği sayısını ayarlıyoruz. Performansı artırmak için daha fazla çekirdek seçebiliriz; ancak bu seçimde ana sistemin kaynak ihtiyaçlarını da göz ardı etmiyoruz.

![image](https://github.com/user-attachments/assets/e774f16e-cce1-4f25-b3f5-57d821c520af)



**Bu bölümde, "Finish" butonuna tıklayarak işlemleri tamamlıyor ve yapılandırma ekranından çıkıyoruz.**

 ![image](https://github.com/user-attachments/assets/1bb05b25-9d40-4032-ad09-c72025bd651b)



 

**Bu bölümde, sanal makineyi başlatmak ve işletim sistemi yükleme işlemini başlatmak için "Start" butonuna tıklıyoruz.**

**Sanal Makineyi Başlatırken Karşılaşılan Hata ve Çözümü**

-Sanal makineyi başlatırken **EFI Secure Boot** hatasıyla karşılaşıldığında, bu sorunun çözülmesi için şu adımlar izlenmiştir:

- **EFI Secure Boot Kontrolü**: Secure Boot'un aktif olduğu tespit edilmiştir. Bu sebeple, BIOS/UEFI ayarlarına girilerek Secure Boot özelliği devre dışı bırakılmıştır.

-Yapılan bu işlem sonrasında sorun çözülmüş ve sanal makine sorunsuz bir şekilde başlatılabilmiştir.

![image](https://github.com/user-attachments/assets/f09c9b77-c15c-45cb-8cd5-d196bf1ca349)





**Bu bölümde, sunucunun dil ayarları yapılandırıyorur.**

-Seçilen dil, sunucu arayüzü ve diğer sistem mesajlarında kullanılacak varsayılan dili belirler.

![image](https://github.com/user-attachments/assets/c42b8777-ad8b-470b-8d3c-8097a8458621)




**Bu bölümde, sunucunun klavye dilini yapılandırıyoruz.**

-Seçilen klavye dili, sunucu üzerinde yapılacak giriş işlemlerinde kullanılan varsayılan düzeni belirler.

![image](https://github.com/user-attachments/assets/0af0b49a-a46e-49f0-b4bb-4091d9705de2)




**Bu bölümde, sunucunun ağ yapılandırması gerçekleştiriyoruz.**

-Ağ ayarları, sunucunun doğru bir şekilde iletişim kurabilmesi ve dış bağlantılarla etkileşim sağlayabilmesi için yapılandırıyoruz..

![image](https://github.com/user-attachments/assets/b38b595d-fc8e-470e-befb-8a545f2d931b)




**Bu bölümde, sunucu için profil yapılandırmasını gerçekleştiriyoruz**

-Profil ayarları, sunucunun kullanıcı gereksinimlerine uygun şekilde kişiselleştirilmesi ve optimize edilmesi amacıyla yapılandırıyoruz.

![image](https://github.com/user-attachments/assets/9cf8306e-2bcb-4bec-92ac-d0d961ef7ea9)




**Bu bölümde, SSH paketlerini yüklenmesini gerçekleştiriyoruz.**

-SSH ayarları, sunucunun uzaktan güvenli bir şekilde yönetilmesi ve erişilmesi için optimize ediyoruz.

![image](https://github.com/user-attachments/assets/b7ba2228-d05d-47b5-9641-715d7e9b1bf9)




**Bu bölümde, sunucunun snap paketleri yapılandırılmış ve yalnızca gerekli olanlar seçiyoruz.**

-Snap paketleri, sunucunun ihtiyaçlarına uygun olarak optimize edilmiş ve gereksiz paketlerin yüklenmesi engellenmiştir.

![image](https://github.com/user-attachments/assets/4025e7ee-f459-4688-9dda-a83f732e0c7d)




**Yükleme İşlemi Sonrası Karşılaşılan Hata ve Çözümü**

-Yükleme işlemi başlatıldıktan sonra **"failed unmounting cdrom.mount - /cdrom"** hatasıyla karşılaşılmıştır. Bu hatayı çözmek için aşağıdaki adımlar izlenmiştir:
1. VirtualBox ana penceresinden sanal makine seçilmiştir.
2. Üst menüdeki **Settings (Ayarlar)** kısmına tıklanmıştır.
3. **Storage (Depolama)** sekmesine geçilmiştir.
4. Sağ tarafta bulunan CD simgesine tıklanıp, **Remove Disk from Virtual Drive** seçeneği seçilmiştir.

**-Bu adımlar takip edilerek sorun çözülmüş ve yükleme işlemi sorunsuz bir şekilde devam etmiştir.**




**Bu bölümde, kullanıcı adı ve parolayla sunucuya giriş yapıyoruz.**
-Sunucuya güvenli bir şekilde erişim sağlanabilmesi için kullanıcı bilgileri doğru ve eksiksiz girilmelidir.

![image](https://github.com/user-attachments/assets/224ae1d4-6fc3-4b1c-9614-81762016c2b2)






**2. Temel Sistem Ayarları**

**A. Genel Yapı**

-Sunucu Tipleri ve 	IP Adresleri :

-Web Sunucusunda	(192.168.176.89)	Apache, WordPress, 2025ozgur.com kurulumlarını yapazacaz

-Veritabanı Sunucusunda	(192.168.176.146)	MariaDB kurulumunu yapacaz

-Host (192.168.176.136)	SSH ile sunuculara bağlanacaz


**B. Güncellemeler ve Paket Yönetimi**

```
bash
sudo apt update && sudo apt upgrade -y # Sistem paketlerini günceller ve mevcut yazılımları en son sürüme yükseltir
```


**C. Veritabanı Sunucusu (192.168.176.146) Ayarları**

**1. MariaDB Kurulumu ve Yapılandırma İşlemelri**

**Root SSH Anahtarını Kopyalama (Host Makineden)**
```
# Host makineden (192.168.176.136):
ssh-copy-id -i ~/.ssh/id_ed25519.pub root@192.168.176.146
```

# MariaDB Kurmak için aşağıdaki komutu giriyoruz:
```
sudo apt update && sudo apt install mariadb-server -y
```

![image](https://github.com/user-attachments/assets/eb7cc7d7-3780-496d-a98f-5f05f42774fd)


# Güvenlik Ayarları için aşağıdaki komutları giriyoruz:
```
sudo mysql_secure_installation
#Root parola belirle (Ör: DBrootPass123!), anonim kullanıcıları siler, root uzaktan erişimi engeller.
```
![image](https://github.com/user-attachments/assets/63458cda-a614-4444-b2e1-aa41c5a10ccf)


# WordPress için Veritabanı ve Kullanıcı Oluşturuyoruz:
```
sudo mysql -u root -p
```

![image](https://github.com/user-attachments/assets/dbfe80dc-7235-4dda-b486-2054e6c57109)

```
CREATE DATABASE wp_bugday;
CREATE USER 'wp_user'@'192.168.176.89' IDENTIFIED BY 'password!';
GRANT ALL PRIVILEGES ON wp_bugday.* TO 'wp_user'@'192.168.176.89';
FLUSH PRIVILEGES;
EXIT;
```

![image](https://github.com/user-attachments/assets/35c531e1-871c-4537-8db5-22aedaa8d955)

**Uzak Erişim İzni ve Güvenlik Duvarı :**

```
sudo nano /etc/mysql/mariadb.conf.d/50-server.cnf  # bind-address = 0.0.0.0
sudo systemctl restart mariadb
sudo ufw allow from 192.168.176.89 to any port 3306/tcp
sudo ufw enable

```

![image](https://github.com/user-attachments/assets/af440c0e-3767-47a5-8588-a044fbc24533)




**2. Web Sunucusu (192.168.176.89) Kurulumu**

**Root SSH Anahtarını Kopyalama (Host Makineden) :**

```
# Host makineden (192.168.176.136):
ssh-copy-id -i ~/.ssh/id_ed25519.pub root@192.168.176.89
```

**Apache ve PHP Kurulum Komutları**

```
sudo apt update && sudo apt install apache2 php php-mysql php-curl php-gd php-xml php-mbstring -y
sudo systemctl enable apache2
```


```
sudo mkdir -p /var/www/bugday.org/public_html        # Web sitesi dizinini oluşturur (-p ile varsa hata vermez)

sudo chown -R www-data:www-data /var/www/bugday.org    # Web sunucusunun (Apache/Nginx) dizine erişmesini sağlar

cd /tmp                                                   # Geçici dizine gider, burada dosya indirilecek

wget https://wordpress.org/latest.tar.gz               # WordPress'in en son sürümünü indirir

tar -xzvf latest.tar.gz                               # İndirilen WordPress dosyasını çıkarır

sudo cp -R wordpress/* /var/www/bugday.org/public_html/        # WordPress dosyalarını hedef dizine kopyalar

sudo cp /var/www/bugday.org/public_html/wp-config-sample.php /var/www/bugday.org/public_html/wp-config.php  # Örnek yapılandırma dosyasını kopyalar
```



**WordPress yapılandırma dosyasını düzenlemek için aşağıdaki komutu giriyoruz**

```
sudo nano /var/www/bugday.org/public_html/wp-config.php 
```
**Değiştirilecek Satırlar:**
```
php
define('DB_NAME', 'wp_bugday');
define('DB_USER', 'database');
define('DB_PASSWORD', 'password!');
define('DB_HOST', '192.168.176.146');

```

![image](https://github.com/user-attachments/assets/c1a39d9a-47f8-43e7-8ec5-51235c7c4cac)

**Apache VirtualHost (bugday.org & buğday.org) Ayarlamaları :**

```
sudo nano /etc/apache2/sites-available/bugday.conf
```

**içerik şöyle olacak :**
```
<VirtualHost *:80>
    ServerName bugday.org
    ServerAlias xn--bday-0qa.org # buğday.org'un Punycode karşılığı türkçe karakterde sıkıntı olmaması için
    DocumentRoot /var/www/bugday.org/public_html
    <Directory /var/www/bugday.org/public_html>
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>
```

![image](https://github.com/user-attachments/assets/76e93493-68a5-4ab3-a3b6-cba310c44e4b)

```
sudo a2ensite bugday.conf        # Apache'de bugday.conf adlı sanal host (VirtualHost) dosyasını etkinleştirir
sudo a2enmod rewrite             # Apache'nin mod_rewrite özelliğini etkinleştirir (URL yönlendirme için gereklidir)
sudo systemctl reload apache2    # Apache'yi yeniden yükleyerek yapılan değişiklikleri uygular (servisi tamamen kapatıp açmaz)
```

**2025ozgur.com Kurulumu**

```
sudo mkdir -p /var/www/2025ozgur.com/public_html
sudo nano /var/www/2025ozgur.com/public_html/index.html
```

**içerik :**

```                                                               
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>
<body>
    <div id="output"></div>

    <script>
        let output = "";
        for (let i = 0; i < 100; i++) {
            output += "Kullanıcıların kişisel verilerini toplamayacağım.<br>";
        }
        document.getElementById("output").innerHTML = output;
    </script>
</body>
</html>

```

![image](https://github.com/user-attachments/assets/96583964-6c17-4827-aa1b-912587a1b87a)

**Parola Korumalı Dizin:**

```
sudo htpasswd -c /etc/apache2/.htpasswd ad.soyad  # Parola: parola
sudo mkdir /var/www/2025ozgur.com/public_html/yonetim
sudo nano /var/www/2025ozgur.com/public_html/yonetim/.htaccess

```

**içerik :**
```                                                                   
AuthType Basic
AuthName "Yönetim Paneli"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

![image](https://github.com/user-attachments/assets/67570c5a-3cf2-44b1-97f5-30411eeab4f8)

**VirtualHost:**

```
sudo nano /etc/apache2/sites-available/2025ozgur.conf
```

**içerik :**

```
<VirtualHost *:80>
    ServerName 2025ozgur.com
    ServerAlias www.2025ozgur.com
    DocumentRoot /var/www/2025ozgur.com/public_html

    <Directory "/var/www/2025ozgur.com/public_html/yonetim">
        AuthType Basic
        AuthName "Yönetim Paneli"
        AuthUserFile /etc/apache2/.htpasswd
        Require valid-user
    </Directory>
</VirtualHost>
```

![image](https://github.com/user-attachments/assets/3b2c58c4-4d25-4caa-bd5b-87e2093410ad)

```
sudo a2ensite 2025ozgur.conf      # Apache'de 2025ozgur.conf adlı sanal host (VirtualHost) dosyasını etkinleştirir
sudo systemctl reload apache2     # Apache'yi yeniden yükleyerek yapılan değişiklikleri uygular (servisi tamamen kapatıp açmaz)

```


**Son Kontroller**

**WordPress Testi:**

-http://bugday.org üzerinden kurulumu tamamlıyoruz.

-ilk olarrak dil ayarlamasını yapıyoruz
![image](https://github.com/user-attachments/assets/8b49b83e-05c5-4dbb-973a-d4b849a62b12)

-sonrasında temel biligiler girildikten sonra ad.soyad kullanıcı adı ve parola şeklinde şifreyı giriyoruz
![image](https://github.com/user-attachments/assets/2b3dbec7-dea4-40a8-a29d-295c52089973)



**Kalıcı Bağlantılar için ayarlar >  kalıcı bağlantılar > kalıcı bağlantı yapısı > ozel yapı >  "%postname%" olarak ayarlıyoruz.**

![image](https://github.com/user-attachments/assets/92c58524-7ed2-4ff5-9c3f-2906439aa66c)



**Yeni bir yazı eklemek için yazılar > yeni yazı ekle adımlarını takip ediyoruz**

![image](https://github.com/user-attachments/assets/74829710-f517-4613-8d7d-772d8c38f79a)

![image](https://github.com/user-attachments/assets/88fa749b-de82-4ba3-b8f7-a18617b9c680)


**2025ozgur.com Testi**

-www.2025ozgur.com ve 2025ozgur.com web sitelerinin görünümü :
![image](https://github.com/user-attachments/assets/2228ad51-6d2f-40b6-8b09-2f6667c5fe63)




