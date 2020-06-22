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
