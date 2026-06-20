# 🔬 Regex Playground

Regex desenlerini yazarken eşleşmeleri **canlı olarak** test metni
üzerinde renklendiren, tek dosyalık bir tarayıcı uygulaması. Kurulum
gerektirmez — `index.html`'i açmanız yeterli.


## Özellikler

- 🎨 Eşleşmeleri test metninde anlık renklendirme (her eşleşme farklı renk)
- 🧬 **Desen anatomisi**: Yazdığınız regex'te hangi özel karakterlerin
  (`\d`, `\w`, `(...)`, `^`, `$` vb.) kullanıldığını ve ne işe yaradığını
  otomatik tespit edip gösterir
- 🚩 Tıklanabilir flag'ler (`g`, `i`, `m`, `s`) — her birinin ne işe
  yaradığı tooltip olarak görünür
- 📋 Yakalama grupları ve isimli gruplar (`(?<ad>...)`) için ayrı gösterim
- 📍 Her eşleşmenin metindeki konumu (index)
- 📚 Tıklanabilir hazır desen örnekleri (telefon, hex renk, URL, vb.)
- ⚠️ Geçersiz regex yazıldığında anlık hata mesajı (sayfa çökmez)

## Kullanım

Kurulum gerekmez:

```bash
# Doğrudan tarayıcıda aç
open index.html        # macOS
xdg-open index.html     # Linux

# Veya basit bir yerel sunucu ile
python3 -m http.server 8000
# sonra http://localhost:8000 adresine gidin
```

1. Üstteki kutuya regex deseninizi yazın (örn. `\d{3}-\d{4}`)
2. Altındaki metin kutusuna test etmek istediğiniz metni yazın
3. Eşleşmeler anında metinde renklenir, altta liste olarak görünür
4. Sağ üstteki `g`, `i`, `m`, `s` butonlarına tıklayarak flag'leri açıp kapatabilirsiniz

## Neden bu araç?

Çoğu regex test sitesi reklam, hesap oluşturma veya internet bağlantısı
gerektirir. Bu araç tamamen **tek bir HTML dosyası** — internet
bağlantısı, build aracı veya `npm install` olmadan, dosyayı kopyalayıp
herhangi bir tarayıcıda açarak kullanabilirsiniz.

## Teknik notlar

- Saf JavaScript (framework yok), tek dosyada HTML + CSS + JS
- `RegExp.prototype.matchAll()` kullanılarak tüm eşleşmeler ve gruplar yakalanır
- Vurgulama, metnin üstüne yarı saydam bir katman (`<mark>` etiketleri
  ile) bindirilerek yapılır — bu sayede textarea'nın normal davranışı
  (seçim, imleç, kaydırma) korunur

## Lisans

MIT
