# NFTm MCP server

NFTm lets an AI assistant quote a Solana NFT collection launch and prepare a signing page. The creator approves every transaction in Phantom. NFTm never asks for a private key or seed phrase.

Endpoint: `https://www.nftm.app/api/mcp` (Streamable HTTP, no login, no API key)

Registry name: `app.nftm/nftm`

## Tools

| Tool | What it does |
|---|---|
| `nftm_quote_launch` | Read only. Returns the cost to launch from the supply, image sizes, and mint price. Nothing is uploaded. |
| `nftm_launch_collection` | Saves a draft and returns a link to `nftm.app/launch/sign/...`. The creator opens it and signs in Phantom. It requires `confirm: true`. Drafts expire after 30 minutes. |

## Install

Gemini CLI:

```bash
gemini extensions install https://github.com/agvelarde/nftm-mcp
```

Or add the server alone:

```bash
gemini mcp add --transport http NFTm https://www.nftm.app/api/mcp
```

Claude, ChatGPT, Cursor, and Grok steps are at [nftm.app/mcp](https://www.nftm.app/mcp).

## Privacy and support

[Privacy Policy](https://www.nftm.app/privacy). Questions: nftmadmin@gmail.com or [@NFTmapp](https://x.com/NFTmapp) on X.

This repository holds only the public install files. The NFTm app source is not public.
