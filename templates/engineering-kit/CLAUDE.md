# <PROJE> — repo çalışma notu

ÖNCE `AGENTS.md`'yi ve oradaki okuma sırasını uygula (`docs/engineering/` = tek kaynak). Bu dosya yalnız bu depoya özgü kısa hatırlatmalardır:

- **Deploy ezber bozar:** <en tehlikeli 1-2 deploy tuzağının tek cümlelik özeti>. Ayrıntı ve doğrulama komutları: `docs/engineering/DEPLOY.md`.
- **Kod okumadan önce:** `.understand-anything/knowledge-graph.json` varsa oradan başla; yapı/impact + sembol işi **CodeGraph** (Serena 2026-08-09'da silindi).
- **Kritik dilim** (para/auth/DB/güvenlik) → merge öncesi risk-review + semgrep; migration staging-first + insan onayı.
- Worktree: `C:\Users\MONSTER\Desktop\procux-umbrella\worktrees\<proje>\<dal>` altında aç; merge'de kapat.
- Workspace bağlamı ve proje portföyü: `C:\Users\MONSTER\Desktop\procux-umbrella\HOME.md`.
