# Free Tier Cloud Rehberi (AWS & Azure)

Bu rehber sayesinde AWS veya Azure gibi bulut servislerini kullanarak, hiçbir ücret ödemeden kendi VPN sunucunuzu, kişisel cloud ortamınızı ve web sitenizi oluşturabilirsiniz. Özellikle öğrenciler için ücretsiz olan bu platformlarla projelerinizi hayata geçirebilirsiniz.

## Gereksinimler

### 1. Sunucu
Ücretsiz ya da ücretli bulut servislerini kullanabilirsiniz. Örneğin, `.edu` uzantılı öğrenci e-posta adresi ile kredi kartı bilgisi eklemeden Azure'a ücretsiz kaydolabilirsiniz. AWS gibi diğer seçenekleri de kullanabilirsiniz.

### 2. Programlar
- **PuTTY**: Sunucuya SSH ile bağlanmak için kullanıcı dostu bir istemci.
- **Kod Editörü**: Kod düzenlemek için **Notepad** veya **Visual Studio Code** kullanabilirsiniz.

### 3. Alan Adı
Projelerinizde alan adı kullanmanız gerekebilir. Uygun fiyatlı bir alan adı için [Porkbun](https://porkbun.com/) üzerinden yaklaşık 0.90 dolara `.xyz` uzantılı bir alan adı alabilirsiniz.

---

## Adım Adım Kurulum

### 1. Ücretsiz Cloud Hesabı Oluşturma

#### **Azure**
- [Azure Portal](https://portal.azure.com) üzerinden ücretsiz hesap oluşturun. Öğrenciyseniz, `.edu` e-posta adresiyle kaydolabilir ve kredi kartı eklemeden hesap oluşturabilirsiniz.

#### **AWS**
- [AWS Free Tier](https://aws.amazon.com/free/) üzerinden bir AWS hesabı açın. AWS'in ücretsiz katmanı bir yıl boyunca sanal makineler ve diğer hizmetlerden ücretsiz yararlanmanızı sağlar.

---

### 2. Sunucuya Bağlanma (SSH)

Cloud sunucunuzun IP adresini aldıktan sonra SSH ile bağlanmanız gerekecek.

1. **PuTTY**'yi indirip kurun.
2. IP adresinizi girin ve bağlantı kurun.
3. Aşağıdaki komutu kullanarak sunucunuza SSH üzerinden bağlanın:

    ```bash
    ssh username@sunucu_ip_adresi
    ```

Sunucular genellikle `ubuntu` veya `root` kullanıcı adıyla gelir.

---

### 3. Sunucuya Yazılım Kurulumu

#### **VPN Sunucusu Kurulumu**
VPN sunucusu kurmak için **OpenVPN** veya **WireGuard** gibi açık kaynaklı yazılımları kullanabilirsiniz.

**OpenVPN** kurulumu için:

```bash
sudo apt update
sudo apt install openvpn
```

Web Sunucusu Kurulumu

Web sitenizi barındırmak için Nginx veya Apache gibi web sunucularını kurabilirsiniz.

Örnek Nginx kurulumu:
```
sudo apt install nginx
sudo systemctl start nginx
```
4. Alan Adı Kaydı

Alan adı kaydı için Porkbun üzerinden uygun fiyatlı bir alan adı alabilirsiniz. .xyz uzantılı alan adları genellikle ucuz olur (~0.90$). Alan adı satın aldıktan sonra, DNS ayarlarını sunucunuzun IP adresi ile yapılandırmanız gerekecektir.
5. Web Sitesi Kurulumu

Sunucunuza bir web sitesi kurmak için WordPress, HTML tabanlı siteler veya başka bir CMS kullanabilirsiniz. Web sunucusu olarak Nginx'i kurup basit bir statik site başlatabilirsiniz.

Örnek Nginx ayarları:
```
sudo apt install nginx
sudo systemctl start nginx
```
6. Alan Adı ile Bağlantı

Alan adınızı sunucunuz ile ilişkilendirdikten sonra, web sunucunuza yönlendirmek için DNS kayıtlarını doğru bir şekilde yapılandırın.
