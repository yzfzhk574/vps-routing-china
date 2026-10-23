# unmanaged vps: what you actually run yourself, when $29/month for China routing is worth it, and which GoMami plan to pick

An unmanaged VPS is capacity plus keys. The provider keeps the hypervisor, the physical host and the network path to your VM alive; you own everything from the guest OS upward — kernel and package updates, firewall rules, SSH hygiene, the web stack, backups and restores. Nobody patches your box for you.

That definition makes the price spread in this category look odd. Across the unmanaged market, the median entry plan runs about **$5.95/month**, and the median renewal among hosts that publish one is **$7.99/month**. GoMami's cheapest plan is **$29/month**. Same category, roughly five times the money, and the company doesn't pretend otherwise — its own positioning is "China route first," not "cheapest box in the rack."

So the useful question isn't whether GoMami wins a price-per-core contest. It's whether paying that premium buys you something an unmanaged box is supposed to buy: predictable performance on a network you don't control.

> **Quick pick, if you're deciding now:** the cheapest way into GoMami's China-optimized routing is the **Nano at $29/month** in Japan, Singapore or Los Angeles (2 vCPU, 2GB RAM, 40GB NVMe, 500GB–1TB traffic). Hong Kong starts at $49. If your users are in mainland China and you're comfortable being your own sysadmin, that's the entry point — 👉 [check the Japan Nano at $29/month before you commit](https://gomami.io/aff.php?aff=415&pid=13&billingcycle=monthly). If all you need is the cheapest Linux box on earth, close this tab; the market has $6 options and this isn't one of them.

## What "unmanaged" actually splits between you and the provider

The provider owns the hypervisor, the host hardware, connectivity to your VM, and the CPU/RAM/disk slice you bought. You own the operating system and every process running on it.

| Area | Provider | You |
| --- | --- | --- |
| Hypervisor, host hardware | Yes | No |
| Network path to the VM | Yes | No |
| Allocated CPU / RAM / disk | Yes, per plan | You pick the plan |
| Guest OS and updates | No | Yes |
| Firewall, SSH hardening | No | Yes |
| App stack, monitoring | No | Yes |
| Backups and restore drills | No | Yes |

That split is why unmanaged plans are cheap: you're buying hardware and bandwidth, and the labor is yours. It also explains a common mistake — treating a $6 VPS as a $6 hosting package. Managed entry tiers generally start around $15–30/month because someone else is doing the patching, monitoring and basic hardening.

GoMami sits on the "you do the work" side of that line, even though the word *unmanaged* doesn't appear on its site. What is documented is the toolkit that lets you behave like an unmanaged customer: a VirtFusion-based control panel with one-click OS rebuild, a custom ISO option for anything not in the template list, real-time CPU, memory and network graphs, and a RESTful API for programmatic management. The official docs are written as self-service instructions — how to purchase an instance, how to connect over SSH, how to deploy Nginx, how to reinstall the OS. They publish procedures, not a patching service.

One caveat worth stating plainly: the docs describe SSH access, password resets and OS reinstalls, but root or Administrator access isn't spelled out as a guarantee anywhere in the public documentation. If privileged access is a hard requirement for your setup, confirm it before you pay rather than after.

## The price reality check: where $29 sits in the unmanaged market

GoMami is not competing with budget unmanaged hosts, and the numbers make that obvious. A sub-$10 unmanaged VPS in 2026 typically gets you 1 vCPU, 1–4GB RAM, 20–50GB NVMe and 1–4TB of monthly traffic, with renewals often landing at 1.5–2× the intro price. The category leader in one recent survey is a **$6.49/month** KVM plan that renews at **$11.99** on a 24-month term.

GoMami's floor is $29. That's roughly 4.9× the median entry price, and no intro-versus-renewal split shows up in the published pricing — the $29 is the listed monthly price, and every other plan on the store is priced the same way, with no "first term only" figure anywhere in evidence.

What the premium buys instead:

- **Return routing across all three Chinese carriers** — China Telecom CN2, China Unicom AS9929, China Mobile CMIN2 — rather than one optimized path and two afterthoughts.
- **A stated latency target of RTT under 50ms to mainland China**, which holds best for Hong Kong and varies for Singapore and Japan depending on city and carrier.
- **DDoS mitigation up to 600Gbps**, with best-effort scrubbing included by default and an optional advanced tier.
- **Recent AMD silicon**: EPYC 9575F (Zen 5, up to 5.0GHz) in Hong Kong Turin, EPYC 7763 across the Pulse lines, Ryzen 9 9950X at up to 5.7GHz on the homepage series.

If your traffic never touches China, none of that is worth a dollar to you. A $6 unmanaged box in Frankfurt will out-spec GoMami's $29 Nano on paper and cost a fifth as much.

## Every GoMami plan currently listed

Everything on the store pages is below. Prices are monthly, in USD, and all plans carry the China Mainland Optimized Pro routing tag, are provisioned through a VirtFusion control panel, and run on AMD EPYC or Ryzen hardware.

**The Pulse family — HKG, JPN and SIN in one table**

| Location | Plan | vCPU / RAM / NVMe | Traffic · Port | Price/mo | Order |
| --- | --- | --- | --- | --- | --- |
| Hong Kong | Pulse Nano | 2 / 2GB / 40GB | 500GB · 1Gbps | $49 | [Order HKG Nano](https://gomami.io/aff.php?aff=415&pid=26&billingcycle=monthly) |
| Hong Kong | Pulse Mini | 2 / 4GB / 60GB | 1TB · 1Gbps | $59 | [Order HKG Mini](https://gomami.io/aff.php?aff=415&pid=4&billingcycle=monthly) |
| Hong Kong | Pulse Air | 4 / 8GB / 80GB | 2TB · 1Gbps | $119 | [Order HKG Air](https://gomami.io/aff.php?aff=415&pid=5&billingcycle=monthly) |
| Hong Kong | Pulse Pro | 8 / 16GB / 100GB | 5TB · 3Gbps | $269 | [Order HKG Pro](https://gomami.io/aff.php?aff=415&pid=6&billingcycle=monthly) |
| Hong Kong | Pulse Ultra | 16 / 32GB / 300GB | 10TB · 3–5Gbps | $499 | [Order HKG Ultra](https://gomami.io/aff.php?aff=415&pid=25&billingcycle=monthly) |
| Japan | Pulse Nano | 2 / 2GB / 40GB | 500GB · 1Gbps | $29 | [Order JPN Nano](https://gomami.io/aff.php?aff=415&pid=13&billingcycle=monthly) |
| Japan | Pulse Mini | 2 / 4GB / 60GB | 1TB · 1.5Gbps | $49 | [Order JPN Mini](https://gomami.io/aff.php?aff=415&pid=10&billingcycle=monthly) |
| Japan | Pulse Air | 4 / 8GB / 80GB | 2TB · 1Gbps | $89 | [Order JPN Air](https://gomami.io/aff.php?aff=415&pid=11&billingcycle=monthly) |
| Japan | Pulse Pro | 8 / 16GB / 100GB | 5TB · 3Gbps | $169 | [Order JPN Pro](https://gomami.io/aff.php?aff=415&pid=12&billingcycle=monthly) |
| Japan | Pulse Ultra | 12 / 32GB / 300GB | 10TB · 3Gbps | $338 | [Order JPN Ultra](https://gomami.io/aff.php?aff=415&pid=24&billingcycle=monthly) |
| Singapore | Pulse Nano | 2 / 2GB / 40GB | 500GB · 1Gbps | $29 | [Order SIN Nano](https://gomami.io/aff.php?aff=415&pid=21&billingcycle=monthly) |
| Singapore | Pulse Mini | 2 / 4GB / 60GB | 1TB · 1Gbps | $49 | [Order SIN Mini](https://gomami.io/aff.php?aff=415&pid=17&billingcycle=monthly) |
| Singapore | Pulse Air | 4 / 8GB / 80GB | 2TB · 1Gbps | $89 | [Order SIN Air](https://gomami.io/aff.php?aff=415&pid=18&billingcycle=monthly) |
| Singapore | Pulse Pro | 8 / 16GB / 100GB | 5TB · 3Gbps | $169 | [Order SIN Pro](https://gomami.io/aff.php?aff=415&pid=19&billingcycle=monthly) |
| Singapore | Pulse Ultra | 12 / 32GB / 300GB | 10TB · 3–5Gbps | $338 | [Order SIN Ultra](https://gomami.io/aff.php?aff=415&pid=23&billingcycle=monthly) |

**HKG Turin — AMD EPYC 9575F (Zen 5, up to 5.0GHz, DDR5-6400, PCIe Gen5 NVMe)**

| Plan | vCPU / RAM / NVMe | Traffic · Port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| Turin Mini | 2 / 4GB / 100GB | 1TB · 2Gbps | $69 | [Order Turin Mini](https://gomami.io/aff.php?aff=415&pid=14&billingcycle=monthly) |
| Turin Air | 4 / 8GB / 140GB | 2TB · 2Gbps | $129 | [Order Turin Air](https://gomami.io/aff.php?aff=415&pid=15&billingcycle=monthly) |
| Turin Pro | 6 / 16GB / 180GB | 5TB · 5Gbps | $299 | [Order Turin Pro](https://gomami.io/aff.php?aff=415&pid=16&billingcycle=monthly) |
| Turin Ultra | 12 / 32GB / 220GB | 10TB · 5Gbps | $599 | [Order Turin Ultra](https://gomami.io/aff.php?aff=415&pid=22&billingcycle=monthly) |

**LAX Pulse — Los Angeles, dual-direction premium routing**

| Plan | vCPU / RAM / NVMe | Traffic · Port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| LAX Nano | 2 / 2GB / 40GB | 1TB · 1Gbps | $29 | [Order LAX Nano](https://gomami.io/aff.php?aff=415&pid=27&billingcycle=monthly) |
| LAX Mini | 2 / 4GB / 60GB | 2TB · 1Gbps | $59 | [Order LAX Mini](https://gomami.io/aff.php?aff=415&pid=28&billingcycle=monthly) |
| LAX Air | 4 / 8GB / 80GB | 4TB · 2Gbps | $129 | [Order LAX Air](https://gomami.io/aff.php?aff=415&pid=29&billingcycle=monthly) |
| LAX Pro | 6 / 16GB / 100GB | 8TB · 3Gbps | $259 | [Order LAX Pro](https://gomami.io/aff.php?aff=415&pid=30&billingcycle=monthly) |
| LAX Ultra | 12 / 32GB / 300GB | 15TB · 5Gbps | $599 | [Order LAX Ultra](https://gomami.io/aff.php?aff=415&pid=31&billingcycle=monthly) |
| LAX Titan | 12 / 32GB / 600GB | 30TB · 10Gbps | $999 | [Order LAX Titan](https://gomami.io/aff.php?aff=415&pid=32&billingcycle=monthly) |

A practical warning on Los Angeles: the official documentation and the homepage point-of-presence list still show only Hong Kong, Japan and Singapore. LAX exists, is in stock and has been reviewed independently, but the docs haven't caught up. If you go looking for a "Los Angeles" entry in the left-hand menu and don't find one, you're not imagining it — order from the store page, not the docs.

**Ryzen 9 9950X line — the homepage headline series (up to 5.7GHz)**

| Plan | vCPU / RAM / NVMe | Traffic · Port | Price/mo | Order |
| --- | --- | --- | --- | --- |
| Ryzen Mini | 2 / 4GB / 40GB | 1TB · 2Gbps | $59 | [Check the Ryzen line price](https://bit.ly/Gomami) |
| Ryzen Air | 4 / 8GB / 60GB | 2TB · 2Gbps | $99 | [Check the Ryzen line price](https://bit.ly/Gomami) |
| Ryzen Pro | 6 / 16GB / 80GB | 5TB · 5Gbps | $199 | [Check the Ryzen line price](https://bit.ly/Gomami) |

That series is sold as a newer, limited line, so treat availability as less settled than the Pulse and Turin catalogues.

**HKG Forge — a dedicated server, not a VPS.** An EPYC 7663 with 56 cores/112 threads, 128GB RAM, 960GB NVMe and 10TB traffic on the Mini tier; 256GB, 4TB NVMe and 20TB on the Air. Published prices for it run between $399 and $599 (Mini) and $699 to $899 (Air), sometimes with a one-time $68 setup fee — no official store page appears in the public documentation, so confirm the figure and the fee with support before budgeting.

Two discrepancies to know about before you trust those tables blindly. The homepage shows an EPYC 7763 block at **$39 / $79 / $169** with configurations matching HKG Pulse Mini, Air and Pro, while the Pulse store page lists **$59 / $119 / $269** for the same specs — treat the store page as current and verify in the cart. Separately, the HKG and SIN Pulse Ultra port speeds read as 3Gbps on the store pages and 5Gbps in several third-party tables; CPU, RAM, disk, traffic and price agree everywhere.

## The annual math that actually changes the bill

GoMami's pricing has no intro-versus-renewal split in the published figures, but there is one lever worth pulling: **`GOMAMI365`**, a 20% recurring discount on annual billing across the product line. Recurring means every invoice, not just the first.

| Plan | Monthly × 12 | With `GOMAMI365` | Saved per year |
| --- | --- | --- | --- |
| JPN / SIN / LAX Nano ($29) | $348 | $278.40 | $69.60 |
| HKG Pulse Mini ($59) | $708 | $566.40 | $141.60 |
| HKG Turin Mini ($69) | $828 | $662.40 | $165.60 |

At that rate the $29 Nano works out to about $23.20/month effective, and the Hong Kong Pulse Mini to about $47.20. LAX also has a launch code, **`Hi,LAX`**, advertised as 20% recurring on the LAX line only. Both codes come from promotional listings rather than a public pricing page, so paste them into the promo field at checkout and watch the total change before you pay — 👉 [test both codes against the plan you want in the GoMami cart](https://bit.ly/Gomami).

Nothing in the documentation confirms whether an annual discount stacks with a launch code, or whether quarterly billing carries any discount at all. Assume it doesn't until the invoice says otherwise.

## Six things the product pages don't tell you

These come from GoMami's own billing and operations documentation — plus one item that only appears in third-party write-ups. They matter more for an unmanaged box than any spec sheet, because a self-managed server you can't access is just a bill.

**1. There is no grace period on renewals.** A renewal invoice goes out 7 days before the due date with an automatic charge attempt. On the due date itself, unpaid service is suspended immediately. Five days overdue, the service is terminated and data may not be recoverable. Six days overdue, the invoice is auto-cancelled. If you're used to hosts that let a card quietly fail for a week, this will bite you.

**2. You cannot resize a plan yourself.** Changing plans currently requires a support ticket. Instances can be transferred to another GoMami account through the Push service at **$10 per transfer**, handled manually within 24 hours, after which the original account loses management access. Neither is a dealbreaker; both are friction an unmanaged buyer should plan around.

**3. The refund window is 24 hours, first purchase only, once per user.** Full refund within 24 hours of activation, returned to the original payment method — Alipay in 1–3 business days, credit cards in 5–10. Renewal orders are excluded. Twenty-four hours is enough to run ping, traceroute and an evening-peak throughput test against your own users; it is not enough to discover that your workload outgrew the plan three weeks later.

**4. Traffic accounting isn't documented in the official FAQ.** Third-party roundups consistently state that only outbound traffic counts, that exceeding the allowance throttles you to roughly 20KB/s until the next cycle rather than billing overages, and that Forge plans bill excess at $0.06/GB. The official FAQ lists the question "what happens if I reach my traffic limit" without a published answer in the documentation. Treat the outbound-only model as likely but unconfirmed, and check before committing a bandwidth-heavy workload.

**5. Two official pages disagree about OS templates.** The FAQ lists Ubuntu 22.04/24.04, Debian 11/12, CentOS Stream 9, AlmaLinux 8/9 and Windows Server 2019/2022. The rebuild page lists a longer set including Ubuntu 20.04, Debian 13, CentOS 7, Rocky 8/9/10 and Fedora 41/42, but no Windows. Custom ISO mounting covers anything else. Windows appears in exactly one of the two lists and whether a licence is bundled is never stated — if you need Windows, ask, don't assume.

**6. Daily backups to AWS S3 are claimed by third-party write-ups, not the official docs.** Several independent roundups state that VPS plans include automatic daily backups to AWS S3. I couldn't find a corresponding statement in GoMami's own documentation. If off-host backups are part of your decision, treat this as a question for support rather than a feature — and if it's wrong, you're still the backup policy owner, which is the whole premise of an unmanaged plan.

Deployment itself is quick: payment clears, the system provisions automatically in about 1–5 minutes, and an email with the IP and login credentials lands in your inbox.

## What the routing premium buys, according to people who measured it

The China-route claim is the entire justification for the price gap, so it deserves evidence rather than adjectives. Independent testing has been consistently positive but not uniformly so.

digvps rates the Hong Kong Turin and Pulse lines **E2 (excellent)**, Japan and Singapore **E3 (good)**, and Los Angeles started at E3 before being upgraded to **E2 in July 2026** once a stability observation period passed. Their Hong Kong notes flag the honest weak spot: after return routes switched to CN2/9929/CMIN2 in October 2025, Telecom and Mobile held up during evening peak while **Unicom dropped roughly 30% with visible jitter and retransmits**. An earlier re-test in late August 2025 had seen Hunan Unicom climb from 400–500Mbps to near 1Gbps, but that predates the route change and isn't evidence of a post-switch recovery. Three-carrier optimization is real; it doesn't make all three carriers equal on every night.

Hardware numbers back the Turin premium. A Geekbench 5 run on the Turin Mini recorded **1,101 single-core / 2,116 multi-core**, against roughly 123.8% and 130% improvements over the older 7763 platform — exactly the gap you'd expect from 5.0GHz Zen 5 with DDR5-6400, and exactly why database workloads (MySQL InnoDB, where a single query runs on a single thread) benefit more than a static site does.

A Singapore Pulse Mini test showed sysbench at 3,886 single-thread and 7,748 dual-thread — near-linear scaling, no obvious core stealing — with fio 4K random writes around 793MB/s and 128K sequential reads near 3.85GB/s. Evening-peak throughput to Shenzhen Telecom hit 922/888Mbps on eight threads; Jiangsu Mobile 906/871Mbps.

On latency, the official target is under 50ms to mainland China. Third-party measurements on the Singapore node ranged from about 48ms (Guangzhou Telecom) to 86ms (Beijing Mobile). Geography and carrier still decide the number; the target is a best case, not a promise per city.

## Who shouldn't buy this

Be honest about the shape of the product before you spend:

- **You want the cheapest unmanaged box.** $29 is the floor here. The market's median entry is $5.95.
- **Your audience isn't in China.** The premium exists to fix a routing problem you don't have.
- **You want someone else to patch the server.** That's a managed VPS at $15–30/month, and GoMami's docs assume the opposite arrangement.
- **You need one-click vertical scaling.** Plan changes go through a ticket.
- **You'll forget the due date.** Suspension on the due date, termination at five days. Calendar reminder or automatic payment, no exceptions.
- **You need a confirmed backup guarantee.** Until support confirms it, assume the backup policy is whatever you build yourself.

## The decision, by situation

**A WordPress site or small SaaS with mainland readers:** HKG Pulse Mini at $59/month — 2 vCPU, 4GB, 60GB NVMe, 1TB — runs a standard LNMP stack without drama, and Hong Kong keeps latency lowest. Annual with `GOMAMI365` brings it to about $47.20/month effective.

**A game server or anything single-thread bound:** HKG Turin Mini at $69/month. The extra $10 over Pulse buys 5.0GHz Zen 5 and 100GB of disk instead of 60GB. For Counter-Strike, Minecraft or a real-time API, the clock speed is the product.

**Just testing whether the routing is real:** JPN, SIN or LAX Nano at $29/month. Cheap enough to run a week of your own traceroutes, and covered by the 24-hour refund if it fails immediately.

**Serving China and North America from one box:** LAX Pulse, where both directions ride premium routes and the traffic allowances are the most generous per dollar — 1TB on the $29 Nano versus 500GB on the Asian nodes. Remember the docs still don't list the location.

**Heavy database, transcoding or crawling:** HKG Forge, the dedicated 56-core box. Confirm the price and setup fee with support first.

Three things before you check out: verify the cart price against the plan table you're reading, since the homepage and store pages don't always agree; test `GOMAMI365` and, if relevant, `Hi,LAX` in the promo field; and set the billing reminder for seven days before the due date so the no-grace-period policy never applies to you.

👉 [Start with the current GoMami plan list and cart](https://bit.ly/Gomami) — the $29 Nano if you're testing the route, the Hong Kong Pulse Mini if you already know you're staying.
