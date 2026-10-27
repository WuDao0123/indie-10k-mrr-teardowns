# 独立开发者万刀站真实 SEO 与落地页拆解库
## The $10k+ MRR Indie SaaS SEO & Landing Page Teardown Library

[![Verified Revenue Only](https://img.shields.io/badge/Revenue_Data-100%25_Founder_Verified-10b981)](#1-已收录的-20-个万刀独立站索引--verified-10k-mrr-indie-saas-index)
[![Zero Paid APIs](https://img.shields.io/badge/Methodology-Live_Sitemap_%2B_DOM_%2B_llms.txt-6366f1)](#2-硬核拆解方法论--zero-fluff-methodology)
[![Powered by Agent Skills](https://img.shields.io/badge/Built_With-Taste_%26_Growth_Agent_Skills-f59e0b)](#4-如何把这些套路一键装进你的项目--turn-teardowns-into-shipped-code)

> **中文导读**：大多数独立开发者写得出好代码，却卡在「不知道做什么 SEO 页面能带来精准注册」、「不知道对比页怎么写才不违规又有转化」、「不知道定价页怎么锚定」。本开源库严选 **创始人公开披露过月收入 ≥ $10,000 MRR（附一手出处 URL 与披露日期）** 的真实独立开发者/自举（Bootstrapped）SaaS 站点，用自动化脚本直接拆解它们的 **`robots.txt`、`sitemap.xml` 全量 URL 路由树、`/llms.txt` AI 搜索索引、首屏 H1/Schema 结构与真实定价页心理设计**。**绝不编造流量数字，绝不用第三方估算水份，只看真金白银跑出来的页面工程结构。**
>
> **English Summary**: Most indie hackers can ship great code, yet stall on distribution, programmatic SEO (pSEO), comparison pages, and pricing psychology. This open-source repository reverse-engineers **bootstrapped & indie SaaS products with publicly verified revenue $\ge$ $10,000 MRR** (every single revenue figure cites a primary founder disclosure URL and date). Using deterministic Node.js + Playwright scripts, we inspect their live `robots.txt`, recursive `sitemap.xml` URL trees, `/llms.txt` AI search indexes, above-the-fold copy, and `/pricing` architecture. **Zero fabricated traffic estimates. Zero paid SEO APIs. 100% reproducible engineering patterns.**

---

> 🌐 **在线交互工作台（53 页静态站 + 实时截图转 SKILL.md 演示）**: [https://wudao0123.github.io/taste-skill/](https://wudao0123.github.io/taste-skill/)  
> 🎨 **配套开源视觉逆向 CLI (`taste-skill`)**: [https://github.com/WuDao0123/taste-skill](https://github.com/WuDao0123/taste-skill)  
> 📦 **本仓库地址 (`indie-10k-mrr-teardowns`)**: [https://github.com/WuDao0123/indie-10k-mrr-teardowns](https://github.com/WuDao0123/indie-10k-mrr-teardowns)

---

## 1. 已收录的 20 个万刀独立站索引 / Verified $10k+ MRR Indie SaaS Index

| # | 站点 (Product) | 公开披露收入 (Verified Revenue) | 披露日期 (Date) | 一手出处 (Primary Source) | 实测索引页数 (URLs) | `/llms.txt` 状态 | 核心程序化 SEO / 增长杀手锏 (Primary pSEO & Growth Wedge) | 深度拆解报告 (Teardown) |
| :- | :--- | :--- | :--- | :--- | ---: | :--- | :--- | :--- |
| 1 | **Tally** (`tally.so`) | **$422,000 MRR ($5,000,000 ARR)** | `2026-04-15` | [Primary Proof](https://blog.tally.so/the-road-from-4m-to-5m-arr/) | 445 (92.8% pSEO) | ✅ `4.2 KB` | `/templates/[template_slug]/[sub_item_slug]` (179) + `/help/[help_slug]` (142) — Disrupts Typeform & Jotform predatory response caps by offering unlimited f... | [`teardowns/tally.md`](./teardowns/tally.md) |
| 2 | **Typefully** (`typefully.com`) | **~$167,000/mo (~$2,000,000 ARR)** | `2026-03-15` | [Primary Proof](https://indiemakerlist.com/leaderboard/saas/) | 228 (93% pSEO) | ✅ `1.6 KB` | `/changelog/[changelog_slug]` (111) + `/blog/[blog_slug]` (63) — Replaces clunky enterprise social schedulers (Hootsuite, Sprout Social) wit... | [`teardowns/typefully.md`](./teardowns/typefully.md) |
| 3 | **Carrd** (`carrd.co`) | **$85,000+ MRR ($1,000,000+ ARR, 2.5M+ sites)** | `2021-04-30` | [Primary Proof](https://www.indiehackers.com/post/hi-im-aj-maker-of-carrd-and-after-2-5m-sites-1m-arr-and-a-funding-round-probably-time-for-an-ama-1b7fcf52fe) | 18 (22.2% pSEO) | ❌ | `/docs/[doc_slug]/[sub_item_slug]` (2) — Eliminates the complexity and $20–$30/month cost of Squarespace, Webflow, a... | [`teardowns/carrd.md`](./teardowns/carrd.md) |
| 4 | **Plausible Analytics** (`plausible.io`) | **$83,637 MRR ($1,000,000+ ARR)** | `2022-06-02` | [Primary Proof](https://plausible.io/blog/open-source-saas) | 180 (83.3% pSEO) | ❌ | `/blog/[blog_slug]` (104) + `/[root-landing-slug]` (26) — Positions directly against Google Analytics 4 (GA4) bloat, cookie banner re... | [`teardowns/plausible.md`](./teardowns/plausible.md) |
| 5 | **StandOut CV** (`standout-cv.com`) | **£40,000 MRR (~$52,000/mo)** | `2025-09-25` | [Primary Proof](https://www.indiehackers.com/post/how-i-grew-my-saas-business-to-40k-mrr-with-seo-3287452853) | 1,103 (98.7% pSEO) | ✅ `264.5 KB` | `/cv-examples/[cv_example_slug]/[sub_item_slug]` (809) + `/usa/[usa_slug]/[sub_item_slug]` (43) — Captures job seekers at the exact moment they search for role-specific CV e... | [`teardowns/standout-cv.md`](./teardowns/standout-cv.md) |
| 6 | **Bannerbear** (`bannerbear.com`) | **$50,000 MRR (~$600,000+ ARR)** | `2023-07-15` | [Primary Proof](https://www.bannerbear.com/open/) | 1,372 (98.5% pSEO) | ✅ `8.5 KB` | `/templates/[template_slug]` (319) + `/help/[help_slug]/[sub_item_slug]` (195) — Replaces brittle headless Puppeteer scripts and manual Canva design workflo... | [`teardowns/bannerbear.md`](./teardowns/bannerbear.md) |
| 7 | **Senja** (`senja.io`) | **$50,000 MRR ($600,000 ARR)** | `2024-11-19` | [Primary Proof](https://www.indiehackers.com/post/from-zero-to-50k-mrr-the-story-of-senjas-growth-6874d85edd) | 733 (96.9% pSEO) | ❌ | `/use-cases/[use_case_slug]` (360) + `/testimonial-examples/[testimonial_example_slug]` (112) — Out-executes legacy enterprise review widgets and early indie tools (Testim... | [`teardowns/senja.md`](./teardowns/senja.md) |
| 8 | **FlowMapp** (`flowmapp.com`) | **$50,000 MRR ($600,000 ARR)** | `2026-02-10` | [Primary Proof](https://indiemakerlist.com/leaderboard/saas/) | 175 (87.4% pSEO) | ✅ `10.7 KB` | `/blog/[blog_slug]/[sub_item_slug]` (58) + `/features/[feature_slug]` (53) — Replaces messy spreadsheets and over-complicated Figma files during the pre... | [`teardowns/flowmapp.md`](./teardowns/flowmapp.md) |
| 9 | **Simple Analytics** (`simpleanalytics.com`) | **$45,000 MRR ($540,000 ARR)** | `2025-10-15` | [Primary Proof](https://www.indiehackers.com/post/tech/joining-a-technical-co-founder-and-growing-the-product-to-45k-mrr-119Zbnde7pTET0QOiZLH) | 487 (81.7% pSEO) | ✅ `16.8 KB` | `/blog/[blog_slug]` (167) + `/[root-landing-slug]` (76) — Positions on strict EU data sovereignty (100% EU-hosted, zero PII, GDPR/PEC... | [`teardowns/simple-analytics.md`](./teardowns/simple-analytics.md) |
| 10 | **Papermark** (`papermark.com`) | **$45,000 MRR ($540,000 ARR)** | `2025-08-20` | [Primary Proof](https://www.indiehackers.com/post/tech/after-11-failed-products-this-founder-hit-45k-mrr-in-a-little-over-a-year-xyRkxAsD8Rys7URjYd5d) | 2,732 (96.6% pSEO) | ✅ `11.6 KB` | `/blog/[blog_slug]` (1,030) + `/help/[help_slug]/[sub_item_slug]` (491) — Attacks DocSend's expensive per-user pricing ($15–$65/user/mo) and dated UI... | [`teardowns/papermark.md`](./teardowns/papermark.md) |
| 11 | **Subscribr** (`subscribr.ai`) | **$41,600+ MRR ($500k+ YTD, $1M/yr run-rate)** | `2025-08-27` | [Primary Proof](https://www.indiehackers.com/post/tech/leaving-a-funded-startup-and-bootstrapping-to-1m-yr-in-18-months-kPBpdxsTeQitOWOOVs2g) | 747 (96% pSEO) | ✅ `1.6 KB` | `/youtube-strategy/[youtube_strategy_slug]` (588) + `/help/[help_slug]/[sub_item_slug]` (44) — Replaces generic ChatGPT prompts and scattered Google Docs with a YouTube-n... | [`teardowns/subscribr.md`](./teardowns/subscribr.md) |
| 12 | **My AskAI** (`myaskai.com`) | **$40,000 MRR (~$500,000 ARR)** | `2025-07-10` | [Primary Proof](https://www.indiehackers.com/post/tech/bootstrapping-to-40k-mrr-after-his-vc-backed-startup-failed-LF1CwRs1vL3oVLcuoIoE) | 99 (80.8% pSEO) | ❌ | `/blog/[blog_slug]` (24) + `/compare/[tool_a]-vs-[tool_b]` (10) — Undercuts Intercom Fin and Zendesk AI ($0.99/resolution) by nearly 90% ($0.... | [`teardowns/myaskai.md`](./teardowns/myaskai.md) |
| 13 | **Testimonial.to** (`testimonial.to`) | **$33,333+ MRR ($400,000+ ARR, later $800k+ ARR)** | `2022-11-18` | [Primary Proof](https://thebootstrappedfounder.com/a-conversation-with-damon-chen/) | 802 (97.3% pSEO) | ✅ `0.8 KB` | `/resources/[resource_slug]` (455) + `/integrations/[integration_slug]` (141) — Pioneered the frictionless browser-based video testimonial collector and em... | [`teardowns/testimonial.md`](./teardowns/testimonial.md) |
| 14 | **ScreenshotOne** (`screenshotone.com`) | **$33,000 MRR (~$400k ARR; ~$36k MRR by Sept 2026)** | `2026-05-29` | [Primary Proof](https://dmytrokrasun.com/posts/screenshotone-4-years/) | 644 (95.8% pSEO) | ✅ `0.9 KB` | `/changelog/[changelog_slug]` (165) + `/blog/[blog_slug]` (134) — Solves the nightmare of maintaining headless Chromium clusters, cookie-bann... | [`teardowns/screenshotone.md`](./teardowns/screenshotone.md) |
| 15 | **SuperX** (`superx.so`) | **$23,000 MRR ($276,000 ARR)** | `2025-09-10` | [Primary Proof](https://www.indiehackers.com/post/tech/hitting-23k-mrr-in-six-months-after-five-failures-4d64o9ev4AXXhX9ogHQQ) | 1,664 (98.3% pSEO) | ❌ | `/creators/[creator_slug]` (828) + `/blog/[blog_slug]` (546) — Out-positions legacy Twitter schedulers (TweetHunter, Hypefury, Typefully) ... | [`teardowns/superx.md`](./teardowns/superx.md) |
| 16 | **Hypefury** (`hypefury.com`) | **$23,000+ MRR ($276,000+ ARR)** | `2021-08-15` | [Primary Proof](https://www.indiehackers.com/post/flying-past-23k-mrr-in-2-years-hypefury-45f73f0c0a) | 548 (85% pSEO) | ❌ | `/blog/[blog_slug]/[sub_item_slug]` (219) + `/[root-landing-slug]` (63) — Differentiated from Buffer and Hootsuite by focusing purely on audience gro... | [`teardowns/hypefury.md`](./teardowns/hypefury.md) |
| 17 | **Pirsch Analytics** (`pirsch.io`) | **$14,300 MRR (~$130,000/yr net volume)** | `2025-12-20` | [Primary Proof](https://pirsch.io/blog/our-recap-of-2025/) | 938 (84.1% pSEO) | ❌ | `/glossary/[glossary_slug]` (560) + `/atlas/[atla_slug]` (144) — Competes with GA4, Plausible, and Fathom by offering an ultra-fast Go backe... | [`teardowns/pirsch.md`](./teardowns/pirsch.md) |
| 18 | **SiteGuru** (`siteguru.co`) | **$14,000 MRR ($168,000 ARR)** | `2025-10-02` | [Primary Proof](https://www.indiehackers.com/post/tech/building-an-seo-product-to-14k-mrr-in-a-crowded-market-gU4DE1l094cpj1GjNHwu) | 254 (89.8% pSEO) | ❌ | `/seo-academy/[seo_academy_slug]` (172) + `/features/[feature_slug]` (21) — Replaces overwhelming 500-column enterprise crawlers (Screaming Frog, Ahref... | [`teardowns/siteguru.md`](./teardowns/siteguru.md) |
| 19 | **SEO Utils** (`seoutils.app`) | **~$10,400/mo ($15,800/mo founder portfolio)** | `2026-02-24` | [Primary Proof](https://www.indiehackers.com/post/tech/staying-close-to-customers-and-hitting-16k-mo-VTKxLk4uanWJbmSdG4km) | 19 (84.2% pSEO) | ❌ | `/_nuxt/[_nuxt_slug]` (13) + `/[root-landing-slug]` (2) — Eliminates $129–$499/mo recurring Ahrefs/Semrush subscriptions by offering ... | [`teardowns/seoutils.md`](./teardowns/seoutils.md) |
| 20 | **Leave Me Alone** (`leavemealone.com`) | **$10,000/mo (Open Startup verified)** | `2023-08-15` | [Primary Proof](https://leavemealone.com/blog/from-indie-side-project-to-profitable-business/) | 14,802 (98.8% pSEO) | ❌ | `/how-to-unsubscribe-from/[how_to_unsubscribe_from_slug]` (14,264) + `/blog/[blog_slug]` (153) — Competes with 'free' email cleaners (Unroll.me, which famously got caught s... | [`teardowns/leavemealone.md`](./teardowns/leavemealone.md) |

*(注：另附企业级 pSEO 天花板基准测试 **Zapier (`zapier.com`)** 实测拆解：单次抓取发现 **17,792 个 URL**，其中 `/apps/[app_slug]/integrations/[deep_slug]` 占 **17,500 页**，并同时部署了 `12.6 KB` `/llms.txt` 与 `16.5 KB` `/llms-full.txt`，完整报告位于 `../examples/pseo/zapier-com-pseo-blueprint.md`。)*

---

## 2. 横向拆解发现的 5 个反共识增长规律 / 5 Counter-Intuitive Findings Across $10k–$422k MRR Indie Sites

### 规律一：50% 的高增长独立站已经悄悄部署了 `/llms.txt`（GEO 抢位战）
在我们的实测抓取中，**Tally** (`4.3 KB`)、**Bannerbear** (`8.7 KB`)、**Simple Analytics** (`17.2 KB`)、**Papermark** (`11.9 KB` `/llms.txt` + `246 KB` `/llms-full.txt`) 和 **StandOut CV** (`270.8 KB`) 均已在根目录上线 `/llms.txt`。当用户在 ChatGPT、Claude 或 Perplexity 询问 *"best free Typeform alternative"* 或 *"open source DocSend alternative"* 时，提供结构化 Markdown 索引的独立站被 AI 引用的概率远高于纯 JS 渲染站。

### 规律二：最高效的 pSEO 不是“用 AI 批量水博客”，而是「数据库实体公开化 + 笛卡尔积路由」
- **Senja (`$50k MRR`)**：把 20 个评价来源平台 $\times$ 18 个建站工具做笛卡尔积，生成 **360 个** `/use-cases/add-[source]-to-[cms]` 页面（如 `/use-cases/add-airbnb-reviews-to-carrd`），页页直击长尾安装意图。
- **SuperX (`$23k MRR`)**：直接用自家的分析引擎预生成 **828 个** X 大 V 的公开数据分析页 `/creators/[handle]`，既截获粉丝搜索流量，又激发创作者自发转发。
- **Bannerbear (`$50k MRR`)**：把数据库里的 **319 个**设计模板全部暴露为静态 SEO 落地页 `/templates/[slug]`。

### 规律三：竞品对比页（`X Alternative` / `A vs B`）不仅写「我 vs 巨头」，更要写「巨头 A vs 巨头 B」
- **Plausible (`$83.6k MRR`)** 不仅写 `/vs-google-analytics`，还专门写了 `/matomo-vs-google-analytics`、`/fathom-analytics-vs-plausible`，在用户对比两个竞品时作为“更轻量的第三选择”完成截胡。
- **Tally (`$422k MRR`)** 在 `/help/[competitor]-alternatives` 下布局了 13 个高转化替代页，专门承接被 Typeform 涨价逼走的用户。

### 规律四：多语言子目录（`/de/`、`/es/`、`/fr/`、`/nl/`）是零边际成本的流量倍增器
- **Papermark (`$45k MRR`)** 将跑通的英文文档分享与数据室页面同步裂变出德语 `/de/` (449 页)、西语 `/es/` (449 页) 和法语 `/fr/` (448 页)，总索引页数直接跃升至 **2,732 页**，轻松吃下竞争极低的欧洲本土 B2B 搜索词。

### 规律五：定价页的胜负手在于「打穿巨头的计费痛点」与「清晰的三档锚定」
- **打穿计费维度**：Typeform 按回答数卡脖子 $\rightarrow$ Tally 免费无限回答，只收 `$29/mo` 去水印与自定义域名费；Ahrefs/Semrush 每年收 `$1,950–$4,200` $\rightarrow$ SEO Utils 收 `$69` 桌面端买断 + 几分钱 BYOK API。
- **“2 Months Free” 比 “16.7% Off” 转化更高**：Plausible、Senja、Simple Analytics 等几乎清一色在年付切换按钮上标注 **`2 months free`** 而非冷冰冰的百分比。

---

## 3. 仓库目录结构 / Repository Structure

```text
teardown-library/
├── README.md                  # 中英双语总览与横向规律总结
├── TEMPLATE.md                # 单站标准拆解模板（含合规与出处核验规范）
├── build-library.js           # 从实测 JSON 自动编译拆解报告的构建脚本
├── data/
│   └── sites.json             # 20 个万刀站的结构化索引（收入、出处、URL族、定价）
└── teardowns/                 # 20 份单站深度拆解报告
    ├── tally.md               # Tally ($422k MRR)
    ├── plausible.md           # Plausible Analytics ($83.6k MRR)
    ├── standout-cv.md         # StandOut CV (£40k / ~$52k MRR)
    ├── bannerbear.md          # Bannerbear ($50k MRR)
    ├── senja.md               # Senja ($50k MRR)
    ├── simple-analytics.md    # Simple Analytics ($45k MRR)
    ├── papermark.md           # Papermark ($45k MRR)
    ├── superx.md              # SuperX ($23k MRR)
    ├── siteguru.md            # SiteGuru ($14k MRR)
    └── seoutils.md            # SEO Utils (~$10.4k/mo)
```

---

## 4. 如何把这些套路一键装进你的项目 / Turn Teardowns into Shipped Code

看完拆解只是第一步——真正决定收入的是**把这些增长工程结构装进你自己的产品里，并且做出让人一眼信任的专业视觉质感**。我们为此打造了完整的 **Agent Skills 双剑合璧工具链**（支持 Cursor、Claude Code、Windsurf）：

### 🎨 第一步（免费开源）：用 `taste-skill` 复刻顶级 SaaS 视觉神韵
别让你的落地页带着一眼假的大模型“蓝紫渐变塑料感”。丢进任意标杆 URL（或从预热的 Linear、Stripe、Cursor、Resend 等 30 个顶级审美站中按自然语言搜索），30 秒生成精确到计算色值、字距、多层微阴影与反模式禁令的 `SKILL.md`：
```bash
# 零配置直接从 GitHub 运行（无需注册或全局安装）：
npx --yes github:WuDao0123/taste-skill find "warm editorial minimalist ai"
npx --yes github:WuDao0123/taste-skill add cursor
# （若已全局安装也可简写为 npx taste-skill add cursor）
```
👉 **在线体验与 30 站审美库预览**：[https://wudao0123.github.io/taste-skill/](https://wudao0123.github.io/taste-skill/) （GitHub: [WuDao0123/taste-skill](https://github.com/WuDao0123/taste-skill)）

### 🚀 第二步（Pro 实战套件）：用 `Growth & Monetization Agent Skills Suite` 一键生成增长基建
本开源拆解库中的所有实测数据，全部由我们的 **4 大商业化增长 Agent Skills** 自动抓取与构建。获取完整 Pro 套件，让你的 Coding Agent 直接为你执行：
1. **`pseo-competitor-teardown`**：输入任意竞品域名 $\rightarrow$ 自动抓取 `robots.txt` / 递归 `sitemap.xml` / `/llms.txt` $\rightarrow$ 拆解 URL 模板族与词根变量 $\rightarrow$ 一键生成 Next.js App Router / Astro 程序化 SEO 页面脚手架与 `/llms.txt`。
2. **`x-alternative-pages`**：自动核验竞品公开定价与特性（强制带 `verifiedAt` 与来源 URL） $\rightarrow$ 结合 `taste-skill` 视觉 Token 生成 `en` / `zh` / `ja` / `es` 四语种高转化对比页 + `FAQPage` JSON-LD + `hreflang` 互链 + 商标合规护栏。
3. **`pricing-paywall-retention`**：一键抓取竞品 `/pricing` 页结构 $\rightarrow$ 生成含锚定心理学、推荐档高亮、价值计量墙（Paywall Modal）及**合规 3 步取消挽留流（原因问卷 $\rightarrow$ 暂停/折扣/降级 $\rightarrow$ 永不隐藏的一键取消）**的 React/Tailwind 组件与 Stripe / Polar / Creem / Lemon Squeezy Webhook 模板。
4. **`launch-kit`**：内置 Apple App Store（含 100 UTF-8 字节与跨字段重词校验）、Google Play、Product Hunt、Show HN、Reddit 官方规则校验器与冷启动全套文案生成器。

### 💰 锁定定价矩阵 / Locked Pricing Matrix (One-Time Payment, Zero Subscription Fatigue)

| 档位 (Tier) | 价格 (Price) | 核心交付内容 (What You Get) |
| :--- | :--- | :--- |
| **Community / Free Tier** | **$0** *(MIT Open-Source)* | `npx taste-skill` CLI + Top 30 Flagship Aesthetic `SKILL.md`s + 本《20 个万刀站真实 SEO 与落地页拆解库》 |
| **Single Growth Skill** | **$29** *(One-time)* | 任选 4 大付费增长 Skill 中的 1 个（含对应 Node.js/Playwright 逆向脚本 + 组件模板；单买 4 个需 $116） |
| **Growth & Revenue Pro Pack 🌟** | **$69 Early-Bird** *(~~$99~~ Regular)* | **全部 4 大付费 Skills** + **5 个本地 Playwright/Node 脚本** + Next.js/Astro/React 模板 + **22 站完整原始 JSON 蓝图包（20 万刀独立站 + Skillry + Zapier + Zapier 基准）** + 终身更新 |
| **Team / Agency License** | **$169** *(One-time)* | 最多 5 人团队共享 + **不限客户项目商业交付与白标授权** + 优先新增站点拆解请求权 |

👉 **在线交互预览与获取 Growth & Monetization Agent Skills Pro 套件（早鸟价 $69）**：[https://wudao0123.github.io/taste-skill/#pricing-section](https://wudao0123.github.io/taste-skill/#pricing-section)

---

## License & Compliance
- Code & Templates: MIT License.
- All company names, logos, and trademarks mentioned in the teardowns belong to their respective owners and are analyzed strictly under nominative fair use for educational and market research purposes.
