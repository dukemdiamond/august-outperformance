# S&P 500 August 2025 Outperformers Analysis

A Python analysis tool that identifies stocks that went up on days when the S&P 500 was down during August 2025.

## Overview

This project analyzes stock performance during market downturns, specifically finding stocks that were 'green' while the market (^GSPC) was 'red'. 

## Features

- Downloads stock data for 34 tickers using yFinance
- Identifies all S&P 500 down days in August 2025
- Finds stocks that went up on those down days
- Calculates outperformance metrics
- Generates visualizations and exports results to CSV

## Requirements

```bash
pip install yfinance pandas matplotlib sqlite3


```

## Usage

Run the Jupyter notebook cells sequentially to:
1. Download market and stock data
2. Identify market down days
3. Find outperforming stocks
4. Generate analysis and visualizations

## Results Summary

### S&P 500 Down Days in August 2025

The S&P 500 was down on **6 days** in August 2025:

| Date | Market Change |
|------|--------------|
| 2025-08-01 | -0.78% |
| 2025-08-05 | -0.59% |
| 2025-08-07 | -0.54% |
| 2025-08-11 | -0.25% |
| 2025-08-15 | -0.43% |
| 2025-08-19 | -0.54% |

### Outperformers by Day

#### August 1, 2025 (Market: -0.78%)

| Ticker | Open | Close | Stock Change | Outperformance |
|--------|------|-------|--------------|----------------|
| KLAC | 854.34 | 884.71 | +3.56% | 4.34% |
| GNRC | 189.35 | 193.63 | +2.26% | 3.04% |
| ILMN | 92.61 | 94.66 | +2.21% | 3.00% |
| JCI | 104.27 | 106.48 | +2.12% | 2.90% |
| LLY | 745.18 | 760.66 | +2.08% | 2.86% |

#### August 5, 2025 (Market: -0.59%)

| Ticker | Open | Close | Stock Change | Outperformance |
|--------|------|-------|--------------|----------------|
| UNH | 241.16 | 251.00 | +4.08% | 4.67% |
| BP | 32.45 | 33.12 | +2.07% | 2.66% |
| GRAL | 33.21 | 33.75 | +1.63% | 2.22% |
| GNRC | 196.40 | 197.28 | +0.45% | 1.04% |
| NOK | 4.08 | 4.09 | +0.25% | 0.84% |

#### August 7, 2025 (Market: -0.54%)

| Ticker | Open | Close | Stock Change | Outperformance |
|--------|------|-------|--------------|----------------|
| AMD | 166.84 | 172.40 | +3.33% | 3.87% |
| DELL | 130.17 | 133.93 | +2.89% | 3.43% |
| NVO | 48.47 | 48.76 | +0.60% | 1.14% |
| REGN | 556.81 | 558.95 | +0.38% | 0.92% |
| EL | 90.99 | 91.22 | +0.25% | 0.79% |

#### August 11, 2025 (Market: -0.25%)

| Ticker | Open | Close | Stock Change | Outperformance |
|--------|------|-------|--------------|----------------|
| AMD | 170.04 | 172.28 | +1.32% | 1.57% |
| GILD | 119.23 | 120.47 | +1.04% | 1.29% |
| LLY | 628.04 | 633.83 | +0.92% | 1.18% |
| CRWD | 423.82 | 426.43 | +0.62% | 0.87% |
| IDCC | 264.74 | 266.31 | +0.59% | 0.85% |

#### August 15, 2025 (Market: -0.43%)

| Ticker | Open | Close | Stock Change | Outperformance |
|--------|------|-------|--------------|----------------|
| MRNA | 26.97 | 28.02 | +3.89% | 4.32% |
| NICE | 130.60 | 133.16 | +1.96% | 2.39% |
| NVO | 51.44 | 52.41 | +1.89% | 2.31% |
| NOW | 851.77 | 867.24 | +1.82% | 2.24% |
| EL | 89.77 | 90.97 | +1.34% | 1.76% |

#### August 19, 2025 (Market: -0.54%)

| Ticker | Open | Close | Stock Change | Outperformance |
|--------|------|-------|--------------|----------------|
| FI | 137.59 | 139.11 | +1.10% | 1.65% |
| ILMN | 100.82 | 101.60 | +0.77% | 1.31% |
| TXN | 194.67 | 195.94 | +0.65% | 1.19% |
| WFC | 77.16 | 77.53 | +0.48% | 1.02% |
| NVO | 54.57 | 54.78 | +0.38% | 0.93% |

### Top 10 Outperformances in August 2025

| Rank | Ticker | Date | Stock Change | Market Change | Outperformance |
|------|--------|------|--------------|---------------|----------------|
| 1 | UNH | 08/05 | +4.08% | -0.59% | 4.67% |
| 2 | MRNA | 08/15 | +3.89% | -0.43% | 4.32% |
| 3 | KLAC | 08/01 | +3.56% | -0.78% | 4.34% |
| 4 | AMD | 08/07 | +3.33% | -0.54% | 3.87% |
| 5 | DELL | 08/07 | +2.89% | -0.54% | 3.43% |
| 6 | GNRC | 08/01 | +2.26% | -0.78% | 3.04% |
| 7 | ILMN | 08/01 | +2.21% | -0.78% | 3.00% |
| 8 | JCI | 08/01 | +2.12% | -0.78% | 2.90% |
| 9 | LLY | 08/01 | +2.08% | -0.78% | 2.86% |
| 10 | BP | 08/05 | +2.07% | -0.59% | 2.66% |

## Key Findings

- **Total outperformance instances**: 68
- **Unique stocks that outperformed**: 24
- **Average outperformance**: 1.66%
- **Best single-day outperformance**: 4.67% (UNH on August 5)

## Output Files

- `august_outperformers.csv` - Complete dataset of all outperforming instances
- `august_summary_stats.csv` - Summary statistics by stock
