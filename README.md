# P-CSO Writing Skills for Claude Code

**P-CSO**: Pinker's Cognitive Style Optimization
**Framework**: Steven Pinker's "The Sense of Style" (Chapters 4 & 5)
**Version**: 0.9.0 (Preview)
**Author**: Sau-Chin Chen

---

## 關於 P-CSO

P-CSO（Pinker's Cognitive Style Optimization）是基於認知科學原理的學術寫作優化系統，源自 Steven Pinker 的《The Sense of Style》。該系統通過減少讀者的認知負擔，提升文本的清晰度和連貫性。

### 核心原則

**句子層級優化**（第 4 章）：
- 降低工作記憶負荷
- 消除解析困難
- 提高資訊密度
- 消除歧義

**段落層級優化**（第 5 章）：
- 建立清晰的主題導向
- 確保資訊流暢性
- 維持實體追蹤一致性
- 明確邏輯連接

---

## 安裝

### 方式 1: Claude Code Marketplace（推薦）

```bash
/plugin marketplace add SCgeeker/P-CSO
/plugin install p-cso-skills
```

### 方式 2: 本地安裝

1. 克隆或下載此倉庫
2. 將整個目錄放置在你的專案中
3. Claude Code 將自動識別 `.claude-plugin/` 配置

---

## Skills 總覽

本系統包含 **6 個專業 skills**，涵蓋從草稿到定稿的完整寫作流程：

### 核心優化 Skills

#### 1. `p-cso-workflow` - 完整流程
**用途**：從研究筆記到認知優化稿件的完整管線
**包含**：組織筆記 → 生成草稿 → 句法優化 → 連貫性增強 → 診斷報告
**適用**：需要系統化優化的手稿準備
**時間**：2-4 小時（完整章節）

#### 2. `pinker-syntax` - 句法優化
**用途**：應用 Pinker 第 4 章的 6 條句法規則優化句子結構
**解決**：複雜句法、冗長表述、歧義結構、語法不一致
**適用**：句子難以理解、中心嵌入、左分支結構過多的文本
**時間**：30 分鐘

#### 3. `pinker-coherence` - 連貫性優化
**用途**：應用 Pinker 第 5 章的 7 條原則優化段落與多句流暢度
**解決**：主題模糊、過渡不清、實體追蹤混亂、邏輯隱含
**適用**：段落流暢性弱、過渡不自然的文本
**時間**：30 分鐘

#### 4. `pinker-quick` - 快速清理
**用途**：在起草階段快速反饋，應用前 3 條高影響力規則
**包含**：刪除冗詞、修復主題-評論順序、添加邏輯連接詞
**適用**：需要快速迭代、保持寫作動能的場景
**時間**：5-10 分鐘

### 輔助 Skills

#### 5. `notes-to-manuscript` - 筆記轉手稿
**用途**：將分散的研究筆記轉換為結構化手稿草稿
**強調**：AI 作為腳手架（非最終輸出），保護學術誠信
**適用**：從原始筆記開始撰寫，需要結構化組織
**時間**：1-2 小時

#### 6. `english-editing` - 學術英文編輯
**用途**：專業學術英文校對，改善清晰度、語法和風格
**包含**：冠詞使用、語法修正、標點符號、詞彙選擇、格式
**適用**：手稿最終潤色或語言精修
**時間**：15-30 分鐘

---

## 快速開始

### 從草稿開始

如果你已有文字需要改進：

```
情境 1: 需要全面優化
→ 使用 /p-cso-workflow

情境 2: 句子難以理解
→ 使用 /pinker-syntax

情境 3: 段落之間流暢性差
→ 使用 /pinker-coherence

情境 4: 正在起草，需要快速反饋
→ 使用 /pinker-quick

情境 5: 只需語法和冠詞修正
→ 使用 /english-editing
```

### 從筆記開始

如果你從研究筆記開始撰寫：

```
選項 A: 完整優化流程
→ 使用 /p-cso-workflow（包含起草階段）

選項 B: 簡單腳手架
→ 使用 /notes-to-manuscript
```

---

## 工作流程範例

### 工作流程 A：全面流程（筆記 → 發表）

**適用**：從研究筆記開始的完整手稿準備

```
步驟 1: 組織與起草
└─ 使用 /p-cso-workflow 處理你的筆記
└─ 收到組織好的焦點陳述 + 腳手架
└─ 用你自己的話重寫腳手架（關鍵！）

步驟 2: 認知優化（/p-cso-workflow 自動包含）
└─ 句法優化（第 4 章：6 條規則）
└─ 連貫性優化（第 5 章：7 條原則）
└─ 收到解釋變更的診斷報告

步驟 3: 語法潤色
└─ 使用 /english-editing
└─ 修正冠詞、語法、術語

步驟 4: 外部工具
└─ 添加引用（Zotero 等）
└─ 格式化為期刊要求
```

**預計時間**：完整手稿章節 2-4 小時

---

### 工作流程 B：迭代起草

**適用**：寫作中需要即時反饋

```
撰寫第 1 段（用你自己的話）
└─ 使用 /pinker-quick
└─ 應用快速修正
└─ 繼續

撰寫第 2 段
└─ 使用 /pinker-quick
└─ 應用快速修正
└─ 繼續

[完成章節]

全面修訂
└─ 使用 /p-cso-workflow（或 /pinker-syntax + /pinker-coherence）
└─ 審查全面優化
└─ 使用 /english-editing
```

**預計時間**：每個章節 30-60 分鐘

---

### 工作流程 C：模組化修訂

**適用**：針對特定問題的定向改進

```
診斷階段
└─ 分享有問題的文本
└─ 確定問題類型

針對性修正
├─ 句法問題 → /pinker-syntax
├─ 連貫性問題 → /pinker-coherence
├─ 兩者都有 → /p-cso-workflow
└─ 僅語法 → /english-editing

根據需要迭代
```

**預計時間**：每種問題類型 15-30 分鐘

---

### 工作流程 D：最小化（快速清理）

**適用**：時間緊迫或文本已相當完善

```
步驟 1: /pinker-quick（捕捉主要問題）
步驟 2: /english-editing（語法潤色）
步驟 3: 提交
```

**預計時間**：總計 15-30 分鐘

---

## P-CSO 原則概覽

### 第 4 章：句法優化（6 條規則）

**解決**：句子層級的解析困難

| 規則 | 問題 | 解決方案 | 範例 |
|------|------|---------|------|
| 1. 記憶負荷 | 開頭的複雜短語 | 移至句尾 | "We tested..." 而非 "The hypothesis...was tested" |
| 2. 解析崩潰 | 嵌套從句 | 拆分為簡單句 | 避免 "The X who did Y that Z designed..." |
| 3. 資訊密度 | 冗長表述 | 刪除冗餘詞彙 | "decide" 而非 "make a decision" |
| 4. 預期順序 | 新資訊在前 | 已知資訊在前 | "Results are explained by..." |
| 5. 歧義 | 花園路徑 | 添加標記、重新排序 | 恢復 "that"、"which" 如需要 |
| 6. 一致性 | 一致性錯誤 | 修復平行結構 | "both X and Y" 使用匹配結構 |

**使用 `/pinker-syntax` 處理這些問題**

---

### 第 5 章：連貫性優化（7 條原則）

**解決**：篇章層級的流暢度和邏輯

| 原則 | 問題 | 解決方案 | 範例 |
|------|------|---------|------|
| 1. 主題/要點 | 埋藏主旨 | 早期陳述主題和要點 | 開篇明確主要論點 |
| 2. 資訊流 | 斷裂的主題鏈 | 維持一致主題 | 每句連接前句 |
| 3. 實體追蹤 | 混淆的指代 | 使用定冠詞，避免同義詞 | "a task" → "the task"（不是 "the paradigm"） |
| 4. 邏輯 | 隱含關係 | 添加連接詞 | "Consequently," "However," 等 |
| 5. 比較 | 非平行結構 | 強制平行句法 | "X increased Y" / "Z increased Y" |
| 6. 抽象指代 | 重複 | 名詞化事件（第二次提及） | "verified" → "this verification" |
| 7. 元話語 | 以作者為中心的文本 | 刪除 "I will discuss" 短語 | 直接討論 |

**使用 `/pinker-coherence` 處理這些問題**

---

## 理解診斷報告

所有 P-CSO skills 提供診斷性解釋：

```markdown
### 問題 1: [具體問題]
- **認知負擔**: 這對讀者造成的困難
- **Pinker 原則**: 違反了哪條規則/原則
- **應用修正**: 改變了什麼
- **認知收益**: 這如何幫助讀者
```

**如何使用診斷**：
1. **學習模式**：注意你寫作中的重複問題
2. **應用於未來**：起草新文本時使用原則
3. **自訂**：告訴系統你的常見問題以獲得針對性幫助

---

## 最佳實踐

### 應該做的 ✅

1. **用你自己的話重寫腳手架**（學術誠信）
2. **審查所有變更的準確性**（你是內容專家）
3. **從診斷中學習**（理解認知原則）
4. **按順序使用 skills**（草稿 → P-CSO → 語法）
5. **迭代使用**（在寫作時使用 `/pinker-quick` 以獲得更好的初稿）
6. **保留專業術語**（不要為簡化犧牲精確性）

### 不應該做的 ❌

1. **不要直接複製 AI 文本**（違反學術誠信）
2. **不要忽略解釋**（你會重複問題）
3. **不要過度優化**（邊際遞減；有時足夠好就是足夠好）
4. **不要抗拒所有建議**（認知原則基於證據）
5. **不要跳過手動重寫**（如使用腳手架 skills）

---

## 快速參考表

| 任務 | 使用此 Skill | 時間 |
|------|-------------|------|
| 從筆記起草 | `/p-cso-workflow` | 2-4h |
| 快速草稿反饋 | `/pinker-quick` | 5-10min |
| 修正複雜句子 | `/pinker-syntax` | 30min |
| 修正段落流暢性 | `/pinker-coherence` | 30min |
| 最終語法潤色 | `/english-editing` | 15-30min |
| 全面綜合 | `/p-cso-workflow` + `/english-editing` | 3-5h |

---

## 與外部工具整合

### P-CSO 之前
- **文獻管理**：Zotero、Mendeley（收集來源）
- **筆記**：Obsidian、Notion（組織想法）
- **大綱**：心智圖、大綱（結構論證）

### P-CSO 期間
- **起草**：P-CSO skills（組織、起草、優化）
- **迭代**：`/pinker-quick`（即時反饋）

### P-CSO 之後
- **引用格式**：Zotero、Citation Machine
- **引用檢查**：Grammarly、ProWritingAid（補充）
- **期刊格式**：LaTeX、Word 模板
- **提交**：期刊系統

**P-CSO 定位**：核心認知優化；外部工具處理引用和格式化

---

## 自訂

所有檔案都是純 Markdown，可以編輯：

**自訂 skill**：
1. 打開 `skills/[skill-name]/SKILL.md`
2. 編輯指令、範例或規則
3. 保存
4. 用樣本文本測試

**版本控制**：編輯後考慮提交到 Git

---

## 學習資源

**理解 P-CSO 框架**：
- 閱讀：Steven Pinker《The Sense of Style》（第 4 和 5 章）
- 關鍵洞察：好的寫作減少讀者的認知負擔

**實踐 P-CSO 原則**：
1. 在你的文本上運行 `/p-cso-workflow`
2. 研究診斷
3. 識別你的重複問題（例如"我總是埋藏主旨"）
4. 在下一個草稿中主動應用該原則
5. 使用 `/pinker-quick` 驗證

**目標**：內化原則，使初稿需要更少修訂

---

## 技術細節

### 系統結構

```
plugin/
├── .claude-plugin/
│   └── marketplace.json     # Marketplace 配置
├── skills/
│   ├── p-cso-workflow/      # 完整流程
│   ├── pinker-syntax/       # 句法優化
│   ├── pinker-coherence/    # 連貫性優化
│   ├── pinker-quick/        # 快速清理
│   ├── notes-to-manuscript/ # 筆記轉手稿
│   └── english-editing/     # 英文編輯
└── README.md                # 本文件
```

### YAML Frontmatter

每個 SKILL.md 包含：
```yaml
---
name: skill-identifier
description: Skill 用途和使用時機的簡要描述（最多 1024 字符）
---
```

這使 Claude Code 能夠智能地推薦和調用合適的 skills。

---

## 支援與回饋

- **Claude Code 問題**：https://github.com/anthropics/claude-code/issues
- **P-CSO 問題**：參考 Pinker 的《The Sense of Style》
- **自訂幫助**：編輯 skill 檔案；迭代測試
- **貢獻與建議**：歡迎透過 GitHub Issues 或 Pull Requests 貢獻

---

## 授權與引用

**Framework**: 基於 Steven Pinker 的《The Sense of Style: The Thinking Person's Guide to Writing in the 21st Century》（2014）

**建議引用**：
```
Chen, S.-C. (2025). P-CSO Writing Skills: Pinker's Cognitive Style Optimization
  for Academic Writing (Version 0.9.0). https://github.com/SCgeeker/claude-writing-config
```

---

## 版本資訊

**當前版本**: 0.9.0 (Preview/Beta)
**發布日期**: 2025
**狀態**: ✅ 可用於生產環境，歡迎反饋
**下一步**: 收集用戶反饋後發布 v1.0.0 正式版

---

**系統狀態**: ✅ 完全運作
**下一步**: 安裝並使用樣本文本測試
