# finance-manage-qoder

> 🚧 **SCAFFOLD** — khung sườn Agent-First cho quản lý tài chính cá nhân. Chưa có DB/kernel/scripts implementation.
> Đọc [`PLAN.md`](PLAN.md) để biết lộ trình & bước tiếp theo. Kiến trúc đã duyệt: [`docs/architecture/agent-first-blueprint.md`](docs/architecture/agent-first-blueprint.md).

Repo **độc lập, cùng cấp** `money-gemini` (không lồng). Git remote: `finance-manage-ag` (chờ push 1st commit).

## Đây là gì

Hệ thống tài chính cá nhân **Agent-First / Zero App-Code**: AI Agent + Markdown skills + MCP kernel + engine deterministic + **Neon Postgres** (append-only ledger) + **Obsidian** (local-first dashboard) + Google Sheets (projection qua GAS).

Phạm vi: txn cá nhân · chuyển khoản · trả nợ thẻ · **batch transfer** (`/batch` tự fill xlsx) · cashback 26 thẻ · nợ person · túi sinh lời · đối soát · refund/FX · vàng/wealth · **report tháng**.

## Cấu trúc repo

| Thư mục | Nội dung | Trạng thái |
| :--- | :--- | :---: |
| `skills/` | 13 SKILL.md + `invariants.md` + `_INDEX.md` | 🚧 skeleton |
| `accounts/cards/` | 26 thẻ + `_INDEX` (structural pre-fill, rules TODO) | 🚧 skeleton |
| `accounts/banks/` | 25 bank/wallet + linked cards | 🚧 skeleton |
| `accounts/yield-pockets/` | 3 túi sinh lời (MSB, Shinhan, VPBank) | 🚧 skeleton |
| `accounts/wealth/` | Vàng & chứng chỉ quỹ | 🚧 skeleton |
| `people/` | 16 person + `_INDEX` | 🚧 skeleton |
| `config/` | bank-mappings, mcc, subscriptions, installments | 🚧 skeleton |
| `batches/templates/` | `_TEMPLATE_SCHEMAS.md` (chờ attach xlsx) | 🚧 skeleton |
| `dashboards/` | 4 Obsidian DataviewJS view (read-only) | 🚧 skeleton |
| `docs/architecture/` | Blueprint đã duyệt | ✅ |
| `docs/knowledge/` | Bridge 22 knowledge docs (chờ port) | 🚧 skeleton |
| `kernel/` | engine · mcp · worker | ⬜ trống (P2+) |
| `db/` | schema · views · functions | ⬜ trống (P2) |
| `scripts/` | neon_cli.py, batch_xlsx.py | ⬜ trống (P2+) |
| `reports/` · `runs/` · `reconcile/` | Output artifacts | ⬜ trống |

## Bắt đầu

1. **Đọc plan:** mở [`PLAN.md`](PLAN.md) — heatmap, timeline, phase/sprint, bước tiếp theo (P2).
2. **Obsidian:** *Open folder as vault* → chọn repo này → bật Dataview (Enable JavaScript Queries). Dashboard sẽ live sau khi kernel views tồn tại (P4+).
3. **Bất biến:** [`skills/invariants.md`](skills/invariants.md) — mọi skill phải tuân thủ.

## Bước tiếp theo (P2)

Neon DB migration → parity gate → tạo kernel/MCP → connect MCP → push 1st commit. Chi tiết: [`PLAN.md` §5](PLAN.md).

## Bảo mật

- Repo nên để **private** (chứa số tài khoản, tên người nhận).
- `.env.local` gitignored. Không commit secret / production `service_role` key.
- MD `accounts/`·`people/` là projection 1 chiều từ DB — không sửa tay làm nguồn sự thật.

## Nguồn sự thật

- `money-gemini` — DB schema + `cashback.pure.ts` + 22 knowledge docs (read-only reference).
- `finance-manage-ag` — draft tham khảo (read-only, không touch).