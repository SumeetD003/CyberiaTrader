# CyberiaTrader Expert Advisor

**CyberiaTrader** is a custom Expert Advisor (EA) for MetaTrader 4 (MT4).
It is designed to automate trading strategies with configurable parameters for money management, trade entry/exit logic, and risk control.

This repository includes:

* `cyberiatrader.mq4` – The source code of the EA (MQL4).
* `cyberiatrader.ex4` – The compiled EA file (ready to use in MT4).
* `cyberiatrader.ini` – Example configuration file with optimized parameters.

---

##  Installation

1. Copy `cyberiatrader.ex4` into your MT4 directory:

   ```
   MQL4/Experts/
   ```
2. (Optional) Copy `cyberiatrader.mq4` to the same folder if you want to edit/compile the code.
3. Place `cyberiatrader.ini` in the `tester` or `presets` folder:

   ```
   MQL4/Presets/
   ```
4. Restart MetaTrader 4.
5. Attach **CyberiaTrader** to a chart or load it in the **Strategy Tester**.

---

##  Configuration

The EA behavior is controlled through the `.ini` (preset) file.
Key parameters include:

### General

* **positions**: Maximum number of open trades.
* **deposit**: Starting deposit (for backtests).
* **currency**: Account currency.
* **fitnes / genetic**: Optimization controls in the tester.

### Inputs (Trading Logic)

* **ExitMarket** – Enable/disable market exits.
* **ShowSuitablePeriod / ShowMarketInfo / ShowAccountStatus / ShowStat / ShowDecision / ShowDirection** – Debugging & chart display options.
* **BlockSell / BlockBuy** – Restrict trade directions.
* **StopLoss / TakeProfit / Risk** – Classic risk management.
* **AutoLots** – Enable dynamic lot sizing.
* **EnableMACD / EnableMA / EnableCyberiaLogic / EnableMoneyTrain / EnableReverceDetector** – Activate strategy modules.
* **ReverceIndex, MoneyTrainLevel, MACDLevel** – Strategy thresholds.
* **SlipPage** – Maximum slippage allowed.
* **SymbolsCount** – Number of symbols to trade simultaneously.
* **AutoStopLossIndex / StopLossIndex** – Automatic stop-loss logic.

### Limits (Safety Net)

* **balance\_enable, balance** – Minimum balance filter.
* **profit\_enable, profit** – Profit target to stop trading.
* **marginlevel\_enable, marginlevel** – Minimum margin level.
* **maxdrawdown\_enable, maxdrawdown** – Max allowed drawdown (%).
* **consecloss\_enable, consecloss** – Limit consecutive losses.
* **consecwin\_enable, consecwin** – Limit consecutive wins.

---

##  Usage

* Run **Strategy Tester** in MT4 with `cyberiatrader.ini` to optimize settings.
* Apply on live or demo accounts with caution.
* Always test with risk management enabled (`StopLoss`, `TakeProfit`, `Risk`).
