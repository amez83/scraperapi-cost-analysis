# Web Scraping API Cost Explained: What Does ScraperAPI Actually Charge Per Request — How to Pick the Right Plan, Decode the Credit System, and Avoid Bill Shock (With Full Plan Breakdown and Cost Calculator)

So you Googled "web scraping API cost" and landed here. Same story as a lot of developers: you saw a $49/month price tag, did some rough math in your head, thought *that seems manageable*, and then three weeks later stared at a near-empty credit dashboard wondering where everything went.

Here's the thing — the headline number on any scraping API pricing page is mostly decorative. The real cost depends on what you're scraping, which features you flip on, and whether you understand the multiplier system before your billing cycle starts. This guide is specifically about ScraperAPI, one of the most popular web scraping APIs on the market, but the logic applies across most credit-based scraping platforms. By the end you'll know exactly what web scraping API cost looks like in practice — not just on paper.

---

**What Is ScraperAPI and Who Actually Uses It?**

ScraperAPI is a web scraping API that sits between your code and the open internet, handling all the infrastructure headaches: rotating proxies across 40 million+ IPs in 50+ countries, automatic CAPTCHA solving, JavaScript rendering via headless browsers, and automatic retries on failures. You send it a URL, it sends back clean HTML or parsed JSON. Simple concept, nuanced pricing.

The platform was founded in 2018 and now processes over 36 billion API requests per month for more than 10,000 brands — including Deloitte, Sony, and Alibaba. Its core audience is developer teams building automated data pipelines for e-commerce monitoring, SEO tracking, market research, and AI training data collection.

If you're non-technical — no Python, no HTTP calls — ScraperAPI probably isn't built for you. But if you write code and need large-scale, reliable scraping without maintaining your own proxy infrastructure, it's worth a serious look.

👉 [Start a free 7-day trial with 5,000 credits — no credit card needed](https://www.scraperapi.com/?fp_ref=coupons)

---

**The Credit System: Why "100,000 Credits" Doesn't Mean 100,000 Requests**

This is the most important thing to understand about web scraping API cost in general, and ScraperAPI specifically. The advertised credit number is your *budget*, not your *request count*. How far that budget stretches depends entirely on two variables: the domain you're targeting, and the feature flags you enable.

**Domain-Based Credit Multipliers**

ScraperAPI applies automatic per-domain pricing. You don't opt into this — it's applied the moment their system detects what site you're hitting:

| Domain Category | Credits per Request | Examples |
|---|---|---|
| Normal (plain HTML) | 1 | Blogs, news sites, static pages |
| E-commerce | 5 | Amazon, eBay, Walmart |
| Search engines (SERP) | 25 | Google, Bing and all subdomains |
| Social media | 30 | LinkedIn |

**Feature Flag Multipliers (Stack on Top)**

On top of domain pricing, optional parameters add extra credits:

| Parameter | Extra Credits | Notes |
|---|---|---|
| `render=true` (JavaScript rendering) | +10 | Available all plans |
| `screenshot=true` | +10 | Available all plans |
| `premium=true` (premium proxy) | +10 | Available all plans |
| `ultra_premium=true` | +30 | Paid plans only |
| Anti-bot bypass (Cloudflare, DataDome, PerimeterX) | +10 each | Auto-detected, not opt-in |
| `premium=true` + `render=true` combined | **+25 total** | Not +20 — non-linear |
| `ultra_premium=true` + `render=true` combined | **+75 total** | Not +40 — nearly double |

That last point is where a lot of people get stung. You'd expect combining two features to cost the sum of their individual costs. ScraperAPI charges more than the sum — the premium + render combo costs 25 credits extra (not 20), and ultra-premium + render costs 75 (not 40). This isn't buried in the terms of service, but it's not prominently featured on the pricing page either.

**What This Means in Real Numbers**

Take the Hobby plan: $49/month, 100,000 credits. Sounds reasonable. Now run the real math:

- Scraping plain blog pages: 100,000 requests per month ✓
- Scraping Amazon product pages (5 credits each): ~20,000 requests per month
- Scraping Google search results (25 credits each): ~4,000 requests per month
- Scraping Amazon with JavaScript rendering (5 + 10 = 15 credits): ~6,666 requests
- Scraping a Cloudflare-protected site with ultra-premium + JS rendering (75 credits): **~1,333 requests**

That last scenario works out to $36.75 per 1,000 pages — which is more expensive than many fully managed scraping services. This isn't a gotcha on ScraperAPI's part; it's just how resource-intensive bypassing enterprise anti-bot systems actually is. But it's essential math to do before choosing a plan.

> **Pro tip**: ScraperAPI's dashboard has a free [Domain Cost Estimator](https://www.scraperapi.com/?fp_ref=coupons) tool. Before running any job at scale, plug in your target URL to see the exact credit cost per request. Saves a lot of confusion later.

---

**Full ScraperAPI Plan Comparison Table**

Here's the complete current plan lineup including the new Growth-tier plans (Professional and Advanced) launched in May 2026. All plans include JavaScript rendering, premium proxy access, JSON auto-parsing, CAPTCHA/anti-bot bypass, rotating proxy pools, custom headers, session support, automatic retries, unlimited bandwidth, and a 99.9% uptime guarantee. The differences between tiers are volume, concurrency limits, and geotargeting scope.

| Plan | Monthly Price | Annual Price/mo (10% off) | API Credits/Month | Concurrent Threads | Geotargeting | Pay-as-You-Go | Purchase |
|---|---|---|---|---|---|---|---|
| **Free** | $0 | — | 1,000 | 5 | None | No |  [Get Free Access](https://www.scraperapi.com/?fp_ref=coupons) |
| **Hobby** | $49/mo | $44.10/mo | 100,000 | 20 | US & EU only | No |  [Get Hobby Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Startup** | $149/mo | $134.10/mo | 1,000,000 | 50 | US & EU only | No |  [Get Startup Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Business** | $299/mo | $269.10/mo | 3,000,000 | 100 | Global (50+ countries) | No |  [Get Business Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Scaling** | $475/mo | $427.50/mo | 5,000,000 | 200 | Global | ✓ |  [Get Scaling Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Professional** *(Growth)* | $975/mo | $877.50/mo | 10,500,000 + 250K bonus | 300 | Global | ✓ |  [Get Professional Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Advanced** *(Growth)* | $1,975/mo | $1,777.50/mo | 21,500,000 + 500K bonus | 500 | Global | ✓ |  [Get Advanced Plan](https://www.scraperapi.com/?fp_ref=coupons) |
| **Enterprise** | Custom | Custom | 22,000,000+ | 500+ | Global | ✓ |  [Contact Sales](https://www.scraperapi.com/?fp_ref=coupons) |

**Key things not immediately obvious from the table:**

- **Geotargeting is gated.** If your project needs proxies outside the US and EU (Asia, Latin America, Middle East), you need at least the Business plan. Hobby and Startup are US/EU only.
- **Pay-as-you-go is Scaling and above only.** On the lower three tiers, running out of credits mid-month means you're cut off — no overflow option. Your choices are upgrading or contacting support.
- **Credits don't roll over.** Whatever you don't use resets at renewal. Buying a plan bigger than your actual usage wastes money.
- **Analytics history** is limited to 30 days on Hobby/Startup; unlimited on Business and above.
- **The Professional and Advanced plans** are the new "Growth" tier added in May 2026 — designed for teams who've outgrown Scaling but aren't ready for custom Enterprise quotes.

---

**Effective Cost per 1,000 Requests Across Plans**

The headline price per month tells you almost nothing about cost efficiency. The number that actually matters is cost per 1,000 successful requests, which varies by plan and target type:

| Plan | Price/mo | Standard (1 credit) | E-commerce (5 credits) | SERP (25 credits) | Ultra-Premium + JS (75 credits) |
|---|---|---|---|---|---|
| Hobby | $49 | $0.49 | $2.45 | $12.25 | $36.75 |
| Startup | $149 | $0.15 | $0.75 | $3.73 | $11.18 |
| Business | $299 | $0.10 | $0.50 | $2.49 | $7.48 |
| Scaling | $475 | $0.10 | $0.48 | $2.38 | $7.13 |
| Professional | $975 | $0.09 | $0.46 | $2.29 | $6.86 |
| Advanced | $1,975 | $0.09 | $0.46 | $2.29 | $6.86 |

The efficiency gain from Hobby to Startup is massive — cost per standard request drops by 70%. From Startup to Business, the jump is smaller but you get global geotargeting and unlimited analytics. Above Scaling, you're really paying for volume, concurrent threads, and pay-as-you-go flexibility.

---

**Which Plan Should You Actually Pick?**

Let's skip the vague "it depends on your needs" non-answer and get specific.

**Free tier** — best for kicking the tires. 1,000 credits per month is enough to run maybe 200 Amazon requests or 40 Google SERP queries. Combine that with the 7-day, 5,000-credit trial you get at signup, and you have a real opportunity to test your specific targets before spending anything. Highly recommended as a first step.

**Hobby ($49/mo)** — personal projects, side projects, prototypes. If you're scraping plain web pages (not Google, not Amazon) in moderate volume, 100,000 credits genuinely covers a lot of ground. The moment you hit Amazon or need JavaScript rendering regularly, this plan gets expensive fast. It's also US/EU only for proxy geotargeting, which limits international targeting.

**Startup ($149/mo)** — small SaaS products, agencies running scraping for a handful of clients, consistent recurring jobs. The jump to 1,000,000 credits dramatically improves cost-per-request. Still US/EU only for geotargeting, which matters if your data needs aren't geographically limited to North America and Europe.

**Business ($299/mo)** — production-grade pipelines, global data collection. The key unlock here is worldwide geotargeting (50+ countries), unlimited analytics history, and 100 concurrent threads. If your team's infrastructure depends on this data being reliable and globally sourced, this is the first tier that's really built for serious operations.

**Scaling ($475/mo)** — the first plan with pay-as-you-go overflow. For teams that can't afford to be hard-stopped mid-month, this is significant. You can keep scraping past your credit limit at a predictable per-credit rate instead of scrambling to upgrade or waiting for renewal.

**Professional and Advanced ($975–$1,975/mo)** — high-volume teams that need significantly more than 5M credits monthly but want to stay out of custom Enterprise negotiations. Both plans come with limited-time credit bonuses (250K and 500K respectively, as of the May 2026 Growth plan launch) and full pay-as-you-go access.

**Enterprise (custom)** — 22M+ credits, 500+ concurrent threads, custom pricing, dedicated support. If you're at this scale, you're probably not reading a pricing guide to make your decision.

---

**Where ScraperAPI Works Well (And Where It Doesn't)**

Web scraping API cost is only half the equation. Success rate on your specific targets is the other half — because paying $0.10 per request and getting a 50% success rate is worse than paying $0.20 and getting 98%.

Independent benchmarks from Scrapeway (April 2026) show ScraperAPI's performance is sharply bimodal: excellent on major e-commerce and real estate sites, essentially useless on certain social platforms.

| Target | Success Rate | Notes |
|---|---|---|
| Zillow | 100% | Outstanding |
| Etsy | 99% | Very reliable |
| Amazon | 98% | Strong, especially with Structured Data Endpoint |
| LinkedIn | 95% | Works but expensive (30 credits/request) |
| Walmart | 93% | Solid |
| Indeed | 90% | Good |
| StockX | 84% | Moderate |
| Realtor.com | 12% | Near-failure |
| Instagram | 0% | Complete failure |
| Booking.com | 0% | Complete failure |
| Twitter/X | 0% | Complete failure |

ScraperAPI's overall average success rate is around 63%, slightly above the industry average of 58–59%. Its average response time of 5–7 seconds beats the industry average of 9.8 seconds.

The structured data endpoints for Amazon (returning 18+ parsed fields including price, ratings, BSR, reviews, images) and Google (SERP organic results, featured snippets, People Also Ask, Shopping, Maps, News, Jobs) are genuinely strong. These return clean JSON without requiring you to write your own parser — a real time-saver for smaller teams.

The place ScraperAPI explicitly can't go: **login-required pages**. Their terms of service prohibit scraping data behind authentication walls. Sessions persist (via `session_number` parameter) but the API won't handle form fills, 2FA, or complex auth flows. If login-gated content is your target, a browser-based tool is what you actually need.

---

**The DataPipeline Credit Trap (Most Reviews Skip This)**

ScraperAPI offers a no-code DataPipeline product for automated, scheduled scraping with webhook delivery — appealing if you want to collect data on autopilot without writing scheduling logic. What's easy to miss: DataPipeline uses a separate, significantly higher credit schedule.

| Request Type | Standard API Credits | DataPipeline Credits |
|---|---|---|
| Basic normal request | 1 | 6 |
| E-commerce basic | 5 | 10 |
| SERP basic | 25 | 30 |
| Ultra-premium + JS | 75 | 80 |

A basic request that costs 1 credit via the standard API costs 6 credits through DataPipeline — a 6x increase. This is documented in ScraperAPI's documentation, but it's not surfaced prominently in the DataPipeline product UI. If you set up no-code pipelines expecting standard credit costs and run a few hundred thousand requests, the bill will be very different from what you modeled.

---

**Is There a Discount Code or Promotional Offer?**

The cleanest discount available is the **automatic 10% off annual billing** — no code needed, just switch from monthly to annual at checkout. On the Hobby plan, that drops you from $49/month to $44.10. On Business, it's $269.10 instead of $299. For any plan you intend to use for a full year, this is a straightforward saving.

For new users, the 7-day free trial (5,000 credits, no credit card required) is effectively a risk-free way to test the service before spending anything. The free tier (1,000 credits/month permanently) also remains available after the trial period.

ScraperAPI also offers a **7-day no-questions-asked refund policy** — if you sign up, pay, and don't like what you see in the first week, you can get your money back.

👉 [Claim your free 7-day trial and start testing now](https://www.scraperapi.com/?fp_ref=coupons)

---

**ScraperAPI vs. Competitors: How Does the Cost Compare?**

At the ~$300/month tier, here's how web scraping API cost compares across common scraping scenarios:

**Basic HTML scraping (no JS rendering, no premium proxy):**

| Provider | ~$300/mo Plan | Cost per 1,000 requests |
|---|---|---|
| ScrapingBee | Business $249 | $0.08 |
| ScraperAPI | Business $299 | $0.10 |
| Scrapfly | Startup $250 | $0.10 |
| ZenRows | Business $300 | $0.28 |
| Bright Data | Pay-as-you-go | $1.50 |

**JavaScript rendering required:**

| Provider | ~$300/mo Plan | Cost per 1,000 requests |
|---|---|---|
| ScrapingBee | Business $249 | $0.42 |
| Scrapfly | Startup $250 | $0.60 |
| ScraperAPI | Business $299 | $1.00 |
| ZenRows | Business $300 | $1.40 |
| Bright Data | Pay-as-you-go | $1.50 |

**Premium/residential proxy + JS rendering (anti-bot-protected sites):**

| Provider | ~$300/mo Plan | Cost per 1,000 requests |
|---|---|---|
| Bright Data | Pay-as-you-go | $1.50 |
| ScrapingBee | Business $249 | $2.08 |
| ScraperAPI | Business $299 | $2.49 |
| Scrapfly | Startup $250 | $3.10 |
| ZenRows | Business $300 | $7.00 |

ScraperAPI is competitive — not always the cheapest, not the most expensive. For plain HTML scraping, ScrapingBee edges it out slightly. For heavily protected sites requiring premium proxies and rendering, ScraperAPI and ScrapingBee sit in a similar range, with Bright Data's flat-rate model being the most predictable option regardless of rendering needs. ZenRows is notably expensive for protected site scenarios.

---

**What Real Users Actually Say**

Review aggregates from multiple platforms give a consistent picture:

| Platform | Rating | Reviews |
|---|---|---|
| Trustpilot | 4.5/5 | 43 reviews |
| Capterra | 4.6/5 | 62 reviews |
| G2 | 4.4/5 | 16 reviews |

Capterra sub-ratings: Ease of Use **4.9/5**, Customer Service **4.6/5**, Features **4.5/5**, Value for Money **4.5/5**.

The praise is consistent across platforms: easy integration (you can often drop ScraperAPI in as a proxy replacement with minimal code changes), clean documentation, responsive support, and reliable performance on mainstream e-commerce and SERP targets.

The criticism is also consistent: the credit math surprised people who didn't run the multiplier calculations upfront. One Capterra reviewer noted "the breakdown of credit costs can be confusing." A Reddit thread documented a user being quoted a price per credit, then discovering domain multipliers applied post-payment — effectively an 80% shortfall from expected capacity.

There's also a segment of users who found the service less reliable at scale on harder, frequently-rotating anti-bot targets. For difficult sites that regularly update their protection systems, performance can degrade and require support intervention.

The practical takeaway: use the free trial to test your specific targets *before* committing. Don't assume the headline numbers apply to your use case.

---

**Five Things to Do Before Spending Money on Any Scraping API**

Having gone through all of this, here's the actual workflow that saves most people from billing surprises:

1. **Sign up for the free trial.** 5,000 credits, no card required. Run your actual target URLs through it — not example.com or a Wikipedia page. Your real targets.

2. **Use the Domain Cost Estimator.** Available in the ScraperAPI dashboard, it tells you the exact credit cost for any URL with any parameter combination before you run a batch job.

3. **Calculate your monthly request volume.** If you need 500,000 Amazon page scrapes per month, that's 2.5 million credits minimum (5 credits each) — which puts you on the Business plan, not Hobby.

4. **Account for JS rendering separately.** If you need `render=true`, add 10 credits to every request in your calculation. If you need `premium=true` + `render=true`, add 25 instead of 20.

5. **Choose whether you need pay-as-you-go.** If your scraping volume is unpredictable month-to-month, the hard credit cap on Hobby/Startup/Business is a real operational risk. Scaling and above give you overflow capacity.

👉 [Start your free ScraperAPI trial — 5,000 credits, no credit card required](https://www.scraperapi.com/?fp_ref=coupons)

---

**Practical Tips to Stretch Your Credits Further**

Once you're on a plan, a few habits make a measurable difference in how far your credits go:

- **Disable JS rendering unless the site requires it.** Many sites serve clean HTML without rendering. Test first; adding `render=true` blindly costs 10 credits per request unnecessarily.
- **Use the Structured Data Endpoints for Amazon and Google.** SDEs return parsed JSON without requiring you to write and maintain custom parsers. For those specific targets, they're often worth the credit premium.
- **Set spending limits on PAYG.** ScraperAPI lets you cap monthly pay-as-you-go spending so you don't get surprise overages. Use this.
- **Check the sa-credit-cost response header.** Every API response includes this header showing the actual credits consumed. Parse it in your logging to monitor real costs in real-time.
- **Use the API Playground** before running batch jobs. It's a lightweight way to verify a target URL's behavior and cost without committing a large credit block to an exploratory run.

---

**Bottom Line: What Does Web Scraping API Cost Actually Look Like With ScraperAPI?**

At the simplest: $49/month if you're scraping plain pages in modest volume. Significantly more — potentially $299 or above — if your targets include Amazon, Google, globally distributed sites, or heavily protected domains.

ScraperAPI is a solid choice for developer teams hitting mainstream e-commerce, SERP, and real estate targets. The infrastructure is robust, the documentation is above average, and the structured data endpoints for Amazon and Google are genuinely useful. Where it struggles: social media (Instagram and Twitter/X are essentially non-functional), login-gated content, and any target with aggressive, frequently-changing anti-bot systems.

The single most important thing before picking a plan: run the multiplier math for your specific use case. The effective cost per request — not the headline plan price — is what determines whether ScraperAPI is affordable for your workload.

The trial period exists precisely for this. 5,000 credits, no card required. Spend a day testing your targets, watch the credit dashboard, and do the extrapolation. You'll know exactly which plan fits before committing to anything.

👉 [Try ScraperAPI free — 5,000 credits, 7 days, no credit card required](https://www.scraperapi.com/?fp_ref=coupons)
