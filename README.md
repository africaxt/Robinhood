# africaxt/Robinhood — Superseded

> **This repo is no longer actively maintained.**
> The Robinhood integration has moved to [africaxt/Tanulytics](https://github.com/africaxt/Tanulytics).

## Migration

| This repo | Tanulytics equivalent |
|---|---|
| `Robinhood.py` | `scripts/robinhood_fetch.py` |
| `trade_history_downloader.py` | `scripts/aggregator.py` (Trade History table) |
| Manual auth flow | TOTP-automated via `ROBINHOOD_TOTP_SECRET` in `config/.env` |

The Tanulytics implementation:
- Uses `robin_stocks` (maintained, TOTP-automated 2FA)
- Normalises Robinhood data into a unified schema alongside IBKR, FXCM, Schwab
- Pushes to Airtable and Notion automatically via `python scripts/run_all.py`

## Why this fork exists

Originally forked from [robinhood-unofficial/pyrh](https://github.com/robinhood-unofficial/pyrh) in 2021 for
standalone Robinhood access. The `api-token-auth` endpoint used here was deprecated by Robinhood and
no longer works as of 2024.

---

*Part of the [africaxt](https://github.com/africaxt) trading ecosystem.*
