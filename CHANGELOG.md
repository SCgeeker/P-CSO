# Changelog

All notable changes to P-CSO Writing Skills will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-08-28

### Changed - Thin Orchestrator Architecture

技能改為「薄協調器 + 規則歸屬子技能」的架構。每條規則只住在一個地方，
直接呼叫子技能時同樣生效，不必每次都跑完整管線。

#### Added
- `manuscript-writing-review` skill：六道稽核（冗詞、被動語態、句構、術語、
  數值與引註、主張紀律），加入 marketplace 清單
- `pinker-syntax` Rules 7-11：四條子句規範加連接詞負荷檢查
- `pinker-coherence` Principle 8（主語施事）與 Principle 7D（學術語域）：
  偵測預告句、以交叉引用開頭的段落、作者姿態、報告立場而非提出主張、
  短平觀察堆疊
- `pinker-coherence` Principle 3C/3D：跨段抽象回指、代名詞收尾、
  讀者尚未取得概念前不使用該術語
- `manuscript-writing-review` Pass 4 領域用詞檢查與 Pass 6 主張紀律
- `p-cso-workflow` 改寫協定：改寫檔獨立、逐段新舊對照、
  HTML 註解回饋迴圈、整合後掃描過期數字
- `p-cso-workflow` 溝通語言規則：大幅改寫用中文討論、逐行編輯用英文、
  稿件文字恆為英文

#### Changed
- `p-cso-workflow` 由三階段擴為四階段，並移除自帶規則，全部委派子技能
- `pinker-syntax` 與 `pinker-coherence` 拆為 SKILL.md + references/，
  細則與校準範例移入 references/

#### Notes
- 本版例句一律使用公開文獻題材，不含未發表稿件內容

## [0.9.0] - 2025-11-07

### Changed - Marketplace Format Migration

**🚀 Major Update: Claude Code Marketplace Format**

This release represents a complete restructuring to support Claude Code marketplace distribution.

#### Added
- `.claude-plugin/marketplace.json` - Marketplace configuration file
- YAML frontmatter to all SKILL.md files with `name` and `description` fields
- Comprehensive README.md in Traditional Chinese with:
  - Installation instructions for marketplace
  - Complete workflow examples (A/B/C/D)
  - Quick reference tables
  - Best practices guide
  - P-CSO principles overview
- LICENSE file (MIT License)
- CHANGELOG.md (this file)
- Enhanced .gitignore

#### Changed
- Renamed all `skill.md` → `SKILL.md` (uppercase, marketplace requirement)
- Restructured repository for marketplace compatibility:
  - Root-level `.claude-plugin/` directory
  - Simplified directory structure
  - Skills-only distribution (agents removed)
- Updated README.md from English to Traditional Chinese
- Consolidated documentation from separate `docs/` folder into README

#### Removed
- `agents/writing-manager/` - Moved to separate development repository
- `docs/` directory - Content integrated into README.md
- Legacy file naming conventions
- English-only documentation

### Technical Details

**Skills Included (6 total):**
1. `p-cso-workflow` - Complete notes-to-manuscript pipeline
2. `pinker-syntax` - Sentence-level syntax optimization (Chapter 4)
3. `pinker-coherence` - Discourse-level coherence optimization (Chapter 5)
4. `pinker-quick` - Rapid cognitive cleanup for active drafting
5. `notes-to-manuscript` - Ethical AI-assisted scaffolding
6. `english-editing` - Academic English copyediting

**Installation:**
```bash
/plugin marketplace add SCgeeker/P-SCO
/plugin install p-cso-skills
```

**Status:** Preview/Beta - Ready for testing and feedback

---

## [1.0.0] - 2025-10-26

### Initial Release

**Personal Writing System (Pre-Marketplace Format)**

First implementation of P-CSO (Pinker's Cognitive Style Optimization) framework for academic writing assistance.

#### Components
- 1 agent: writing-manager (orchestration)
- 6 skills: p-cso-workflow, pinker-syntax, pinker-coherence, pinker-quick, notes-to-manuscript, english-editing
- Documentation: p-cso-writing-workflow.md, skills-vs-agents-guide.md, cross-device-setup.md
- Academic manuscript example

**Format:** Personal `.claude/` directory structure
**Language:** English
**Total:** ~25,000 words of prompts and documentation

---

## Future Plans

### [1.0.0] - Planned
- Incorporate user feedback from 0.9.0 preview
- Refine YAML descriptions based on usage patterns
- Add troubleshooting section based on common issues
- Potential addition of example use cases
- Consider multilingual support (English version of README)

### [1.1.0] - Ideas
- Advanced skills for specific academic disciplines
- Integration guides for popular tools (Zotero, Obsidian)
- Video tutorials or interactive examples
- Community-contributed examples

---

**Framework:** Based on Steven Pinker's "The Sense of Style" (2014)
**Maintainer:** Sau-Chin Chen (pmsp96@gmail.com)
**Repository:** https://github.com/SCgeeker/P-SCO
