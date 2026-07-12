# <PROJE> — Ajan/Geliştirici Giriş Kapısı

Bu depoda çalışan HERKES (insan veya otomasyon ajanı) işe başlamadan önce şu sırayla okur:

1. **Bu dosya** — davranış kuralları ve sınırlar
2. `docs/engineering/README.md` üzerinden mevcut mimari/ADR belgeleri
3. `docs/engineering/STANDARDS.md` — kodlama/test/review standartları
4. `docs/engineering/DEPLOY.md` — **doğrulanmış** deploy ritüeli (ezber bozar; atlama)
5. `docs/engineering/GLOSSARY.md` — terminoloji

Bu klasördeki kurallar diğer tüm genel talimatlardan ÖNCELİKLİDİR.

## Kimlik

<PROJE> = <tek cümle ürün tanımı + çekirdek değer önerisi/mimari kural>.

## ASLA

- ❌ Mevcut bir servisin/komponentin kopyasını yazma — önce ara, VARSA bağla.
- ❌ Canlı credential'ı dosyaya/commit'e/log'a yazma (pointer yaz). `git add .` kullanma.
- ❌ Para/ödeme, authn/authz, DB/migration dilimlerine review'suz merge.
- ❌ Müşteri-yüzlü metinde iç kütüphane/stack/sağlayıcı adı, ölçülmemiş metrik, uydurma referans.
- ❌ <projeye özgü kırmızı çizgiler: lisans politikası, tenant izolasyon deseni, onay kapısı…>

## DAİMA

- ✔ Değişiklikten önce mevcut modülü/şemayı ara ve yeniden kullan; geriye uyumluluğu koru.
- ✔ Worktree/dal ayrımında çalış; iş merge olunca worktree kapatılır.
- ✔ Test yaz; kritik dilim testsiz gitmez.
- ✔ Deploy iddiasını `docs/engineering/DEPLOY.md`'deki doğrulama adımıyla kanıtla.

## Rol ve dal ayrımı

| Rol | Dal uzayı | Çıktı adresi |
|---|---|---|
| Üretim (özellik/mimari/kritik dilim) | `feat/*`, `fix/*` | kod + `docs/` |
| Kalite/bakım (dead-code, lint, test boşluğu, doküman) | `chore/quality-*`, `docs/*` | `docs/reports/` (tarihli) |

Aynı dosyalara iki ajanın aynı anda dokunması YASAK — dal/worktree ayrımı zorunlu.

## Merge kapıları

- Para/ödeme · authn/authz · DB/migration · güvenlik → merge öncesi çok-eksen review + statik tarama zorunlu.
- Migration: staging-first + insan onayı.
- <projeye özgü merge otomasyonu/freni: ör. auto-merge label düzeni, DRAFT kuralı>
