# CONSTITUTION_BLOCK

一份可貼給任何新專案的 Claude Code 安裝包 — 一次貼上，自動長出 14 條開發憲法 + 8 個薄命令 + 活文件骨架。

**全部檔案都建在專案本地（`<專案>/.claude/`、`<專案>/CLAUDE.md` 等），不動全域 `~/.claude/`。**

## 用法

1. 打開 [`INSTALL.md`](./INSTALL.md) 的 **Raw** 檔（GitHub 右上角 Raw 按鈕）
2. 全選複製
3. 到你的新專案：`cd <專案> && claude`
4. 貼成第一則訊息
5. Claude 會自動建好所有檔案，並詢問是否加 hooks、填 Override

## 產出的檔案結構

```
<你的專案>/
├── CLAUDE.md              # loader + 白話→緊實 翻譯表 + Override 區塊
├── CONSTITUTION.md        # 憲法全文 v3（14 節）
├── CONTEXT.md             # 詞彙表（空模板）
├── SPEC.md                # 活規格（空模板）
├── LESSONS.md             # 踩坑日誌（空模板）
├── docs/adr/README.md     # ADR 說明
└── .claude/
    ├── settings.json      # 可選 hooks（會問才建）
    └── commands/
        ├── grill.md       # /grill  — §1 對齊 grilling
        ├── debug.md       # /debug  — §6 tight loop 才准假設
        ├── review.md      # /review — §11 拆軸 review
        ├── spec-out.md    # /spec-out — 對話壓成 spec
        ├── lesson.md      # /lesson  — 記踩坑
        ├── deep.md        # /deep    — §7 模組檢查
        ├── handoff.md     # /handoff — §10 交接
        └── twice.md       # /twice   — §7 Design It Twice
```

## 憲法內容（v3, 14 節）

0. 根本 — 決定性優於聰明
1. 動手前：想清楚 + 對齊（grilling）
2. 只做被要求的事（Simplicity + Surgical Changes）
3. 工作切分：Tracer Bullet + Expand–Contract
4. TDD 為預設 + Mock 邊界
5. 測試隔離
6. Debug 唯一真理：tight red-capable loop 為前提
7. Deep Module 設計 + Design It Twice
8. Primary Source 紀律
9. 文件（活文件即時更新）
10. Context Hygiene（session 管理）
11. Code Review 拆軸
12. 模型調度（T1–T4，找便宜判貴）
13. 行動邊界
14. 輸出（六大自檢）

## 白話 → 緊實詞自動翻譯

Loader 內建翻譯表：你講白話，Claude 自動對應到章節。範例：

| 白話 | 對應 |
|---|---|
| 「先問清楚再做」 | §1 grilling |
| 「先能重現」 | §6 tight loop |
| 「幫我 review」 | §11 拆軸 |
| 「這模組太薄」 | §7 deletion test |

完整表格見 `INSTALL.md` 資產 B。

## 更新憲法

改 `INSTALL.md`，push。未來新專案貼的就是新版。已建好的舊專案要手動同步。

## 來源

思路整合自：
- [mattpocock/skills](https://github.com/mattpocock/skills) — grilling / TDD / Deep Module / Code Review 拆軸 / Tracer Bullet
- [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) — Think Before Coding / Simplicity / Surgical Changes / Goal-Driven

## License

MIT
