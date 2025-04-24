

Bu proje dizini, SQL Server Management Studio (SSMS) ortamında yürütülen üç farklı veritabanı uygulamasını içermektedir. Her bir proje, gerçek dünyadaki senaryolara uygun olarak planlanmış ve SQL komutlarıyla adım adım uygulanmıştır.

## 📁 Veritabanı Yedekleme ve Felaketten Kurtarma Planı

**Amaç:** Veritabanı yedekleme ve kurtarma süreçlerini test etmek, felaket anında veriyi geri yükleyebilmek.

### İçerik:
- `01_veritabani_yedekleme.sql`: Northwind veritabanının tam yedeğini `.bak` dosyası olarak alma.
- `02_drop_temizmusteriler.sql`: TemizMusteriler adlı tabloyu silerek veri kaybı simülasyonu oluşturma.
- `03_veritabani_geri_yukleme.sql`: Yedekten `Northwind_Kurtarildi` adında yeni bir veritabanı oluşturma.
- `04_geri_yuklenen_veriyi_kontrol.sql`: Geri yüklenen veritabanının içeriğini doğrulama amaçlı SELECT sorgusu.

## 📁 Veritabanı Güvenliği ve Erişim Kontrolü

**Amaç:** SQL Server üzerinde kullanıcı erişim yönetimi, SQL Injection'a karşı koruma ve loglama sistemleri kurmak.

### İçerik:
- `01_create_login.sql`: SQL Server Authentication ile login oluşturma.
- `02_create_user.sql`: Login'e bağlı kullanıcı oluşturma.
- `03_yetki_duzenleme.sql`: Kullanıcıya sadece SELECT yetkisi verme.
- `04_ornek_select.sql`: Yetkili kullanıcının SELECT işlemi.
- `05_update_yetki_hatasi.sql`: Yetkisiz UPDATE girişimi ile hata alma.
- `06_injection_ornegi.sql`: SQL injection açığı içeren sorgu.
- `07_injection_guvenli.sql`: Parametreli sorgu ile güvenli sorgu kullanımı.
- `08_audit_olustur.sql`: Audit sisteminin dosya yoluna kaydedecek şekilde oluşturulması.
- `09_audit_specification.sql`: Belirli kullanıcı işlemlerinin loglanması için audit tanımı.
- `10_denetim_update_test.sql`: Kullanıcı ile UPDATE ve SELECT işlemi gerçekleştirme.
- `11_audit_sonuc_kontrol.sql`: `sys.fn_get_audit_file` fonksiyonu ile logların sorgulanması.

## 📁  Veri Temizleme ve ETL Süreçleri

**Amaç:** Hatalı ve eksik verilerin tespiti, düzeltilmesi ve temiz verinin ayrı tabloya aktarılması.

### İçerik:
- `01_veri_girisi.sql`: Eksik/hatalı örnek verilerin eklenmesi.
- `02_veri_temizligi.sql`: NULL ve boş değerlerin tespiti.
- `03_sehirbuyuk_sutun_ekle.sql`: SehirBuyuk adında yeni sütun eklenmesi.
- `04_veri_temizleme_ve_donusturme.sql`: NULL değerlerin standart hale getirilmesi ve verilerin dönüştürülmesi.
- `05_donusturulmus_veri_sorgusu.sql`: City ve SehirBuyuk sütunlarının kontrol edilmesi.
- `06_temiz_veri_kopyala.sql`: Temiz verilerin yeni tabloya kopyalanması (TemizMusteriler).
- `07_temiz_veri_sorgu.sql`: TemizMusteriler tablosundan örnek veri sorgulama.
- `08_veri_kalitesi_raporu.sql`: Temizlik öncesi ve sonrası veri karşılaştırması.

---

Her bir `.sql` dosyası, SSMS ortamında sırasıyla çalıştırılabilir yapıdadır.
