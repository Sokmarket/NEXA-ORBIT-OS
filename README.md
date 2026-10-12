# NEXA ORBIT OS — Virtual Phone & Network Lab

**Sürüm:** 1.0.0  
**Tür:** GitHub Pages üzerinde yayınlanabilen, tek sayfalı çevrimdışı öncelikli PWA.

NEXA ORBIT; iOS'un sade etkileşim yaklaşımı ve Android/One UI'ın kişiselleştirme esnekliğinden ilham alan **özgün bir arayüzdür**. Apple veya Samsung'un resmî ürünü değildir.

## Özellikler
- Mobil öncelikli, responsive ana ekran; tema, vurgu rengi, saat biçimi ve hareket azaltma.
- Telefon tuş takımı ve arama akışı simülasyonu.
- Yerel mesaj kutusu ve sanal kişi defteri.
- SIM/sinyal/uçak modu durumlarının sanal operatör simülatörü.
- Güvenli, sabit izin listeli sanal terminal ve başlangıç AppSec senaryoları.
- JSON yedeği dışa/içe aktarma; yerel veri yönetimi.
- Service Worker ile temel uygulama dosyaları için çevrimdışı önbellek.
- GitHub Actions ile GitHub Pages dağıtımı.

## Gerçeklik ve güvenlik sınırları
Bu sürüm **gerçek telekom operatörü değildir**. Gerçek telefon numarası tahsis etmez; SIM/eSIM, baz istasyonu, mobil veri, telefon araması, SMS, WhatsApp doğrulaması veya Android sistem yetkisi sağlamaz. Şebeke ve arama ekranları yerel simülasyondur. Gerçek operatör işlevi için telekom sağlayıcısı, uygun yasal yetkilendirme, backend, kimlik doğrulama, webhook doğrulaması ve kötüye kullanım kontrolleri gerekir.

Terminal sadece sabit izin listesinde tanımlı komutları işler; işletim sistemi kabuğuna erişmez. Güvenlik alıştırmaları yerel ve zararsızdır; harici hedeflere tarama yapmaz. Bu, Android ROM'u veya native APK değildir.

## Çalıştırma — Termux
```sh
pkg update -y
pkg install -y python
unzip NEXA-ORBIT-OS-v1.0.0.zip
cd NEXA-ORBIT-OS
python -m http.server 8080 --bind 127.0.0.1
```
Ardından `http://127.0.0.1:8080` adresini açın. Service Worker için `localhost` veya HTTPS gerekir.

## GitHub Pages ile yayınlama
1. ZIP içeriğini bir GitHub deposunun kök dizinine çıkarıp dosyaları yükleyin.
2. `Settings → Pages → Build and deployment → Source` bölümünde **GitHub Actions** seçin.
3. `main` dalına push yaptığınızda `.github/workflows/pages.yml` statik siteyi yayınlar.
4. Uygulama kök dizinde bulunduğu için göreli yollar (`./manifest.json`, `./sw.js`) depo/Pages yolu ile uyumludur.

## Test
`tests/QA_CHECKLIST.md` manuel kontrol listesidir. Otomatik tarayıcı testi yapılmış olduğu anlamına gelmez.
