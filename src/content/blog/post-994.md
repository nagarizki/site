<!-- ---
title: "Pine Script: Creating first working strategy"
meta_title: ""
description: "this is meta description"
date: 2026-04-26T05:00:00Z
image: "/images/blog-post-994-1.png"
categories: ["Pine Script", "Financial Market"]
author: "Rizki"
tags: ["pine script", "tradingview", "strategy"]
draft: false
---

#

#####

#

Ever wondered how people write scripts and create strategies on TradingView? With the help of AI, now strategy creation can be very simple and no coding skills are needed. Nevertheless, knowledge of algorithms, data structures, and logical thinking will help a lot in developing the strategy further.

#

#####

#

I have created a simple working strategy to buy and sell Bitcoin based on trend and momentum. First, before going too deep, I have to make a disclaimer: this strategy is for educational and research purposes. I DO NOT recommend any of you inexperienced people trade your hard-earned money on Bitcoin. If anything, the best advice I can give is for you to just buy and hold, and learn to optimize your buy timing and sizing, and then be patient and let your money work by itself, nothing more and nothing less than that.

#

#####

#

Even if you are an experienced trader, there is a good chance that your strategy won’t beat a buy-and-hold strategy, especially if you started from a deep bear market. So, what I’m trying to say is, even if you’re an experienced Bitcoin trader, you should have your investment account and trading account separated. And I think at this point, you must understand how important the investment account is.

#

######

#

The strategy is a one-directional strategy. This is a long-only strategy, or a spot trading strategy. The time frame used in this strategy is 4h, and the type of trade is swing trading.

#

<p align="center">
<img src="/site/images/blog-post-994-8.png" alt="BTCUSDT.P chart 4H" style="max-width: 80%; height: auto;">
</p>

#

For the trend indicator, I use EMA 22 and EMA 49 crosses. The trend is bullish when EMA 22 is above EMA 49 and both slopes are either neutral or positive. For the momentum indicator, I use Stochastic with %K length 14, %K smoothing 3, and %D smoothing 3.

#

#####

#

The full criteria I set for this strategy are as follows:

- Swing trade based on the 4h time frame with Stochastic (14, 3, 3), EMA 22, and EMA 49
- Entry when Stochastic crosses up and the %K line is at ≤ 60 during the cross
- Entry only when EMA 22 is above EMA 49
- Entry and close at candle close
- Risk:reward 1:1 with full TP, with options to move SL to BEP and do partial TP
- Start date from 2023/01/01 until the current time, 26 April 2026, as of when this article was written
- Initial capital of USDT 10,000 with order size of $5,000, without pyramiding, and with a commission fee of 0.03%
- EMA slope is either neutral or positive on both EMAs

#

<div style="display: flex; justify-content: space-around; gap: 0px; align-items: flex-start;">
<img src="/site/images/blog-post-994-2.png" alt="Strategy results comparison" style="max-width: 24%; height: auto; flex: 1;">
<img src="/site/images/blog-post-994-3.png" alt="Strategy results comparison" style="max-width: 24%; height: auto; flex: 1;">
<img src="/site/images/blog-post-994-4.png" alt="Strategy results comparison" style="max-width: 24%; height: auto;">
<img src="/site/images/blog-post-994-5.png" alt="Strategy results comparison" style="max-width: 24%; height: auto;">
</div>

#

The results are as follows. Equity was down a bit at the beginning and then moved up to the right with higher highs and higher lows since then. Total profit as of 26 April 2026 is 1,343 USDT, or 13.44%. The current win rate is 55.65% with a profit factor of 1.342.

And here comes the fun part. this strategy is not your typical static and boring strategy, as I have set the parameters to support dynamic input. I have, of course, made my own optimization that turns this “first working strategy” into a highly optimized simple trend and momentum strategy. You can see the comparison between the default setting and the tweaked setting results as follows:

#

<p align="center">
<img src="/site/images/blog-post-994-6.png" alt="Strategy results comparison" style="max-width: 80%; height: auto;">
</p>
<p align="center">
<img src="/site/images/blog-post-994-7.png" alt="Strategy results comparison" style="max-width: 80%; height: auto;">
</p>

#

Last but not least, please note that this strategy, or any strategy, is based on past data that we, as creators, have optimized to the best possible version. As we all know, past performance is not a guarantee of future results. A truly robust strategy should still perform well even if its settings are slightly adjusted. However, over time, it may struggle as market conditions evolve.

#

######

# -->
