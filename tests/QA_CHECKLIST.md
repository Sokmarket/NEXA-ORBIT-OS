# NEXA ORBIT OS — QA Checklist

## Responsive / erişilebilirlik
- [ ] 320, 360, 390, 430 ve 560 px genişlikte yatay taşma yok.
- [ ] Android Chrome ve masaüstü tarayıcıda okunabilir metin/odak durumu.
- [ ] Koyu/açık/sistem teması ve vurgu rengi yenileme sonrasında korunuyor.
- [ ] Hareket azaltma tercihi çalışıyor.

## Modüller
- [ ] Ana ekran, Uygulamalar, Şebeke ve Ayarlar navigasyonu.
- [ ] Uygulama araması filtreleme.
- [ ] Sanal tuş takımı, silme ve arama simülasyonu.
- [ ] Mesaj ekleme, sayfa yenileme sonrası yerel kayıt, silme.
- [ ] Kişi ekleme/silme ve yerel kayıt.
- [ ] SIM, sinyal ve uçak modu ayarlarının uygulanması.
- [ ] Terminal: help/date/status/apps/network/version; bilinmeyen komut reddedilir.
- [ ] Güvenlik senaryoları yerel açıklama gösterir.
- [ ] JSON dışa/içe aktarma ve bozuk yedek reddi.
- [ ] Yerel verileri sıfırlama onayı.

## PWA / dağıtım
- [ ] HTTPS/localhost üzerinde manifest ve Service Worker kaydı.
- [ ] İlk açılıştan sonra uçak modunda temel uygulama kabuğu açılıyor.
- [ ] GitHub Pages Actions dağıtımı başarılı.
- [ ] Depo alt yolu altında manifest ve service worker göreli yolları çalışıyor.

## Dürüstlük / güvenlik
- [ ] UI gerçek SIM/arama/SMS veya gerçek operatör bağlantısı iddia etmiyor.
- [ ] Terminalde `eval`, shell, ağ tarama veya keyfî komut çalıştırma yok.
- [ ] Mesaj ve kişiler yalnızca tarayıcının yerel depolamasında.
