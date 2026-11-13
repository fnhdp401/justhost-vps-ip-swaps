# VPS Change IP Free: How JustHost's 50 Free Swaps Work, What the Client Area Does, and Why 24-Hour and 72-Hour Windows Aren't Universal (Plans From $1.99)

JustHost doesn't charge for an IP change. Its support documentation puts the allowance at **50 free changes** made from the client area, and states that the data on the server is kept. The same article sets no 24-hour or 72-hour clock; the limit is a count, not a countdown. What the free swap doesn't include is any say over which address you receive, any promise about the country external GeoIP databases report, or a permanent hold on the address you're giving up.

Below: every VPS plan on the current price list, the exact click path through the client area, the one documented failure mode that stops a change, and what five IP swaps a year cost at JustHost versus four providers that bill per change.

> **Most readers should start with Sirius:** 1 core, 1 GB RAM, 20 GB NVMe, 300 Mbps fair-share port. **$4.85/mo**, or **$3.88/mo** when you pay for 12 months. It handles a VPN endpoint, a small scraper, or a staging box without the 512 MB ceiling that makes the $1.99 plan frustrating after a week.
> 👉 [Check the Sirius plan and current price](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392)

## All JustHost VPS plans and prices

Prices below are the monthly rate the price page lists, with the 12-month rate where one is shown. All plans include unmetered traffic on a fair-share port and a free IPv6 address.

| Plan | CPU / RAM / NVMe | Port | Price | Order |
| --- | --- | --- | --- | --- |
| VPS Promo | 1 core / 512 MB / 5 GB | 10 Mbps | $1.99/mo | [Order Promo](https://justhost.asia/en/services/vps/tariffs/promo-c1r512nvme?ref=196392) |
| New Star | 1 core / 1 GB / 10 GB | 100 Mbps | $3.81/mo, $3.05 on 12 mo | [Order New Star](https://justhost.asia/en/services/vps/tariffs/new-star-c1r1024nvme?ref=196392) |
| Sirius | 1 core / 1 GB / 20 GB | 300 Mbps | $4.85/mo, $3.88 on 12 mo | [Order Sirius](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392) |
| Arcturus | 1 core / 2 GB / 30 GB | 300 Mbps | $6.92/mo, $5.53 on 12 mo | [Order Arcturus](https://justhost.asia/en/services/vps/tariffs/arcturus?ref=196392) |
| Double Star | 2 cores / 2 GB / 20 GB | 200 Mbps | $7.08/mo, $5.67 on 12 mo | [Order Double Star](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392) |
| Alpha Centauri | 2 cores / 2 GB / 40 GB | 400 Mbps | $8.99/mo, $7.19 on 12 mo | [Order Alpha Centauri](https://justhost.asia/en/services/vps/tariffs/alpha_centauri?ref=196392) |
| Bright Star | 4 cores / 4 GB / 30 GB | 300 Mbps | $9.80/mo, $7.84 on 12 mo | [Order Bright Star](https://justhost.asia/en/services/vps/tariffs/bright-star-c4r4096nvme?ref=196392) |
| Vega | 2 cores / 4 GB / 80 GB | 500 Mbps | $13.44/mo, $10.75 on 12 mo | [Order Vega](https://justhost.asia/en/services/vps/tariffs/vega?ref=196392) |
| Capella | 4 cores / 4 GB / 120 GB | 750 Mbps | $18.30/mo, $14.64 on 12 mo | [Order Capella](https://justhost.asia/en/services/vps/tariffs/capella?ref=196392) |
| Rigel | 4 cores / 8 GB / 200 GB | 750 Mbps | $27.94/mo, $22.35 on 12 mo | [Order Rigel](https://justhost.asia/en/services/vps/tariffs/rigel?ref=196392) |
| Antares | 5 cores / 8 GB / 300 GB | 750 Mbps | $33.12/mo, $26.49 on 12 mo | [Order Antares](https://justhost.asia/en/services/vps/tariffs/antares?ref=196392) |
| Betelgeuse | 6 cores / 12 GB / 400 GB | 750 Mbps | $45.54/mo, $36.43 on 12 mo | [Order Betelgeuse](https://justhost.asia/en/services/vps/tariffs/betelgeuse?ref=196392) |
| Spica | 8 cores / 16 GB / 500 GB | 750 Mbps | $61.06/mo, $48.85 on 12 mo | [Order Spica](https://justhost.asia/en/services/vps/tariffs/spica?ref=196392) |
| Altair | 8 cores / 24 GB / 600 GB | 750 Mbps | $81.76/mo, $65.41 on 12 mo | [Order Altair](https://justhost.asia/en/services/vps/tariffs/altair?ref=196392) |
| Aldebaran | 8 cores / 32 GB / 700 GB | 750 Mbps | $123.16/mo, $98.53 on 12 mo | [Order Aldebaran](https://justhost.asia/en/services/vps/tariffs/aldebaran?ref=196392) |
| Procyon | 12 cores / 32 GB / 1 TB | 1000 Mbps | $164.56/mo, $131.65 on 12 mo | [Order Procyon](https://justhost.asia/en/services/vps/tariffs/procyon?ref=196392) |

New Star, Double Star and Bright Star list the discounted rate as available when you order three months or longer. The 12-month column for the rest assumes a full year paid upfront.

## The click path: three steps, no ticket

JustHost's own documentation describes a self-service change inside the billing panel:

1. Open **Active Services** in your personal cabinet.
2. Click the **gear icon** on the row of the VPS you want to touch.
3. In the **Management** section, click **Change**.

That's the documented route, and it's why nobody needs to open a support ticket for a routine swap. The docs also state that the data is kept, so this is an address change on an existing service rather than a rebuild. Whether the guest operating system picks up the new address without you touching its network configuration isn't spelled out in the same article, which matters if the box goes unreachable right after the change. Note the new address before you start, and if SSH stops answering, check the interface configuration through the VNC console before assuming something worse happened.

There is a second, slower path for the rare case: an address that's on a block list. JustHost asks you to open a ticket describing the problem. In exceptional cases engineers can hand-pick a free address from another subnet in the same location. That isn't a standard service, the subnet isn't guaranteed and no turnaround is promised. When it happens, the change is applied by an agent running inside your VPS, so the service's SSH access has to be open. If SSH is closed, the job stops with `PROVISION_VM_AUTH_REJECTED` and you finish the address swap yourself through the VNC console.

## What "free" leaves out

The IP guarantee article is short and unusually blunt about the limits. Read it before you buy on the strength of the free swaps alone.

- **The country in GeoIP databases is not guaranteed.** An external service may geolocate your new address somewhere other than the data centre's physical country.
- **The address can change without your request.** JustHost reserves the right to move you when a network is withdrawn from service.
- **Reachability from every network or country is not guaranteed.** Routing and blocks applied by third-party operators sit outside JustHost's control.
- **There is no permanent reservation of an address, no whitelist of subnets to issue from, and no way to ban a pool, subnet or country.** The address is issued automatically from the pool bound to the location you ordered.
- **A dedicated network of your own is a separate IP lease service**, not a toggle on an existing VPS.

If you need to pick the exact address or subnet, JustHost isn't the right shop for that requirement, and no amount of free swaps fixes it. Free here means free to roll the dice again, up to 50 times.

👉 [See the full VPS price list and pick a location](https://justhost.asia/en/services/vps/tariffs-all?ref=196392)

## Five IP changes a year, priced

This is where the 50-change allowance stops being a footnote. Compare what a year of five swaps costs if you actually use them, based on each provider's published policy:

| Provider | Free allowance | Cost of 5 changes in a year |
| --- | --- | --- |
| **JustHost** | Up to 50 free changes from the client area | **$0** |
| RackNerd | One free change within 72 hours of delivery, then $3 each (per its April 2023 policy announcement) | $12–15 |
| EDIS Global | One free change within 24 hours of delivery, then €5 standard | €20–25 |
| GoMami | None, $5 per change | $25 |
| Hostup | First IPv4 change free within 72 hours; IPv6 changes always free | First one $0, later IPv4 changes priced in the client area |

Two things follow. First, the 72-hour window that gets quoted in most "free IP change" threads is one provider's model, not an industry standard; EDIS Global's window is 24 hours and GoMami has no free tier at all. Second, if your reason for wanting a swappable IP is recurring (rotation for scraping, recovering from a block that keeps reappearing), a per-change fee compounds fast. Five changes at $3 is $15; at €5 it's €25; JustHost absorbs all five.

The RackNerd figures come from a 2023 announcement that described the policy as unchanged at the time, so treat them as that provider's stated position rather than a quote from this month.

## Three mistakes that cost people a night

**The old address is gone the moment the new one is assigned.** Every provider that documents this says the same thing, and JustHost doesn't offer a permanent reservation. If a DNS record, a monitoring check, or a client's firewall rule points at the old IP, it breaks at the moment of the swap. Update A records and reverse DNS first, or immediately after.

**Nothing reconfigures your applications for you.** A new public IP means new endpoint settings in your VPN config, new entries in whatever panel your customers log into, and possibly a new gateway inside the guest. EDIS Global is explicit that you either configure the address manually over VNC or reinstall the OS, and reinstalling wipes the disk. Hostup shows a "Server IP configuration needs attention" notice when the server hasn't picked up the new address. JustHost's docs say the data is kept, so the safe assumption is that the disk survives and the network configuration is your job.

**A fresh IP is not an unblock.** Rotating addresses doesn't guarantee access to a specific website, a specific country, or a clean reputation in a blocklist. EDIS Global spells out the mechanics: filtering can apply to an entire prefix or to a protocol, and Russian regulators can filter HTTPS on 443 and SSH alongside anything else. If you're changing IPs because one streaming service stopped working, a new address from the same pool in the same location may land you in exactly the same place. JustHost's manual cross-subnet pick exists for blocklist cases, and even that comes with no guarantee.

## FAQ

**Is the change really free, or free up to a point?**
Free up to 50 changes, per JustHost's support documentation. The article stops at that number. If you expect to go past it, ask support what happens before you order rather than after.

**Does changing the IP wipe the server?**
The documentation says the data is kept. That distinguishes it from providers where the practical recovery route is a reinstall. Even so, take a snapshot or a backup first if the box holds anything you'd hate to rebuild, because a failed network configuration can look a lot like data loss from the outside.

**Will my site go down?**
Only if something depends on the old address. The swap itself doesn't stop the VPS, but DNS propagation and stale service configuration will make it look offline. Check the site over the new IP before you repoint DNS.

**Can I choose the country or the subnet?**
No. The address is issued automatically from the pool bound to the location you ordered, and there's no whitelist or pool-exclusion setting. The only manual selection is the exceptional ticket route described above.

**Can I keep the old IP for later?**
Not permanently. Hostup offers paid reservation of a released address and warns that accounts without permanent-reservation rights only keep it for four hours; JustHost documents no reservation at all. Plan on losing it.

**Do the cheap IPv6-only plans qualify?**
They have no IPv4 address to swap. JustHost sells IPv6-only VPS plans starting at $1.60/mo on a 12-month term ($2 monthly), and a separate extra IPv4 address runs $3.31/month on top of a plan. If a free IPv4 swap is the reason you're here, order an IPv4+IPv6 plan.

## Which one to order

Match the plan to the job, not to the price list:

- **A VPN endpoint, a single scraper, or a jump box:** Sirius at $4.85/mo. The 300 Mbps port and 20 GB of NVMe are the parts you'll notice, and $1.04 over New Star buys triple the port speed and double the disk.
- **Two or three lightweight services on one box:** Arcturus at $6.92/mo for 2 GB of RAM, or Alpha Centauri at $8.99/mo if you want two cores and a 400 Mbps port.
- **Testing whether an IP-sensitive workflow works at all:** VPS Promo at $1.99/mo is fine for a week of experiments. The 10 Mbps fair-share port rules it out as anything permanent.
- **Anything with real traffic:** Vega at $13.44/mo (4 GB RAM, 80 GB NVMe, 500 Mbps) is the first plan where disk and port stop being the bottleneck.
- **You need a specific subnet or a guaranteed clean IP:** none of the above. That's an IP lease conversation, and the free swaps won't substitute for it.

Two things worth confirming at checkout: that your chosen plan is the IPv4+IPv6 variant rather than IPv6-only, and that the 12-month rate applies to the term you're actually buying, since the three cheapest plans tie their discount to a minimum order of three months.

👉 [Start with Sirius at JustHost and keep the IP swaps free](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392)
