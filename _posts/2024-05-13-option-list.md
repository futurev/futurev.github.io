---
layout:     post
title:      Understand Option Strategies
subtitle:   List of strategies
date:       2024-05-13
author:     JX
header-img: img/green.png
catalog: true
tags:
    - Option strategy
---
> overall option strategies

# Understand option strategies

## Option Basics

How to read an options symbol:
TICKER SYMBOL + YEAR OF EXPIRATION + MONTH OF EXPIRATION + DAY OF EXPIRATION + C for call or P for put + the strike price

So if you bought symbol -xyz241231c100 at $1.00, the contract gives you the right to buy typically 100 shares for $1 per share till December 31st, 2024 for a total cost of $100 (price quoted is multiplied typically by 100).

Follow these steps to find the best sectors
To be a successful momentum trader, you need to be able to identify the best sectors quickly and accurately. You can probably do this manually with many screeners out there, but the basic steps are as follows:

First you need to identify the stocks and ETFs you are interested in.
Determine the number of stocks and ETFs trading close to their yearly highs.
Sort the chosen stocks and ETFs from highest to lowest to see which are doing the best.
Devise an entry strategy. You may want to enter when an instrument is showing short-term strength or wait for a pullback and buy on weakness. Either approach can work; the important point is to execute a plan.
Devise an exit strategy. You should know going into the trade at what point (or conditions) you will take profits and at what point (or conditions) you will exit with a loss.

   1. Call vs Put
   
        |         | Buyer     |   Seller   | ITM       | OTM     |
        |---------|-----------|----------- |-----------|-----------|
        | Call    |    buy  |    sell  | strike < stock price | strike > stock price|
        | Put     |    sell |    buy   | strike > stock price | strike < stock price|
   
       - seller to get premium, expect **_OTM_** at expire date, ie. Option writers agree to sell options contracts because they don't think the security will perform like the option buyer expects.
       The option writer is provided income from the premium they received for their obligation in that contract.
        
           strike price > stock price for ${\color{blue}Call}$
           
           strike price < stock price for ${\color{purple}Put}$
           
       - buyer to get profit, expect **_ITM_** at expire date, ie. buy options to help protect existing investments, By buying an agreement that lets them sell at a certain price, they create a higher minimum value for the assets they want to offload.
       
           strike price < stock price for ${\color{blue}Call}$
           
           strike price > stock price for ${\color{purple}Put}$     
    
   2. Greek letters in Option
   
        There are five letter in option pricing as listed in the table.
    
        | Greek Letter | Meaning |
        | ------ | ------- |
        | Delta | The impact of a $1 change in the stock price on the option price |
        | Gamma | The change in delta caused by a $1 change in the stock price |
        | Theta | The rate at which the time value of an option decays |
        | Vega | The change in option price due to a change in implied volatility |
        | Rho | The sensitivity of an option's price to changes in the risk-free interest rate |
        - 2.1 delta
            The sensitivity of an options price to the change in the price of the underlying asset. For instance, delta would measure how much the theoretical value of a call option on XYZ Company stock would change, given a change in the value of XYZ stock. For each dollar move in the underlying asset, the option price would approximately move by the delta. For example, Stock share 242--> 243, delta=0.7, Call 12.8--> 12.8+0.7=13.5. The delta for a put works similarly, but would be a negative number; as the price of the underlying asset decreases in value, the price of the option increases. 
            For buyer, delta the higher the better, for seller, the lower the better.
            delta, in absolute terms, as the probability of an option’s being in the money at expiration. another way to view delta is from a net position on the underlying security. For instance, if a trader holds a call contract with a delta of 0.75, it is equivalent to being long 75 shares of the underlying security. Similarly, holding a put option or shorting a call, with a net delta of –0.75, would be equivalent to being short 75 shares of the underlying security.
            
            All else being equal, an in-the-money call option's delta will move toward 1 at expiration, and an in-the-money put option delta will move toward –1 at expiration.
Delta may be more sensitive to time to expiration and volatility the further in the money or out of the money the option is.
            Delta may be more sensitive to time to expiration and volatility the further in the money or out of the money the option is.
            
         - 2.2 Gamma—This Greek is directly related to delta. Whereas delta will change based on a price move in the underlying asset, gamma is the rate of change, or sensitivity, to a price change in the underlying for delta. Basically, gamma measures how well delta describes an option's sensitivity. Positive gamma accelerates gains and decelerates losses on options contracts; this quality can be found in long calls and long puts(buyers). Alternatively, negative gamma decelerates gains and accelerates losses, and is a characteristic of written calls and puts(sellers). **Gamma’s impact is most noticeable in at-the-money options, and when gamma is large, delta can change rapidly**. For example, AAPL $125 --> $126, delta=0.555, gamma=0.044, then new delta=0.555+0.044=0.599.
         无论是认购期权还是认沽期权，标的证券价格在期权行权价附近时，Gamma最大，表明对Delta的变化速度最快；
        相同标的、到期月份、行权价的认购和认沽期权的Gamma值相同

        平值期权的Gamma相对剩余期限的变化，期限越长，Gamma值越小；而越接近到期日，Gamma越大，Delta变化越剧烈。实质期权和虚值期权的Gamma相对剩余期限的变化，当期限逐渐变长时，Gamma变化愈平缓；当期限逐渐变短时，Gamma变化愈剧烈

        - 2.3 Vega—This is a measure of an option price’s sensitivity for a given change in implied volatility. An increase in the implied volatility (i.e., the expected volatility) of an option will increase the value of both call and put options, and falling implied volatility decreases the value of both types of options. Vega can be an extremely useful Greek, particularly when volatility is expected to increase or decrease.
            Vega的准确定义为期权价值对于标的证券波动率的一阶偏导
            期权的Vega是正的。波动率增加将使期权价值更高，波动率减小将降低期权的价值
            具有相同标的、相同行权价、相同到期日的认购期权与认沽期权的Vega是相等的
            标的资产价格越偏离期权行权价，Vega越小，即期权价格对波动率的变化越不敏感；标的资产价格越接近期权行权价，Vega值越大，即期权价格对波动率的变化越敏感
        
        - 2.4 Theta—This Greek measures the effect that time's decreasing has on an option as it approaches expiration. This is also known as time decay. Theta quantifies how much value is lost on the option due to the passing of time. It is typically negative for purchased calls and puts, and positive for sold calls and puts. Note that it is not advisable for inexperienced traders to trade near expiration, as it can be more complex than when there is more time to expiration.
        1.在其他条件都不变的情况下，越接近到期日，期权的时间价值越小。Theta代表了期权价值随时间推移而逐渐衰减的程度。认购期权的Theta是负的；认沽期权的Theta一般为负的，但在过度实值的情况下也可能为正。

        2.随着标的证券价格的变化，在行权价附近时，Theta的绝对值最大。也就是说，在行权价附近时，到期时间的变化对期权价值的影响最大。

        3.对于实值期权和虚值期权，越接近到期日，Theta越接近于0；而平值期权的Theta，反而绝对值越大。

        - 2.5 Rho—There are several other secondary Greeks that are not as widely used as those listed above. It describes an option's sensitivity to a change in interest rates. Note that the relationship between interest rates and option value is not significant. Strictly speaking, an increase in interest rates will increase the value of a call option and decrease the value of a put option. If rates were expected to change dramatically, some traders might incorporate Rho into their analysis. In practical terms, interest rates influence option prices very little.
        1.认购期权的Rho是正的，认沽期权的Rho是负的。对于认购期权，利率上升使得期权价值上升；对于认沽期权，利率上升使得期权价值下降。

        2.Rho随着标的证券价格单调递增。对于认购期权，标的价格越高，利率对期权价值的影响越大；对于认沽期权，标的价格越低，利率对期权价格的影响越大。越是实值的期权，利率变化对期权价值的影响越大；越是虚值的期权，利率变化对期权的价值影响越小。

        3.Rho随着期权到期，单调收敛为0。也就是说，期权越接近到期日，利率变化对期权价值的影响越小


## Strategy

list from futubull

1. Single Option
    - Definition
    
      buy or sell call/put option

      <img width="323" alt="Screen Shot 2024-05-13 at 1 43 58 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/f2dad543-7900-4a4d-a49f-02e342134763">
    
   - Analysis
   
        | Scenario       | Action       | Max Profit               | Risk                   | Breakeven Point       | Use Cases                                               |
        |----------------|--------------|--------------------------|------------------------|-----------------------|---------------------------------------------------------|
        | Long Call      | buy      | Unlimited                | Premium Paid           | Strike Price + Premium| Bullish speculation, hedging a short position           |
        | Short Call     | sell      | Premium Received         | Unlimited              | Strike Price + Premium| Bearish speculation, generating income                  |
        | Long Put       | sell      | Strike Price - Premium   | Premium Paid           | Strike Price - Premium| Bearish speculation, hedging a long position            |
        | Short Put      | buy      | Premium Received         | Strike Price - Premium | Strike Price - Premium| Bullish speculation, generating income                  |
        
        - long call vs short put: bullish positions, stock price in up trend
        - short call vs long put: bearish positions, stock price in down trend
        - use cases for each scenario

            Long Call: Used when expecting stock price to increase significantly. It allows them to profit from the price appreciation with limited risk.
            
            Short Call: Used when expecting stock price to decrease or remain stagnant. It allows them to collect premium income while capping their potential profit and risking unlimited losses if stock price rises significantly.
            
            Long Put: Used when expecting stock price to decrease significantly. It allows them to profit from the price decline with limited risk.
            
            Short Put: Used when an investor is bullish on the underlying asset and believes the price will remain stable or increase. It allows them to collect premium income while risking potential losses if stock price decreases significantly below the strike price.
    
2. Covered Stock

 <img width="327" alt="Screen Shot 2024-05-13 at 2 35 16 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/b11ffa75-4c53-4f1d-b1a4-ebccd1c79a29">
 
   - 2.1 Covered Call
       - Definition: long stock + short call(OTM, strike > stock price, strike高于可能的涨幅，以确保不被执行)
       - Analysis
       希望股票上涨，但是又不能涨得太快，最好不要涨过call的行权价(strike)。
       Covered call的盈亏是这样计算的，最大盈利是 (strike price-stock price)+option premium。假如购买股票的价格是350，同时covered call的行权价(strike)是360，获得的期权金(premium)是1.63，最大盈利就是(360-350)+1.63=11.63。盈亏点是(stock price-option premium)，按照刚才的例子就是 350-1.63=348.37，也可以理解为成本价降低了。最大亏损取决于股票的跌幅
       第一种情形是股票大涨，超过了行权价。这时候股票是盈利的，但是那个call有可能是亏损的，总体上还是盈利的。但是无法享受行权价以上的利润。收盘时如果不做处理，股票就被call走了，游戏就结束了。

	    第二种情形是股票上涨，但是没有超过行权价。这时候股票盈利，call的价值变为零，call也盈利了，总体上是盈利的。可以再选择一个新的行权价和日期，继续这样的游戏。

	    第三种情形是股票下跌。这时候股票亏损，call的价值变为零，call是盈利的，总体上是亏损的。可以再选择一个新的行权价和日期，继续这样的游戏。
       
       通常适合小牛市，就是总体上是上涨的，但是又不是疯涨的股票。Covered call不适合持续下跌的股票，虽然每次的call都是盈利的，但是股票下跌的亏损远远大于call的盈利。
       当你手里有股票的话，不要闲置，而是要不断卖出call获得期权金获利。
       当你想处理手里的股票的时候，也不要盲目卖出，而是用covered call的方法让别人买走，自己还可以得到期权金。

   <img width="316" alt="covered_call" src="https://github.com/futurev/futurev.github.io/assets/18621736/9124b479-8042-4869-a799-4190534a7fc9">   
   
   - 2.2 Protective Put
       - Definition:
       - Analysis
   
   <img width="316" alt="protective_put" src="https://github.com/futurev/futurev.github.io/assets/18621736/8c6823be-6d78-4b72-9622-a708127feece">

           

3. Vertical Spread

<img width="327" alt="Screen Shot 2024-05-13 at 2 35 27 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/a29ff350-3e04-4c10-b1d9-373cbab9ba4c">
    
   - 3.1 bull spread
        - Bull Put Spread
            - **_Definition_**: 
                sell OTM Put (strike<stock price), buy further OTM Put(<<stock price), premium received upfront
                Put, higher strike, higher pricing
                Put is OTM, if strike < current stock price 
                 
            - **_Example_**: 
                Underlying Stock: XYZ is trading at $50.
            - **_Strategy_**: 
                Sell 1 XYZ $45 Put for $2 and Buy 1 XYZ $40 Put for $1. expect XYZ will not drop under $45,(go up or stable)
            - **_Maximum Profit_**: 
                The maximum profit is the net premium received - cost. 
                In this example, the net premium received is $1. So, the maximum profit is $1.
            - **_Maximum Loss_**: 
                The maximum loss occurs if the price of the underlying stock is below the lower strike price at expiration. 
                In this case, both options would be exercised. The investor would be obligated to buy the stock at the higher strike price and sell it at the lower strike price. 
                The difference in strike prices is $45 - $40 = $5. However, the net premium received is $1. So, the maximum loss is $5 - $1 = $4.  
            - **_Breakeven Point_**: 
                $43 ($45 higher strike price - $2 net premium received).

        - Bull Call Spread
            - **_Definition_**: 
                buy OTM call, buy further OTM call
                Put, higher strike, higher pricing, 
                Put is OTM, if strike < current stock price 
                 
            - **_Example_**: 
                Underlying Stock: XYZ is trading at $50.
            - **_Strategy_**: 
                Sell 1 XYZ $45 Put for $2 and Buy 1 XYZ $40 Put for $1. expect XYZ will not drop under $45,(go up or stable)
            - **_Maximum Profit_**: 
                The maximum profit is the net premium received - cost. 
                In this example, the net premium received is $1. So, the maximum profit is $1.
            - **_Maximum Loss_**: 
                The maximum loss occurs if the price of the underlying stock is below the lower strike price at expiration. 
                In this case, both options would be exercised. The investor would be obligated to buy the stock at the higher strike price and sell it at the lower strike price. 
                The difference in strike prices is $45 - $40 = $5. However, the net premium received is $1. So, the maximum loss is $5 - $1 = $4.  
            - **_Breakeven Point_**: 
                $43 ($45 higher strike price - $2 net premium received).
                
  - 3.2 bear spread
       - Definition:
       - Analysis
    
  - 3.3 box spread
       - Definition:
       - Analysis

4. Straddle

<img width="327" alt="Screen Shot 2024-05-13 at 2 35 32 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/8d7b5c06-4e6e-4cb4-9ce0-21c7e5b4f41e">

   - Definition:
   - Analysis

5. Strangle & Guts

<img width="327" alt="Screen Shot 2024-05-13 at 2 36 09 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/24673104-0998-4f7d-84f1-3c707174154f">


   - Definition:
   - Analysis

6. Collar

<img width="327" alt="Screen Shot 2024-05-13 at 2 36 13 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/e5ae6d64-a638-4b36-8c1f-38300e5a9b9f">

   
   - Definition:
   - Analysis

7. Butterfly

 <img width="327" alt="Screen Shot 2024-05-13 at 2 36 16 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/353b19e8-c240-48ff-b85f-215a3271c481">

   - Definition:
   - Analysis
   
8. Condor

<img width="327" alt="Screen Shot 2024-05-13 at 2 36 20 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/e3e5e443-0869-40e3-b5ef-f03cb2dc7264">

   
    - Definition:
    - Analysis

   
9. Iron Butterfly
    <img width="327" alt="Screen Shot 2024-05-13 at 2 36 23 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/a33e0e6f-f80b-4a33-9604-4fd140b7718f">

    - Definition:
    - Analysis

   
10. Iron Condor
<img width="327" alt="Screen Shot 2024-05-13 at 2 36 27 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/65c24e0c-5844-4665-b3ee-678da0f52568">


    - Definition:
    - Analysis

    
11. Straps & Guts


    - Definition:
    - Analysis

12. Custom

<img width="327" alt="Screen Shot 2024-05-13 at 2 36 30 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/aca76020-8132-470d-9aea-7726d38b16c2">

    
    - Definition:
    - Analysis



    

