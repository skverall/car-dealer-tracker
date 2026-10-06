# Car Dealer Tracker — Gemini CLI Extension

Connect [Gemini CLI](https://github.com/google-gemini/gemini-cli) to your Car Dealer Tracker dealership: live inventory, profit, expenses, sales, debts and cash — asked in plain language.

**Install:**

```bash
gemini extensions install https://github.com/skverall/car-dealer-tracker
```

On first use Gemini opens your browser to sign in to Car Dealer Tracker (OAuth 2.1 with PKCE, dynamic client registration). No API keys to copy.

## Requirements

- A Car Dealer Tracker **Dealer Pro** subscription (checked on every request; free/guest accounts cannot connect).
- Sign-in with email/password, Google or Apple.

## Tools (all read-only)

| Tool | Returns |
|---|---|
| `get_inventory_summary` | Counts by status, capital in stock, days held, 90-day sell-through |
| `list_vehicles` | Inventory search by make, model, VIN, stock number or status |
| `get_vehicle` | One vehicle by UUID |
| `get_profit_summary` | Revenue, profit and expenses for preset or custom periods |
| `list_sales` | Recent sales with amount and profit |
| `list_expenses` | Recon and overhead spend by category/date |
| `get_expense` | One expense by UUID |
| `list_debts` | Payables/receivables with balances and overdue flags |
| `get_accounts_overview` | Cash and account balances grouped by type |

All tools are strictly read-only (`dealer:read`) and respect your team-role permissions.

## Links

- Website: <https://cardealertracker.app/>
- MCP reference: <https://cardealertracker.app/mcp/>
- Privacy: <https://cardealertracker.app/privacy>
- Support: <hello@cardealertracker.app>

## License

MIT
