# 🪐 Antigravity CLI — 3B Uzay & N-Cisim Simülasyonu Model Benchmarkı

Antigravity CLI üzerindeki **5 ana yapay zeka modeline** (Medium düşünme seviyesinde) aynı anda (Swarm paralel çalıştırma ile), başka hiçbir dosya okumadan ve tek seferde (`write_file`) sıfırdan çalışan **3B Etkileşimli Güneş Sistemi & N-Cisim Kütleçekim / Kara Delik Simülasyonu** kodlama görevi verilmiştir.

Tüm düşünme/kodlama süreleri ve yakılan token miktarları doğrudan modellerin `transcript.jsonl` sistem kayıtlarından çıkarılmıştır.

## 📊 Benchmark Sonuç Tablosu

| Model | Düşünme + Kod Süresi | Output Token (Düşünme + Kod) | Input Token | Cache Read Token | Toplam Yakılan Token | Üretim Hızı | Kod Boyutu |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Claude Opus 5.5 (Medium)** | **684 sn** (11dk 24sn) | **78,509** | 109,567 | 0 | **188,076** | 114.8 tok/s | 987 satır (62.7 KB) |
| **Gemini 4 Argon (Medium)** | **208 sn** (3dk 28sn) | **21,970** | 43,167 | 0 | **65,137** | 105.6 tok/s | **1,711 satır** (57.7 KB) |
| **Claude Sonnet 5.5 (Medium)** | **231 sn** (3dk 51sn) | **30,580** | 47,016 | 59,537 | **137,133** | 127.3 tok/s | 523 satır (34.7 KB) |
| **Gemini 3.8 Flash (Medium)** | **120 sn** (2dk 00sn) | **17,265** | 40,454 | 25,658 | **83,377** | **143.9 tok/s** | 1,238 satır (47.7 KB) |
| **GPT-OSS 120B (Medium)** | **55 sn** (toplam 60sn) | **7,122** | 18,279 | 23,744 | **49,145** | 118.7 tok/s | 185 satır (8.1 KB) |

## 📁 Klasör Yapısı

- `index.html` — Tüm modeller arasında canlı geçiş yapabilen, **Yan Yana (Split-Screen)** karşılaştırma moduna ve detaylı **Süre & Token Analizi** grafiklerine sahip ana kontrol merkezi.
- `benchmark-data.json` — Ham telemetri, token ve model düşünme (`thinking`) kayıtları.
- `models/` — Her modelin tek seferde ürettiği bağımsız 3B simülasyon dosyaları:
  - `models/gemini-4-argon-medium.html`
  - `models/claude-opus-5-5-medium.html`
  - `models/claude-sonnet-5-5-medium.html`
  - `models/gemini-3.8-flash-medium.html`
  - `models/gpt-oss-120b-medium.html`
