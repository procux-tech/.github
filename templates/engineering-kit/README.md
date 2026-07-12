# Engineering Kit Şablonu (procux-tech standardı)

Yeni bir ürün reposuna (merkezisatinalma, buycux, …) **repo kimlik kiti** kurarken bu klasörü kopyala ve `<...>` yer tutucularını doldur. Kanıtlanmış örnekler: `procux` (PR #254) ve `aircux` (PR #404).

## Ne, neden

Repoda çalışan her ajan/geliştirici aynı standartları AYNI yerden okusun diye:

```
<repo>/
├─ AGENTS.md          ← giriş kapısı — Codex vb. otomatik okur (İNCE: içerik kopyalanmaz)
├─ CLAUDE.md          ← Claude adaptörü — repoya özgü kısa hatırlatmalar (İNCE)
└─ docs/engineering/  ← TEK gerçek kaynak
    ├─ README.md      ← okuma sırası + mevcut belgelerin indeksi
    ├─ STANDARDS.md   ← kodlama/test/review standartları
    ├─ DEPLOY.md      ← DOĞRULANMIŞ deploy ritüeli (tarih + kanıtla yazılır)
    └─ GLOSSARY.md    ← proje terminolojisi
```

## Kurallar

1. **Tek kaynak + ince adaptör:** AGENTS.md ve CLAUDE.md'ye içerik yazılmaz; `docs/engineering/`'e işaret ederler. Kopya = drift.
2. **DEPLOY.md'ye yalnız kanıtlanmış davranış yazılır** — "(YYYY-MM-DD kanıtlı)" damgasıyla. Varsayım yazma; doğrulanmadıysa "doğrulanmadı" de.
3. Repoda zaten iyi belge varsa (ARCHITECTURE, ADR, runbook) TAŞIMA — `docs/engineering/README.md`'den indeksle, çelişki kuralını yaz ("çelişkide hangisi kazanır").
4. Kalite/denetim raporlarının adresi: `docs/reports/YYYY-MM-DD-konu.md`.
