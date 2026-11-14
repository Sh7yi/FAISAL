# Halal Swing (www.5brgold.com)

Personal halal stock signals. Render runs `node server.js` (one file, no dependencies).

- **Signals**: high-impact good news on stocks that Zoya rates COMPLIANT and XTB sells as real shares, with a verdict, chart, trade plan, 10-point check and explosion check.
- **Penny scalps**: halal XTB stocks under $5 checked every minute on the 1-minute chart.
- **My trades**, **Scorecard**, **How it works** and **Status** pages.

## Settings on Render (Environment)

| Key | What it does |
| --- | --- |
| `ZOYA_API_KEY` | Halal ratings. Without it no stocks are shown. |
| `ALPACA_KEY_ID`, `ALPACA_SECRET_KEY` | Real-time Benzinga news and pre-market prices (free account). |
| `ANTHROPIC_API_KEY` | Claude reads each headline. |
| `TELEGRAM_BOT_TOKEN`, `TELEGRAM_CHAT_ID` | Alerts on your phone. |
| `GITHUB_DATA_TOKEN` | Saves signals, trades and the scorecard to the `halal-data` branch so they survive restarts. Needs Contents: Read and write on this repo. |
| `REQUIRE_PASSWORD`, `SITE_PASSWORD` | Optional login. Set `REQUIRE_PASSWORD=true` to lock the site. |
| `MAX_PRICE`, `SCALP_MAX_PRICE` | Optional price limits (default: any price; penny scalps up to $5). |

The GitHub workflows copy XTB's stock list and earnings dates to the `feeds` branch every 3 hours, and ping the site every 10 minutes so it never sleeps.
