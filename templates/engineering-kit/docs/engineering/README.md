# docs/engineering/ — Mühendislik Tek Kaynağı

Bu klasör, bu depoda çalışan herkesin (insan veya otomasyon ajanı) uyduğu ORTAK standartların tek kaynağıdır. Kökteki `AGENTS.md` ve `CLAUDE.md` bu klasöre işaret eden ince adaptörlerdir — içerik BURADA yaşar, orada kopyalanmaz.

## Okuma sırası

1. `/AGENTS.md` — davranış kuralları, ASLA/DAİMA, rol-dal ayrımı
2. <mevcut mimari belge: ör. `/docs/ARCHITECTURE.md` — varsa taşıma, buradan indeksle>
3. `STANDARDS.md` — kodlama/test/review standartları
4. `DEPLOY.md` — **doğrulanmış** deploy ritüeli ve tuzaklar
5. `GLOSSARY.md` — terminoloji

## Komşu belgeler (mevcut, buradan indekslenir)

| Belge | Rol | Not |
|---|---|---|
| <mevcut belgeleri listele> | | **çelişkide hangisinin kazandığını yaz** |

## Bakım kuralı

- Standart değişikliği = bu klasörde PR; adaptör dosyalara içerik EKLENMEZ.
- Yeni kalıcı bilgi eklerken: doğrulanmış gerçek + tarih yaz (DEPLOY.md formatı örnek).
