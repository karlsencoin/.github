# Karlsen Coin

A **GPU-friendly, ASIC-resistant BlockDAG** implementation powering
decentralized AI inference on consumer hardware.

Karlsen combines the GHOSTDAG consensus protocol with the
**KarlsenHashV2** proof-of-work algorithm (FishHashPlus DAG) — designed
from the ground up to keep mining accessible to everyday GPU owners
while channeling that same hardware into useful AI compute through the
KarlsenAI inference network.

---

## Our Core Ecosystem

| Repository | Description | Status |
|------------|-------------|--------|
| [**rusty-karlsen**](https://github.com/karlsencoin/rusty-karlsen) | Full Karlsen node (Rust). KarlsenHashV2 PoW + GHOSTDAG consensus. | `Stable` |
| [**karlsenminer**](https://github.com/karlsencoin/karlsen-miner) | High-performance GPU miner (AMD OpenCL + NVIDIA CUDA). | `Beta` |
| [**karlsenai-amd**](https://github.com/karlsencoin/karlsenai-amd) | KarlsenAI worker for AMD ROCm GPUs. Earn $KLS by serving LLM / image inference. | `Beta` |
| [**karlsenai-nvidia**](https://github.com/karlsencoin/karlsenai-nvidia) | KarlsenAI worker for NVIDIA CUDA GPUs. Rust + candle inference backend. | `Beta` |
| [**karlsen-mobile**](https://github.com/karlsencoin/karlsen-mobile) | Flutter wallet for iOS and Android. | `Released` |

---

## Quick Start

### Run a Karlsen node
Download the latest release of [rusty-karlsen](https://github.com/karlsencoin/rusty-karlsen/releases/latest)
and run it with the included fallback seeders — no extra configuration needed.

### Mine $KLS
Grab the matching binary from [karlsenminer/releases](https://github.com/karlsencoin/karlsenminer/releases/latest):
- **AMD GPUs:** OpenCL kernel, ~29 MH/s on RX 6800
- **NVIDIA GPUs:** CUDA kernel with `__ldg()` DAG reads and high-priority streams
- **HiveOS / mmpOS:** Linux build with full integration

### Earn $KLS by running an AI worker
Choose the build for your GPU:
- **AMD ROCm** → [karlsenai-amd/releases/latest](https://github.com/karlsencoin/karlsenai-amd/releases/latest)
  Supports LLM chat (companion / character / fiction), multimodal vision
  (DOCUMENT role), and Stable Diffusion image generation.
- **NVIDIA CUDA** → [karlsenai-nvidia/releases/latest](https://github.com/karlsencoin/karlsenai-nvidia/releases/latest)
  Rust + candle backend with multi-model GGUF support.

Workers earn **100% of the prompt reward** (zero platform commission)
paid directly to your $KLS wallet.

### Use KarlsenAI services
- **Web chat & image generation:** [ai.karlsencoin.org](https://ai.karlsencoin.org)
- **Mobile wallet:** [karlsencoin.org/downloads](https://karlsencoin.org/)
- **Swap KLS ↔ USDT / BNB / MATIC / AVAX:** [change.karlsencoin.org](https://change.karlsencoin.org)

---

## Network Infrastructure

- **Mainnet RPC:** `mobile.karlsencoin.org:42110` (TLS-wrapped gRPC)
- **Block explorer:** [explorer.karlsencoin.org](https://explorer.karlsencoin.org)
- **Node map (KGI):** [kgi.karlsencoin.org](https://kgi.karlsencoin.org)
- **Ticker API:** [ticker.karlsencoin.org](https://ticker.karlsencoin.org)
- **DNS seeders:** `seeder1.karlsencoin.org` ... `seeder3.karlsencoin.org`

---

## Community & Support

- **Website:** [karlsencoin.org](https://karlsencoin.org/)
- **Discord:** [discord.gg/QyrvshRBJV](https://discord.gg/QyrvshRBJV)
- **Telegram:** [t.me/KarlsenTaskForce](https://t.me/KarlsenTaskForce)
- **Exchange:** [NonKYC.io — KLS/USDT](https://nonkyc.io/market/KLS_USDT)

---

## Contributing

The repositories listed above accept issues and pull requests. For
larger changes, open an issue first so we can align on approach. The
Discord **#dev** channel is the fastest place to ask questions.

## License

Each repository carries its own license. The Rust node is forked from
the rusty-kaspa codebase and remains under its original ISC / MIT terms.
KarlsenAI worker components are licensed individually — see each repo's
`LICENSE` file.
