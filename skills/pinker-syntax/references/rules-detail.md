# Pinker Syntax — 規則詳解

完整操作細節，供 SKILL.md 摘要之後查閱。範例另見 `examples.md`。

---

## Negative Constraints — 動手前先掃描

掃描以下 pattern，命中即為違規：

1. **無前置修飾語堆疊** — 主詞前超過 6 個字，重新排序。
2. **無名詞堆疊** — 名詞+名詞+名詞 當前置修飾語（如 "teacher strike vote delay"）→ 改用介系詞片語。
3. **無中心內嵌子句** — 多層 that/who/which 互相嵌套 → 拆成獨立句子。
4. **無殘留花園路徑句** — 序列可能被誤讀（即使只是瞬間），加入消歧義的功能詞（that、the、逗號）。
5. **無「重在前、輕在後」排序** — 最重、最複雜的片語留到句尾。
6. **無「新在前、舊在後」排序** — 已知（熟悉）資訊在前，新資訊在主要子句出現。
7. **平行子句不可任意變換句法** — 平行內容用平行結構。
8. **無錯置修飾語** — 修飾語依附於緊鄰的前一個詞，place next to what it modifies。
9. **不用 em-dash 連接子句** — 拆成獨立句子或用明確連接詞。
10. **不用括號放行內列表** — 改用 "including X, Y, and Z"。
11. **不用關係子句（which/that/who）** — 改寫成獨立句子。
12. **能用直接 SVO 句就不用從屬子句** — 優先主詞-動詞-受詞。

---

## 6 大認知優化規則（詳解）

### Rule 1: Reduce Memory Load
**Pinker 概念**：light-before-heavy；右分支結構（right-branching）
**做法**：把複雜片語放到句尾；將沉重內容移出主詞位置，讓讀者一開始就能掌握主詞與動詞。

### Rule 2: Avoid Parsing Collapse
**Pinker 概念**：消除多層中心內嵌句（multiply center-embedded sentences）
**做法**：巢狀關係子句會讓讀者的 parser 當機。拆成多個較短句子。
**紅旗訊號**：多個 that/who/which 互相嵌套；讀到一半找不到主要動詞的句子。

### Rule 3: Optimize Information Density
**Pinker 概念**："Omit needless words"；消除殭屍名詞化（zombie nominalization）與輕動詞（light verb）
**做法**：把名詞化改回動詞；刪除冗贅片語；刪除填充詞。

常見殭屍名詞化修正：
- *prevention of X* → *prevent X*
- *is supportive of* → *supports*
- *conduct an investigation* → *investigate*
- *make a decision* → *decide*
- *have an effect on* → *affect*

常見冗贅片語修正：
- *in the event that* → *if*
- *due to the fact that* → *because*
- *in order to* → *to*
- *a majority of* → *most*

**It is / There is 抽脂**：刪除空洞的 "It is..." / "There are..." 開頭，直接讓真正的主詞和動詞上場。

### Rule 4: Satisfy Expectation Ordering
**Pinker 概念**：given-before-new；策略性被動語態
**做法**：句子安排讓主題（較輕、已知）在前，評論（較重、新資訊）在後。被動語態在能滿足此排序時才有正當性（light topic 先出現，heavy new mechanism 延後）。

### Rule 5: Avoid Ambiguity
**Pinker 概念**：花園路徑句（garden paths）；modifier 誤依附
**做法**：若字詞序列可能被瞬間誤讀，加入消歧義標記（如 "that"）或調整語序。
**檢測法**：朗讀出聲；若第一次唸就誤解句意，就該加標記。

### Rule 6: Check Grammatical Consistency
**Pinker 概念**：Tree-thinking；結構平行性
**做法**：並列結構須用平行句法；主詞與動詞被隔開時，仍需檢查一致性（單複數呼應）。

---

## Rules 7–10（User-Confirmed Style Conventions）詳解

這四條延伸自 6 大 Pinker 規則，源自 2026-02-24、2026-03-06 的 session 確認，是全域 CLAUDE.md 與 `/p-cso-workflow` 引用的 canonical 規範，每次修訂都必須套用：

**Rule 7：不用 em-dash 連接子句**
理由：em-dash 常被用來偷懶地黏合兩個本該獨立的想法。改寫為兩個句子，語意關係更明確。

**Rule 8：不用括號放行內列表**
理由：括號打斷主要語句的閱讀節奏。改用 "including X, Y, and Z" 這類完整的列舉句法。

**Rule 9：不用關係子句（which/that/who）**
理由：關係子句常導致中心內嵌與資訊密度過高。拆成獨立句子，讓每個子句只承載一個命題。

**Rule 10：能用直接句就不用從屬子句**
理由：從屬連接詞（although、because、while 等）製造隱性的邏輯依賴，讀者需要暫存前句才能理解後句。改寫為兩個直述句，邏輯關係用內容本身呈現。

---


---

## Rule 11：連接詞負荷（Conjunction Load）

**問題**：以 and 作為預設接合詞。句子在文法上完全成立，每個 and 單獨看也讀得通，
因此既有的規則都掃不到：它不是 em-dash，不是括號列表，不是關係子句，也不是歧義連接詞。

**兩種子型**

1. **串接（chaining）** — 一句裡三個以上的對等連接詞。論證結構被壓平成清單，
   讀者無從得知哪一個關係才是重點。
2. **加合預設（additive default）** — 關係其實是對比、因果或讓步，卻用 and。
   `/pinker-coherence` 的負面約束第 4 條只點名 while 與 also，未涵蓋 and。

**操作步驟**

1. 逐句清點 and / or / but。
2. 三個以上 → 拆句。
3. 對每一個 and，問：兩端是否真為並列的加合關係？
   - 是 → 保留。
   - 否 → 依實際關係換成 but、however、because、therefore、although。

**判準**：把 and 兩端對調，語意若明顯走樣，該關係就不是加合。

**認知收益**：論證結構浮現；最該被看見的那個轉折不再被埋在清單裡。

## Self-Review Checklist（完成修訂後逐項檢查）

修訂完成後，在最終輸出前，將每個被修改的句子對照以下清單檢查。任一項失敗就要修正：

- [ ] 修訂過程中沒有句子新增關係子句（which/that/who）
- [ ] 修訂沒有引入 em-dash 連接子句
- [ ] 修訂後的句子沒有變成左分支（重修飾語堆在主詞前）
- [ ] 沒有引入新的花園路徑歧義
- [ ] 沒有在缺乏 given-new 正當性的情況下使用被動語態
- [ ] 簡化過程中沒有製造新的名詞堆疊
- [ ] 所有平行結構句法一致
- [ ] 原意完整保留——沒有增刪內容

這一步是為了抓住最常見的失敗模式：修好一個 pattern，卻不小心引入另一個。

---

## Output Format

```markdown
# Pinker Syntax Optimization Results

## Original Text
[User's input text]

---

## Optimized Text
[Revised version with syntax improvements]

---

## Syntax Diagnostics (Chapter 4 Framework)

### Issue 1: [Specific Problem]
- **Rule violated**: [Which rule]
- **Original sentence**: "[Quote]"
- **Cognitive burden**: [How this affected parsing]
- **Fix applied**: "[Revised sentence]"
- **Cognitive gain**: [How this helps]

[Repeat for every change actually made. There is no minimum. Clean text yields no entries, and a passage that needs one fix gets one. Never manufacture a finding to reach a count. When a candidate was inspected and rejected, record it as a no-violation entry with the reason, which is a finding about the text rather than an invented fault.]

---

## Summary

**Rules applied**:
- Rule 1 (Memory load): [X instances]
- Rule 2 (Parsing collapse): [X instances]
- Rule 3 (Information density): [X instances]
- Rule 4 (Expectation ordering): [X instances]
- Rule 5 (Ambiguity): [X instances]
- Rule 6 (Consistency): [X instances]

**User conventions applied**: [list Rules 7–10 that fired]

**Self-review**: [Confirm all checklist items passed, or note any that required a second fix]

**Overall impact**: [Brief assessment]

---

## Next Steps
- [ ] Review changes for content accuracy
- [ ] Check if revisions match your intended meaning
- [ ] Use `/pinker-coherence` if paragraph flow needs work
- [ ] Use `/english-editing` for final grammar polish
```

---

## What This Skill Changes / Preserves

**Changes**：句子結構、冗贅度、句法歧義、文法錯誤、子句層級慣例（Rules 7–10）
**Preserves**：內容與語意、專業術語、作者語氣、引註與參考文獻

---

## Integration with Other Skills

**Before**：使用者寫草稿（或使用 `/p-cso-workflow`）
**After**：`/pinker-coherence` → `/english-editing`
**Full pipeline**：`/p-cso-workflow`（含 syntax + coherence）

---

## Quick Decision Guide

| Symptom | Check |
|---|---|
| Sentence feels awkward | Rules 1, 2, 4 |
| Sentence too long | Rules 2, 3 |
| Sentence ambiguous | Rule 5 |
| Lists / comparisons messy | Rule 6 |
| General wordiness | Rule 3 |
| Contains em-dash / parentheses / which-clause | Rules 7–10 |

---

**Skill Version**: 2.0
**Changes from v1**: Added Negative Constraints section, Few-Shot Examples (5 pairs from Pinker Ch.4), Self-Review Checklist (Recursive Self-Improvement pattern). Rules 1–10 unchanged.
**Framework**: Pinker's "The Sense of Style" — Chapter 4
**Optimized for**: Academic research writing
**Scope**: Sentence-level syntax only (not discourse coherence)
