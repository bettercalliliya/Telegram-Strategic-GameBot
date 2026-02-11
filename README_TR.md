# 🏰 Telegram Strateji Oyun Botu

🌐 **[فارسی](README_FA.md)** | **Türkçe** | **[English](README.md)**

[![MIT Lisansı](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python 3.6+](https://img.shields.io/badge/Python-3.6%2B-brightgreen.svg)](https://www.python.org/)
[![Telegram Bot API](https://img.shields.io/badge/Telegram-Bot%20API-blue.svg?logo=telegram)](https://core.telegram.org/bots/api)
[![SQLite](https://img.shields.io/badge/Database-SQLite-lightgrey.svg?logo=sqlite)](https://www.sqlite.org/)
[![Sponsor](https://img.shields.io/badge/Sponsor-%E2%9D%A4-pink.svg?logo=github-sponsors)](https://github.com/sponsors/iliyadindar)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-%F0%9F%8D%BA-yellow.svg?logo=buy-me-a-coffee)](https://buymeacoffee.com/iliyadindar)

Telegram grupları için **çok oyunculu stratejik kaynak yönetimi oyun botu**. Oyuncular kendi topraklarının lordları olur — ekonomi yönetimi, bina yükseltme, ordu eğitimi, antlaşma yapma ve rakip lordlara saldırı düzenleme — hepsi Telegram üzerinden.

---

## 📑 İçindekiler

- [Özellikler](#-özellikler)
- [Oyun Mekanikleri](#-oyun-mekanikleri)
- [Başlarken](#-başlarken)
  - [Gereksinimler](#gereksinimler)
  - [Kurulum](#kurulum)
  - [Yapılandırma](#yapılandırma)
- [Kullanım](#-kullanım)
  - [Komutlar](#komutlar)
  - [Menü Seçenekleri](#menü-seçenekleri)
- [Proje Yapısı](#-proje-yapısı)
- [Katkıda Bulunma](#-katkıda-bulunma)
- [Lisans](#-lisans)
- [İletişim](#-iletişim)
- [Destek](#-destek)

---

## ✨ Özellikler

| Kategori | Detaylar |
|---|---|
| 🏗️ **Kaynak Yönetimi** | 8 kaynak türünü yönetin: para, taş, odun, demir, altın, yiyecek, et ve giysi |
| 🏭 **Bina ve Fabrika Yükseltmeleri** | Taş ocağı, kereste fabrikası, demir madeni, altın madeni, çiftlik, hayvan çiftliği, giysi fabrikası ve banka yükseltmeleri |
| ⚔️ **Askeri Sistem** | Kılıçlı asker, tüfekçi, atlı süvari, özel muhafız, top ve deniz kuvvetleri eğitimi |
| 📜 **Diplomasi ve Antlaşmalar** | Oyuncular arasında etkileşimli onaylarla antlaşma oluşturma, gönderme ve onaylama |
| 🔔 **Haftalık Üretim Döngüleri** | Fabrika ve bina çıktılarını haftalık olarak toplama |
| 💬 **Oyun İçi İletişim** | Gruplar arası özel mesaj gönderme ve kanala bildiri yayınlama |
| 🛡️ **Saldırı ve Savunma** | Detaylı saldırı takibi ile askeri seferleri planlama ve kaydetme |
| 🔧 **Yönetici Kontrolleri** | Varlık değerlerini ayarlama ve haftalık güncellemeleri tetikleme |

---

## 🎮 Oyun Mekanikleri

### Kaynaklar

Oyuncular temel kaynak ve askeri birim tedarikiyle başlar. Üretimi artırmak için fabrikaları ve binaları yükseltin:

- **Ekonomi**: Para 💰 · Taş 🪨 · Odun 🪵 · Demir ⛏️ · Altın 🥇 · Yiyecek 🌾 · Et 🥩 · Giysi 👕
- **Askeri**: Kılıçlı Asker ⚔️ · Tüfekçi 🔫 · Atlı Kılıçlı 🐴 · Atlı Tüfekçi 🏇 · Özel Muhafız 🛡️ · Orta Top 💣 · Büyük Top 🎯 · Küçük/Orta/Büyük Gemi 🚢

### Binalar ve Fabrikalar

Her bina birden fazla seviyede yükseltilebilir. Daha yüksek seviyeler haftalık döngü başına daha fazla kaynak üretir:

- Taş Fabrikası · Odun Fabrikası · Demir Fabrikası · Altın Madeni
- Çiftlik · Hayvan Çiftliği · Giysi Fabrikası · Banka
- Her birim türü için askeri kamplar ve tersaneler

---

## 🚀 Başlarken

### Gereksinimler

- **Python** 3.6 veya üzeri
- [@BotFather](https://t.me/BotFather)'dan bir **Telegram Bot Token**
- **SQLite3** (Python ile birlikte gelir)

### Kurulum

1. **Depoyu klonlayın:**

   ```bash
   git clone https://github.com/iliyadindar/Telegram-Strategic-GameBot.git
   cd Telegram-Strategic-GameBot
   ```

2. **Bağımlılıkları yükleyin:**

   ```bash
   pip install pyTelegramBotAPI
   ```

### Yapılandırma

`main.py` dosyasını açın ve aşağıdaki değerleri güncelleyin:

```python
API_TOKEN = 'YOUR_TELEGRAM_BOT_API_TOKEN'
ADMIN_ID = 123456789          # Telegram kullanıcı kimliğiniz
CHANNEL_ID = "@your_channel"  # Telegram kanal kullanıcı adınız
```

Ardından botu başlatın:

```bash
python main.py
```

> SQLite veritabanı (`game_bot.db`) ilk çalıştırmada otomatik olarak oluşturulur.

---

## 📖 Kullanım

### Komutlar

| Komut | Açıklama |
|---|---|
| `/setlord` | Mevcut grupta lord olarak kayıt olun |
| `/start` | Ana menüyü açın ve oynamaya başlayın |

### Menü Seçenekleri

| Buton | İşlev |
|---|---|
| 💰 **Varlıklar** | Mevcut kaynaklarınızı ve askeri birimlerinizi görüntüleyin |
| 🛠️ **Yükseltme** | Binaları ve fabrikaları yükseltin |
| 🙌 **Bildiri** | Oyun kanalına bir bildiri yayınlayın |
| ✉️ **Özel Mesaj** | Başka bir gruba özel mesaj gönderin |
| 📜 **Antlaşma** | Diğer oyuncularla antlaşma oluşturun, gönderin veya onaylayın |
| ⚔️ **Askeri Sefer** | Saldırı detaylarını planlayın ve kaydedin |
| 🔨 **Haftalık Güncelleme** | Haftalık fabrika çıktılarını toplayın *(yalnızca yönetici)* |
| 🛠️ **Varlık Ayarı** | Varlık değerlerini ayarlayın *(yalnızca yönetici)* |

---

## 📁 Proje Yapısı

```
Telegram-Strategic-GameBot/
├── main.py          # Bot mantığı, işleyiciler ve veritabanı kurulumu
├── LICENSE          # MIT Lisansı
├── SECURITY.md      # Güvenlik politikası
├── README.md        # Proje dokümantasyonu (İngilizce)
├── README_FA.md     # Proje dokümantasyonu (Farsça)
└── README_TR.md     # Proje dokümantasyonu (Türkçe)
```

---

## 🤝 Katkıda Bulunma

Katkılarınızı bekliyoruz! Başlamak için:

1. Depoyu Fork edin
2. Bir özellik dalı oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi Commit edin (`git commit -m 'Add amazing feature'`)
4. Dalınıza Push edin (`git push origin feature/amazing-feature`)
5. Bir Pull Request açın

Büyük değişiklikler için, lütfen önce ne değiştirmek istediğinizi tartışmak üzere bir Issue açın.

---

## 📄 Lisans

Bu proje **MIT Lisansı** altında lisanslanmıştır. Ayrıntılar için [LICENSE](LICENSE) dosyasına bakın.

---

## 📬 İletişim

**Iliya Dindar** — Geliştirici ve Proje Sahibi

- Telegram: [@iliyadindar](https://t.me/iliyadindar)
- GitHub: [@iliyadindar](https://github.com/iliyadindar)

---

## 💖 Destek

Bu projeyi faydalı bulduysanız, geliştirmeyi desteklemeyi düşünün:

[![GitHub Sponsor](https://img.shields.io/badge/GitHub_Sponsor-%E2%9D%A4-pink.svg?style=for-the-badge&logo=github-sponsors)](https://github.com/sponsors/iliyadindar)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-%F0%9F%8D%BA-yellow.svg?style=for-the-badge&logo=buy-me-a-coffee)](https://buymeacoffee.com/iliyadindar)

<p align="center">
  ⭐ Bu projeyi faydalı bulduysanız, lütfen bir yıldız vermeyi düşünün!
</p>
