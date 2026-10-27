# 独立开发者万刀站真实 SEO 与落地页拆解库
## The $10k+ MRR Indie SaaS SEO & Landing Page Teardown Library

[![Verified Revenue Only](https://img.shields.io/badge/Revenue_Data-100%25_Founder_Verified-10b981)](#1-首批收录的-10-个万刀独立站索引--verified-10k-mrr-indie-saas-index)
[![Zero Paid APIs](https://img.shields.io/badge/Methodology-Live_Sitemap_%2B_DOM_%2B_llms.txt-6366f1)](#2-硬核拆解方法论--zero-fluff-methodology)
[![Powered by Agent Skills](https://img.shields.io/badge/Built_With-Taste_%26_Growth_Agent_Skills-f59e0b)](#4-如何把这些套路一键装进你的项目--turn-teardowns-into-shipped-code)

> **中文导读**：大多数独立开发者写得出好代码，却卡在「不知道做什么 SEO 页面能带来精准注册」、「不知道对比页怎么写才不违规又有转化」、「不知道定价页怎么锚定」。本开源库严选 **创始人公开披露过月收入 ≥ $10,000 MRR（附一手出处 URL 与披露日期）** 的真实独立开发者/自举（Bootstrapped）SaaS 站点，用自动化脚本直接拆解它们的 **`robots.txt`、`sitemap.xml` 全量 URL 路由树、`/llms.txt` AI 搜索索引、首屏 H1/Schema 结构与真实定价页心理设计**。**绝不编造流量数字，绝不用第三方估算水份，只看真金白银跑出来的页面工程结构。**
>
> **English Summary**: Most indie hackers can ship great code, yet stall on distribution, programmatic SEO (pSEO), comparison pages, and pricing psychology. This open-source repository reverse-engineers **bootstrapped & indie SaaS products with publicly verified revenue $\ge$ $10,000 MRR** (every single revenue figure cites a primary founder disclosure URL and date). Using deterministic Node.js + Playwright scripts, we inspect their live `robots.txt`, recursive `sitemap.xml` URL trees, `/llms.txt` AI search indexes, above-the-fold copy, and `/pricing` architecture. **Zero fabricated traffic estimates. Zero paid SEO APIs. 100% reproducible engineering patterns.**

---

## 1. 首批收录的 10 个万刀独立站索引 / Verified $10k+ MRR Indie SaaS Index

| # | 站点 (Product) | 公开披露收入 (Verified Revenue) | 披露日期 (Date) | 一手出处 (Primary Source) | 实测索引页数 (URLs) | `/llms.txt` 状态 | 核心程序化 SEO / 增长杀手锏 (Primary pSEO & Growth Wedge) | 深度拆解报告 (Teardown) |
| :- | :--- | :--- | :--- | :--- | ---: | :--- | :--- | :--- |
| 1 | **Tally** (`tally.so`) | **$422,000 MRR** ($5M ARR) | `2026-04-15` | [Official Blog](https://blog.tally.so/the-road-from-4m-to-5m-arr/) / [IH $150k](https://www.indiehackers.com/post/bootstrapping-tally-to-150k-mrr-by-doing-less-better-68e340156f) | 445 (92.8% pSEO) | ✅ `4.3 KB` | 179 个 `/templates/[cat]/[slug]` + 13 个 `/help/[comp]-alternatives` + 免费无限表单病毒徽章 | [`teardowns/tally.md`](./teardowns/tally.md) |
| 2 | **Plausible** (`plausible.io`) | **$83,637 MRR** ($1M+ ARR) | `2022-06-02` | [Official Blog](https://plausible.io/blog/open-source-saas) | 180 (83.3% pSEO) | ❌ | 8 个高转化 `/[a]-vs-[b]` 对比页（含竞品互打 `matomo-vs-ga`）+ 26 个根路径工具页（`/ad-cost-calculator`） | [`teardowns/plausible.md`](./teardowns/plausible.md) |
| 3 | **StandOut CV** (`standout-cv.com`) | **£40,000 MRR** (~$52,000/mo) | `2025-09-25` | [Indie Hackers](https://www.indiehackers.com/post/how-i-grew-my-saas-business-to-40k-mrr-with-seo-3287452853) | 1,103 (98.7% pSEO) | ✅ `270.8 KB` | 809 个英国岗位 `/cv-examples/[cat]/[role]` + 43 个美国 `/usa/resume-examples/[role]` + 31 个外链诱饵 `/stats/[slug]` | [`teardowns/standout-cv.md`](./teardowns/standout-cv.md) |
| 4 | **Bannerbear** (`bannerbear.com`) | **$50,000 MRR** (~$600k ARR) | `2023-07-15` | [/open Page](https://www.bannerbear.com/open/) / [Founder Blog](https://www.bannerbear.com/blog/7-lessons-growing-a-bootstrapped-saas-to-50k-mrr/) | 1,372 (98.5% pSEO) | ✅ `8.7 KB` | 319 个公开数据库模板页 `/templates/[slug]` + 90 个场景页 `/use-cases/scenarios/[slug]` + 8 个免费工具 `/tools/[slug]` | [`teardowns/bannerbear.md`](./teardowns/bannerbear.md) |
| 5 | **Senja** (`senja.io`) | **$50,000 MRR** ($600k ARR) | `2024-11-19` | [Indie Hackers](https://www.indiehackers.com/post/from-zero-to-50k-mrr-the-story-of-senjas-growth-6874d85edd) | 733 (96.9% pSEO) | ❌ | 笛卡尔积场景页 `/use-cases/add-[source]-to-[cms]` (360 页) + `/testimonial-examples/[slug]` (112 页) + `/compare/[comp]-alternatives` (19 页) | [`teardowns/senja.md`](./teardowns/senja.md) |
| 6 | **Simple Analytics** (`simpleanalytics.com`) | **$45,000 MRR** ($540k ARR) | `2025-10-15` | [Indie Hackers](https://www.indiehackers.com/post/tech/joining-a-technical-co-founder-and-growing-the-product-to-45k-mrr-119Zbnde7pTET0QOiZLH) | 487 (81.7% pSEO) | ✅ `17.2 KB` | 76 个合规痛点与竞品根路径页（`/analytics-without-consent`、`/piwik-pro-alternative`）+ 14 天自服试用/30 天 POC 双漏斗 | [`teardowns/simple-analytics.md`](./teardowns/simple-analytics.md) |
| 7 | **Papermark** (`papermark.com`) | **$45,000 MRR** ($540k ARR) | `2025-08-20` | [Indie Hackers](https://www.indiehackers.com/post/tech/after-11-failed-products-this-founder-hit-45k-mrr-in-a-little-over-a-year-xyRkxAsD8Rys7URjYd5d) | 2,732 (96.6% pSEO) | ✅ `11.9 KB` + `246 KB` full | 4 语言多目录裂变（`en` + `/de/` 449 页 + `/es/` 449 页 + `/fr/` 448 页）+ 开源 DocSend 替代品定位 + 投资人名录钩子 | [`teardowns/papermark.md`](./teardowns/papermark.md) |
| 8 | **SuperX** (`superx.so`) | **$23,000 MRR** ($276k ARR) | `2025-09-10` | [Indie Hackers](https://www.indiehackers.com/post/tech/hitting-23k-mrr-in-six-months-after-five-failures-4d64o9ev4AXXhX9ogHQQ) | 1,664 (98.3% pSEO) | ❌ | 828 个公开创作者分析页 `/creators/[handle]` + 19 个国家趋势页 `/twitter-trends/[country]` + 6 个竞品对比页 `/superx-vs-[comp]` | [`teardowns/superx.md`](./teardowns/superx.md) |
| 9 | **SiteGuru** (`siteguru.co`) | **$14,000 MRR** ($168k ARR) | `2025-10-02` | [Indie Hackers](https://www.indiehackers.com/post/tech/building-an-seo-product-to-14k-mrr-in-a-crowded-market-gU4DE1l094cpj1GjNHwu) | 254 (89.8% pSEO) | ❌ | 16 个免费在线检测微工具 `/free-seo-tools/[slug]` + 172 篇 `/seo-academy/[slug]` + 荷兰语 `/nl/` 多语言覆盖 | [`teardowns/siteguru.md`](./teardowns/siteguru.md) |
| 10 | **SEO Utils** (`seoutils.app`) | **~$10,400/mo** ($15.8k 组合) | `2026-02-24` | [Indie Hackers](https://www.indiehackers.com/post/tech/staying-close-to-customers-and-hitting-16k-mo-VTKxLk4uanWJbmSdG4km) | 19 (DOM 发现) | ❌ | 桌面端买断制（`$69` + BYOK API 按量几分钱）直接锚定 Semrush/Ahrefs 每年 `$4,200` 订阅费 + 新概念页 `/fan-out-query` | [`teardowns/seoutils.md`](./teardowns/seoutils.md) |

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
│   └── sites.json             # 10 个万刀站的结构化索引（收入、出处、URL族、定价）
└── teardowns/                 # 10 份单站深度拆解报告
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
npx taste-skill find "warm editorial minimalist ai"
npx taste-skill add cursor
```
👉 **在线体验与 30 站审美库预览**：`{{B_TASTE_SKILL_WEB_URL}}`

### 🚀 第二步（Pro 实战套件）：用 `Growth & Monetization Agent Skills Suite` 一键生成增长基建
本开源拆解库中的所有实测数据，全部由我们的 **4 大商业化增长 Agent Skills** 自动抓取与构建。获取完整 Pro 套件，让你的 Coding Agent 直接为你执行：
1. **`pseo-competitor-teardown`**：输入任意竞品域名 $\rightarrow$ 自动抓取 `robots.txt` / 递归 `sitemap.xml` / `/llms.txt` $\rightarrow$ 拆解 URL 模板族与词根变量 $\rightarrow$ 一键生成 Next.js App Router / Astro 程序化 SEO 页面脚手架与 `/llms.txt`。
2. **`x-alternative-pages`**：自动核验竞品公开定价与特性（强制带 `verifiedAt` 与来源 URL） $\rightarrow$ 结合 `taste-skill` 视觉 Token 生成 `en` / `zh` / `ja` / `es` 四语种高转化对比页 + `FAQPage` JSON-LD + `hreflang` 互链 + 商标合规护栏。
3. **`pricing-paywall-retention`**：一键抓取竞品 `/pricing` 页结构 $\rightarrow$ 生成含锚定心理学、推荐档高亮、价值计量墙（Paywall Modal）及**合规 3 步取消挽留流（原因问卷 $\rightarrow$ 暂停/折扣/降级 $\rightarrow$ 永不隐藏的一键取消）**的 React/Tailwind 组件与 Stripe / Polar / Creem / Lemon Squeezy Webhook 模板。
4. **`launch-kit`**：内置 Apple App Store（含 100 UTF-8 字节与跨字段重词校验）、Google Play、Product Hunt、Show HN、Reddit 官方规则校验器与冷启动全套文案生成器。

### 💰 锁定定价矩阵 / Locked Pricing Matrix (One-Time Payment, Zero Subscription Fatigue)

| 档位 (Tier) | 价格 (Price) | 核心交付内容 (What You Get) |
| :--- | :--- | :--- |
| **Community / Free Tier** | **$0** *(MIT Open-Source)* | `npx taste-skill` CLI + Top 30 Flagship Aesthetic `SKILL.md`s + 本《10 个万刀站真实 SEO 与落地页拆解库》 |
| **Single Growth Skill** | **$29** *(One-time)* | 任选 4 大付费增长 Skill 中的 1 个（含对应 Node.js/Playwright 逆向脚本 + 组件模板；单买 4 个需 $116） |
| **Growth & Revenue Pro Pack 🌟** | **$69 Early-Bird** *(~~$99~~ Regular)* | **全部 4 大付费 Skills** + **5 个本地 Playwright/Node 脚本** + Next.js/Astro/React 模板 + **11 站完整原始 JSON 蓝图包** + 终身更新 |
| **Team / Agency License** | **$169** *(One-time)* | 最多 5 人团队共享 + **不限客户项目商业交付与白标授权** + 优先新增站点拆解请求权 |

👉 **在线交互预览与获取 Growth & Monetization Agent Skills Pro 套件（早鸟价 $69）**：`{{A_GROWTH_SKILLS_PRO_URL}}`

---

## License & Compliance
- Code & Templates: MIT License.
- All company names, logos, and trademarks mentioned in the teardowns belong to their respective owners and are analyzed strictly under nominative fair use for educational and market research purposes.


---

## 🚀 Upgrade to the Full B + A Agent Skills Arsenal

1. **Free Open-Source Hook (B) — `taste-skill` CLI (30 Flagship Sites)**:
   ```bash
   npx taste-skill find "dark precision saas"
   npx taste-skill add linear
   npx taste-skill extract https://stripe.com
   ```
2. **Executable Growth & Revenue Agent Skills Pro Suite (A)**:
   - **Single Growth Skill**: **$29 USD** (One-time · Choose any 1 Pro Skill; buying all 4 individually costs $116)
   - **Growth & Revenue Pro Pack (Most Popular 🌟)**: **$69 USD Early-Bird** (~~$99~~ Regular · Save $47 vs. single skills · Less than half of Skillry $169) — Includes all 4 Paid Skills (`pseo-competitor-teardown`, `x-alternative-pages`, `pricing-paywall-retention`, `launch-kit`), 5 local Playwright/Node crawlers, Next.js/React components, and 11 raw JSON blueprints.
   - **Team & Agency License**: **$169 USD** (One-time · Up to 5 seats + Unlimited client white-label rights)
