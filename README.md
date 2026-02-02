# Auction Market Theory Indicator

Pine Script v6 indicator that plots Auction Market Theory (AMT) session levels for RTH/ETH, including value area, VPOC, initial balance extensions, and session VWAP.

## Features

- RTH and ETH session detection with configurable session times.
- RTH levels: HOD/LOD, IB30, IB60, IB0.5, IB1.5, IB2.
- Value Area (VAH/VAL) and VPOC computed from a session volume profile histogram.
- ETH levels: ONH/ONL/ONMID/ONVPOC.
- Session VWAP overlay.
- Optional labels and/or lines, with ability to extend lines to the right.
- Previous session level carry-forward.
- Bookmap CSV-style logging and alert payload formatting.

## Inputs

- Sessions: `RTH session time`, `ETH session time`.
- Levels toggles: `Show HOD and LOD`, `Show IB`, `Show IB30`, `Show IB60`, `Show IB1.5`, `Show IB2`, `Show ONH, ONL, ONVPOC, ONMID`, `Show VAH and VAL`, `Show VPOC`.
- Value Area: `Value Area %`, `Number of Histograms`.
- Display: `Show price labels`, `Show Lines at price levels`, `Extend lines to the right`, `Session VWAP`, `VWAP color`.
- Lookback: `Look back time in hours for previous sessions`.
- Logging: `Symbol Prefix` for Bookmap datafeed output.

## Getting started

1. Open TradingView and create a new Pine Script.
2. Paste the contents of [src/auction-market-theory.pine](src/auction-market-theory.pine).
3. Save and add the indicator to a chart.

## Notes

- The indicator is designed to run on intraday timeframes with session boundaries.
- VPOC/VAH/VAL are calculated from a volume profile histogram built from session bars.
- Alerts emit a CSV-style payload containing AMT levels for Bookmap.

## Structure

- [src/auction-market-theory.pine](src/auction-market-theory.pine) — indicator source.
