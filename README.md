# PrometheX Docs

Documentation site for PrometheX, powered by [Mintlify](https://mintlify.com/).

## Tech Stack

- [Mintlify](https://mintlify.com/) -- docs-as-code platform
- MDX content files with Mintlify components (`Steps`, `Card`, `CardGroup`, etc.)
- Configuration via `docs.json`

## Prerequisites

- Node.js >= 18
- Mintlify CLI (`npm install -g mintlify`)

## Quick Start

```bash
# Install the Mintlify CLI (one-time)
npm install -g mintlify

# Start local dev server
mintlify dev
```

The site will be available at `http://localhost:3000`.

## Content Structure

All content lives in `.mdx` files organized by documentation tab:

```
.
├── docs.json                 # Mintlify site configuration (nav, theme, colors)
├── user-guide/               # End-user documentation
│   ├── what-is-promethex.mdx
│   ├── getting-started/      # Wallet setup, get USDC, first trade
│   ├── trading/              # How trading works, fees
│   ├── markets/              # Market lifecycle, resolution, disputes
│   └── faq/                  # Safety, supported chains, geo, glossary
├── platform/                 # B2B / integration docs
│   ├── overview.mdx
│   ├── why-promethex.mdx
│   ├── integration/          # White-label, embedded, API-only
│   ├── deployment/           # Chains, staging env, contract addresses
│   └── security/             # Security model, audits
├── api-reference/            # REST API documentation
│   ├── overview.mdx
│   ├── quickstart.mdx
│   ├── authentication.mdx
│   ├── markets/              # List, get, create markets
│   ├── trading/              # Deposit, withdraw, positions, claim
│   ├── liquidity/            # Add / remove liquidity
│   ├── resolution/           # Settle market, resolution status
│   ├── websocket.mdx
│   ├── errors.mdx
│   ├── rate-limits.mdx
│   └── changelog.mdx
├── contracts/                # Smart contract reference
│   ├── overview.mdx
│   ├── addresses.mdx
│   ├── prediction.mdx
│   └── resolution/           # UMA oracle, multisig modules
├── images/                   # SVG diagrams (architecture, flows)
└── logo/                     # Light / dark logo PNGs
```

Navigation tabs and page ordering are defined in the `navigation` section of `docs.json`.

## Deployment

Mintlify handles deployment automatically. Pushing to the connected branch triggers a rebuild on the Mintlify platform -- no CI/CD pipeline needed on our side.

To preview changes before pushing:

```bash
mintlify dev
```
