# Crypto Buy Signal scheduler

Public, secret-free scheduler for the private Crypto Buy Signal dashboard.

- Runs every 15 minutes at off-peak minute offsets.
- Calls the dashboard's server-side deterministic monitor.
- Stores the private Sites access token only in the GitHub Actions secret `SITES_BYPASS_TOKEN`.
- Does not contain Telegram credentials, portfolio data, or trading orders.
- Can also be launched manually from the Actions tab.

The dashboard sends Telegram messages only for new actionable transitions and deduplicates repeated signals.
