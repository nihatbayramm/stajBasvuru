

### **VirtualBox Kurulumu:**

#### 1. **VirtualBox Paketinin İndirilmesi**

İlk olarak, VirtualBox'ın uygun sürümünü belirliyoruz. Ubuntu 24.04 sürümüne uygun olan **`.deb`** paketini resmi web sitesinden indiriyoruz. Bu aşamada, sistemle uyumlu sürümün seçilmesine dikkat ediyoruz.

**Bash Formatı:**

```
bash
wget https://download.virtualbox.org/virtualbox/6.1.34/virtualbox-6.1_6.1.34-149290~Ubuntu~foc
```



![2025-01-27 16-25-27.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-27%2016-25-27.png?raw=true)






### 2. **Kurulum İşlemi**

İlk olarak, **VirtualBox** paketinin doğru şekilde indirildiğinden emin olduktan sonra, sistemine yüklemek için aşağıdaki komutu kullanıyoruz:

```
bash
sudo dpkg -i virtualbox-7.1_7.1.4-165100~Ubuntu~noble_amd64.deb
```



###  **Bağımlılık Sorunlarının Giderilmesi**

Kurulum işlemi sırasında eksik bağımlılıklar nedeniyle hata mesajları alındığında, aşağıdaki komutu kullanarak eksik bağımlılıkları yükleriz:

```
bash
sudo apt --fix-broken install
```



![Screenshot from 2025-01-11 20-37-14](/home/nihat-bayram/Pictures/Screenshots/Screenshot from 2025-01-11 20-37-14.png)







# SANAL MAKİNE YAPILANDIRMASI : 



**Bu bölümde, oluşturacağımız sanal makine için isim ve işletim sistemi tercihlerini belirliyoruz.**

- **Makine Adı**: Sanal makineyi kolayca tanıyabilmek için anlamlı ve uygun bir isim seçin.
- **İşletim Sistemi Türü ve Sürümü**: Sanal makinenin çalıştıracağı işletim sistemi türünü (örneğin, Windows, Linux, macOS) ve sürümünü doğru şekilde seçin. Bu, sanal makinenin performansı ve uyumluluğu açısından kritik bir adımdır.



![2025-01-11 23-24-06.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-11%2023-24-06.png?raw=true)



**Bu bölümde, sanal makine için bellek ve işlemci çekirdeği ayarlarını yapılandırıyoruz.**

- **Bellek (RAM) Ayarı**: Sanal makinenin ihtiyaçlarını karşılayacak uygun bellek miktarını belirliyoruz. Bellek miktarını seçerken, ana sistemin stabil çalışması için yeterli kaynak bulundurmayı göz önünde bulunduruyoruz.
- **Çekirdek Sayısı**: Sanal makinenin kullanacağı işlemci çekirdeği sayısını ayarlıyoruz. Performansı artırmak için daha fazla çekirdek seçebiliriz; ancak bu seçimde ana sistemin kaynak ihtiyaçlarını da göz ardı etmiyoruz.



![2025-01-11 23-24-47.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-11%2023-24-47.png?raw=true)





**Bu bölümde, "Finish" butonuna tıklayarak işlemleri tamamlıyor ve yapılandırma ekranından çıkıyoruz.**

 

![2025-01-11 23-26-23.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-11%2023-26-23.png?raw=true)









**Bu bölümde, sanal makineyi başlatmak ve işletim sistemi yükleme işlemini başlatmak için "Start" butonuna tıklıyoruz.**

**Sanal Makineyi Başlatırken Karşılaşılan Hata ve Çözümü**

Sanal makineyi başlatırken **EFI Secure Boot** hatasıyla karşılaşıldığında, bu sorunun çözülmesi için şu adımlar izlenmiştir:

- **EFI Secure Boot Kontrolü**: Secure Boot'un aktif olduğu tespit edilmiştir. Bu sebeple, BIOS/UEFI ayarlarına girilerek Secure Boot özelliği devre dışı bırakılmıştır.

Yapılan bu işlem sonrasında sorun çözülmüş ve sanal makine sorunsuz bir şekilde başlatılabilmiştir.

![2025-01-27 19-17-13.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-27%2019-17-13.png?raw=true)





**Bu bölümde, sunucunun dil ayarları yapılandırıyorur.**

Seçilen dil, sunucu arayüzü ve diğer sistem mesajlarında kullanılacak varsayılan dili belirler.



![2025-01-11 23-43-45.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-11%2023-43-45.png?raw=true)



**Bu bölümde, sunucunun klavye dilini yapılandırıyoruz.**

Seçilen klavye dili, sunucu üzerinde yapılacak giriş işlemlerinde kullanılan varsayılan düzeni belirler.

![2025-01-11 23-44-17.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-11%2023-44-17.png?raw=true)



**Bu bölümde, sunucunun ağ yapılandırması gerçekleştiriyoruz.**

Ağ ayarları, sunucunun doğru bir şekilde iletişim kurabilmesi ve dış bağlantılarla etkileşim sağlayabilmesi için yapılandırıyoruz..

![2025-01-11 23-47-54.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-11%2023-47-54.png?raw=true)



**Bu bölümde, sunucu için profil yapılandırmasını gerçekleştiriyoruz**

Profil ayarları, sunucunun kullanıcı gereksinimlerine uygun şekilde kişiselleştirilmesi ve optimize edilmesi amacıyla yapılandırıyoruz.

![2025-01-12 01-08-27.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-12%2001-08-27.png?raw=true)



**Bu bölümde, SSH yapılandırması gerçekleştiriyoruz.**

SSH ayarları, sunucunun uzaktan güvenli bir şekilde yönetilmesi ve erişilmesi için optimize ediyoruz.

![2025-01-12 01-10-33.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-12%2001-10-33.png?raw=true)



**Bu bölümde, sunucunun snap paketleri yapılandırılmış ve yalnızca gerekli olanlar seçiyoruz.**

Snap paketleri, sunucunun ihtiyaçlarına uygun olarak optimize edilmiş ve gereksiz paketlerin yüklenmesi engellenmiştir.

![2025-01-12 01-12-43.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-12%2001-12-43.png?raw=true)



**Yükleme İşlemi Sonrası Karşılaşılan Hata ve Çözümü**

Yükleme işlemi başlatıldıktan sonra **"failed unmounting cdrom.mount - /cdrom"** hatasıyla karşılaşılmıştır. Bu hatayı çözmek için aşağıdaki adımlar izlenmiştir:

1. VirtualBox ana penceresinden sanal makine seçilmiştir.
2. Üst menüdeki **Settings (Ayarlar)** kısmına tıklanmıştır.
3. **Storage (Depolama)** sekmesine geçilmiştir.
4. Sağ tarafta bulunan CD simgesine tıklanıp, **Remove Disk from Virtual Drive** seçeneği seçilmiştir.

Bu adımlar takip edilerek sorun çözülmüş ve yükleme işlemi sorunsuz bir şekilde devam etmiştir.



**Bu bölümde, kullanıcı adı ve parolayla sunucuya giriş yapıyoruz.**

Sunucuya güvenli bir şekilde erişim sağlanabilmesi için kullanıcı bilgileri doğrulanmış ve oturum başlatılmıştır.

![2025-01-12 01-35-37.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-12%2001-35-37.png?raw=true)



![2025-01-12 03-17-46.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-12%2003-17-46.png?raw=true)







## SSH Yapılandırması ve IP Adresi Kullanımı

Ubuntu Server üzerinde oturum açıldıktan sonra aşağıdaki komutu çalıştırarak IP adresi öğrenilmiştir:

```
bash

ip a
```

**Not:** Ağ türü otomatik olarak nat ağı olarak kurulmuştu bunu değiştirerek Bridged Adapter yaptım **Bridged Adapter**  Sanal makinemin fiziksel ağıma bağlanır ve yerel ağdaki cihazlardan erişilebilir olmasını sağlar. IP adresi doğrudan yerel ağımdan alınır.

### ![Screenshot from 2025-01-14 02-53-24](/home/nihat-bayram/Pictures/Screenshots/Screenshot from 2025-01-14 02-53-24.png)





**Ağ türü değiştiği vakit ip adreside değişti**

![2025-01-14 03-06-55.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2003-06-55.png?raw=true)







**SSH İLE BAĞLANTI**

Kendi bilgisayarımdan (host) şu komutu çalıştırarak sanal makineye bağlanıyorum:

```
ssh nihat@192.168.127.127
```

![2025-01-14 03-19-03.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2003-19-03.png?raw=true)



**SSH Anahtar Doğrulama:**

**1) Kendi bilgisayarımızdan bir SSH servisi oluşturuyoruz**

```
bash
ssh-keygen -t rsa -b 4096
```

**2) Anahtarı sanal makinemezi kopyalıyoruz:**

```
bash

ssh-copy-id nihat@192.168.127.127
```

![2025-01-14 03-23-38.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2003-23-38.png?raw=true)





**3) Parola doğrulamasını kapatmak için `/etc/ssh/sshd_config` dosyasını düzenliyoruz:**

```
PasswordAuthentication no
PermitRootLogin no
```

![2025-01-14 03-30-04.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2003-30-04.png?raw=true)



**4) SSH servisini yeniden başlatıyoruz:**

```
bash
sudo systemctl restart sshd
```

![2025-01-14 03-35-20.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2003-35-20.png?raw=true)





**3. Bölüm**

# ***Güvenlik Duvarı (UFW) Yapılandırması***

**1) UFW güvenlik duvarını kuruyor ve etkinleştiriyoruz:**

```
bash
sudo ufw allow OpenSSH
sudo ufw enable
sudo ufw status
```

![2025-01-14 04-08-18.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2004-08-18.png?raw=true)

**Aldığım Hata ve Çözümü:**

Hata: **UFW** (Uncomplicated Firewall) güvenlik duvarı aracının sanal makinemde yüklü olmadığı hatası.

Çözüm olarak:

```
bash
sudo apt update
sudo apt install ufw
```





**4. Bölüm**

# **Web Sunucusu Kurulumu**

### Apache kurmak için aşağıdaki komutu giriyoruz:

```
bash
sudo apt install apache2 -y
```

Sunucuyu başlatıyoruz ve sistem başlangıcında çalışacak şekilde ayarlıyoruz:

```
bash
sudo systemctl enable apache2
sudo systemctl start apache2
```



![2025-01-14 04-15-04.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2004-15-04.png?raw=true)







### **Alan Adları İçin Yapılandırma**

**Apache için sanal host (VirtualHost) ayarlarını yapıyoruz:**

**Aşağıdaki gibi yapılandırıyoruz:**

```plaintext
<VirtualHost *:80>
    ServerName bugday.org
    ServerAlias buğday.org 2025ozgur.com
    DocumentRoot /var/www/html
</VirtualHost>
```



![2025-01-14 04-28-56.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2004-28-56.png?raw=true)



**Değişiklikleri kaydedip Apache’yi yeniden başlatıyoruz:**

![2025-01-14 04-30-06.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2004-30-06.png?raw=true)









**5. Bölüm**

# Wordpress ve 2025ozgur.com Web Sitesi Kurulumu

**PHP ve gerekli modülleri yüklüyoruz:**

```
bash
sudo apt install php libapache2-mod-php php-mysql -y
```

Wordpress’i indirip çıkarmak için aşağıdaki kodları kullanıyoruz:

```bash
wget https://wordpress.org/latest.tar.gz
sudo tar -xvzf latest.tar.gz -C /var/www/html
sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
```



![2025-01-14 04-44-19.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2004-44-19.png?raw=true)



![2025-01-14 04-45-21.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2004-45-21.png?raw=true)



![2025-01-14 04-46-58.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2004-46-58.png?raw=true)



### **2025ozgur.com İçin HTML Sayfası Oluşturma**

**1) HTML sayfası için aşağıdaki kodları kullanıyoruz:**

```
bash
echo '<html><body>' > /var/www/html/index.html
for i in {1..100}; do echo 'Kullanıcılarımın kişisel verilerini toplamayacağım.<br>' >> /var/www/html/index.html; done
echo '</body></html>' >> /var/www/html/index.html
```

![2025-01-14 05-13-31.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2005-13-31.png?raw=true)

![2025-01-14 05-18-06.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2005-18-06.png?raw=true)





**2) Yönetim dizini oluşturup parola korumasını etkinleştirdik, bunun için aşağıdaki kodları kullandıyoruz:**

```
bash
sudo htpasswd -c /etc/apache2/.htpasswd ad.soyad
sudo mkdir /var/www/html/yonetim
sudo nano /etc/apache2/sites-available/000-default.conf
```



![2025-01-14 05-38-06.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2005-38-06.png?raw=true)







![2025-01-14 05-42-44.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-14%2005-42-44.png?raw=true)









**6. Bölüm**

# Veritabanı Sunucusu Kurulumu

### **1. Adım: MySQL Yükleme**

İlk olarak, MySQL sunucusunu yüklüyoruz:

```
bash
sudo apt update
sudo apt install mysql-server -y
```

![2025-01-26 02-08-14.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-26%2002-08-14.png?raw=true)



### **2. Adım: MySQL Güvenlik Ayarları**

Kurulum tamamlandıktan sonra, MySQL güvenlik ayarlarını yapılandırmak için aşağıdaki komutu çalıştırıyoruz:

```
bash
sudo mysql_secure_installation
```



![2025-01-26 02-10-38.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-26%2002-10-38.png?raw=true)





### **3. Adım: MySQL Servisini Başlatmak ve Sistem Başlangıcına Ekleme**

MySQL servisini başlatmak için şu komutları kullanıyoruz:

```
bash
sudo systemctl start mysql
sudo systemctl enable mysql
```



![2025-01-26 02-12-11.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-26%2002-12-11.png?raw=true)





### **4. Adım: MySQL'e Giriş Yapmak**

MySQL'e root kullanıcısıyla giriş yapmak için aşağıdaki komutu kullanıyoruz:

```
bash
sudo mysql -u root -p
```



![2025-01-26 02-12-56.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-26%2002-12-56.png?raw=true)







### **5. Adım: Yeni Veritabanı ve Kullanıcı Oluşturma**

Şimdi bir veritabanı oluşturup ona bir kullanıcı atıyoruz. İlk olarak veritabanını oluşturalım:

```
sql
CREATE DATABASE wordpress;
CREATE USER 'wp_user'@'%' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON wordpress.* TO 'wp_user'@'%';
FLUSH PRIVILEGES;
```







1. # **WordPress Yapılandırması**

   ### **1. Adım: WordPress Yapılandırma Dosyasını Düzenleme**

   WordPress’in yapılandırma dosyasını düzenliyoruz. Bu dosya, WordPress’in MySQL veritabanına bağlanmasını sağlar.

   1. **`wp-config.php` dosyasını düzenliyoruz:**

```
bashCopyEditsudo cp /var/www/html/wordpress/wp-config-sample.php /var/www/html/wordpress/wp-config.php
sudo nano /var/www/html/wordpress/wp-config.php
```

1. **Veritabanı bağlantı bilgilerini güncelliyoruz:**

```
php
define( 'DB_NAME', 'wordpress' );
define( 'DB_USER', 'wp_user' );
define( 'DB_PASSWORD', 'password' );
define( 'DB_HOST', '192.168.80.223' );
```



![2025-01-26 02-29-14.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-26%2002-29-14.png?raw=true)





1. ### **2. Adım: Apache Konfigürasyonunu Güncelleme**

   Apache’nin WordPress dosyalarına doğru şekilde yönlendirme yapabilmesi için sanal host (VirtualHost) yapılandırmasını güncelliyoruz.

   1. **WordPress kök dizini olarak `/var/www/html/wordpress` belirliyoruz:**

```
bash
<VirtualHost *:80>
    DocumentRoot /var/www/html/wordpress
    ServerName 2025ozgur.com

    <Directory /var/www/html/wordpress>
        AllowOverride All
        Require all granted
    </Directory>
</VirtualHost>

```



2.**Değişiklikleri kaydettikten sonra Apache’yi yeniden başlatıyoruz:**

```
bash

sudo systemctl restart apache2
```



### **3. Adım: WordPress Kurulumunu Tamamlama**

Web tarayıcısı üzerinden **http://2025ozgur.com** adresini ziyaret ederek WordPress kurulum ekranını açıyouz. Kurulum sırasında gerekli ayarları yaptıktan sonra  site adı, admin kullanıcı bilgilerini giriyoruz.





![2025-01-27 02-51-45.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-27%2002-51-45.png?raw=true)





![2025-01-27 02-53-08.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-27%2002-53-08.png?raw=true)





**SEO Uyumlu URL:**

- WordPress kontrol paneline gidip, **Ayarlar > Kalıcı Bağlantılar** kısmına tıklıyoruz ve **Post Name** seçeneğini seçiyoruz  Bu, URL'lerin SEO uyumlu olmasını sağlar.

### ![2025-01-27 03-14-04.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-27%2003-14-04.png?raw=true)



100 defa kullanıcı verilerini toplamaycağım sayfası wordpress gorunumu 



![2025-01-27 03-36-43.png'den ekran görüntüsü](https://github.com/nihatbayramm/-zg-ryazilim/blob/main/image/Screenshot%20from%202025-01-27%2003-36-43.png?raw=true)





