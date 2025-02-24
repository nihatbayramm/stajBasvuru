
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

-Bu adımlar takip edilerek sorun çözülmüş ve yükleme işlemi sorunsuz bir şekilde devam etmiştir.


**Bu bölümde, kullanıcı adı ve parolayla sunucuya giriş yapıyoruz.**
-Sunucuya güvenli bir şekilde erişim sağlanabilmesi için kullanıcı bilgileri doğru ve eksiksiz girilmelidir.

![image](https://github.com/user-attachments/assets/224ae1d4-6fc3-4b1c-9614-81762016c2b2)








