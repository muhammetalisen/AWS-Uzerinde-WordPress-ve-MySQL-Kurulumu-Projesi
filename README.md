# AWS Üzerinde WordPress ve MySQL Kurulumu Projesi

## Proje Amacı
Bu proje, AWS üzerinde bir WordPress web sitesi kurmak ve MySQL veritabanını Amazon RDS (Relational Database Service) üzerinde yönetmek amacıyla gerçekleştirilmiştir.

## Kurulum Adımları

### 1. EC2 Sunucusu Kurulumu
- AWS Management Console kullanarak bir EC2 instance'ı başlatıldı. Ubuntu işletim sistemi seçildi.
- Gerekli güvenlik grubu ayarları yapılandırıldı; HTTP (port 80) ve SSH (port 22) izinleri verildi.

### 2. Apache ve PHP Kurulumu
- EC2 instance'ına SSH ile bağlanıldı ve Apache web sunucusu ile PHP yüklendi. Aşağıdaki komutlar kullanılarak kurulum yapıldı:
  ```bash
  sudo apt update -y
  sudo apt install apache2 -y
  sudo apt install php libapache2-mod-php php-mysql -y

### 3. WordPress Kurulumu
WordPress'in en son sürümü indirildi ve gerekli dizine kopyalandı.
wp-config.php dosyası, veritabanı bilgilerini içerecek şekilde düzenlendi.

### 4. RDS MySQL Veritabanı Kurulumu
AWS RDS kullanarak MySQL veritabanı oluşturuldu. Veritabanı adı, kullanıcı adı ve şifre belirlendi.
EC2 instance'ı ile RDS veritabanı arasındaki bağlantı güvenlik grubu ayarları ile sağlandı.

### 5. WordPress ve RDS Entegrasyonu
wp-config.php dosyasındaki veritabanı bilgileri güncellendi ve RDS endpoint bilgileri eklendi.
WordPress arayüzüne erişim sağlanarak site başlığı, kullanıcı adı ve şifre gibi gerekli bilgiler girildi.
Sonuç
Bu proje, AWS üzerinde WordPress kurulumunu ve RDS ile MySQL veritabanı yönetimini başarılı bir şekilde tamamlamıştır. Kullanıcılar, web tarayıcısı üzerinden siteye erişebilirken, veritabanı yönetimi RDS üzerinden güvenli bir şekilde yapılabilmektedir.
