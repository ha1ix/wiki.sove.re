# China — Nomad Notes

*Compiled from community digests.*

## Connectivity & Working Around the Great Firewall

### Accessing Claude from China

Anthropic actively blocks accounts tied to Chinese IPs — reports of accounts being disabled within the first hour of arrival. The working community pattern is **Tailscale with a VPS exit node** outside China: reliable and reportedly no interruptions once set up.

### Vendor Independence for AI Tooling

After performance drops on Anthropic and Codex, part of the community has shifted to **PASEO x OMP x OpenRouter** fronting **GLM** models or **Kimi**. The point isn't the specific stack but keeping the frontend decoupled from any one provider — so when a vendor blocks or degrades, swapping models doesn't break the workflow.

### VPNs

Community-recommended options for working from China:

- **Tailscale + VPS exit node** (as above).
- **JustMySocks Proxy** — mentioned as a dependable commercial option.

## Trains

China's high-speed rail is held up as **the best train network in the world** by community members with heavy use: clean, punctual, affordable, and easy to book. Worth planning around rather than defaulting to flights for intercity travel.

## Shenzhen

### Practical

- Affordable coastal apartments within ~25 minutes of Shenzhen by high-speed rail run roughly **$150–350/month**. These are not listed on major platforms like Trip.com; finding them requires direct contact with local agencies or owners.
- Foreigners renting these units face friction: **police registration** requirements (landlords often unwilling or unaware how to handle) and the absence of a vetted review platform equivalent to Airbnb, so unit quality and landlord reliability are hard to verify in advance.
