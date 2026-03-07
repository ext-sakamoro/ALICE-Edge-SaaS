# ALICE-Edge SaaS

Embedded model generator — send the law, not data

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Edge |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/generate` | エッジモデル生成 |
| `POST /api/v1/deploy` | エッジデバイスへデプロイ |
| `GET  /api/v1/devices` | エッジデバイス一覧 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
