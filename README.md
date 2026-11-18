# VPS money back guarantee: 7 days, 10 days or 30 days? What gets a refund request refused, and what to do when a host offers no window at all

Refund windows on VPS plans, as published by the hosts quoted in this guide, run 7 days, 10 days and 30 days, and one of them excludes VPS from its guarantee entirely. LightLayer, the host this guide is built around, publishes no money-back guarantee at all: its terms only contemplate refunds where the fault is the company's. The question worth asking before you pay is narrower than "who gives 30 days", namely what is refundable, when the clock starts, and which actions cancel your eligibility.

> **Most readers should start on the $4.00/month plan.** LightLayer's cheapest monthly VPS is 1 vCPU, 1 GB RAM and 50 GB SSD in Los Angeles on a 100 Mbps unmetered port. Nothing there is refundable, so a monthly term caps your exposure at **$4.00**. Move to annual billing after a month of real use, not before.
> 👉 [Start on the $4.00/month 1 GB plan](https://account.lightlayer.net/?affid=74)

## LightLayer plans and current prices

LightLayer runs KVM virtualisation on AMD EPYC hardware with NVMe storage. Locations listed across its plan pages include Hong Kong, Taiwan, Japan, Thailand, Singapore, the Philippines, the United States, the United Kingdom and Germany, paid by PayPal, credit card or Alipay. The company operates as Hong Kong Lightlayer Technology Co., Ltd. and is a subsidiary brand of Megalayer, which is why its network records trace back to the older brand name.

| Plan (billing) | vCPU / RAM | Storage | Port and route | Price | Order |
| --- | --- | --- | --- | --- | --- |
| Startup (monthly) | 1 / 1 GB | 50 GB SSD | 100 Mbps unmetered, Global | **$4.00/mo** | [Order the $4.00 monthly plan](https://account.lightlayer.net/?affid=74) |
| Pay As You Go (monthly) | 2+ / 2 GB+ | scalable | 200 Mbps+, Standard | from $5.60/mo | [Configure pay-as-you-go](https://account.lightlayer.net/?affid=74) |
| Mid-tier (monthly) | 4 / 4 GB | 80 GB SSD | 200 Mbps unmetered, Standard or Premium | roughly $11–18/mo | [Order the 4-core plan](https://account.lightlayer.net/?affid=74) |
| Business (monthly) | 32 / 32 GB | scalable | 200 Mbps unmetered, Premium | $53.60/mo | [Order the 32-core plan](https://account.lightlayer.net/?affid=74) |
| Manila (annual) | 1 / 1 GB | 50 GB SSD | entry port | **$24.99/yr** | [Order the $24.99 Manila annual plan](https://account.lightlayer.net/?affid=74) |
| Taiwan (annual) | 1 / 1 GB | 50 GB SSD | entry port | **$24.99/yr** | [Order the $24.99 Taiwan annual plan](https://account.lightlayer.net/?affid=74) |
| Los Angeles Global (annual) | 1 / 1 GB | 50 GB SSD | Global route | $29.99/yr | [Order the $29.99 LA Global plan](https://account.lightlayer.net/?affid=74) |
| Los Angeles Standard (annual) | 1 / 1 GB | 50 GB SSD | Standard route | $39.99/yr | [Order the $39.99 LA Standard plan](https://account.lightlayer.net/?affid=74) |
| Los Angeles Premium (annual) | 1 / 1 GB | 50 GB SSD | Premium route | $49.99/yr | [Order the $49.99 LA Premium plan](https://account.lightlayer.net/?affid=74) |

Two things about that table matter more than the numbers.

First, the cart shows more variants than any single page displays. Per-location and per-route configurations are sold separately, and annual plans carrying the same headline price can differ by port speed and route class, from single-digit Mbps to 200 Mbps depending on where the box sits. Paying $24.99 in two locations does not buy the same bandwidth.

Second, plan cards and the order configurator have been observed to disagree. A $4.00 card advertising 50 Mbps unmetered sat above a selector that defaulted to 10 Mbps; selecting 50 Mbps unmetered in the configurator priced at $800/month, with a $9.00 total recurring shown alongside. Check the configurator's port and the final recurring total before you enter card details, and if the two screens disagree, stop.

## What "no refund window" costs you in practice

With no money-back guarantee, the only thing standing between you and a lost payment is the size of the payment. Monthly at $4.00 caps the loss at four dollars. The $24.99 annual plan works out to about $2.08/month, less than half the monthly rate, but a bad route or a noisy neighbour costs you the full year on day one.

The terms surrounding the refund question are unusually strict, and they are the part buyers skip:

- **Abuse complaints convert to cash penalties.** A first spam complaint means immediate suspension plus a $50 penalty per incident per IP; phishing or fraud complaints carry $20 per incident per IP. A second complaint is suspension without refund. Three complaints and the server is terminated without refund. You get 6 hours to respond and 24 hours to resolve before suspension, and 24 hours to pay a penalty before removal.
- **Cloud instances are suspended without refund on the first abuse complaint.** No warning step is described.
- **The SLA contains no uptime percentage and no credit schedule.** Network faults are explicitly not compensated, so an outage does not turn into money back or account credit.
- **Blocked or flagged IPs are not replaced.** Spam-reported IPs are permanently blocked. Anything that depends on a clean sending reputation should not live here.
- **Account balances cannot be withdrawn.** Where a refund is granted, it can only become balance.
- **IPv6 is not listed on the plans**, and the Taiwan, Hong Kong and Singapore locations use non-native IPs.
- **I/O is the weak point.** The best-documented independent test recorded fio 4K read at 3.71 MB/s, and reviewers flag heavy I/O limits on some products. Database workloads and busy WordPress sites will feel that.

If any of those items breaks your use case, the price is irrelevant. If none of them does, the $4.00 monthly plan is a cheap way to find out how the route behaves from your location.
👉 [Test the route for $4.00 before committing a year](https://account.lightlayer.net/?affid=74)

## The five clauses that quietly cancel a refund request

These are drawn from hosts that do publish a guarantee, which makes them the standard traps to check anywhere, including with a written policy in front of you.

**1. When does the clock start?** Three different answers exist in the policies reviewed: from the order date, from service activation, and from first activation after provisioning. A host that starts the clock at activation is friendlier; one that starts it at order date eats your setup time. Ask billing to state the start date on your account in the ticket, in writing.

**2. Upgrading inside the window voids it.** Both VPS9 and Host9x state that a service upgraded within the guarantee period is no longer covered. Buy the size you need, or accept that scaling up in week one ends the guarantee.

**3. Opening a PayPal dispute or a card chargeback cancels the guarantee.** VPS9, Host9x and Global Servers all exclude accounts with an open dispute from standard refund processing. The order is: billing ticket first, dispute only if the ticket fails. Reversing that sequence forfeits the refund you were entitled to.

**4. One refund per customer, and new accounts do not reset it.** Global Servers limits the guarantee to a customer's first purchase and states that previously refunded accounts are ineligible on a new account. Verpex offers one refund per customer as well.

**5. Only the base product comes back.** Control panel licences, extra IPs, RAM and CPU upgrades, managed add-ons, setup fees, domains and SSL certificates are excluded across every policy reviewed. Crucial phrases it plainly: the guarantee applies to the base product only.

Two further limits show up often enough to check by default. Several guarantees cover **monthly billing only**, so an annual prepayment falls outside them. And dedicated servers sit outside every VPS guarantee reviewed; at Global Servers the only full-refund window is one hour from order placement, before provisioning starts, which typically begins within 4 to 24 hours.

## How long other hosts actually give

| Host | Window for VPS | Conditions worth knowing |
| --- | --- | --- |
| Global Servers | 30 days | VPS plans only, new customers, one refund per customer; after 30 days an annual plan may become pro-rated account credit, never cash |
| VPS9 | 30 days | Monthly VPS only; policy page dated 2022, so confirm the current version before relying on it |
| Host9x | 7 days | Monthly VPS only; dedicated servers and colocation get pro-rated credit or nothing |
| Crucial | 10 days | 30 days applies to shared and reseller hosting only; clock starts at first activation |
| Verpex | None | Shared and reseller hosting carry 30 days; "VPS services are non-refundable" per its policy updated October 2026 |
| LightLayer | None | Refunds limited to faults attributable to the company; regular-priced and promotional products excluded |

The spread is the point. A 30-day guarantee is not the default, a 7-day window is not unusual, and a host can offer 30 days on shared hosting while giving VPS buyers 10 or nothing.

## Where the money actually goes after a refund

Approved refunds go back to the original payment method only. Global Servers quotes card refunds at 5 to 7 business days and PayPal at 3 to 5, with the refund initiated within 2 business days of approval and acknowledged within 1. VPS9 and Host9x quote 24 to 72 working hours for processing. None of them will send a cheque, wire the money, or push it to a different card.

Currency is the quiet loss. Refunds are issued in US dollars; if you paid in another currency and your processor converted, you get the USD amount back and absorb the exchange difference in both directions. Budget a few percent of the purchase price as the cost of changing your mind.

## How to request a refund, step by step

The process below is the one hosts with a written guarantee generally require, using Global Servers' published steps as the reference. It is not LightLayer's policy; LightLayer has no money-back window to invoke.

1. Confirm the window and start date from your invoice and the policy page, on the day you order, not the day you cancel.
2. Open a billing ticket or email from the address registered on the account, with the order number and the reason. Requests from another address usually fail identity checks.
3. Wait for written confirmation of eligibility before cancelling the service, and cancel through the client area if the policy requires it.
4. Expect the refund to be initiated a couple of business days after approval, then 3 to 7 business days for the money to land.
5. If the window has closed, ask about account credit. Global Servers may, at its discretion, credit the full remaining months of an annual plan; credits carry no cash value and cannot be transferred.

With LightLayer, a billing ticket is the only route, and the outcome depends on whether the fault is theirs. Go in expecting account balance rather than a card refund.

## FAQ

**How long is a VPS money back guarantee usually?**
Verified examples run 7 days (Host9x), 10 days (Crucial, VPS side), and 30 days (Global Servers, VPS9). Verpex and LightLayer offer none on VPS. Anyone quoting "the industry standard is 30 days" has not read enough policies.

**Can I get a pro-rated refund on an annual plan?**
Rarely in cash. Global Servers offers no cash refund after 30 days but may credit the full remaining prepaid months to the account, at its discretion. VPS9 and Host9x limit their guarantees to monthly billing, which excludes annual plans from the start.

**Does paying with PayPal change anything?**
Only if you open a dispute. PayPal disputes and card chargebacks void the guarantee at VPS9, Host9x and Global Servers. Paying by PayPal itself is fine, and refunds return to PayPal in 3 to 5 business days.

**Does upgrading my plan cancel the guarantee?**
At VPS9 and Host9x, yes: a service upgraded inside the refund window is not covered. Order the final configuration up front if you think you may need to scale within the first month.

**Does LightLayer have a free trial or a guarantee?**
No free trial is advertised, and no money-back window is published. The cheapest way to evaluate it is the $4.00 monthly plan, which is why the recommendation at the top of this page is monthly first.

## Which option fits you

If you need a cash refund as your safety net, buy from a host with a written VPS window and read the exclusion list before paying. LightLayer is not that host, and no amount of price advantage changes what happens if the route disappoints you.

If you want a cheap box in Asia or Los Angeles, can rebuild from a script, and keep your own off-site backups, LightLayer's economics are hard to argue with: $4.00/month to test, $24.99/year in Manila or Taiwan once you know the route works. Start monthly, confirm the port speed in the cart matches the plan card, and keep mail and anything reputation-dependent off the server.

If you need a contractual uptime credit, an IPv6 address, or a replaceable IP, skip it entirely; the SLA publishes no uptime figure or credit schedule, and blocked IPs are not replaced.

Two things to settle before you pay: the exact recurring total and port speed shown in the configurator, and a billing ticket asking how refunds are handled if the service cannot be provisioned. Get both in writing, then decide.
👉 [Open the $4.00/month plan and check the configurator total](https://account.lightlayer.net/?affid=74)
