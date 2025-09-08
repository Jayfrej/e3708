# Jay Daily Trading EA

## Overview
Jay Daily Trading EA is a MetaTrader 5 Expert Advisor that implements a range breakout strategy. The EA identifies daily trading ranges during specified hours and places pending orders to capture breakout movements with multiple take profit levels.

## Strategy Description
The EA operates on a simple but effective range breakout principle:
1. **Range Formation**: During specified hours (default: 00:00-07:00), the EA tracks the highest high and lowest low to define the daily range
2. **Order Placement**: After the range period ends, it places pending buy stop and sell stop orders above and below the range
3. **Multiple Take Profits**: Uses split orders with different take profit levels (1:1 and 1:2 risk-reward ratios)
4. **Daily Reset**: All activities reset at the start of each new trading day

## Versions Available

### Version 1.01 - Basic Multi-TP Version
- Manual take profit management with partial position closing
- Trailing stop functionality
- Complex trade tracking system

### Version 2.02 - Split Order Version
- Simplified approach using multiple orders with fixed TPs
- Automatic EOD (End of Day) position and order management
- Visual TP level indicators on chart
- More reliable execution

### Version 3.00 - Money Management Version
- **Dynamic lot sizing** based on account balance and risk percentage
- All features from Version 2.02
- Improved risk management
- Professional money management system

## Key Features

### Risk Management
- **Dynamic Position Sizing**: Automatically calculates lot size based on account balance and risk percentage
- **Stop Loss**: Uses range boundaries as natural stop loss levels
- **Multiple Take Profits**: 1:1 and 1:2 risk-reward ratio targets
- **EOD Protection**: Closes all positions and cancels orders at specified time

### Visual Elements
- **Range Box**: Displays the identified range on the chart
- **TP Level Lines**: Shows take profit levels for both buy and sell directions
- **Color-coded indicators**: Green for buy TPs, red for sell TPs

### Automation Features
- **Daily Reset**: Automatically resets for new trading sessions
- **Order Management**: Handles pending order placement and cleanup
- **Position Tracking**: Monitors and manages open positions

## Input Parameters

### Magic & Comment
- **MagicNumber**: Unique identifier for EA trades (default: 12345)
- **OrderComment**: Comment added to all orders (default: "RangeBreakout")

### Money Management (Version 3.00)
- **RiskPercent**: Risk per trade as percentage of account balance (default: 2.0%)

### Time Settings
- **RangeStartHour/Minute**: Start time for range calculation (default: 00:00)
- **RangeEndHour/Minute**: End time for range calculation (default: 07:00)
- **ClosePositions**: Enable/disable EOD closing (default: true)
- **ClosePositionsHour/Minute**: Time to close all trades (default: 22:00)

### Volume & Sizing
- **FixedLots**: Fixed lot size (Versions 1.01 & 2.02 only)
- **OrderBufferPoints**: Buffer in points from range boundaries (default: 5)
- **Slippage**: Allowed slippage for order execution (default: 30)

## Installation Instructions

1. **Download**: Save the .mq5 file to your MetaTrader 5 `Experts` folder
2. **Compile**: Open MetaEditor and compile the EA
3. **Attach**: Drag the EA onto your desired chart
4. **Configure**: Adjust input parameters according to your preferences
5. **Enable**: Ensure automated trading is enabled in MetaTrader 5

## Recommended Settings

### For Forex Majors (EUR/USD, GBP/USD, USD/JPY)
- RiskPercent: 1-2%
- RangeStartHour: 0 (Midnight)
- RangeEndHour: 7 (London Open)
- OrderBufferPoints: 5-10

### For Indices (US30, NAS100, SPX500)
- RiskPercent: 0.5-1%
- RangeStartHour: 0
- RangeEndHour: 9 (Market Open)
- OrderBufferPoints: 10-20

## Risk Warnings

⚠️ **Important Risk Disclosures**:
- Past performance does not guarantee future results
- All trading involves risk of loss
- Never risk more than you can afford to lose
- Test thoroughly on demo accounts before live trading
- Market conditions can change rapidly
- The EA requires active monitoring and periodic adjustment

## Version Comparison

| Feature | v1.01 | v2.02 | v3.00 |
|---------|-------|-------|-------|
| Basic Range Breakout | ✅ | ✅ | ✅ |
| Multiple Take Profits | Manual | Automatic | Automatic |
| Money Management | Fixed Lots | Fixed Lots | Dynamic % Risk |
| EOD Management | Basic | Enhanced | Enhanced |
| Visual Indicators | Basic | Enhanced | Enhanced |
| Complexity | High | Medium | Medium |
| Recommended for | Advanced | Intermediate | All Users |

## Support and Updates

This EA is provided as-is for educational and research purposes. Users should:
- Thoroughly backtest before live use
- Start with small position sizes
- Monitor performance regularly
- Adjust parameters based on market conditions

## Technical Requirements
- MetaTrader 5 platform
- Minimum account balance: $1,000 (recommended)
- Stable internet connection
- VPS recommended for 24/7 operation

## Disclaimer
This software is provided for educational purposes only. Trading involves substantial risk of loss and may not be suitable for all investors. The developers assume no responsibility for trading losses incurred through the use of this EA.
