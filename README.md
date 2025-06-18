
## Proje Videoları:
https://drive.google.com/drive/folders/1VHescsVjVs9wswfoyq-fI1isCB9GeOsv?usp=sharing


Bu proje dizini, SQL Server Management Studio (SSMS) ortamında yürütülen 7 farklı veritabanı uygulamasını, kullanılan veritabanını, proje raporunu ve proje tanıtım videolarını içermektedir. Her bir proje, gerçek dünyadaki senaryolara uygun olarak planlanmış ve SQL komutlarıyla adım adım uygulanmıştır.

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

## 📁 Veritabanı Performans Optimizasyonu ve İzleme

**Amaç:** Veritabanı üzerindeki sorgu performansını analiz etmek, darboğazları belirlemek ve iyileştirme adımlarını uygulamak.

### İçerik:
- `01_sorgu_uygulamasi_ve_izleme.sql`: Performans takibi yapılacak sorguların örnek çalıştırılması.
- `02_Dynamic_Management_Views_(DMV)_ile_Performans_Analizi.sql`: DMV (Dynamic Management Views) ile aktif sorguların, kilitlerin ve kaynak tüketiminin izlenmesi.
- `03_index_yonetimi.sql`: Mevcut indekslerin durumu ve kullanım verilerinin analizi.
- `04_index_olusturma_komutu.sql`: Sorgu performansını artırmaya yönelik indeks oluşturma komutu.
- `06_yavas_sorgu.sql`: Performansı düşük, yavaş çalışan sorgu örnekleri.
- `07_optimize_edilmis_sorgu.sql`: Yavaş sorguların optimize edilmiş, iyileştirilmiş versiyonları.
- `08_veri_yoneticisi_rolleri.sql`: Performans yönetiminde rolü olan kullanıcı yetkileri ve rollerin atanması.
- `09_tracefile.trc`: SQL Server Profiler ile kaydedilmiş izleme dosyası (trace).

## 📁 Veritabanı Yedekleme ve Otomasyon Çalışması

**Amaç:** SQL Server Agent, Database Mail ve otomatik görevler kullanarak yedekleme işlemlerini planlamak, izlemek ve raporlamak.

### İçerik:
- `01_agent_xps_etkinlestir.sql`: SQL Server Agent için gerekli uzantıların (XP'ler) etkinleştirilmesi.
- `02_tam_yedek_alma.sql`: Veritabanının tam yedeğini alma komutu.
- `03_yedek_gecmisi_sorgu.sql`: Alınan yedeklerin geçmişini listeleyen sorgu.
- `04_rapor_proseduru_olustur.sql`: Yedekleme bilgilerini içeren e-posta raporu için prosedür oluşturma.
- `05_raporu_gonder.sql`: Oluşturulan raporun e-posta ile gönderilmesi.
- `06_database_mail_xps_ve_baslat.sql`: Database Mail yapılandırması ve servis başlatma adımları.
- `07_test_email_gonder.sql`: Mail yapılandırmasının doğru çalışıp çalışmadığını test etmek için e-posta gönderimi.
- `08_mail_kuyruk_ve_durum_sorgu.sql`: Gönderilen e-postaların kuyruk ve durum bilgilerini sorgulama.
- `09_event_log_sorgu.sql`: SQL Server olay günlüklerinden hata ve uyarı kayıtlarını sorgulama.

## 📁 Veritabanı Yük Dengeleme ve Dağıtık Veritabanı Yapıları

**Amaç:** Veritabanı erişim sürekliliğini artırmak, yük dengeleme sağlamak ve yüksek erişilebilirlik senaryolarını test etmek.

### İçerik:
- `01_replikasyon.sql`: Transactional replikasyon kurulumu ve temel yapılandırma adımları.
- `02_mirroring_ornegi.sql`: Veritabanı yansıtma (mirroring) örneği ve temel konfigürasyonu.
- `03_always_on_availability_ornegi.sql`: Always On Availability Groups kullanılarak yüksek erişilebilirlik yapısı oluşturma örneği.
- `04_principal_mirror_veritabani.sql`: Principal ve Mirror rollerinin veritabanına atanması.
- `05_mirror_sunucu_atama.sql`: Mirroring yapısında kullanılacak sunucuların atanması.
- `06_failover.sql`: Manuel failover işlemiyle sistemin yedek sunucuya geçişinin test edilmesi.

## 📁 Veritabanı Yükseltme ve Sürüm Yönetimi

**Amaç:** Veritabanı sürüm geçişlerini güvenli şekilde gerçekleştirmek, yeni sürümler öncesinde test ve yedekleme adımlarını uygulamak.

### İçerik:
- `00_tablo_olustur.sql`: Sürüm yönetimi ve testler için örnek tablo oluşturulması.
- `01_surum_yonetimi.sql`: Sürüm kontrolü ve geçiş planlaması için temel komutlar.
- `02_test_amacli_komut_1.sql`: Yeni sürümde uygulanacak ilk test komutu.
- `03_test_amacli_komut_2.sql`: Yeni sürümde uygulanacak ikinci test komutu.
- `04_backup.sql`: Güncel veritabanının yedeklenmesi.
- `05_restore.sql`: Gerekli durumda geri dönüş için yedeğin geri yüklenmesi.

---

Her bir `.sql` dosyası, SSMS ortamında sırasıyla çalıştırılabilir yapıdadır.
