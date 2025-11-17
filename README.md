<div align="center">

# 🎯 Tenny-Progresbar

### Modern Bullet-Themed Progress Bar for FiveM
### FiveM için Modern Mermi Temalı Progress Bar

[![FiveM](https://img.shields.io/badge/FiveM-Ready-green.svg)](https://fivem.net/)

</div>

---

## 📖 Description / Açıklama

**EN:** A modern and stylish bullet-themed progress bar script optimized for FiveM servers. Features 14 customizable color themes with smooth animations and easy integration.

**TR:** FiveM sunucuları için optimize edilmiş modern ve şık mermi temalı progress bar scripti. Yumuşak animasyonlar ve kolay entegrasyon ile 14 özelleştirilebilir renk teması sunar.

---

## ✨ Features / Özellikler

- 🎨 **14 Color Themes** / **14 Renk Teması**
- 🔫 **Bullet Animation Design** / **Mermi Animasyonlu Tasarım**
- ⌨️ **Cancellable with X Key** / **X Tuşu ile İptal Edilebilir**
- 🚀 **Easy Integration** / **Kolay Entegrasyon**
- 📱 **Responsive Design** / **Responsive Tasarım**
- ⚡ **Lightweight & Optimized** / **Hafif ve Optimize**
- 🎯 **Export Functions** / **Export Fonksiyonları**

---

## 📦 Installation / Kurulum

### English

1. Download the latest release
2. Extract `Tenny-Progresbar` folder to your `resources` directory
3. Add to your `server.cfg`:
```lua
ensure Tenny-Progresbar
```
4. Restart your server

### Türkçe

1. Son sürümü indirin
2. `Tenny-Progresbar` klasörünü `resources` dizinine çıkarın
3. `server.cfg` dosyanıza ekleyin:
```lua
ensure Tenny-Progresbar
```
4. Sunucunuzu yeniden başlatın

---

## 🎮 Usage / Kullanım

### Basic Usage / Basit Kullanım

```lua
exports['Tenny-Progresbar']:StartProgress(5000, "Loading...", function()
    print("Completed!")
end)
```

### Advanced Usage / Gelişmiş Kullanım

```lua
exports['Tenny-Progresbar']:StartProgress(
    5000,                    -- Duration in ms / Süre (milisaniye)
    "Processing...",         -- Display text / Gösterilecek metin
    function()               -- On finish callback / Tamamlanma fonksiyonu
        print("Success!")
        -- Your code here / Kodunuz buraya
    end,
    function()               -- On cancel callback / İptal fonksiyonu
        print("Cancelled!")
        -- Your code here / Kodunuz buraya
    end,
    'pink'                   -- Theme (optional) / Tema (opsiyonel)
)
```

### Stop Progress Manually / Manuel Durdurma

```lua
exports['Tenny-Progresbar']:StopProgress()
```

---

## 🎨 Available Themes / Mevcut Temalar

<table>
<tr>
<td><code>default</code> - Green / Yeşil</td>
<td><code>pink</code> - Pink / Pembe</td>
<td><code>blue</code> - Blue / Mavi</td>
</tr>
<tr>
<td><code>cyan</code> - Cyan / Cyan</td>
<td><code>purple</code> - Purple / Mor</td>
<td><code>white</code> - White / Beyaz</td>
</tr>
<tr>
<td><code>red</code> - Red / Kırmızı</td>
<td><code>orange</code> - Orange / Turuncu</td>
<td><code>yellow</code> - Yellow / Sarı</td>
</tr>
<tr>
<td><code>lime</code> - Lime / Lime Yeşil</td>
<td><code>indigo</code> - Indigo / İndigo</td>
<td><code>gray</code> - Gray / Gri</td>
</tr>
<tr>
<td><code>gold</code> - Gold / Altın</td>
<td><code>silver</code> - Silver / Gümüş</td>
<td></td>
</tr>
</table>

---

## 🧪 Test Commands / Test Komutları

| Command / Komut | Description / Açıklama |
|-----------------|------------------------|
| `/testprogress` | Default theme test / Varsayılan tema testi |
| `/testpink` | Pink theme test / Pembe tema testi |
| `/testblue` | Blue theme test / Mavi tema testi |
| `/testcyan` | Cyan theme test / Cyan tema testi |
| `/testpurple` | Purple theme test / Mor tema testi |
| `/testred` | Red theme test / Kırmızı tema testi |
| `/testorangetheme` | Orange theme test / Turuncu tema testi |
| `/testyellow` | Yellow theme test / Sarı tema testi |
| `/testlime` | Lime theme test / Lime tema testi |
| `/testindigo` | Indigo theme test / İndigo tema testi |
| `/testgray` | Gray theme test / Gri tema testi |
| `/testgold` | Gold theme test / Altın tema testi |
| `/testsilver` | Silver theme test / Gümüş tema testi |

---

## 📝 API Reference / API Referansı

### StartProgress

```lua
exports['Tenny-Progresbar']:StartProgress(duration, text, onFinish, onCancel, theme)
```

| Parameter / Parametre | Type / Tip | Required / Gerekli | Description / Açıklama |
|-----------|------|----------|-------------|
| `duration` | `number` | ✅ Yes / Evet | Duration in milliseconds / Süre (milisaniye) |
| `text` | `string` | ❌ No / Hayır | Text to display / Gösterilecek metin |
| `onFinish` | `function` | ❌ No / Hayır | Callback when completed / Tamamlandığında çalışacak fonksiyon |
| `onCancel` | `function` | ❌ No / Hayır | Callback when cancelled / İptal edildiğinde çalışacak fonksiyon |
| `theme` | `string` | ❌ No / Hayır | Color theme / Renk teması |

**Returns / Döndürür:** `boolean` - Success status / Başarı durumu

### StopProgress

```lua
exports['Tenny-Progresbar']:StopProgress()
```

**Returns / Döndürür:** `boolean` - Success status / Başarı durumu

---

## ⚙️ Configuration / Yapılandırma

Edit `config.lua` to customize default settings / Varsayılan ayarları özelleştirmek için `config.lua` dosyasını düzenleyin:

```lua
Config = {}

-- Available themes / Mevcut temalar
Config.Themes = {
    'default', 'pink', 'blue', 'cyan', 'purple', 'white',
    'red', 'orange', 'yellow', 'lime', 'indigo', 'gray',
    'gold', 'silver'
}

-- Default theme / Varsayılan tema
Config.DefaultTheme = 'default'
```

---

## 💡 Examples / Örnekler

### Example 1: Harvesting / Toplama İşlemi

```lua
-- Weed harvesting / Kenevir toplama
exports['Tenny-Progresbar']:StartProgress(10000, "Harvesting Weed...", function()
    -- Give item to player / Oyuncuya item ver
    TriggerEvent('inventory:addItem', 'weed', 1)
end, function()
    -- Cancelled / İptal edildi
    TriggerEvent('chat:addMessage', { args = { 'Harvesting cancelled!' } })
end, 'lime')
```

### Example 2: Lockpicking / Kilit Açma

```lua
-- Lockpicking a vehicle / Araç kilidi açma
exports['Tenny-Progresbar']:StartProgress(8000, "Lockpicking...", function()
    -- Unlock vehicle / Aracı aç
    SetVehicleDoorsLocked(vehicle, 1)
end, function()
    -- Failed / Başarısız
    TriggerEvent('chat:addMessage', { args = { 'Lockpicking failed!' } })
end, 'red')
```

### Example 3: Crafting / Üretim

```lua
-- Crafting item / Item üretimi
exports['Tenny-Progresbar']:StartProgress(15000, "Crafting...", function()
    -- Give crafted item / Üretilen item'i ver
    TriggerEvent('inventory:addItem', 'weapon_pistol', 1)
end, nil, 'gold')
```

---

## 📌 Notes / Notlar

**EN:**
- Press **X** key to cancel the progress bar
- Only one progress bar can be active at a time
- Progress bar automatically disables player controls
- Default theme is green
- Compatible with all major frameworks (QBCore, ESX, etc.)

**TR:**
- Progress bar'ı iptal etmek için **X** tuşuna basın
- Aynı anda sadece bir progress bar aktif olabilir
- Progress bar otomatik olarak oyuncu kontrollerini devre dışı bırakır
- Varsayılan tema yeşildir
- Tüm büyük framework'lerle uyumludur (QBCore, ESX, vb.)


---

## 👤 Developer / Geliştirici

**Tenny** - Modern FiveM Scripts

- Discord: https://discord.gg/ZBuNKA6ZxQ

---

## 🌟 Support / Destek

**EN:** If you like this project, please give it a ⭐ on GitHub!

**TR:** Bu projeyi beğendiyseniz, lütfen GitHub'da ⭐ verin!

---

<div align="center">

### Made with ❤️ by Tenny

**[⬆ Back to Top / Başa Dön](#-tenny-progresbar)**

</div>
