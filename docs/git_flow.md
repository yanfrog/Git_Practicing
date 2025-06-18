# Git Flow 圖解

Git Flow 是一種常見的 Git 分支管理策略，適合多人開發、版本控管的情境。

---

## 分支角色簡介

| 分支 | 作用 | 說明 |
|------|------|------|
| `main` / `master` | 穩定主線 | 僅放正式發布版本 |
| `develop` | 開發主線 | 所有新功能從這裡分出 |
| `feature/*` | 新功能開發 | 每個功能有獨立分支 |
| `release/*` | 發佈準備 | 測試、修復 bug |
| `hotfix/*` | 緊急修復 | 緊急修補正式版的 bug |

---

## Git Flow 圖解

```text
main ────────────────●───────────────●───────────────▶
                     ▲               ▲
                   merge           merge
                     │               │
hotfix/fix1 ─────────●               ●───▶

develop ──●─────────●─────────●─────────●─────────▶
          │         │         │         │
        merge     merge     merge     merge
          ▼         ▼         ▼         ▼
    feature/a  feature/b  feature/c  feature/d

（中間可穿插 release/*）
