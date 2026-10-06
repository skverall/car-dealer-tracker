# Car Dealer Tracker MCP

This extension connects Gemini to the user's Car Dealer Tracker dealership account through the MCP server at `https://mcp.cardealertracker.app/mcp` (OAuth 2.1 with PKCE; sign-in opens in the browser on first use).

## What the tools return

| Tool | Use it for |
|---|---|
| `get_inventory_summary` | Inventory counts by status, capital tied up in stock, average/longest days held, 90-day sell-through |
| `list_vehicles` | Searching the lot by make, model, VIN, stock number, or status (newest first) |
| `get_vehicle` | One vehicle by its exact UUID, including `updated_at` |
| `get_profit_summary` | Revenue, profit and expenses for a preset or custom period |
| `list_sales` | Recent vehicle sales with amount, profit (if permitted) and vehicle name |
| `list_expenses` | Recon and overhead spend, filterable by category and date |
| `get_expense` | One expense by its exact UUID, including `updated_at` |
| `list_debts` | Payables/receivables with balances, due dates and overdue flags |
| `get_accounts_overview` | Cash and financial account balances grouped by type |

## Behavior rules

- Every public tool is read-only (`dealer:read`). The server offers no way to create, change or delete records.
- Amounts are shown in the dealership's own currency and are never converted.
- Results respect the signed-in user's team-role permissions: fields hidden by the user's role are omitted from responses, not zeroed.
- Guests cannot connect; a Dealer Pro subscription is required.
- Vehicle and expense UUIDs must be taken verbatim from `list_vehicles` / `list_expenses` responses.

## Support

Docs: <https://cardealertracker.app/mcp/> — Support: <hello@cardealertracker.app>
