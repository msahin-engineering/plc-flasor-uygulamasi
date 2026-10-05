# PLC Flaşör Uygulaması

Bu projede Siemens S7-1200 PLC ve TIA Portal V18 kullanılarak TON zamanlayıcıları ile periyodik çalışan bir flaşör uygulaması gerçekleştirilmiştir.

## Kullanılan Teknolojiler

- Siemens S7-1200 PLC
- TIA Portal V18
- Ladder (LAD)
- TON zamanlayıcıları

## Program Yapısı

### Network 1 – Sistem Start/Stop

Start butonu ile sistem devreye alınır ve M10.0 "SISTEM MEM" biti kullanılarak mühürleme yapılır. Stop butonuna basıldığında sistem durdurulur.

### Network 2 – Flaşör Yanma ve Sönme Süreleri

İki adet TON zamanlayıcısı kullanılmıştır. TIMER 1 için 8 saniye, TIMER 2 için 4 saniye süre tanımlanmıştır. Zamanlayıcıların çıkışları kullanılarak flaşörün periyodik olarak çalışması sağlanır.

### Network 3 – Flaşör Çıkışı

Sistem aktif olduğunda zamanlayıcı durumuna bağlı olarak Q0.0 "FLASOR" çıkışı kontrol edilir. Böylece çıkış belirlenen sürelerde yanıp söner.

## Proje Dosyası

Repository içerisinde TIA Portal V18 ile oluşturulmuş `.zap18` proje arşivi bulunmaktadır.

## Ladder Diyagramı

Programın Ladder diyagramı aşağıda gösterilmektedir.
