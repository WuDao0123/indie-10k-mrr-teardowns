# 对标站 `skillry.dev` 深度拆解与「B + A 组合拳」降维打击作战报告
## Full Technical, Programmatic SEO & Pricing Teardown of `skillry.dev`

> **实测核验声明**：本报告全部数据由 `/workspace/growth-skills/skills/pseo-competitor-teardown/scripts/teardown-pseo.js` 与 `teardown-pricing.js` 于 `2026-10-27` 对 `https://skillry.dev` 线上真实 `robots.txt`、`sitemap.xml`、`/llms.txt` 与 DOM 进行无头浏览器实测抓取生成。原始数据存档于 `examples/pseo/skillry-dev-pseo-blueprint.json` 与 `examples/pricing/skillry-dev-pricing-teardown.json`。

---

## 一、 核心基建与流量盘子总览 (Executive Telemetry Summary)

| 维度 (Dimension) | `skillry.dev` 实测数据 | 我们的 `taste-skill` (B + A 组合拳) | 胜负手诊断 (Strategic Verdict) |
| :--- | :--- | :--- | :--- |
| **首页定位 (`<h1>`)** | `Skillry - Agent Skills with taste` | `Clone any website’s visual soul & growth engine into Cursor.` | Skillry 主打「有审美的静态 Agent Skills 库」；我们主打**「实时 URL/截图逆向引擎 (B) + 可执行增长爬虫与变现基建 (A)」** |
| **Sitemap 总 URL 数** | **16,341 个 URL** (99.6% 程序化 SEO) | **53 个高密度静态 pSEO 页**（支持无限裂变） | Skillry 靠 **9 语言子目录裂变（$\times 9$）** 把 ~1,815 个原始页面放大到 16,341 个索引页 |
| **`/llms.txt` 部署状态** | ✅ 已部署（**246,610 chars / 240.8 KB**） | ✅ 已部署 `/llms.txt` (`15.6 KB`) + `/llms-full.txt` (`37.8 KB`) | Skillry 把全部 618 个独立 Skill 的标题与简介塞进了 240KB 的 `/llms.txt`，极具 GEO 侵略性 |
| **多语言 (`hreflang`) 矩阵** | **9 种语言**：`en`（默认）+ `/zh/`、`/zh-tw/`、`/ja/`、`/ko/`、`/es/`、`/pt-br/`、`/de/`、`/fr/` | 已内置 `EN / 中文 / 日本語 / ES` 四语种对比矩阵与多语言脚手架 | 9 语言全站镜像是 Skillry 低成本获取非英语长尾流量的第一大杠杆 |
| **定价模型 (Pricing)** | • 免费：`$0`（仅 3 个免费 Skill）<br>• 月付：`$9.99/mo`<br>• 年付：`$79/yr` (`Most popular`)<br>• 买断：**`$169`** (`Founding Lifetime`) | • 社区版：**`$0`**（CLI + 30 个旗舰审美 Skill + 20 个万刀站拆解库）<br>• 单品：**`$29`**（任选 1 个增长 Skill）<br>• Pro 套件：**`$69 Early-Bird`** (`~~$99~~`)<br>• 团队/Agency：**`$169`**（5 席位 + 白标交付） | Skillry 买断价高达 **`$169`** 且只给静态 Markdown；我们以 **`$69`**（不到其 41% 的价格）交付 **4 大增长 Skill + 5 个本地 Playwright 爬虫脚本 + 20 站真实拆解数据** |

---

## 二、 `skillry.dev` 的 16,341 个 URL 路由树全解剖 (Sitemap Route Anatomy)

通过递归解析 `https://skillry.dev/sitemap.xml`，我们发现其 **16,341 个 URL** 并非手工撰写，而是由 **1,815 个英文母本页面 $\times$ 9 个语言区域（`en`, `zh`, `zh-tw`, `ja`, `ko`, `es`, `pt-br`, `de`, `fr`）** 构成的典型程序化 SEO 矩阵：

| 排名 | URL 路由模式 (Route Pattern) | 页面族类型 | 总 URL 数 (含 9 语种) | 折算英文母本数 ($\div 9$) | 真实抽样 URL 与截流意图 |
| :- | :--- | :--- | ---: | ---: | :--- |
| 1 | `/ai-videos/[model_slug]/[video_id]` | AI 视频提示词库 | **9,720** (59.5%) | **1,080 页** | `skillry.dev/ai-videos/opus-5-5/heyiamnick-119558`<br>👉 **高频热点截流**：抓取 X 上热门的 Opus 5.5 / Kimi K3.1 视频案例并拆解 Prompt，吃大模型热点搜索词 |
| 2 | `/skills/[skill_slug]` | 单个 Skill 详情落地页 | **5,562** (34.0%) | **618 页** | `skillry.dev/skills/html-slides`、`bs-a24-style-og`<br>👉 **长尾任务截流**：针对 PPT 生成、OG 图生成、网页排版等具体任务词做单页转化 |
| 3 | `/skills/[filter_type]/[sub_slug]` | Skill 分类聚合目录页 | **639** (3.9%) | **71 页** | `skillry.dev/skills/output/web`<br>👉 **品类词截流**：Title 公式为 `Frontend Design Skills for Claude Code, Codex & Cursor` |
| 4 | `/learn/[learn_slug]` 及子目录 | 教程与概念科普页 | **171** (1.0%) | **19 页** | `skillry.dev/learn/can-claude-generate-images`、`/learn/agents/claude-code` |
| 5 | `/ai-videos/[model_slug]` | 视频模型聚合页 | **63** (0.4%) | **7 页** | `skillry.dev/ai-videos/kimi-k3-1` |
| 6 | `/learn/.../[tool_a]-vs-[tool_b]` | 生态对比页 (`A vs B`) | **36** (0.2%) | **4 页** | `skillry.dev/learn/ecosystem/skills-vs-mcp`、`/learn/remotion-vs-hyperframes` |
| 7 | `/[root-landing-slug]` | 根路径免费微工具引流钩子 | **20** (0.1%) | **~2–3 个工具** | `skillry.dev/dot-avatar-maker`（点阵头像生成器，免费玩工具 $\rightarrow$ 导流买 Skill） |
| 8 | `/learn/[competitor]-alternatives` | 竞品替代页 | **18** (0.1%) | **2 页** | `skillry.dev/learn/gamma-alternative`（截流 Gamma PPT 用户去买它的 HTML Slides Skill） |

---

## 三、 `skillry.dev` 的三大增长亮点与四大致命软肋

### ✅ 值得我们直接吸收的 3 个工程亮点
1. **9 语种全站镜像裂变 (`hreflang` $\times 9$)**：连 `/robots.txt` 都整齐配置了 9 个语种的 `/auth`、`/admin`、`/settings` 屏蔽规则，一篇 `/learn/gamma-alternative` 自动变成 9 个语种页面。
2. **微型交互工具引流 (`/dot-avatar-maker`)**：在根路径挂免费小工具（如像素点阵头像生成），吸引设计师和开发者转发，再顺势推销 `$79/yr` 或 `$169` 的 Skill 包。
3. **超大体量 `/llms.txt` (`246.6 KB`)**：把全站 618 个 Skill 的名称、URL 和一句话功能描述全部列在 `/llms.txt` 中，确保当用户在 Claude / ChatGPT 问“有没有做 A24 风格海报或学术 PPT 的 Claude Skill”时被直接命中。

### ❌ `skillry.dev` 的 4 大致命软肋（我们的降维打击切口）
1. **软肋一：只有静态预制 Prompt，没有「实时 URL / 截图逆向提取引擎」**
   - 用户在 Skillry 只能从它写好的静态模板里挑；如果用户看中了某个新上线的网站或手里有一张 UI 截图，Skillry 完全无能为力。
   - **我们的打击点（B 套件免费送）**：`npx taste-skill extract <url>` + `npx taste-skill from-image <png>`（或网页端 `Cmd+V` 粘贴截图），32ms 本地 Canvas 聚类 + Chromium 真实计算样式，**把任何网站或截图当场变成 `SKILL.md` 并且完全免费开源**！直接把 Skillry 收费的核心卖点变成我们的免费引流钩子。
2. **软肋二：重“视觉/PPT 表面美化”，完全缺失「真金白银的增长、SEO 与变现脚本」**
   - Skillry 的 618 个 Skill 集中在做 PPT（`html-slides`）、画海报（`bs-a24-style-og`）、写文案，**没有任何一个 Skill 附带真正可运行的 Node.js / Playwright 爬虫去帮独立开发者抓竞品 Sitemap、抓定价页 DOM、生成合规取消挽留流或校验 App Store 100 字节关键词**。
   - **我们的打击点（A 套件核心壁垒）**：我们的付费包不卖“水词 Prompt”，而是交付 **4 大增长变现 Skill + 5 个零成本本地 Playwright/Node 逆向脚本 + 20 个已核验万刀站（`$10k–$422k MRR`）的完整 JSON 蓝图库**。
3. **软肋三：买断定价过高（`$169 Founding Lifetime`）且强推订阅制（`$9.99/mo` / `$79/yr`）**
   - 开发者对“纯 Markdown 提示词还要每月交 `$9.99` 订阅费或花 `$169` 买断”存在强烈的订阅疲劳（Subscription Fatigue）。
   - **我们的打击点（价格锚定截胡）**：我们在 `/showcase/tasteskill-vs-skillry/` 页面直接拉出事实核验对比表（附 `verifiedAt: 2026-10-27`），用 **`$69 早鸟一次买断`** 锚定它的 **`$169 Lifetime`**，不仅便宜 **59%（立省 $100）**，还多送 5 个自动化爬虫脚本和 20 个万刀站数据库。
4. **软肋四：9,720 个 `/ai-videos/*` 页面存在明显的 SEO 内容稀释**
   - 其 Sitemap 中近 60% 是搬运 X 帖子的短视频 Prompt 页面，与核心 Coding Agent 用户画像脱节；而我们的 53+ 个静态 pSEO 页面 100% 聚焦在 `<Brand> Design System Tokens` 与 `<Indie SaaS> $10k+ MRR SEO Teardown`，转化路径极短且高度精准。
