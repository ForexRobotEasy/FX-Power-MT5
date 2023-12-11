# FX Power MT5

This is a trading robot designed to automate forex trading using the MetaTrader 5 platform. The FX Power MT5 robot is developed by the Forex Robot Easy Team, and you can find more information about the product and its trading results on their website [here](https://forexroboteasy.com/forex-robot-review/fx-power-mt5-review-elevate-forex-trading-with-2020-strategy-update/). Please note that ForexRobotEasy is not the official developer of this product, but we are providing this sample code that can work as described in the product.

## Functionality

The FX Power MT5 robot uses historical data and technical indicators to calculate the strength of different currencies. It then executes trades based on the calculated currency strength and other trading conditions. The robot continuously updates the currency strength history and executes trading logic when trading is allowed.

## Code Structure

The code is structured into several functions that handle different aspects of the trading robot.

### Global Variables

- `trade`: An object of the `CTrade` class used for executing trades.
- `isTradingEnabled`: A boolean flag indicating whether trading is enabled or not.

### Function: `IsTradingAllowed()`

This function checks if trading is allowed based on market conditions, time, and other factors. It returns a boolean value indicating whether trading is allowed or not.

### Function: `SendAlert(string message)`

This function is responsible for sending alerts via email, message, and mobile notifications. It takes a message parameter and adds the necessary logic to send the alerts.

### Function: `CalculateStrength(string currency)`

This function calculates the strength of the specified currency using historical data and technical indicators. It returns the calculated strength value as a double.

### Function: `UpdateStrengthHistory()`

This function updates the strength history for all major currencies using the `CalculateStrength` function. It calculates the strength for each currency and stores the calculated value in a data structure or file.

### Function: `ExecuteTradingLogic()`

This function executes the trading logic based on the calculated currency strength and other trading conditions. It performs actions such as executing trades using the `trade` object when specific conditions are met.

### Function: `OnTick()`

This function handles the `OnTick` event, which is triggered on each tick of the market. It checks if trading is enabled and allowed, updates the strength history, and executes the trading logic.

### Function: `OnInit()`

This function initializes the trading robot. It enables trading, sets the expert magic number, and configures the terminal for ease of use. It may also optimize the software for high-resolution displays and tablet/touchscreen usage.

### Function: `OnDeinit(const int reason)`

This function handles the `OnDeinit` event, which is triggered when the trading robot is deactivated or removed from the chart. It performs cleanup tasks such as closing open trades and releasing resources.

### Function: `OnStart()`

This function handles the `OnStart` event, which is triggered when the trading robot is started. It starts the trading robot and sets a timer to trigger the `OnTick` event every second.

### Function: `OnTimer()`

This function handles the `OnTimer` event, which is triggered when the timer set in the `OnStart` function expires. It triggers the `OnTick` event to update the trading logic.

## Conclusion

The FX Power MT5 trading robot automates forex trading by calculating the strength of different currencies and executing trades based on the calculated values. It is a powerful tool that can help traders make informed trading decisions. For more information about this product and its trading results, please visit the developer's website [here](https://forexroboteasy.com/forex-robot-review/fx-power-mt5-review-elevate-forex-trading-with-2020-strategy-update/).
