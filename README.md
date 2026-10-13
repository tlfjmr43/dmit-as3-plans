# DMIT AS3: Plan-by-Plan Prices, Pro vs Eyeball vs Tier 1 Line Differences, and Which LAX VPS to Buy

Two kinds of people search "DMIT AS3". One saw the code in a restock post and wants to know what it is. The other already knows it's a hardware generation and wants to know whether the cheaper AS3 boxes are worth it next to DMIT's newer AN5 machines. Both questions get answered below, along with the full current price list.

## AS3 is a hardware label, not a network tier

DMIT names its host platforms by generation:

- **AS3** — AMD EPYC 7003 Series
- **AN4** — AMD EPYC 9004 Series
- **AN5** — AMD EPYC 9005 Series (Zen 5, DDR5 ECC, PCIe 5.0 NVMe)

The letters are DMIT's internal shorthand; what matters is that AS3 is the oldest of the three and the cheapest per core. It's the same silicon generation that sat behind a lot of the mainstream EPYC VPS inventory from 2022 onward, so nothing exotic is happening under the hood.

The part people trip over: generation and network are separate axes. DMIT sells three network profiles — Premium, Eyeball, Tier 1 — and each of them has been offered on more than one hardware generation. So "LAX.AS3.Pro" and "LAX.AN5.Pro" run the same Premium routing profile; they differ in CPU, memory speed, storage and price. If you're choosing between them, you're choosing compute, not route quality.

That's why AS3 keeps coming back into stock after newer platforms launch. It's the budget lane.

## Where AS3 actually appears in the catalog

Los Angeles is where the AS3 lineup is most complete. The LAX node currently lists all three network profiles on AS3 — Pro, Eyeball and Tier 1 — which is why "DMIT AS3" searches spike whenever LAX restocks.

Hong Kong is messier. The HKG Tier 1 line is AS3-only (it's the one place where AS3 isn't optional), HKG Eyeball has been offered on both AS3 and AN5, and the Hong Kong Premium line has largely moved to AN5 through 2026. Tokyo runs its own Pro/Eyeball/Tier 1 structure. If you specifically want AS3, Los Angeles and Hong Kong Tier 1 are the two reliable places to find it.

## Premium, Eyeball, Tier 1 — what the three lines mean on AS3

DMIT's own cart copy is blunt about it: Premium includes Tier 1 plus all Premium Transit providers, including DMIT's backbone and China Telecom CN2 GIA. That's the profile buyers care about when they say they need a China-optimized US VPS.

The routing as listed for LAX AS3 Premium:

- China Telecom inbound: CN2 GIA (AS4809)
- China Unicom inbound: AS4837 direct
- China Mobile inbound: Hong Kong Mobile (AS58453)
- All three carriers outbound: AS4809

Eyeball is the middle tier — Tier 1 routing plus a best-effort China path, in practice load-balanced across AS9929 and AS58807 depending on carrier. You give up some route guarantee and get noticeably more monthly traffic at the same price.

Tier 1 is straight international transit with no China optimization at all. It's the cheapest and the roomiest.

> The trade-off between the lines isn't speed at 3 a.m. from your own laptop. It's how the route behaves at 8 p.m. on a weekday from a residential connection in a Chinese province. If that sentence doesn't describe your users, Tier 1 is usually the correct answer, and the Premium premium is money you don't need to spend.

## LAX AS3 Premium (Pro) plans

Prices are list prices from DMIT's cart pages, monthly unless noted. Traffic on Pro is metered bidirectionally.

| Plan | vCPU | RAM | SSD | Monthly traffic | Port | Overage | Price | Order |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| LAX.AS3.Pro.TINY | 1 | 2 GB | 20 GB | 1000 GB | 1 Gbps | Unmetered @ 4 Mbps | $10.90/mo | [ Check LAX AS3 Pro TINY pricing](https://www.dmit.io/aff.php?aff=12046&pid=253) |
| LAX.AS3.Pro.Pocket | 2 | 2 GB | 40 GB | 1500 GB | 4 Gbps | Unmetered @ 4 Mbps | $16.90/mo | [ View the Pocket plan](https://www.dmit.io/aff.php?aff=12046&pid=254) |
| LAX.AS3.Pro.STARTER | 2 | 2 GB | 80 GB | 3000 GB | 10 Gbps | Unmetered @ 4 Mbps | $34.90/mo | [ See STARTER specs and stock](https://www.dmit.io/aff.php?aff=12046&pid=255) |
| LAX.AS3.Pro.MINI | 4 | 4 GB | 80 GB | 5000 GB | 10 Gbps | Unmetered @ 8 Mbps | $62.90/mo | [ Check MINI availability](https://www.dmit.io/aff.php?aff=12046&pid=256) |
| LAX.AS3.Pro.MICRO | 4 | 4 GB | 160 GB | 7000 GB | 10 Gbps | Unmetered @ 8 Mbps | $87.90/mo | [ View MICRO configuration](https://www.dmit.io/aff.php?aff=12046&pid=257) |
| LAX.AS3.Pro.MEDIUM | 6 | 8 GB | 160 GB | 14000 GB | 10 Gbps | Unmetered @ 10 Mbps | $199.90/mo | [ Check MEDIUM pricing](https://www.dmit.io/aff.php?aff=12046&pid=258) |

Every Pro plan includes 1 IPv4 and a /64 IPv6 block; MEDIUM doubles the IPv4 count. RAM and SSD are expandable at order time through the customize option, which is worth knowing if 20 GB of disk is the thing that would have pushed you to a bigger plan.

## LAX AS3 Eyeball (EB) plans

Same price ladder as Pro, more traffic, weaker route guarantee.

| Plan | vCPU | RAM | SSD | Monthly traffic | Port | Overage | Price | Order |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| LAX.AS3.EB.TINY | 1 | 2 GB | 20 GB | 1500 GB | 2 Gbps | Unmetered @ 4 Mbps | $10.90/mo | [ See EB TINY traffic allowance](https://www.dmit.io/aff.php?aff=12046&pid=259) |
| LAX.AS3.EB.Pocket | 2 | 2 GB | 40 GB | 3000 GB | 4 Gbps | Unmetered @ 4 Mbps | $16.90/mo | [ View EB Pocket plan](https://www.dmit.io/aff.php?aff=12046&pid=260) |
| LAX.AS3.EB.STARTER | 2 | 2 GB | 80 GB | 5000 GB | 10 Gbps | Unmetered @ 4 Mbps | $34.90/mo | [ Check EB STARTER stock](https://www.dmit.io/aff.php?aff=12046&pid=261) |
| LAX.AS3.EB.MINI | 4 | 4 GB | 80 GB | 10000 GB | 10 Gbps | Unmetered @ 8 Mbps | $62.90/mo | [ View EB MINI details](https://www.dmit.io/aff.php?aff=12046&pid=262) |
| LAX.AS3.EB.MICRO | 4 | 4 GB | 160 GB | 14000 GB | 10 Gbps | Unmetered @ 8 Mbps | $87.90/mo | [ Check EB MICRO availability](https://www.dmit.io/aff.php?aff=12046&pid=263) |
| LAX.AS3.EB.MEDIUM | 6 | 8 GB | 160 GB | 30000 GB | 10 Gbps | Unmetered @ 10 Mbps | $199.90/mo | [ See EB MEDIUM traffic quota](https://www.dmit.io/aff.php?aff=12046&pid=264) |

The numbers to stare at: EB.TINY gives 1500 GB where Pro.TINY gives 1000 GB for the same $10.90, and EB.MEDIUM gives 30 TB against Pro.MEDIUM's 14 TB — both at $199.90. If your workload is video, file distribution, or anything measured in terabytes rather than requests, Eyeball is the better buy and the extra routing risk is usually the smaller problem.

## LAX AS3 Tier 1 plans

No China optimization, cheapest entry point, and by far the most usable overage behaviour — you get shaped to somewhere between 100 and 500 Mbps instead of single-digit Mbips.

| Plan | vCPU | RAM | SSD | Monthly traffic | Port | Overage | Price | Order |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| LAX.AS3.T1.WEE | 1 | 1 GB | 20 GB | 1000 GB | 4 Gbps | Unmetered @ 100 Mbps | $36.90/year | [ Grab the T1 WEE annual plan](https://www.dmit.io/aff.php?aff=12046&pid=270) |
| LAX.AS3.T1.TINY | 1 | 1 GB | 20 GB | 2000 GB | 4 Gbps | Unmetered @ 200 Mbps | $6.90/mo | [ View T1 TINY](https://www.dmit.io/aff.php?aff=12046&pid=271) |
| LAX.AS3.T1.STARTER | 2 | 2 GB | 40 GB | 4000 GB | 10 Gbps | Unmetered @ 200 Mbps | $12.90/mo | [ Check T1 STARTER](https://www.dmit.io/aff.php?aff=12046&pid=272) |
| LAX.AS3.T1.MINI | 2 | 4 GB | 80 GB | 8000 GB | 10 Gbps | Unmetered @ 200 Mbps | $21.90/mo | [ View T1 MINI specs](https://www.dmit.io/aff.php?aff=12046&pid=273) |
| LAX.AS3.T1.MICRO | 4 | 4 GB | 120 GB | 16000 GB | 10 Gbps | Unmetered @ 500 Mbps | $32.90/mo | [ See T1 MICRO quota](https://www.dmit.io/aff.php?aff=12046&pid=274) |

T1.WEE at $36.90 a year works out to a bit over $3 per month, and it's the plan that gets quoted in every restock post. It's also the one that doesn't need a coupon — DMIT lists it at that price outright.

Hong Kong's Tier 1 line is the AS3 option for a Hong Kong IP, starting at the same $36.90/year for HKG.AS3.T1.WEE with a 4 Gbps port and 1 TB of transfer. Hong Kong Premium on AS3 has been largely displaced by AN5 hardware, and HKG Eyeball has alternated between AS3 and AN5 depending on restock batches, so treat any Hong Kong listing as something to confirm on the cart page rather than assume.

## What you're actually paying for at each step

Three break points matter more than the rest.

**$10.90 → $34.90 in the Pro line** buys you a lot: 20 GB of disk becomes 80 GB, 1 TB of traffic becomes 3 TB, and the port goes from 1 Gbps to 10 Gbps. Two cores and 2 GB of RAM stay the same, which is odd until you realise DMIT prices these plans around network commitments, not around compute. If you're running anything with images or a database, stepping from TINY to STARTER is the difference between a box you fight with and a box you forget about.

**Pro vs EB at identical prices** is a routing-versus-traffic decision, and it's the single most common mistake in plan selection. People buy Pro for a project whose audience is in Frankfurt, then wonder why they're paying for CN2 GIA they never touch.

**Tier 1's overage shaping** is the underrated feature. Pro and EB throttle you to 4–10 Mbps once the monthly quota is gone — enough for SSH and a monitoring agent, not enough for anything else. Tier 1 drops to 100–500 Mbps with unlimited volume. If your traffic is spiky and unpredictable, a T1 plan with a smaller quota will serve you better than a Pro plan you're scared to use.

## Caveats DMIT publishes about AS3 itself

This is the part most write-ups skip. DMIT's own product notes describe the LAX AS3 platform as still being in a continuous optimization phase, with disk performance and SLA potentially below what a mature platform delivers. Hong Kong's Eyeball network carries a Beta label for the same reason. That's DMIT telling you the older generation is also the one that hasn't had years of tuning.

What to do with that: use AS3 for sites, dev environments, APIs, monitoring, and international traffic. If you're deploying something where a storage stall in the wrong hour costs money, either test first with the official test IPs and Looking Glass, or pay for the newer platform.

Two other operational details worth budgeting time for:

- Pro and EB traffic is metered bidirectionally on LAX. Inbound and outbound both count against the quota, so a 1000 GB plan is not 1000 GB of outbound.
- Stock on these plans moves in batches. DMIT has suspended and restarted sales on LAX before when rack space, power or storage capacity ran short, and restocks have a habit of clearing out. If the plan you want is listed, it's listed today.

## Coupon reality check

DMIT doesn't run sitewide sales, and this is where most coupon pages mislead people. Its codes are tied to specific product lines and billing terms, so a code that's "live" for one cart can be dead in another.

The code that shows up most consistently across listings is `LAX-EB-LAUNCH-NON-MONTHLY-RECURRING-20OFF`, aimed at LAX Eyeball plans on non-monthly billing cycles. There are also recurring-code sets that circulated for LAX Pro/EB orders. None of that is worth trusting blindly: paste the code into the cart, hit **Validate Code**, and see whether the total changes. If nothing moves, the code doesn't apply to your combination of plan and term, and no amount of reading coupon blogs changes that.

Two things that do reliably reduce the bill: annual billing (T1.WEE's $36.90/year is the clearest example) and picking the network line that matches where your users are.

## Picking your AS3 plan

- **Personal blog, portfolio, or small business site with mainland Chinese visitors:** Pro TINY at $10.90/mo, or Pro Pocket at $16.90 once you need disk. [👉 Compare LAX AS3 Pro plans side by side](https://www.dmit.io/aff.php?aff=12046&pid=253)
- **Media-heavy workload, Chinese audience, budget-sensitive:** Eyeball TINY or STARTER. Same money as Pro, 50–65% more traffic.
- **Overseas audience, dev/test, backups, monitoring, international transit:** Tier 1. WEE at $36.90/year is the entry point; T1.TINY at $6.90/mo is the same box on a monthly term. [👉 Check LAX Tier 1 stock and pricing](https://www.dmit.io/aff.php?aff=12046&pid=271)
- **Applications that need four real cores:** Pro MINI/MICRO or EB MINI/MICRO, $62.90–$87.90/mo. EB buys more bandwidth for the same core count.
- **Hong Kong IP without China optimization:** HKG.AS3.T1.WEE, $36.90/year, 4 Gbps port.

One thing worth saying plainly: if your users are entirely outside mainland China and Hong Kong, the AS3 Premium and Eyeball tiers are the wrong purchase. Paying CN2 GIA prices for a route nobody traverses is the most common way people overspend at DMIT.

## Questions that come up before ordering

**Is AS3 slower than AN5?** Per-core, yes — EPYC 7003 is two generations behind the 9005 parts, and AN5 also brings DDR5 and PCIe 5.0 storage. For web serving, APIs and most containers, the gap rarely shows. For compute-bound workloads it will.

**Can I switch network lines after purchase?** No. The line is tied to the product you order, so pick Pro, EB or T1 before checkout rather than after.

**What payments work?** Alipay, PayPal and credit cards are all supported, which is part of why the provider is popular with Chinese users despite being a US-registered company.

**What happens when traffic runs out?** On Pro and EB, shaping to 4–10 Mbps and no suspension. On Tier 1, shaping to 100–500 Mbps depending on plan. Nothing gets shut off mid-cycle.

Ready to see what's actually in stock right now — [👉 check the DMIT Los Angeles AS3 lineup and current inventory](https://www.dmit.io/aff.php?aff=12046). Inventory on these plans has a short shelf life, and the cart is the only thing that tells you the truth about what's available.
