# <PROJE> Mühendislik Standartları

> Kısa ve bağlayıcı. Mimari bağlam için <ARCHITECTURE belgesi>; deploy için `DEPLOY.md`.

## Yeniden-kullanım (en kritik kural)

Yeni servis/komponent/endpoint yazmadan önce:

1. Mevcut olanı ara.
2. Varsa **bağla/genişlet**; kopyalama.
3. Gerçekten yoksa, en yakın mevcut desenin dosya düzenini ve isimlendirmesini birebir izle.

## Backend (<framework + ORM>)

- <async/sync disiplini, tek-Base benzeri kırmızı çizgiler, katman sınırları, auth zinciri, migration kuralları, hata yönetimi>

## Frontend (<framework>)

- <TS strict, veri çekme deseni, stil sistemi, hata izleme, para birimi/i18n kuralları>

## Test

- <test araçları + hangi dilim testsiz merge edilemez>

## Dürüstlük ve gizlilik (müşteri-yüzlü yüzeyler)

- Uydurma metrik, testimonial, logo, vaka yazılmaz.
- Pazarlama/ürün arayüzü/operatör yüzeylerinde iç kütüphane/OSS/stack/sağlayıcı adı geçmez — yalnız yetenek-düzeyi dil. İstisna: hukuki/uyum metinleri.

## Güvenlik / secrets

- Canlı credential dosyaya/commit'e/log'a YAZILMAZ (pointer yaz). Commit öncesi staged diff'te secret taraması.
- `git add .` yasak — açık yol ile stage.

## Dal / commit / review

- Dallar: `feat/*` `fix/*` (üretim) · `chore/quality-*` `docs/*` (kalite/bakım). Worktree'de çalış, merge'de kapat.
- Commit: conventional (`feat(scope): özet`); araç/otomasyon imzası eklenmez.
- Review kapıları: para/ödeme · authn/authz · DB/migration · güvenlik → çok-eksen review + statik tarama zorunlu.
- Kalite raporları `docs/reports/` altına tarihli (`YYYY-MM-DD-konu.md`).
