# Triple Moving Average EA MT4

This code is an Expert Advisor (EA) for MetaTrader 4 (MT4) that uses a triple moving average strategy to open trades in the forex market. The EA is developed by Forex Robot Easy Team and is designed to be used by professional traders.

## Global Variables

The EA uses the following global variables, which can be adjusted by the user:

- `MA1Period`: The period of the first moving average.
- `MA2Period`: The period of the second moving average.
- `MA3Period`: The period of the third moving average.
- `lotSize`: The trading lot size.
- `stopLoss`: The stop loss level in pips.
- `takeProfit`: The take profit level in pips.
- `spreadFilter`: The maximum allowed spread.
- `timeFilterStartHour`: The start hour for the time filter.
- `timeFilterEndHour`: The end hour for the time filter.
- `newsFilter`: A boolean value to enable or disable the news filter.
- `maFilter`: A boolean value to enable or disable the moving average filter.

## Expert Initialization

The `OnInit` function is called during the initialization of the EA. This is where any necessary initialization logic can be added. In this code, no specific initialization logic is implemented.

## Expert Deinitialization

The `OnDeinit` function is called during the deinitialization of the EA. This is where any necessary deinitialization logic can be added. In this code, no specific deinitialization logic is implemented.

## Expert Tick

The `OnTick` function is called on every tick of the market. This is where the main trading logic of the EA is implemented.

1. The code first checks if the current spread is within the allowed range. If the spread is too high, the code skips the current tick.
2. Next, the code checks if the current time is within the allowed trading hours. If the current time is not within the allowed hours, the code skips the current tick.
3. If the news filter is enabled, the code checks if there are any high-impact news events. If a high-impact news event is detected, the code skips the current tick.
4. The code calculates the values of the three moving averages using the `iMA` function.
5. If the moving average filter is enabled and the moving averages are aligned in the correct order (ma1 > ma2 > ma3), a trade is opened using the `OrderSend` function.
6. If the trade is executed successfully, any necessary logic can be added. If there is an error while opening the trade, error handling logic can be implemented.

## Expert Start

The `OnStart` function is called once when the EA starts. This is where any necessary start logic can be implemented. In this code, no specific start logic is implemented.

## Product Description

This code is a sample Expert Advisor that implements a triple moving average strategy for trading in the forex market. The EA uses three moving averages with adjustable periods to determine the entry and exit points for trades. The EA also includes additional features such as spread filtering, time filtering, and news filtering.

Please note that Forex Robot Easy Team is not the official developer of this product. This code is provided as a sample that can work as described in the product. To find the official developer of this product, please refer to the link provided: [Triple Moving Average EA MT4 - Forex Software for Professional Traders](https://forexroboteasy.com/forex-robot-review/review-triple-moving-average-ea-mt4-forex-software-for-professional-traders/).

For detailed reviews and trading results of this product, please visit the provided link.
