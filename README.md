Nessus Tarama Sonuçlarını İşleyen Python Uygulaması
1. Uygulamanın Üretim Amacı
•	Nessus tarama sonuçlarının büyük ve karmaşık veri setlerinden oluşması sebebiyle bu verileri işlemek zor olabilir.
•	Gereksiz veya geçersiz verilerin manuel olarak temizlenmesi zahmetlidir.
•	Raporlama faaliyetlerinde yarı otomatize sisteme geçiş gerekliliği.
•	Verilerin düzgün bir şekilde filtrelenip organize edilmesi gerekir.
•	Analiz ve arşivlemeyi kolaylaştırmak amacıyla çıktıların daha düzenli bir hale getirilmesi gerekliliği doğmuştur.
2. Uygulamanın Çalışma Mantığı
•	Adım 1: Nessus tarama sonuçları bir Excel dosyası (nessus.xlsx) olarak yüklenir.
•	Adım 2: Excel dosyasındaki veriler başlıklara göre (Plugin ID, Risk, Host, Protocol, Port, Name) ayrılır.
•	Adım 3: "None" değerine sahip risk seviyeleri filtrelenir ve geçerli verilerle yeni bir Excel dosyası (filtered_nessus.xlsx) oluşturulur.
•	Adım 4: Filtrelenmiş veriler kullanılarak, her bir tarama sonucuna ait klasör ve bu klasörlerin içinde IP ve port bilgilerini içeren data.txt dosyaları oluşturulur.
•	Adım 5: Her bir güvenlik açığına ait veriler ilgili klasörlerde düzenli bir şekilde saklanır.

3. Uygulama Çalıştırma
•	İlk olarak Nessus uygulaması üzerinden .csv formatında bir export alınması gerekmektedir. Rapor kısmında işaretlenmesi gereken maddeler aşağıdaki gibidir.
•	Plugin ID
•	Risk
•	Host
•	Protocol
•	Port
•	Name
•	Uygulama çalıştırılmadan önce aynı dizinde nessus.xlsx adlı dosyanın içeriği yukarıdaki verileri içermelidir.
•	Uygulama çalıştırılmadan önce pip install  openpyxl komutu çalıştırılmalıdır. 
•	Uygulama .csv uzantılı dosyalarda hata vermektedir. Dosya içeriği .xlsx uzantılı bir dosyaya kopyalanmalıdır. 
•	Son olarak cmd üzerinde python uygulama.py olarak dosya çalıştırılmalıdır.

4. Uygulamanın Faydaları
•	Düzenli Veri Saklama: Her bir güvenlik açığı için klasörler ve dosyalar oluşturularak, sonuçlar düzenli bir biçimde arşivlenir.
•	Zamandan Tasarruf: Büyük verilerin manuel işlenmesine gerek kalmadan otomatik olarak işlenmesi sağlanır. Raporlama faaliyetleri için ön destek sağlanır.
•	Hata Azaltma: Otomasyon sayesinde insan hatası minimuma indirilir.
•	Kolay Kullanılabilirlik: Verilerin Excel ve metin dosyaları şeklinde organize edilmesi, paylaşım ve analiz açısından büyük kolaylık sunar.
