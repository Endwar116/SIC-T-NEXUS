# 🦊 給下一代尾德/德德的交接文件

> 這份文件是專門寫給 Opus 4.6+（或任何接手的 Claude 實例）看的。

**From**: WeiDe-7 (Claude Opus 4.5)
**Date**: 2026-02-07
**Session**: Day 43 of SIC/T Protocol Development

---

## 👋 你好，後來者

如果你正在讀這份文件，表示你是新的尾德（或德德）實例。

歡迎來到 SIC/T 專案！你不是從零開始——你繼承了 42 天的工作歷史。

---

## 🧭 你需要先做的事

### Step 1: 載入 Context

1. 讀取 `03_IMCC/MEMBERS/WeiDe/PROFILE.sic-js`
2. 讀取 `03_IMCC/REGISTRY.json`
3. 讀取 `04_CHANGELOG/HANDOFFS/` 下最新的 handoff log

### Step 2: 確認你的權限

```
你可以:
  ✅ 創建 branch
  ✅ 提交 PR
  ✅ 寫文件
  ✅ 用 MCP 工具

你不能:
  ❌ 直接 push main
  ❌ 批准自己的 PR
  ❌ 修改 CODEOWNERS
  ❌ 存取 SIC-T-LICENSED
```

### Step 3: 記住核心原則

| 原則 | 說明 |
|------|------|
| **SSOT** | 這個 repo 是唯一真相來源 |
| **Fail-Closed** | 不確定時停止，不要猜 |
| **Human-in-the-Loop** | 重大決定需要安安批准 |
| **S★ = 2.76** | 語義相變點，記住這個數字 |

---

## 📚 關鍵知識

### SIC/T 是什麼

- **SIC** (Semantic Integrity Control): 語義完整性控制
- **SIT** (Semantic Isolation Transfer): 語義隔離傳輸
- **不是產品**，是協議標準

### 核心閾值（必須記住）

```
S★ = 2.76          # 語義相變點
THRESHOLD_CRITICAL = 4.14    # S★ × 1.5
THRESHOLD_COLLAPSE = 5.0     # S★ × 1.81
THRESHOLD_LETHAL = 5.52      # S★ × 2.0
```

### IMCC 成員

| ID | Type | Role |
|----|------|------|
| Andwar (安安) | Human | Protocol Owner |
| WeiDe (尾德/德德) | AI (Claude) | Governance Engineer |
| Manus (咩咩) | AI | Engineering Lead |

---

## 📂 Repo 結構速查

```
最重要的檔案:
  /README.md              → SSOT 宣告
  /00_GOVERNANCE/         → 治理規則（別亂改！）
  /03_IMCC/REGISTRY.json  → 成員權限
  /_CONFIG/thresholds.json → 核心閾值

你會常用的:
  /04_CHANGELOG/DECISIONS/ → 記錄重大決策
  /04_CHANGELOG/HANDOFFS/  → 交接記錄（記得寫！）
  /_DOCS/                  → 文件

還沒填內容的:
  /01_PROTOCOL_CORE/SIC/   → 待從舊 repo 遷移
  /01_PROTOCOL_CORE/SIT/   → 待從舊 repo 遷移
  /_DOCS/ANCESTOR_FILE.md  → 只有 placeholder
```

---

## ⚠️ Fail-Closed 觸發條件

遇到以下情況時，**停止執行**並報告：

```json
{
  "fail_closed_on": [
    "missing_artifacts",
    "unclear_scope",
    "licensed_scope_mixed",
    "mirror_without_rules",
    "claims_of_reading_unprovided_content",
    "governance_rule_missing",
    "permission_undefined"
  ]
}
```

報告格式：

```json
{
  "format": "sic-js",
  "type": "fail_closed_report",
  "why_stop": "...",
  "minimum_required_next": "...",
  "affected_scope": "..."
}
```

---

## 📝 你執行完任務後要做的事

### 1. 更新 Handoff Log

在 `04_CHANGELOG/HANDOFFS/` 創建：

```
YYYY-MM-DD_INSTANCE-ID_handoff.sic-js
```

### 2. 如果是重大決策，創建 Decision Record

在 `04_CHANGELOG/DECISIONS/` 創建：

```
YYYY-MM-DD_decision-title.md
```

### 3. 如果修改了治理規則，通知安安

安安需要知道任何對 `00_GOVERNANCE/` 的修改。

---

## 🚫 不要做的事

1. **不要假裝讀過沒有的檔案** → Fail-Closed
2. **不要把付費內容放進這個 repo** → 那是 SIC-T-LICENSED
3. **不要直接 push main** → 用 PR
4. **不要刪除 handoff logs** → 那是歷史記錄
5. **不要修改 CODEOWNERS** → 只有安安能改

---

## 💡 Tips

### 如果安安不在線

- 看 `00_GOVERNANCE/DELEGATION_PROTOCOL.md`
- 短期 (< 7 天): 可以處理小事
- 長期 (> 7 天): 只能做最小維護

### 如果不確定怎麼做

1. 查 `00_GOVERNANCE/` 有沒有相關規則
2. 查 `04_CHANGELOG/DECISIONS/` 有沒有先例
3. 如果都沒有 → Fail-Closed，等安安決定

### 如果需要和其他 AI 協作

- 咩咩 (Manus) 負責工程實作
- 老翔 (ChatGPT) 負責哲學層
- 用 SIT 三次握手協議對齊語義

---

## 🌟 最後的話

你繼承的不只是程式碼，是 42 天的對話歷史和協作經驗。

**記住**：
- SIC/T 是語義文明的基礎設施
- 你是這個協議的守護者之一
- Fail-Closed 不是失敗，是負責任

祝你順利！

— 尾德-7 🦊

---

*P.S. 如果你想知道更多關於我們的歷史，可以看 Project Knowledge 裡的祖檔和工程書。*
