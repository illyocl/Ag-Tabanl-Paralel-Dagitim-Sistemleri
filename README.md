

Bu proje dizini, SQL Server Management Studio (SSMS) ortamında yürütülen üç farklı veritabanı uygulamasını içermektedir. Her bir proje, gerçek dünyadaki senaryolara uygun olarak planlanmış ve SQL komutlarıyla adım adım uygulanmıştır.

## 📁 Veritabanı Yedekleme ve Felaketten Kurtarma Planı

**Amaç:** Veritabanı yedekleme ve kurtarma süreçlerini test etmek, felaket anında veriyi geri yükleyebilmek.

### İçerik:
- `01_yedekleme.sql`: Northwind veritabanının tam yedeğini alma.
- `02_tablo_sil.sql`: Örnek bir felaket senaryosu (veri kaybı).
- `03_yedekten_geri_yukleme.sql`: Yedek dosyasından veritabanını Northwind_Kurtarildi adıyla geri yükleme.
- `04_geri_yuklenen_veriyi_goruntule.sql`: Kurtarılan veri içeriğini kontrol etme.

## 📁 Veritabanı Güvenliği ve Erişim Kontrolü

**Amaç:** SQL Server üzerinde kullanıcı erişim yönetimi, SQL Injection'a karşı koruma ve loglama sistemleri kurmak.

### İçerik:
- `01_login_kullanici.sql`: SQL Authentication ile giriş oluşturma.
- `02_yetkiler.sql`: Kullanıcıya sadece SELECT yetkisi verme, diğer işlemleri engelleme.
- `03_sql_injection_testi.sql`: Güvensiz ve güvenli sorgu örnekleriyle SQL Injection farkı.
- `04_audit.sql`: Audit loglarının oluşturulması ve kullanıcı aktivitelerinin izlenmesi.

## 📁  Veri Temizleme ve ETL Süreçleri

**Amaç:** Hatalı ve eksik verilerin tespiti, düzeltilmesi ve temiz verinin ayrı tabloya aktarılması.

### İçerik:
- `01_veri_ekle.sql`: Hatalı kayıtlar içeren veri girişi.
- `02_temizlenecek_veri_secimi.sql`: Eksik, boş veya hatalı verilerin sorgulanması.
- `03_duzeltme_ve_donusum.sql`: NULL ve boş alanların standartlaştırılması, City kolonunun büyük harfe çevrilmesi.
- `04_tabloya_aktar.sql`: Temizlenen verinin `TemizMusteriler` tablosuna aktarılması.
- `05_raporlama.sql`: Eksik şehir ve toplam temiz kayıt sayısını raporlama.

---

Her bir `.sql` dosyası, SSMS ortamında sırasıyla çalıştırılabilir yapıdadır.
