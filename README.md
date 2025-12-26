# Türkçe Haber Veri Seti - Varlık Çıkarımı ile

Türkçe haber makalelerinden çıkarılmış varlıklar ve bilgi grafı bilgileri içeren bir veri seti.

## Veri Seti Yapısı

- **`data/raw/`**: JSON formatında 200 ham haber makalesi
- **`data/labeled/`**: Varlık çıkarımı ile etiketlenmiş veriler
  - `labeled_news_without_cardinalities.json`: Tam etiketlenmiş veri seti
  - `selected_50_examples_for_operations.json`: İşlemler için örnek alt küme
- **`data/schema/`**: Finansal bilgi grafı şema tanımı
  - `schema.json`: Varlık tipleri, özellikler ve ilişkiler içeren tam şema

## Veri Formatı

Her makale şunları içerir:
- `title`: Makale başlığı
- `content`: Tam makale metni
- `source`: Haber kaynağı (örn. bigpara_hurriyet, euronews, haberturk, investing)
- `url`: Orijinal makale URL'i
- `date`: Yayın tarihi
- `entities`: Özelliklerle birlikte çıkarılmış varlıklar

## Şema

Veri seti, `data/schema/schema.json` dosyasında tanımlanan bir bilgi grafı şemasını takip eder. Şema şunları içerir:

**Varlık Tipleri:**
- Person, Company, Institution, Organization
- Sector, Financial_Instrument, Financial_Market, Financial_Index, Financial_Concept
- Country, City, Location, Product, Facility

Her varlık tipi şunları içerir:
- Açıklama ve özellikler
- Kardinalite kısıtlamaları ile çıkan ilişkiler
- Uygulanabilir olduğunda ilişki özellikleri

Tam şema tanımı için `data/schema/schema.json` dosyasına bakın.

## Kullanım

Bu veri seti araştırma amaçlı sağlanmaktadır. Akademik çalışmalarda kullanılırsa lütfen uygun şekilde atıf yapın.

**Not:** Etiketli açıklamalar yalnızca değerlendirme amaçlıdır ve kapsamlı veya mutlak doğruluk olarak kabul edilmemelidir.

## Lisans

Detaylar için [LICENSE](LICENSE) dosyasına bakın.
