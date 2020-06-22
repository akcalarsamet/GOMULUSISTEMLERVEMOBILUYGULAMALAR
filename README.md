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

