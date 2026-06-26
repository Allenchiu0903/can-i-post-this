# Threads Post Scorer

AI 驅動的 Threads 貼文評分工具。貼上草稿，拿到 0-100 分數 + 逐句診斷 + 改寫版——全部根據你的個人品牌校準。

AI-powered scoring tool for Threads posts. Paste a draft, get a 0-100 score + line-by-line diagnosis + rewrite — all calibrated to your personal brand.

## 功能 What It Does

貼上你的草稿 → 拿到三樣東西：

1. **分數（0-100）** 涵蓋 8 個維度：Hook 力、對話引力、情緒共鳴、原創密度、格式節奏、行動觸發、品牌一致性、殺觸及偵測
2. **逐句診斷** — 每一句標記 🟢（強句）、🟡（可改）、🔴（殺觸及），附具體原因
3. **改寫版** — 目標 70 分以上，保留你的觀點，優化表達方式

## 個人化校準 Personal Calibration

第一次使用時，評分器會問你 3-5 個問題：

- 你在哪個平台發文？（Threads / IG / X / LinkedIn）
- 你的內容主題是什麼？列 3-5 個關鍵字
- 你發文的主要目標？（漲粉 / 賣東西 / 建立專業形象 / 純分享）
- 你的受眾是誰？一句話描述 *（選填）*
- 貼一篇你寫過最滿意的文章 *（選填——用它來反推你的寫作風格）*

答案會存成 `MY_PROFILE.md`。之後每次評分都根據你的設定來打，不是通用邏輯。隨時說「重新校準」就能改。

## 安裝方式 How to Install

### Claude Code（CLI / 桌面版 / 網頁版）

把 `SKILL.md` 複製到 Claude Code 的 skills 資料夾：

```bash
# 建立 skill 資料夾
mkdir -p ~/.claude/skills/threads-post-scorer

# 複製 skill 檔案
cp SKILL.md ~/.claude/skills/threads-post-scorer/SKILL.md
```

啟動 Claude Code，說「幫我評分」或直接貼草稿就能用。

### 其他 AI 工具（ChatGPT / Gemini / 任何 LLM）

把 `SKILL.md` 的內容複製到你的 system prompt 或自訂指令。評分邏輯適用於任何能遵循結構化指令的 LLM。

## 分數區間 Score Ranges

| 區間 | 含義 |
|------|------|
| 80-100 | 直接發，高機率表現好 |
| 70-79 | 小改即可，調整 Hook 或收尾 |
| 50-69 | 結構有問題，需要改寫 |
| 0-49 | 建議換個角度重新來 |

## 使用範例 Example

**輸入：**
> 52 歲才開始學 AI，來得及嗎
>
> 我不是工程師，不會寫程式，半年前連 ChatGPT 都沒用過。
>
> 現在我的 AI 系統每天凌晨四點自動抓 40 個來源的新聞、自動寫好 3 篇社群草稿。我一早起來，只需要選一篇發出去。

**輸出：**
```
分數：82/100

Hook 力：14/15 — 年齡反差 + 疑問句，直接勾起好奇心和共鳴
對話引力：12/20 — 結尾有力但封閉，缺少讓人想回覆的開口
情緒共鳴：14/15 — 三連否定堆疊痛點，凌晨四點場景重建，翻轉有力
原創密度：9/10 — 第一人稱真實經歷 + 具體數據
...

改寫版（目標 85+）：

52 歲才開始學 AI，來得及嗎

我不是工程師，不會寫程式，半年前連 ChatGPT 都沒用過。

現在我的 AI 系統每天凌晨四點自動抓 40 個來源的新聞、
自動寫好 3 篇社群草稿。

我一早起來，只需要選一篇發出去。

重點從來不是你幾歲、會不會寫程式。
重點是你願不願意花時間搞懂一件新東西。

你現在卡在哪一步？留言跟我說，我來拆給你聽。
```

## 評分依據 Research Basis

評分基於以下公開研究：
- Meta 官方內容分發指南（Engagement Bait 政策）
- Buffer 分析 250 萬篇 Threads 貼文（最佳發布時間）和 4500 萬篇貼文（最佳內容格式）
- 各平台演算法公開文件

完整來源列表在 `SKILL.md` 底部。

## 授權 License

MIT — 隨便你怎麼用。

---

由 [Allen](https://www.threads.net/@allenchiu0903) 製作 — 52 歲一人公司創業者，用 AI 建立睡覺時還在工作的系統。追蹤看更多 AI 工作流工具和實戰故事。

Built by [Allen](https://www.threads.net/@allenchiu0903) — a 52-year-old solo entrepreneur using AI to build systems that work while he sleeps.
