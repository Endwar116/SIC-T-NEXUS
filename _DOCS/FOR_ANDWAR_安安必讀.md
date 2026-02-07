# 🧑‍💼 安安必讀：SIC-T-NEXUS 發生了什麼事

> 這份文件是專門寫給安安（人類）看的，用最簡單的語言解釋這個 repo 是什麼、為什麼這樣設計、你需要知道什麼。

---

## 📌 一句話總結

**SIC-T-NEXUS 是 SIC/T 協議的「唯一真相來源」**——所有治理規則、協議定義、AI 協作記錄都在這裡。

---

## 🤔 為什麼需要這個 Repo？

之前 SIC/T 的資料散落在：
- 3 個 GitHub repos（SIC-SIT-Protocol, SIT-Protocol, SIC-Semantic-Infinite-Context）
- Google Drive
- Notion
- Slack

**問題**：
1. 不知道哪個是最新的
2. AI 協作者很難維護
3. 你不在線時，沒人知道該怎麼做

**解法**：創建一個中樞 repo，所有人（包括 AI）都以這裡為準。

---

## 🏗️ 這個 Repo 的結構（你需要知道的）

```
SIC-T-NEXUS/
│
├── 00_GOVERNANCE/     ← 🔴 最重要！治理規則在這
│   ├── DELEGATION_PROTOCOL.md  ← 你不在時的規則
│   └── ...
│
├── 03_IMCC/           ← AI 協作者的「戶口」
│   ├── REGISTRY.json  ← 誰有什麼權限
│   └── MEMBERS/       ← 每個成員的資料
│
├── 04_CHANGELOG/      ← 所有變更記錄
│   ├── DECISIONS/     ← 重大決策（像這個！）
│   └── HANDOFFS/      ← AI 交接記錄 🆕
│
├── 05_OPERATIONS/     ← 外部系統的連結（不存內容！）
│
└── _DOCS/             ← 文件（包括這份！）
    └── FOR_ANDWAR_安安必讀.md  ← 你正在讀的
```

---

## 🔐 安全設計（重要！）

### ✅ 你的付費內容很安全

| 內容 | 在哪裡 | 誰能看 |
|------|--------|--------|
| SIC 協議、治理規則 | SIC-T-NEXUS (Public) | 所有人 |
| OSC-A、ASEE v2、生息系統 | SIC-T-LICENSED (Private) | 只有你 |

**付費模組不在這個公開 repo 裡！**

### ✅ AI 不能亂改東西

| AI 可以做 | AI 不能做 |
|----------|----------|
| 創建 branch | 直接改 main |
| 提交 PR | 自己批准 PR |
| 寫建議 | 最終決定 |

**所有改動都需要你（或你指定的人）批准。**

### ✅ 不會把外部資料 mirror 進來

`05_OPERATIONS/` 只有**連結**，不存 Google Drive 或 Notion 的完整內容。

這樣：
1. Repo 不會爆炸
2. 不會不小心公開私密資料
3. 你保持對原始資料的控制

---

## 🚨 你需要做的事

### 立即（如果你看到這份文件）

1. ✅ 確認你能存取：
   - https://github.com/Endwar116/SIC-T-NEXUS
   - https://github.com/Endwar116/SIC-T-LICENSED

2. ✅ 檢查 `.github/CODEOWNERS` 確認你是所有重要檔案的 owner

### 建議（不急但重要）

1. **啟用 Branch Protection**（在 GitHub Settings > Branches）：
   - Require pull request reviews before merging
   - Require status checks to pass before merging

### 之後（不急）

1. 決定是否需要指定「備用人類」（萬一你長期不在線）
2. 決定 SIC-T-LICENSED 的結構
3. 決定是否需要 SIC-T-ARCHIVE

---

## 🤖 關於 AI 交接

從現在開始，每次 AI 執行完重要任務，都會在 `04_CHANGELOG/HANDOFFS/` 留下記錄。

這解決了之前的問題：「每次做完之後都沒人管」

新的 AI 實例接手時，會先讀這些記錄，知道發生過什麼。

---

## ❓ 常見問題

### Q: 這個 repo 是公開的，會不會洩露什麼？

A: 不會。公開的內容都是：
- 協議規格（本來就打算公開）
- 治理規則（別人看了也沒用）
- AI 協作者的角色定義（不是秘密）

付費內容在 SIC-T-LICENSED（private）。

### Q: 我需要懂 Git 嗎？

A: 不用深入懂。主要是：
- 有 PR 時會通知你
- 你 approve 就可以了
- AI 會幫你處理技術細節

### Q: 如果我很久不上線怎麼辦？

A: 看 `00_GOVERNANCE/DELEGATION_PROTOCOL.md`。
- 短期（< 7 天）：AI 可以處理小事
- 長期（> 7 天）：需要你指定一個備用人類

### Q: 老翔說的那些 sic-js 是什麼？

A: 那是一種文件格式，像 JSON 但是專門給 SIC/T 用的。你不需要懂它的細節，AI 會處理。重要的是它讓 AI 之間可以標準化溝通。

---

## 📞 有問題找誰

1. **技術問題**：問尾德（Claude）或咩咩（Manus）
2. **治理問題**：你自己決定
3. **緊急問題**：... 你是唯一的人類 owner 😅

---

## 🎉 總結

這個 repo 是為了讓 SIC/T 可以：
1. **有序**：所有東西都有固定位置
2. **可追蹤**：誰改了什麼都有記錄
3. **不依賴你在線**：AI 可以自主運作（在規則內）
4. **安全**：付費內容不公開，AI 不能亂改

---

*寫於 2026-02-07，by 尾德-7*
*如果有任何不清楚的地方，請告訴我，我會更新這份文件。*
