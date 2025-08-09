# ADC Configuration with STM32

![Potansiyometre Bağlantısı](https://github.com/user-attachments/assets/7465c22f-0b0e-49c8-9eb2-2cf86cc4704e)

Bu proje, **STM32** üzerinde **ADC (Analog-to-Digital Converter)** kullanarak potansiyometreden okunan değerlerle LED’leri kontrol etmeyi amaçlamaktadır.  
Potansiyometreden gelen gerilim değeri ADC ile sayısal değere dönüştürülür ve bu değere göre **4 adet LED** kademeli olarak yakılır.

## Çalışma Mantığı
- Potansiyometreden alınan ADC değeri belirli eşiklerle karşılaştırılır.
- Değer arttıkça LED sayısı da artar:
  - **0 - 400** → 0 LED yanar
  - **400 - 1200** → 1 LED yanar
  - **1200 - 2500** → 2 LED yanar
  - **2500 - 3800** → 3 LED yanar
  - **3800 ve üzeri** → 4 LED yanar
- Kod içerisinde **global değişken** kullanılmıştır.

## Kullanılan Donanımlar
- STM32 mikrodenetleyici kartı
- Potansiyometre
- 4x LED
- Bağlantı kabloları

## Kod Yapısı
- **adc.c / adc.h** → ADC konfigürasyonu ve veri okuma işlemleri
- **main.c** → Ana program döngüsü, LED kontrol mantığı
- **global değişkenler** → ADC değeri saklama ve işlem için

## Nasıl Çalıştırılır?
1. Potansiyometreyi şemadaki gibi bağlayın.
2. Projeyi STM32CubeIDE ile açın.
3. Kodları kartınıza yükleyin.
4. Potansiyometreyi çevirerek LED’lerin kademeli olarak yanmasını gözlemleyin.
