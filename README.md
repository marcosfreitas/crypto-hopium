# Crypto Hopium — Reality Check

A single-file web tool for checking whether a cryptocurrency price prediction is mathematically plausible or delusional.

## What it does

When someone claims a coin will reach a certain price — "XRP will hit $10!", "SHIB will reach $0.01!" — it sounds exciting. But the missing variable is always **market cap**. If that price requires the coin to be worth more than all human wealth combined, it's not a prediction, it's a fantasy.

This tool calculates:

- **Projected market cap** at the claimed price, compared to real-world reference points (Bitcoin, all gold ever mined, global stock markets, total human wealth)
- **Required price multiplier** from today's price
- **Your projected return** on a given investment
- **Required CAGR** if a timeframe is given — how fast would the price need to grow each year?
- **Opportunity cost** — what would the same money earn in an S&P 500 index fund?
- **Where that market cap lands** on a log-scale money ruler, from $1B to $10 quadrillion, with real reference points marked on it
- **Delusion score** on a seven-step verdict ladder

The verdict scale runs: Plausible → Speculative → Ambitious → Unlikely → Delusional → Mathematically Impossible → Cosmic Delusion.

Annual world GDP appears in the reference table but not on the ruler. GDP is output per year; every other reference is an accumulated total, and plotting a flow against stocks on one money axis compares two different things.

## Why it exists

Crypto communities produce a constant stream of price predictions designed to trigger FOMO. Most people do not stop to check whether the required market cap is physically possible. A little arithmetic is the best sobriety test.

The tool is intentionally opinionated: it treats "delusional" as a mathematically defined term, not a moral judgement.

## How to use

Open `index.html` in any browser. No build step. No dependencies. No server required.

Select a coin from the preset list (~50 top coins) or enter the circulating supply and current price manually, then fill in the claimed target price. Everything else is optional but adds more context to the analysis.

Live price data is fetched from the Binance API when a coin is selected. All other calculations are local.

## Technical notes

- Single HTML file with vanilla JS
- No frameworks, no npm, no build process
- ~50 coin presets with live price data via Binance API (fetched on coin selection)
- Supply values are approximate; verify current figures on CoinGecko before drawing serious conclusions
- Reference point values (Bitcoin mcap, total gold, etc.) are approximate order-of-magnitude anchors
- Available in English and Brazilian Portuguese (auto-detected from browser language)
- Every analysis can be shared as a link: the coin, supply, price, target, timeframe and language travel in the query string, and opening the link re-runs the case
- Developer utilities: open the browser console and run `runTests()` for unit tests, `runApiTests()` to verify all Binance pairs

## Status

Personal tool. Open source, but not actively maintained or seeking contributions.

## License

© 2026 Crypto Hopium. Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).

You are free to use, share, and adapt this tool for non-commercial purposes, provided you give appropriate credit. Commercial use is not permitted.
