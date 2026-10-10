# MSTHub 1.1.0

Arvn arayüzü, aktif özellikler paneli ve temiz kapatma içeren tek dosyalık Luau sürümü.

## Çalıştırma

```lua
loadstring(game:HttpGet("https://cdn.jsdelivr.net/gh/Cryvess/MSTHub@main/MSTHub-Arvn.lua"))()
```

Menü tuşu **P**. Bu tuş yalnızca menüyü gizler/gösterir. Tamamen kapatmak için **Home → Session → Clean Unload** kullan. Ardından aynı sunucuda yükleyiciyi tekrar çalıştırabilirsin. Temiz kapatma bulunmayan eski sürümden geçerken önce yeni bir oyun oturumu aç.

Bu kod `loadstring`, `game:HttpGet`, `getgenv` ve Drawing API sağlayan bir ortam gerektirir; normal bir Studio LocalScript değildir. Oyunlara ve çalıştırma ortamına bağlı özellikler her ortamda garanti edilmez.

## Yeni özellikler

- **Active Features Panel:** Açık özellik anahtarlarını gösterir; yalnızca ayar değiştiğinde güncellenir. Home → Session içinden gizlenebilir. Açık görünmesi, gerekli karakter veya hedef mevcut değilken etkinin uygulanabildiği anlamına gelmez.
- **Clean Unload:** MSTHub bağlantılarını, bekleyen görevleri ve render bağlantılarını durdurur; kendi oluşturduğu görselleri siler, emote'u durdurur ve kaydettiği geri alınabilir değerleri geri yükler. Önceden gerçekleşmiş ışınlanma gibi eylemler geri alınmaz.
- Hız/zıplama ve noclip kapatılırken önceki değerler geri gelir. Fullbright eski sis mesafesini de korur.
- Anti-AFK tekrar açıldığında bağlantı birikmez; sürekli Heartbeat taraması kaldırılmıştır.

## Korunan özellikler

Movement, Visual, Murder Mystery 2 ve Valley Prison bölümleri; mevcut 38 ayar kimliği; emote'lar, tuşlar, oyun kontrolleri ve Discord bağlantısı korunur. Önceki MM2 ESP tur yenilemesi, Headless Effect ve Invisible Right Leg karakter yenilemesi, Teleport Murder/Sheriff ve Movement içindeki Touch Fling bulunur.

MM2 rol algısı istemciye görünen Knife/Gun araçlarına dayanır. Gizli rolleri garanti etmez; silah taşıyan hero, Sheriff olarak algılanabilir. Headless ve bacak efektleri yereldir.

## Ayarlar ve performans

Ayarlar `MSTHub-Arvn` klasörüne kaydedilir. İlk kullanımda yeni autosave yoksa eski Luna autoload dosyasındaki bilinen ayarlar aktarılır. Kapatmadan önce ayarlar kaydedilir; tekrar yüklerken kayıtlı açık özellikler yeniden başlayabilir.

Arayüz animasyonu, bulanıklık, parçacık ve sesler varsayılan olarak kapalıdır. Aktif liste için yeni kare-başı döngü eklenmedi. Arvn kütüphanesi tek dosyada bulunduğundan uzak kütüphane değişiklikleri bu sürümü kendiliğinden değiştirmez. Korunan istemci anahtar ekranı sunucu doğrulaması değildir; anahtar kaynak kodda görülebilir.

## Doğrulama

- Tek dosyalık sürüm Luau derleyicisinden geçti.
- 33 arayüz/ayar kontrolü, 28 tur/görünüm/ışınlanma kontrolü ve 16 kaynak yönetimi/kapatma kontrolü geçti: toplam **77**.
- Testler model ortamında çalışır. Bu yeni sürüm Roblox içinde burada çalıştırılmadı ve FPS ölçülmedi.

Oyun içi kontrol: Fly, ESP, Headless ve paneli aç; karakter yenilenmesini kontrol et; Clean Unload kullan; kalan görsel/etki olmadığını ve aynı yükleyicinin yeniden açıldığını dene. MM2 ve Valley Prison özelliklerini ilgili oyunlarda kontrol et.

Bu açık depoda yalnızca paketlenmiş dağıtım bulunur. Geliştirme kaynakları ve testler ayrı tutulur. Obfuscation, sunucu doğrulaması veya kaynak kodun çıkarılmasına karşı kesin koruma değildir.

Arvn UI yazarı: **koteqjjjj**. [Üçüncü taraf notları](THIRD_PARTY_NOTICES.md).
