# <PROJE> Deploy Ritüeli — DOĞRULANMIŞ operasyonel gerçekler

> Bu belge varsayım değil, canlıda kanıtlanmış davranışları yazar (doğrulama tarihleri parantezde).
> Doğrulanmamış iddia YAZILMAZ; bilinmiyorsa "doğrulanmadı" denir.

## Topoloji

| Yüzey | Nerede | Kaynak |
|---|---|---|
| <www/frontend> | <Vercel/…> | <dal> |
| <api/backend> | <Railway/Coolify/…> | <dal> |

## 🔴 Tuzaklar (her biri tarih + kanıtla)

- **<tuzak adı> (YYYY-MM-DD kanıtlı):** <davranış + kanıt + ritüel/çare>
  - Örnekler (kardeş repolardan): "Vercel'de main push ≠ otomatik prod — READY deployment'ı manuel promote et" (procux) · "auto-merge label'lı PR ~30sn'de insansız merge olur — insan kararı isteyen PR DRAFT açılır" (aircux)

## DB / Migration

- <alembic head durumu / staging özelliği / bilinen açıklar>

## Merge → deploy zinciri (özet ritüel)

1. Dal → PR → (kritik dilimse çok-eksen review) → merge kapısı.
2. Merge → <deploy tetikleme adımı — otomatik mi, insan kararı mı?>.
3. Canlı doğrulama: <health endpoint + değişen akışın tek uçtan-uca provası>.
4. Deploy iddiası ancak 3. adımdan sonra "canlıda" diye raporlanır.
