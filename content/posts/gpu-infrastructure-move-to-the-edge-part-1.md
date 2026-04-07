---
title: "GPU Infrastructure Will Move to the Edge (Part 1)"
date: 2026-03-06T10:00:00-05:00
draft: false
tags: ["AI", "Cloud Computing", "Infrastructure", "DePIN"]
categories: ["Tech Trends", "Consulting"]
author: "Daniel Peña Chaves"
description: "By 2030, data centers are projected to require $6.7 trillion worldwide in capital expenditures yet this bet is hitting reality checks"
---

By the time of writing this, we are two years into the largest infrastructure spending cycle in the history of the technology industry — nearly $700 billion committed in 2026 alone, *much of it borrowed against future revenues that don’t yet exist.*

Amazon Web Services (AWS) launched in 2006 with a simple premise: instead of every company buying and maintaining its own servers, they could rent compute from a shared pool, on demand. The economics were compelling. A data center running at 80% utilization is dramatically more efficient than thousands of corporate server rooms limping along at 15%. Centralization meant shared cooling, shared power infrastructure, shared security, shared staffing — and the savings compounded with scale.

By late 2025, the three dominant players — **AWS, Microsoft Azure, and Google Cloud — controlled roughly two-thirds of global cloud infrastructure services spending, cementing their grip on the market.** What they built works . For most enterprise workloads — databases, web applications, storage, analytics — centralized cloud remains the most cost-effective, reliable, and secure option available.

Yet the centralized cloud was engineered for predictable, enterprise workloads — not the relentless, always-on demand of frontier AI training and inference. What once scaled with elegant efficiency is now colliding with physics, geography, and geopolitics in ways the original architects never anticipated.

![BIG-5 Combined Capex Trajectory](/images/posts/big5.png)
<p align="center">
  <em><strong>Figure 1:</strong> BIG-5 Combined Capex Trajectory (2023–2028). Actual + projected spend. Sources: Bloomberg, CreditSights, Futurum Group (Feb 2026), Morgan Stanley, CNBC, Axios.</em>
</p>

We are effectively living the “AI arms race”. The chart above captures the trajectory: combined Big-5 capex rocketing from hundreds of billions toward trillions, with AI claiming ~75% of the pie and projections showing no slowdown in sight.

Amazon staring down negative free cash flow, Alphabet turning to century-long bonds, Meta plowing $115–135 billion into AI infrastructure this year — a staggering 60–90% jump from last year’s spend — Microsoft dropping a record $80 billion in a single fiscal year, while Oracle sprints to catch up.

**And it still won’t be enough.**

By 2030, data centers are projected to require $6.7 trillion worldwide in capital expenditures — with $5.2 trillion dedicated specifically to AI-ready infrastructure. **That’s more than Germany’s GDP** (~$5.1 trillion in 2026 projections), crammed into five years of frantic building.

However the $6.7 trillion infrastructure bet is already running into walls no amount of capital can move.

### What “AI-Ready” Infrastructure Actually Means

Training a frontier AI model requires thousands of GPUs running in tight coordination, connected by ultra-high-bandwidth interconnects that transfer data between chips so fast they make the best fiber connections look almost like dial-up in comparison.

The density of compute in a single AI rack generates so much heat that traditional air cooling — the default for decades — is no longer sufficient. Modern AI facilities require direct liquid cooling: water or dielectric fluid running through or across the chips themselves.

A standard server rack consumes 5–15 kilowatts. A dense GPU cluster rack can draw 60–120 kW. Scale that across a 100-megawatt campus, and you have a facility that consumes as much electricity as a city — continuously, not at peak.

The cost of training reflects this too. A medium-sized model (7–13B parameters) can be trained for $1,000–$10,000. A large model at 70B+ parameters exceeds $300,000 while frontier models cost millions. And all these ranges keep increasing as newer models become more complex.

Press enter or click to view image in full size

Nearly 100 GW of new data centers will be added between 2026 and 2030, doubling global capacity. **But communities increasingly don’t want them**. The combination of power consumption, water usage, and minimal local employment creates perfect conditions for NIMBY — Not In My Backyard — opposition.

## Power, Water, and Geography

![AI Data Centers Share of US Electricity Grid](/images/posts/shareus.png)
<p align="center">
  <em><strong>Figure 2:</strong> AI data centers' share of US electricity grid (2023–2030) Projections. Sources: McKinsey, IEA, Goldman Sachs, EIA.</em>
</p>

In 2023, data centers consumed 26% of Virginia’s total electricity supply, with significant shares in North Dakota (15%), Nebraska (12%), Iowa (11%) and Oregon (11%). These aren’t abstract grid statistics or projections. They translate directly into higher bills for everyone nearby — it’s expected that U.S. households could see electricity costs rise 8% by 2030 on average, exceeding 25% in the most affected markets.

Power is only part of the story. Data centers consumed approximately 17 billion gallons of water for cooling in 2023 alone — and **that figure is projected to double or quadruple by 2028**. Not industrial wastewater. Potable water. The same water that comes out of household taps and irrigates crops in some regions that are already water-stressed.

![Estimated Water Consumption](/images/posts/watercons.png)
<p align="center">
  <em><strong>Figure 3:</strong> Estimated water consumption by facility type. Sources: Brookings Institution, Meta filings, Goldman Sachs, Uptime Institute.</em>
</p>

## When Infrastructure Becomes a Target

On March 2nd, 2026, Iranian drone strikes hit three Amazon Web Services facilities in the Middle East — two in the UAE directly struck, one in Bahrain damaged by a nearby impact. Structural damage, power disruptions, and water damage from fire suppression knocked all three facilities offline. Banking apps, payments platforms, and enterprise software providers across the region went down with them.

![Capital Committed to Middle East Cloud](/images/posts/caprisk.png)
<p align="center">
  <em><strong>Figure 4:</strong>Capital committed to Middle East cloud regions(2022–2036).
Sources: AWS UAE Economic Impact Study (2022), Microsoft UAE investment announcement (Nov 2025), Google Cloud–Saudi PIF AI partnership announcement (2025), Gulf Data Hub and industry investment estimates.
</em>
</p>

These were the first known military strikes on a physical cloud infrastructure. **As AI becomes more central to military and government operations, the facilities running it become high-value targets**. The more critical the infrastructure, the more attractive it becomes to strike.

The internet was architected to route around damage. The hyperscale AI buildout is doing the opposite: concentrating critical compute into fewer, larger, more identifiable locations. The bigger the campus, the bigger the target.

## A System Under Stress

The centralized cloud model worked brilliantly when compute demand was linear and predictable. *But AI has changed the equation — and the cracks are showing.*

Power grid capacity, water supplies, and community opposition are creating 24–72 month delays on new facilities.

The majority of global AI compute runs through a handful of metros — Northern Virginia, Frankfurt, Singapore, Dublin, Tokyo. Lose one to a grid failure, a natural disaster, or a conflict — as the attacks on AWS just demonstrated — and entire regions lose access overnight.

The economics are breaking for everyone except the biggest players. Compute now consumes 50–70% of an AI startup’s budget before a single dollar goes to talent, sales, or operations. Startups aren’t negotiating on price — they’re negotiating for access.

## The Infrastructure That Already Exists

While hyperscalers continue pouring concrete into ever-larger campuses, a parallel infrastructure is quietly taking shape — one that doesn’t require new power plants, rezoned land, or multi-year construction timelines. It draws from what already exists: millions of underutilized GPUs sitting in data centers, research labs, gaming rigs, and enterprise servers around the world.

This is Decentralized Physical Infrastructure (DePIN) — a system that coordinates idle hardware into on-demand clusters capable of training models, running inference, and rendering at scale.

This shift isn’t theoretical. By early 2026, networks like Render, io.net, and Akash have demonstrated real traction. Render continues to process millions of frames monthly while expanding into AI workloads; io.net aggregates thousands of verified GPUs across dozens of countries for cluster-ready AI tasks; Akash offers a decentralized marketplace where developers deploy models directly onto global hardware at fractions of hyperscaler prices.

What makes this viable at scale comes down to three interlocking pieces: architecture that treats the planet as a single, elastic supercomputer; verification systems that cryptographically attest hardware specs and output integrity; and job matching economics that function like real-time auctions, aligning idle resources toward the highest-value work.

The hyperscale race is meeting its natural limits. Meanwhile, DePIN is assembling the alternative from hardware that’s already online — turning excess capacity into the next layer of AI infrastructure. The edge isn’t coming. It’s already here.

In the next article, we’ll explore how DePIN works — the architecture, verification systems, job matching economics, and real-world deployments that make distributed GPU compute possible.

# Sources

*Infrastructure & Capex*

McKinsey & Company (April 2025): “The Cost of Compute: A $7 Trillion Race to Scale Data Centers” https://www.mckinsey.com/industries/technology-media-and-telecommunications/our-insights/the-cost-of-compute-a-7-trillion-dollar-race-to-scale-data-centers

McKinsey & Company (October 2025): “Beyond Compute: Infrastructure that Powers and Cools AI Data Centers” https://www.mckinsey.com/industries/industrials/our-insights/beyond-compute-infrastructure-that-powers-and-cools-ai-data-centers

CNBC (January 2025): “Microsoft expects to spend $80 billion on AI-enabled data centers in fiscal 2025” https://www.cnbc.com/2025/01/03/microsoft-expects-to-spend-80-billion-on-ai-data-centers-in-fy-2025.html

CNBC (February 2026): “Tech AI spending approaches $700 billion in 2026, cash taking big hit” https://www.cnbc.com/2026/02/06/google-microsoft-meta-amazon-ai-cash.html

Futurum Group (February 2026): “AI Capex 2026: The $690B Infrastructure Sprint” https://futurumgroup.com/insights/ai-capex-2026-the-690b-infrastructure-sprint/

Fortune (February 2026): “Big Tech approaches ‘red flag’ moment: AI capex is so great hyperscalers could go cash-flow negative” https://fortune.com/2026/02/17/ai-tech-red-flag-capex-hyperscalers-cash-flow-negative-evercore/

Fortune (December 2025): “Oracle slides by most since January on mounting AI spending” https://fortune.com/2025/12/11/oracle-earnings-stock-falls-11-percent-why-investors-disappointed-data-centers-cloud/

Data Centre Magazine (October 2025): “Oracle’s Data Centre Strategy: Cloud, AI and More Capacity” https://datacentremagazine.com/news/oracles-data-centre-strategy-cloud-ai-and-more-capacity

IEEE ComSoc Technology Blog (December 2025): “Hyperscaler capex > $600bn in 2026, a 36% increase over 2025” https://techblog.comsoc.org/2025/12/22/hyperscaler-capex-600-bn-in-2026-a-36-increase-over-2025-while-global-spending-on-cloud-infrastructure-services-skyrockets/

TechCrunch (February 2026): “The billion-dollar infrastructure deals powering the AI boom” https://techcrunch.com/2026/02/28/billion-dollar-infrastructure-deals-ai-boom-data-centers-openai-oracle-nvidia-microsoft-google-meta/

*Power & Water*

Goldman Sachs (February 2025): “AI to Drive 165% Increase in Data Center Power Demand by 2030” https://www.goldmansachs.com/insights/articles/ai-to-drive-165-increase-in-data-center-power-demand-by-2030

Uptime Institute (July 2025): Global Data Center Survey 2025 https://uptimeinstitute.com/resources/research-and-reports/uptime-institute-global-data-center-survey-results-2025

Uptime Institute Blog (May 2025): “Water is Local: Generalities Do Not Apply” https://journal.uptimeinstitute.com/water-is-local-generalities-do-not-apply/

*AI Compute Growth*

Stanford HAI (2025): AI Index Report 2025 https://aiindex.stanford.edu/report/

Epoch AI (January 2026): “Global AI Computing Capacity is Doubling Every 7 Months” https://epoch.ai/data-insights/ai-chip-production

Epoch AI (January 2026): “Global AI Power Capacity is Now Comparable to Peak Power Usage of New York State” https://epoch.ai/data-insights/ai-datacenter-power

*Geopolitical Risk — AWS Middle East Strikes*

CNBC (March 2, 2026): “Amazon says drone strikes damaged 3 facilities in UAE and Bahrain” https://www.cnbc.com/2026/03/02/amazon-says-drone-strikes-damaged-3-facilities-in-uae-and-bahrain.html

CNBC (March 3, 2026): “Banking, payments services disrupted after Amazon UAE data centers hit in drone strikes” https://www.cnbc.com/2026/03/03/iran-war-uae-drone-strikes-aws-data-centers.html

CNBC (March 4, 2026): “Amazon’s Bahrain data center targeted by Iran for support of U.S. military, state media says” https://www.cnbc.com/2026/03/04/amazon-bahrain-data-centers-targeted-iran-drone-strike.html

Rest of World (March 2, 2026): “Amazon Fire in UAE: The End of the Gulf’s Safe AI Promise?” https://restofworld.org/2026/amazon-uae-data-center-fire-iran-strike/

Rest of World (March 4, 2026): “Iranian Strikes at Amazon Sites Raise Alarms” https://restofworld.org/2026/iran-amazon-data-center-strikes/

Rest of World (March 5, 2026): “U.S.-Iran War Threatens Gulf AI Infrastructure as Both Data Chokepoints Close” https://restofworld.org/2026/us-iran-war-gulf-ai-submarine-cables/

The Register (March 2, 2026): “AWS Says Drones Hit Two of Its Datacenters in UAE” https://www.theregister.com/2026/03/02/amazon_outages_middle_east/

Fortune (March 3, 2026): “Iran’s Revenge: Drones Damage Data Centers for Amazon Web Services” https://fortune.com/2026/03/03/irans-revenge-drones-damage-data-centers-for-amazon-web-services-reveal-wests-achilles-heel/

Bloomberg (March 3, 2026): “Drone Strikes Damage Amazon Data Centers in the UAE and Bahrain” https://www.bloomberg.com/news/articles/2026-03-03/drone-strikes-damage-amazon-data-centers-in-the-uae-and-bahrain

CBS News (March 2, 2026): “Amazon Says Drones Hit 3 of Its Middle East Data Centers Amid Iran Conflict” https://www.cbsnews.com/news/amazon-drone-strike-aws-data-center-uae-bahrain-iran/

DefenseScoop (March 3, 2026): “Commercial Data Centers Emerge as Targets in Modern Warfare After Drones Hit 3 AWS Facilities” https://defensescoop.com/2026/03/03/commercial-data-centers-drone-warfare-amazon-aws/