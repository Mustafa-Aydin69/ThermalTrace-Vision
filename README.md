# ThermalTrace Vision 

**Soğuk Zincir ve Medikal Lojistik Takip Ağı**

ThermalTrace Vision, aşı, kan torbası veya hassas gıda gibi hayati önem taşıyan yükleri taşıyan araçların anlık durumlarını takip eden kritik bir operasyon panelidir. Bu sistem, medikal ve hassas lojistik süreçlerinde güvenliği, kaliteyi ve uçtan uca izlenebilirliği en üst düzeye çıkarmayı hedefler.

## Teknik Odak ve Mimari

Projenin merkezinde, kesintisiz veri akışı ve anında reaksiyon gösteren bir uyarı mekanizması bulunmaktadır:

*   **Sürekli Veri Akışı:** Araçlarda bulunan IoT sensörlerinden gelen sıcaklık, nem ve sarsıntı verileri sürekli ve gerçek zamanlı olarak sunucuya akar.
*   **Otomatik Kırmızı Alarm (Red Alarm):** Eğer taşıma sıcaklığı (veya diğer kritik parametreler) belirlenen güvenli derecelerin dışına çıkarsa, sistem otomatik olarak bir alarm durumu başlatır.
*   **OpenTelemetry Destekli İzleme:** Sistemdeki tüm olaylar, eşik aşımları ve veri akışı, OpenTelemetry destekli modern bir loglama mimarisi üzerinden izlenir. Bu sayede darboğazlar ve kritik olaylar milisaniyeler içinde tespit edilir.
*   **Çift Yönlü Anlık Bildirim:** Kritik bir ihlal durumunda, loglama mimarisi üzerinden hem **şoförün mobil uygulamasına** hem de **merkezdeki operasyon sorumlusunun paneline** eş zamanlı olarak "Kırmızı Alarm" düşer. Bu sayede ürüne zarar gelmeden anında fiziksel müdahale imkanı sağlanır.

## Temel Özellikler

*   **Gerçek Zamanlı Harita ve Sensör İzleme:** Araçların anlık konumu ile birlikte taşıdıkları yükün sıcaklık, nem ve sarsıntı durumlarının tek ekrandan takibi.
*   **Gelişmiş Alarm Yönetimi:** Farklı kargo tipleri (örn: aşı için ayrı, kan torbası için ayrı) için özelleştirilebilir eşik değerleri.
*   **Mobil Şoför Uygulaması:** Şoförlerin kargo durumunu anlık görebileceği ve acil durumlarda sesli/görsel uyarılar alabileceği mobil arayüz.
*   **Uçtan Uca Loglama:** Operasyonel şeffaflık ve geçmişe dönük denetimler (audit) için tüm verilerin ve alarmların güvenli bir şekilde saklanması.

##  Olası Teknoloji Yığını

*   **IoT İletişimi:** MQTT, WebSockets
*   **Backend & Veri İşleme:** Node.js / Go / Python, Apache Kafka / RabbitMQ
*   **Loglama ve Gözlemlenebilirlik (Observability):** OpenTelemetry, Prometheus, Grafana, ELK Stack
*   **Frontend (Operasyon Paneli):** React.js / Vue.js / Next.js
*   **Mobil Uygulama:** React Native / Flutter
*   **Veritabanı:** Time-series veritabanları (örn: InfluxDB, TimescaleDB) ve PostgreSQL / MongoDB

---
