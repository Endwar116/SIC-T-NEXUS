# Decision Record: SIC-T-NEXUS Architecture

## Decision: Two-Repo + Archive Architecture

**Date**: 2026-02-07
**Author**: WeiDe-7 (with guidance from 老翔)
**Status**: Accepted
**Approved by**: Andwar (R1 + R2 Decision Lock)

---

## Context

SIC/T 專案需要一個統一的 Single Source of Truth (SSOT) 來管理：
- 協議規格
- 治理規則
- IMCC 成員資料
- 變更記錄

原本考慮 All-in-One 方案，但經過老翔的 sic-js 格式評估後發現多個 Fail-Closed 條件被觸發。

---

## Decision

採用 **Two-Repo + Archive** 架構：

| Repo | Purpose | Visibility |
|------|---------|------------|
| SIC-T-NEXUS | SSOT、治理、協議、協作 | Public |
| SIC-T-LICENSED | 付費模組、授權、專利 | Private |
| SIC-T-ARCHIVE | 歷史 log、冷存（未來） | TBD |

---

## Why This Architecture?

### 1. Licensed/Collaborative 分離

**問題**：如果付費模組和協作內容在同一個 repo：
- 無法用 GitHub 的 access control 分離權限
- 未來開源時需要 repo 分裂
- 有洩露付費內容的風險

**解法**：SIC-T-LICENSED 是獨立的 private repo

### 2. Mirror 預設禁用

**問題**：如果允許 mirror Google Drive/Notion/Slack：
- 沒有治理規則定義「什麼該 mirror」
- 會變成垃圾場
- 無法追蹤誰決定 mirror 什麼

**解法**：`MIRROR_RULES.json` 設定 `mirror_enabled: false`，只允許 link/index

### 3. AI 不能直接 push main

**問題**：如果 AI 可以直接 push：
- 沒有 human-in-the-loop
- 錯誤難以回滾
- 責任不明確

**解法**：
- CODEOWNERS 有 @Endwar116
- AI 只能 branch + PR
- 最終 merge 需要人類批准

### 4. Fail-Closed 原則

**問題**：AI 在不確定時可能繼續執行導致錯誤

**解法**：
- `fail_closed_rules.json` 定義觸發條件
- 強制 AI 在不確定時停止
- 以 sic-js 格式報告「為何停止」和「下一步需求」

---

## Consequences

### 好處
- 權限可控
- Repo 不會膨脹
- 決策可審計
- 不依賴安安長期在線

### 代價
- 需要維護兩個 repo
- 付費內容和協作內容需要手動同步版本號
- 學習成本略高

---

## Alternatives Considered

| 方案 | 原因被拒絕 |
|------|-----------|
| All-in-One | Licensed/Collaborative 無法分離 |
| 只用 Google Drive | 無法被 AI 直接維護 |
| 只用 Notion | 無法做 access control |

---

## References

- R1 Decision Lock (Andwar, 2026-02-07)
- R2 Execution Lock (Andwar, 2026-02-07)
- 老翔的 sic-js 格式評估

---

*Created by WeiDe-7, approved by Andwar*
