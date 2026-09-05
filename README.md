# WhatsApp Bridge (Custom)

![Node.js](https://img.shields.io/badge/Node.js-20+-68a063?logo=node.js&logoColor=white)
![Baileys](https://img.shields.io/badge/Baileys-v6.x-25D366?logo=whatsapp&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue.svg)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)
![Status](https://img.shields.io/badge/Status-Active-success)

A customized WhatsApp bridge built on [Baileys](https://github.com/WhiskeySockets/Baileys) with extended group management endpoints.

## Custom Endpoints Added

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/groups` | List all participating groups |
| `GET` | `/invite/:id` | Generate invite link for a group |
| `POST` | `/create-group` | Create a new WhatsApp group |
| `POST` | `/add-member` | Add participants to a group |
| `POST` | `/promote` | Promote participants to admin |
| `POST` | `/update-description` | Update group description |
| `POST` | `/send` | Send message (supports `noPrefix` flag) |

## Stock Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/health` | Bridge health check |
| `GET` | `/messages` | Get messages |
| `GET` | `/chat/:id` | Get chat/group info |
| `POST` | `/send-media` | Send media files |
| `POST` | `/send-poll` | Send polls |
| `POST` | `/send-location` | Send location |
| `POST` | `/edit` | Edit a sent message |
| `POST` | `/typing` | Send typing indicator |
| `POST` | `/read` | Send read receipt |

## Setup

```bash
npm install
node bridge.js --port 3000 --session ./session --mode self-chat
```

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `WHATSAPP_MODE` | `bot` or `self-chat` | `self-chat` |
| `WHATSAPP_ALLOWED_USERS` | Comma-separated phone numbers | - |
| `WHATSAPP_REPLY_PREFIX` | Message prefix | `⚕ *Hermes Agent*\n────────────\n` |
| `WHATSAPP_DEBUG` | Enable debug logging | `false` |
| `WHATSAPP_SEND_READ_RECEIPTS` | Auto-send read receipts | `false` |

## License

MIT
