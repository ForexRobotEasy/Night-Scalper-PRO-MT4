# Night Scalper PRO MT4 Expert Advisor

This is the code for the Night Scalper PRO MT4 Expert Advisor, developed by the Forex Robot Easy Team. This Expert Advisor is designed to trade multiple currency pairs during the night trading session. It utilizes various parameters and functions to execute trades based on specific trading signals and conditions.

## Input Parameters

- StopLoss: The stop loss level in pips for each trade.
- TakeProfit: The take profit level in pips for each trade.
- LotSize: The lot size for trading.
- NewsFilter: Enable or disable the news filter functionality.
- DrawdownPercent: The maximum allowed drawdown percentage.

## Global Variables

- AccountBalance: The current account balance.
- MaxDrawdown: The maximum allowed drawdown.

## Initialization Function

The OnInit() function is responsible for initializing the Expert Advisor. It retrieves the current account balance and calculates the maximum drawdown based on the specified drawdown percentage. If the news filter is enabled, it initializes the news filter functionality.

## Deinitialization Function

The OnDeinit() function is called when the Expert Advisor is being stopped or removed. It performs any necessary cleanup tasks.

## Trading Function

The OnTick() function is the main trading function of the Expert Advisor. It is called on each tick of the market. It first checks if the news filter is enabled and if a news event is approaching. If so, it disables trading until the news event is over. 

If trading is enabled, it checks for buy and sell trading signals using the BuySignal() and SellSignal() functions. If a buy signal is present, it opens a buy position with the specified stop loss and take profit levels. If a sell signal is present, it opens a sell position.

After executing the trades, it checks for drawdown using the CheckDrawdown() function. If the current drawdown exceeds the maximum drawdown, it closes all open positions using the CloseAllPositions() function.

## Additional Functions

- IsNewsEventApproaching(): This function checks if a news event is approaching. It can be implemented to retrieve news event data and determine if a news event is within a specified time frame.
- BuySignal(): This function checks for a buy trading signal. It can be implemented to analyze market conditions and generate a buy signal based on specific criteria.
- SellSignal(): This function checks for a sell trading signal. It can be implemented to analyze market conditions and generate a sell signal based on specific criteria.
- CheckDrawdown(): This function calculates the current drawdown and checks if it exceeds the maximum drawdown. It returns true if the maximum drawdown is reached, indicating the need to close all positions.
- CloseAllPositions(): This function closes all open positions by iterating through each position and using the OrderClose() function.

Please note that Forex Robot Easy is not the official developer of this product. This code is provided as a sample and can work as described in the product. For detailed reviews and trading results of this product, you can visit the official developer's site at [Night Scalper PRO MT4 Review](https://forexroboteasy.com/forex-robot-review/night-scalper-pro-mt4-review-multi-currency-expert-advisor/). To find the official developer of this product, you can use MQL5.
