# Olimpiyat Sporcuları Veri Analizi

Bu proje, Olimpiyatlar veri seti üzerinde gerçekleştirilen detaylı veri analizi çalışmasını içermektedir. Amaç, sporcuların demografik özellikleri, branşlara göre dağılımları ve madalya kazanma eğilimlerini incelemektir.

## Veri Seti Hakkında

- Toplam kayıt: 271.116  
- Sütunlar:
  Name, Sex, Age, Height, Weight, Team, NOC, Year, Season, City, Sport, Event, Medal
- Eksik veriler:
   Age, Height, Weight, Medal sütunlarında bazı eksik değerler mevcut

## Veri Temizleme ve Ön İşleme

- Gereksiz sütunlar (`ID`, `Games`) kaldırıldı  
- `Age`, `Height` ve `Weight` sütunlarındaki eksik değerler mantıklı şekilde dolduruldu:
  
   `Age`: Event + Height + Weight ortalamaları kullanılarak  
   `Height` ve `Weight`: Sport + Sex ortalamaları kullanılarak  
- `Medal` sütunundaki eksik değerler, sporcuların madalya kazanmadığını belirtmek için `No Medal` olarak dolduruldu

## Keşifsel Veri Analizi (EDA)

- **Genel istatistikler:** Sporcuların yaş, boy, kilo dağılımları ve branş/cinsiyet dağılımları  
- **Cinsiyet ve branş analizi:** Kadın ve erkek sporcuların branşlara göre dağılımı  
- **Madalya analizi:** Ülke ve branş bazında madalya sayıları ve oranları  
- **Trend analizi:** Yıllara göre sporcu sayısı ve ülke bazında madalya kazanma trendleri  
- **Korelasyon analizi:** Age, Height, Weight ve Madalya arasındaki ilişkiler  
- **Branşlara göre madalya olasılıkları:** Her branşta madalya kazanma dağılımları görselleştirildi

## Görselleştirmeler

- Bar ve line grafikleri ile branş ve ülke bazlı dağılımlar  
- Korelasyon heatmap ile sayısal değişkenlerin ilişkileri  
- Branş bazlı stacked bar grafikleri ile madalya kazanma olasılıkları  

## Kullanılan Araçlar

- Python   
- Pandas, NumPy (veri işleme)  
- Matplotlib, Seaborn (görselleştirme)

## Sonuçlar

- Sporcuların yaş, boy ve kilo dağılımları branş ve cinsiyete göre farklılık göstermektedir  
- Madalya kazanma olasılıkları branşa göre çeşitlilik göstermektedir  
- Korelasyon analizi, bazı branşlarda boy ve kilonun madalya kazanma ile pozitif ilişkili olduğunu göstermektedir  
