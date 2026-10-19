# JackAI Platform OS — Official Python SDK (`jackai-sdk-python`)

Official **Python** SDK for **JackAI Platform OS** (`v1.0.0`), generated via [OmniWrap](https://github.com/JacquesGariepy/omniwrap) from `openapi/jackai-v1.openapi.json` and verified in E2B sandboxes.

- **GitHub Organization:** [`github.com/orgs/jackai-dev`](https://github.com/orgs/jackai-dev)
- **Dedicated SDK Repository:** [`jackai-dev/jackai-sdk-python`](https://github.com/jackai-dev/jackai-sdk-python)
- **Umbrella SDK & MCP Hub:** [`jackai-dev/jackai-sdk`](https://github.com/jackai-dev/jackai-sdk)
- **Ecosystem:** PyPI / Python 3.10+ (httpx + pydantic)

## Installation

```bash
pip install jackai-sdk
```

## Supported Granular Spheres (`@jackai/app-sdk` Parity)

Every sphere can be enabled or disabled independently per SaaS (`CodeJackRabbit`, `BoxFleet`, `OmniWrap`) or per customer tenant:
- `auth`: Unified SSO, OIDC/OAuth2 PKCE, Passkeys WebAuthn, Device Flow (`RFC 8628`), V1 Waitlist Gate
- `accounts`: Multi-tenant Organizations, Members, Custom RBAC
- `plans`: Governed Multi-Product Plan Catalog (`free`, `pro`, `team`, `business`, `enterprise`)
- `billing`: Optional 6-Provider Checkout (`stripe`, `polar`, `paddle`, `lemon-squeezy`, `paypal`, `manual`)
- `payouts`: Real-Money Treasury Balance, Bank Payouts (`Standard J+2` & `Instant ~30 min`), Multi-SaaS Revenue Split
- `entitlements` & `metering`: Feature Flags, `-1` Unlimited Quotas, 2-Phase Atomic Usage (`reserve` / `finalize` / `release`)
- `agentic`: Supervised Non-Destructive AI Agent Client (`AgentDestructiveActionBlockedError` hardware guard)

## License

MIT — Copyright (c) 2026 JackAI Platform.
