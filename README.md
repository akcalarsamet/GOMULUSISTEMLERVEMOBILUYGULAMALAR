# Raspberry Pi ile Personel Takip Sistemi
## Projenin Amacı
ARM mimarisine sahip bir mikrodenetleyici olan Raspberry Pi kartı ile  RFID RC522 sensörü kullanılarak ,okutulan kartlarla personelin girişinin çıkışının control edilip,2*16 LCD ekranda gösterlip,web arayüz ve amazon veritabanına aktarılması.

# Proje Gereksinimleri
1-Raspberry Pi 3B+ <br/>
2- RFID RC522 <br/>
3-2*16 LCD Ekran <br/>
4-Breadboard<br/>
5-Potansiyometre<br/>
6-Micro SD Kart 16 GB<br/>
7-Adaptör 5V-3A USB-C<br/>
8-Bağlantı için gerekli kablolar<br/>
İşletim Sistemi<br/>
Raspbian İşletim Sistemi<br/>

## İşletim Sisteminin Kurulumu

SD Card Formatter programı ile SD Kart formatlanabilir. Daha sonra "Win32 Disk Imager" programı ile SD Kart'a önceden indirilen Rasbian işletim sistemi yüklenebilir.

[Rasbian işletim sistemi indirme linki](https://www.raspberrypi.org/downloads/raspberry-pi-os/) <br/>
[SD Card Formatter programı indirme linki](https://www.sdcard.org/downloads/formatter/) <br/>
[Win32 Disk Imager programı indirme linki](https://sourceforge.net/projects/win32diskimager/) <br/>

## RFID Nedir?

 RFID, (RADIO FREQUENCY IDENTIFICATION) açılımının kısaltmasıdır. Radyo frekansı ile haberleşen ve içinde bilgi depolayabilen chip teknolojisi olarak da tanımlanabilir. Chip' in kullandığı frekansa, hafızaya, haberleşmede kullanılan protokole ve ürünün şekline göre çok farklı RFID tipleri vardır. Bir RFID ürünü kart şeklinde olabileceği gibi, disk, tüp veya herhangi bir geometride de olabilir. Bilgi alışverişi sırasında tamamen radyo frekansı kullanıldığı için temassız kontrol sistemi olarak da bilinmektedir. Bugün bilgi saklayabilen tanımlama için teknolojinin ulaştığı son noktadır.
 
   RFID teknolojisine sahip ürünler pasif ve aktif olmak üzere 2 temel sınıfa ayrılır. Pasif tipteki ürünlerin içinde bir pil kaynağı yoktur. Gerekli enerjyi kendilerini okuyan cihazların antenlerinden dolayı oluşan elektrik alanından elde ederler. Bu yüzden ömürleri yaklaşık 100 yıl gibi uzun bir süredir. Ancak okuma mesafeleri kullanılan frekansa da bağlı olarak oldukça kısadır. Aktif ürünler ise enerji elde etmek için dahili bir enerji kaynağı bulundurur. Bu kartların ömürleri genelde 5-10 yıl civarındadır. Ancak okuma mesafeleri daha uzundur. ülkemizde otoyollarda kullanılan OGS sistemi aktif, HGS ve KGS sistemi ise pasif ürün grubuna ait birer örnektir.


  RFID teknolojisi bugün tüm dünyada yaygın bir kullanım alanına sahiptir. Personel kontrolü, ürün ve hayvan takibi, güvenlik bunlardan sadece birkaçıdır. RFID kartların yüksek güvenliğe sahip olanları Dünya'da kimlik kartı ve kredi kartı olarak da kullanılmaktadır.
 RFID, ingilizce RADIO FREQUENCY IDENTIFICATION açılımının kısaltmasıdır. Radyo frekansı ile haberleşen ve içinde bilgi depolayabilen chip teknolojisi olarak da tanımlanabilir. Chip' in kullandığı frekansa, hafızaya, haberleşmede kullanılan protokole ve ürünün şekline göre çok farklı RFID tipleri vardır. Bir RFID ürünü kart şeklinde olabileceği gibi, disk, tüp veya herhangi bir geometride de olabilir. Bilgi alışverişi sırasında tamamen radyo frekansı kullanıldığı için temassız kontrol sistemi olarak da bilinmektedir. Bugün bilgi saklayabilen tanımlama için teknolojinin ulaştığı son noktadır.


  RFID teknolojisine sahip ürünler pasif ve aktif olmak üzere 2 temel sınıfa ayrılır. Pasif tipteki ürünlerin içinde bir pil kaynağı yoktur. Gerekli enerjyi kendilerini okuyan cihazların antenlerinden dolayı oluşan elektrik alanından elde ederler. Bu yüzden ömürleri yaklaşık 100 yıl gibi uzun bir süredir. Ancak okuma mesafeleri kullanılan frekansa da bağlı olarak oldukça kısadır. Aktif ürünler ise enerji elde etmek için dahili bir enerji kaynağı bulundurur. Bu kartların ömürleri genelde 5-10 yıl civarındadır. Ancak okuma mesafeleri daha uzundur. ülkemizde otoyollarda kullanılan OGS sistemi aktif, HGS ve KGS sistemi ise pasif ürün grubuna ait birer örnektir.


  RFID teknolojisi bugün tüm dünyada yaygın bir kullanım alanına sahiptir. Personel kontrolü, ürün ve hayvan takibi, güvenlik bunlardan sadece birkaçıdır. RFID kartların yüksek güvenliğe sahip olanları Dünya'da kimlik kartı ve kredi kartı olarak da kullanılmaktadır.

## RFID RC522 Sensör

RC522 RFID Okuyucu Kartı, NFC frekansı olan 13,56 MHz frekansında çalışan tagler üzerinde okuma ve yazma işlemeni yapabilen, düşük güç tüketimli, ufak boyutlu bir karttır.
Raspberry pi,arduino başta olmak üzere bir çok mikrodenetleyeci platformu ile beraber rahatlıkla kullanılabilir. 424 kbit/s haberleşme hızına sahiptir. RFID üzerinde farklı şifreleme türlerini desteklemektedir. Desteklediği kart türleri mifare1 S50, mifare1 S70 mifare ultralight, mifare pro ve  mifare desfire'dir. 

**Not:** 125 KHz frekansında çalışan RFID kartlarını desteklememektedir. Yalnızca 13,56 MHz frekansında çalışan kartları desteklemektedir. NFC modülleri bu frekansta çalıştığı için NFC kartları ile beraber kullanılabilir.

## RFID Kart Teknolojileri

RFID kartlar kronolojik olarak bakıldığında; sadece okunabilir ve içinde seri numarası bulundurabilen basit bir yapıdan hem okunabilir hem de yazılabilir, içinde bir çok bilgiyi saklayabilecek yüksek hafızaya sahip, kopyalanmaya karşı güvenli, şifreli haberleşen karmaşık bir yapıya ulaşmıştır. Bu süreçte çok değişik özelliklere sahip RFID kartlar üretilmiştir.
 Her RFID kart hafızasında fabrikasyon olarak kodlanmış bir kart numarası ile tedarik edilir. Bu kart numarasının aynısı başka hiç bir kartta tekrar kullanılmaz. Bunu üretici firmalar garanti etmektedirler. Dünya üzerinde birbirinden farklı olan bu numaralar ' Unique ID ' olarak bilinmektedir.
## Donanım Yapısı

Yazılım aşamsına geçmeden donanım bağlantısını yapmak,yazılım aşamasında bize kolaylık sağlayacaktır. RC522 modülü 8 pine sahiptir ama biz sadece okuma yapacagımız için kartlar üzerinde herhangi bir yazma işlemi olmayacağından(IRQ pini kullanılmayacak) 7 pinini kullanarak Raspberry Pi GPIO pinleri ile bağlantı kuracağız.

RFID RC522 ile Raspberry Pi Arasındaki Bağlantı <br/>
•	RC522 SDA pini     => Raspberry Pi Pin 24.  <br/>
•	RC522  SCK pini     => Raspberry Pi Pin 23. <br/>
•	RC522  MOSI pini  => Raspberry Pi Pin 19. <br/>
•	RC522 MISO pini   => Raspberry Pi Pin 21. <br/>
•	RC522 GND pini    => Raspberry Pi Pin 6. <br/>
•	RC522 RST pini     => Raspberry Pi Pin 22. <br/>
•	RC522 3.3v pini    => Raspberry Pi Pin 1. <br/>

## LCD Ekran ve Potansiyometre Bağlantıları 

•	LCD’nin 1.pini (Ground) Breadboardın toprak hattına <br/>
•	LCD’nin 2.pini (VCC / 5V) Breadboardın pozitif hattına <br/>
•	LCD’nin 3.pini (V0) to potansiyometrenin 2. pinine <br/>
•	LCD’nin 4.pini (RS) Raspberry pi 7.pinine (GPIO4) <br/>
•	LCD’nin 5.pini (RW) Breadboardın toprak hattına <br/>
•	LCD’nin 6.pini (EN)   Raspberry pi 18.pinine (GPIO24 ) <br/>
•	LCD’nin 11.pini of LCD (D4) Raspberry pi 16.pinine (GPIO23 ) <br/>
•	LCD’nin 12.pini of LCD (D5) Raspberry pi 11.pinine (GPIO17) <br/>
•	LCD’nin 13.pini of LCD (D6) Raspberry pi 12.pinine  (GPIO18) <br/>
•	LCD’nin 14.pini of LCD (D7) Raspberry pi 15.pinine  (GPIO22) <br/>
•	LCD’nin 15.pini of LCD (LED +) Breadboardın pozitif hattına <br/>
•	LCD’nin 16.pini of LCD (LED -) Breadboardın toprak hattına <br/>
•	Potansiyometrnin sol pini Breadboardın toprak hattına <br/>
•	Potansiyometrnin sağ pini  Breadboardın pozitif hattına <br/>

## 16*2 LCD Ekranın Test Edilmesi ve Gerekli Kütüphanin İndirilmesi

Gerekli bağlantılar sağlandıysa.Kütüphaneyi klonlayarak test edebiliriz.

'git clone https://github.com/pimylifeup/Adafruit_Python_CharLCD.git'

Kütüphaneyi klonladıgınız dizine gidiniz ve aşadaki komutları kullanarak setup.py sriptini çalıştırın.

'cd ./Adafruit_Python_CharLCD'
