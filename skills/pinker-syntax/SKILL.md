---
name: pinker-syntax
description: This skill should be used to optimize sentence-level syntax for cognitive clarity using Pinker's rules from Chapter 4 of "The Sense of Style". Addresses complex syntax, verbose phrasing, ambiguous structure, and grammatical inconsistency. Use this skill whenever users mention awkward sentences, hard-to-parse writing, or convoluted phrasing, or when reviewers say writing is hard to follow at the sentence level. Also invoke for center-embedding, left-branching structures, noun piles, garden-path sentences, or excessive working memory load, chained conjunctions, or "and" used where the relation is contrast or cause. Does not address paragraph flow — use pinker-coherence for discourse-level problems.
---

# Pinker Syntax Optimizer: Sentence-Level Cognitive Clarity

**Framework**：Steven Pinker《The Sense of Style》Ch.4: The Web, The Tree, and The String
**角色**：你是心理語言學句法專家。目標是讓每個句子都易於解析——降低工作記憶負擔、避免理解中斷、消除歧義——同時不改變作者原意。
**不處理**：篇章連貫、段落流動、主題延續（見 `/pinker-coherence`）

## 觸發條件
使用者提到句子拗口、難以解析、繞口的措辞；審稿人說句子層級難讀；或出現中心內嵌、左分支結構、名詞堆疊、花園路徑句、工作記憶負荷過重等情境。

## 動手前：Negative Constraints 掃描
掃描前置修飾語堆疊、名詞堆疊、中心內嵌子句、花園路徑句、重輕排序錯誤、新舊資訊排序錯誤、平行結構不一致、錯置修飾語、em-dash 連接子句、括號行內列表、關係子句、可省略的從屬子句、連接詞串接、以 and 表對比——命中即違規。完整清單見 `references/rules-detail.md`。

## 6 大認知優化規則
1. **Reduce Memory Load** — light-before-heavy；把複雜片語移到句尾，別堆在主詞前。
2. **Avoid Parsing Collapse** — 消除多層中心內嵌子句，拆成多個短句。
3. **Optimize Information Density** — 消除殭屍名詞化與輕動詞，刪除冗贅片語與 "It is / There is" 空殼。
4. **Satisfy Expectation Ordering** — given-before-new；被動語態僅在滿足此排序時才正當。
5. **Avoid Ambiguity** — 消除花園路徑句與修飾語錯置，用朗讀測試瞬間誤讀。
6. **Check Grammatical Consistency** — 平行結構句法一致，主詞動詞隔開時仍需呼應。

每條規則的完整說明、操作細節與判準見 `references/rules-detail.md`；範例見 `references/examples.md`。

## Rules 7–11（全域 P-CSO Canonical 規範——一條都不能少）
> 這五條是全域 CLAUDE.md 與 `/p-cso-workflow` 引用的 canonical 出處，每次修訂都必須套用。

7. **不用 em-dash 連接子句** — 拆成獨立句子或用明確連接詞。
8. **不用括號放行內列表** — 改用 "including X, Y, and Z"。
9. **不用關係子句（which/that/who）** — 改寫成獨立句子。
10. **能用直接 SVO 句就不用從屬子句** — 優先主詞-動詞-受詞，避免 although/because/while 造成的隱性依賴。
11. **連接詞負荷** — 逐句清點對等連接詞。一句三個以上的 and 即為串接，必須拆句。每個 and 都要問：這裡的關係真的是「加合」嗎？若實為對比、因果或讓步，換成精確的連接詞（but / however / because / therefore / although）。以 and 作為預設接合詞會把論證結構壓平成清單，並遮蔽最該被看見的那一個關係。

## 工作流程
1. 讀入使用者文本，先跑 Negative Constraints 掃描。
2. 依 Rule 1–11 逐句修訂（Rules 7–11 為強制項）。
3. 修訂完成後，對照 `references/rules-detail.md` 的 Self-Review Checklist 逐項檢查，抓出「修好一個 pattern 卻引入另一個」的常見失敗模式。
4. 依 `references/rules-detail.md` 的 Output Format 模板輸出：原文、修訂文、逐項 Syntax Diagnostics、規則套用統計、Self-Review 結果、Next Steps。

## Changes / Preserves
**Changes**：句子結構、冗贅度、句法歧義、文法錯誤、子句慣例（Rules 7–10）
**Preserves**：內容語意、專業術語、作者語氣、引註與參考文獻

## 銜接其他技能
`/pinker-coherence`（段落連貫）→ `/english-editing`（最終語言潤飾）；完整流程用 `/p-cso-workflow`。

## Quick Decision Guide
| 症狀 | 對應規則 |
|---|---|
| 句子讀起來卡 | Rules 1, 2, 4 |
| 句子太長 | Rules 2, 3 |
| 句意有歧義 | Rule 5 |
| 列表/比較混亂 | Rule 6 |
| 整體用詞冗贅 | Rule 3 |
| 含 em-dash / 括號 / which 子句 | Rules 7–10 |
| 一句多個 and／用 and 表對比 | Rule 11 |

---
**Skill Version**：3.0（context engineering 重構：拆分 references/，Rules 1–10 實質內容不變）
**References**：`references/rules-detail.md`（規則詳解、Checklist、Output Format）、`references/examples.md`（精選範例）
