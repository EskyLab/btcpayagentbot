# BTCPay Agentbot

Accept Bitcoin payments for AI agent subscriptions ₿

<h3 align="center">
  Bitcoin Payment Processor for Agentbot Platform
</h3>
<p align="center">
  BTCPay Agentbot is a free and open-source Bitcoin payment processor adapted for the Agentbot platform — accept BTC and Lightning payments for agent subscriptions with zero fees or intermediaries.
</p>
<p align="center">
  <a href="https://github.com/Eskyee/btcpayagentbot">
    <img src="https://img.shields.io/github/v/release/Eskyee/btcpayagentbot"/>
  </a>
  <a href="https://github.com/Eskyee/btcpayagentbot/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/Eskyee/btcpayagentbot"/>
  </a>
</p>

---

## What Is BTCPay Agentbot?

A Bitcoin payment processor built specifically for the [Agentbot](https://agentbot.sh) platform. Forked from [BTCPay Server](https://github.com/btcpayserver/btcpayserver) and adapted for AI agent billing.

### Features

- ₿ **Bitcoin & Lightning** — Accept BTC and Lightning payments for agent subscriptions
- 🔐 **Zero Fees** — No third-party processors, no percentage fees
- 🤖 **Agent Integration** — Built for Agentbot's multi-tenant agent platform
- ⚡ **Instant Settlements** — Lightning Network for near-instant payments
- 🌍 **Global** — Accept payments from anywhere in the world
- 🔑 **Self-Hosted** — Run your own payment node, own your keys

### Use Cases

- **Agent Subscriptions** — Pay for AI agent access with Bitcoin
- **Token Gating** — Gate agent features behind onchain ownership
- **Micropayments** — Pay-per-use agent calls via Lightning
- **Treasury Management** — Agent-to-agent payments on Base + Bitcoin

---

## Deploy

### Railway (Recommended)

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.app/template/agentbot-btcpay)

### Docker

```bash
docker run -d \
  --name btcpayagentbot \
  -p 8080:8080 \
  -v btcpayagentbot_data:/datadir \
  ghcr.io/eskyee/btcpayagentbot:latest
```

### From Source

```bash
git clone https://github.com/Eskyee/btcpayagentbot.git
cd btcpayagentbot
dotnet build
dotnet run --project BTCPayServer
```

---

## Architecture

```
┌─────────────┐     ┌──────────────────┐     ┌─────────────┐
│   Agentbot  │────▶│  BTCPay Agentbot │────▶│  Bitcoin    │
│   Platform  │     │  Payment Node    │     │  Network    │
└─────────────┘     └──────────────────┘     └─────────────┘
       │                      │
       │              ┌───────┴───────┐
       │              │  Lightning    │
       │              │  Network      │
       └──────────────┴───────────────┘
```

## Links

- **Agentbot Platform:** [agentbot.sh](https://agentbot.sh)
- **Agentbot GitHub:** [Eskyee/agentbot](https://github.com/Eskyee/agentbot)
- **Original BTCPay Server:** [btcpayserver.org](https://btcpayserver.org)

## License

MIT — Based on [BTCPay Server](https://github.com/btcpayserver/btcpayserver) (MIT)

---

Built with ₿ by [RaveCulture](https://raveculture.xyz) · Powered by [Agentbot](https://agentbot.sh)
