# TileWhisper Landing Page

Static landing page for TileWhisper plugin — deployed at [tilewhisper.com](https://tilewhisper.com).

## Deploy

Via Docker (recommended):

```bash
cd /home/andy/projects  # Or wherever docker-compose.yml lives
docker compose up -d
```

This runs:
- `tilewhisper-web` on port `2377` → nginx proxy serves at `tilewhisper.com`
- `tilewhisper-relay` on port `2376` → Node.js WebSocket server at `relay.tilewhisper.com`

## Configure NPM Proxy Manager

Set up both routes in NPM:

1. **tilewhisper.com** → target: `2377` (landing page)
2. **relay.tilewhisper.com** → target: `2376` (relay server)

NPM will handle SSL certificates automatically via Let's Encrypt.
