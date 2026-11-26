## Ortak ajan düzeni (PROCUX)
Bu repo, Codex ve Claude için ortak çalışma düzenine tabidir. Bu dosyadaki diğer kurallarla çelişki olursa repoya özel kural geçerlidir.
- Çalışma yeri: WSL `~/code`. Her iş kendi worktree'sinde yapılır: `~/code/.worktrees/<repo>/<ajan>-<iş>`. İki ajan aynı worktree'de çalışmaz.
- Branch: Repo kendi branch düzenini tanımlıyorsa o kullanılır; tanımlamıyorsa `codex/<iş>` veya `claude/<iş>`. Varsayılan branch'e doğrudan commit atılmaz.
- Bitirme: Testler çalıştırılır, draft PR açılır. Merge ve deploy yalnızca Abdullah'ın onayıyla yapılır.
- Docker: Her worktree için `COMPOSE_PROJECT_NAME=<repo>-<worktree-adı>`. Başka projenin container'larına dokunulmaz, prune çalıştırılmaz.
- Gizli bilgiler: .env repoya girmez, gizli değerler çıktıya veya loga yazılmaz.
- Komutlar:
  - setup — TANIMSIZ
  - test — TANIMSIZ
  - lint — TANIMSIZ
