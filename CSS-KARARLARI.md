# CSS Kararlari

## 1. Breakpoint Secimi
- Neden 640px ve 1024px sectim? Cunku icerikler bu genisliklerde yapi degistirmeye en uygun hale geliyor; tablet ve masaustu standart genisliklerine denk dusuyor.
- Icerigim bu noktalarda mobildeki (0-639px) dikey yigindan (column) yatay Flex hizanlamasi (row) ve cok sutunlu Grid duzenine terfi ediyor.

## 2. Layout Tercihleri
- Header icin Flexbox sectim cunku logoyu bir tarafa, navigasyon menulerini ise diger tarafa yaslamak araliga dagitmak (`justify-content: space-between`) acisindan cok pratiktir.
- Proje kartlari icin Grid sectim cunku iki boyutlu bir yapi ile listeleme olusturmak Grid ile cok kolaydir.
- `auto-fit` kullandim, boylece ekran genisledikce sabit kalan bos alanlarin elemanlari daraltmasi engellendi, o sutunlara yenileri yerlesti, eger baska eleman yoksa da mevcut elemanlar o yerleri orantili olarak doldurdu.

## 3. Design Tokens
- Renk paletinde modern, koyu mavi vurgulu pastel bir ton sectim (`#1E3A8A` / `#2563EB`) ki guvenilir bir portfolyo hissi yaratsin.
- Spacing skalasini 4px'in (0.25rem) katlari olacak sekilde (xs, sm, md, lg, xl, 2xl, 3xl) duzenledim, boylece orantilar tutarli durdu.
- Fluid typography icin `clamp` degerleri alt sinirda ufak metin boyutlari, genis ekranlarda ise ust sinirda cok buyuk olup rahatsiz etmeyecek ama hiyerarsiyi koruyacak sekilde sinirlandirilarak tasarlandi.

## 4. Responsive Stratejiler
- Projeyi bastan mobile-first metodolojisine alistirarak yazdim; `index.css` dosyasindaki varsayilan ve media query icinde olmayan tum kurallarim mobil cihazlari baz aldi.
- Yukaridaki kurali yalnizca ekran yetersizliginden oturu buyuk hale geldiginde bozmamak adina `min-width` kurallari (640px ve 1024px) kullanildi.
- Gorsellerde boyut asimina neden olmamak adina `max-width: 100%` ve `object-fit: cover` standart tutuldu.
