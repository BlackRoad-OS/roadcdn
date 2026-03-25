<!-- BlackRoad SEO Enhanced -->

# roadcdn

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad OS](https://img.shields.io/badge/Org-BlackRoad-OS-2979ff?style=for-the-badge)](https://github.com/BlackRoad-OS)
[![License](https://img.shields.io/badge/License-Proprietary-f5a623?style=for-the-badge)](LICENSE)

**roadcdn** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

## About BlackRoad OS

BlackRoad OS is a sovereign computing platform that runs AI locally on your own hardware. No cloud dependencies. No API keys. No surveillance. Built by [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc), a Delaware C-Corp founded in 2025.

### Key Features
- **Local AI** — Run LLMs on Raspberry Pi, Hailo-8, and commodity hardware
- **Mesh Networking** — WireGuard VPN, NATS pub/sub, peer-to-peer communication
- **Edge Computing** — 52 TOPS of AI acceleration across a Pi fleet
- **Self-Hosted Everything** — Git, DNS, storage, CI/CD, chat — all sovereign
- **Zero Cloud Dependencies** — Your data stays on your hardware

### The BlackRoad Ecosystem
| Organization | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform and applications |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate and enterprise |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | Artificial intelligence and ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware and IoT |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity and auditing |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing research |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | Autonomous AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh and distributed networking |
| [BlackRoad Education](https://github.com/BlackRoad-Education) | Learning and tutoring platforms |
| [BlackRoad Labs](https://github.com/BlackRoad-Labs) | Research and experiments |
| [BlackRoad Cloud](https://github.com/BlackRoad-Cloud) | Self-hosted cloud infrastructure |
| [BlackRoad Forge](https://github.com/BlackRoad-Forge) | Developer tools and utilities |

### Links
- **Website**: [blackroad.io](https://blackroad.io)
- **Documentation**: [docs.blackroad.io](https://docs.blackroad.io)
- **Chat**: [chat.blackroad.io](https://chat.blackroad.io)
- **Search**: [search.blackroad.io](https://search.blackroad.io)

---


Content Delivery Network for the BlackRoad ecosystem.

## Features

- **Edge Caching** - KV-based cache at the edge
- **R2 Origin** - Store assets in R2
- **Image Optimization** - Resize and compress images
- **Cache Purging** - Purge by path or all
- **Proxy Caching** - Cache external URLs
- **Analytics** - Cache hit stats

## Quick Start

```bash
npm install
wrangler deploy
```

## API Endpoints

### Assets
- `GET /cdn/:path` - Serve cached asset
- `PUT /cdn/:path` - Upload asset
- `DELETE /cdn/:path` - Delete asset
- `GET /assets` - List all assets

### Cache
- `POST /purge` - Purge cache
- `GET /stats` - Cache statistics

### Image Optimization
```
GET /image/photo.jpg?w=800&h=600&q=80&f=webp
```

### Proxy
- `POST /proxy` - Cache external URL
- `GET /proxy?url=...` - Serve proxied content

### Preload
```bash
POST /preload
{
  "urls": ["https://example.com/image.png"]
}
```

## Headers

- `X-Cache: HIT/MISS` - Cache status
- `X-Cache-Hits: N` - Number of cache hits
- `ETag` - Entity tag for conditional requests

## License

Proprietary - BlackRoad OS, Inc.
