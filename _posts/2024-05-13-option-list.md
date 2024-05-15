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

   1. Call vs Put
   
        |         | Buyer     |   Seller   | ITM       | OTM     |
        |---------|-----------|----------- |-----------|-----------|
        | Call    |    buy  |    sell  | strike < stock price | strike > stock price|
        | Put     |    sell |    buy   | strike > stock price | strike < stock price|
   
       - seller to get premium, expect **_OTM_** at expire date, ie.
        
           strike price > stock price for ${\color{blue}Call}$
           
           strike price < stock price for ${\color{purple}Put}$
           
       - buyer to get profit, expect **_ITM_** at expire date, ie.
       
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

  
    2.1 Covered Call
       - Definition: long stock + short call
       - Analysis

   <img width="316" alt="covered_call" src="https://github.com/futurev/futurev.github.io/assets/18621736/9124b479-8042-4869-a799-4190534a7fc9">
   
   
    
    2.2 Protective Put
       - Definition:
       - Analysis
   
   <img width="316" alt="protective_put" src="https://github.com/futurev/futurev.github.io/assets/18621736/8c6823be-6d78-4b72-9622-a708127feece">

           

4. Vertical Spread

<img width="327" alt="Screen Shot 2024-05-13 at 2 35 27 PM" src="https://github.com/futurev/futurev.github.io/assets/18621736/a29ff350-3e04-4c10-b1d9-373cbab9ba4c">

    3.1 bull spread
       - Definition:
       - Analysis
       
    3.2 bear spread
       - Definition:
       - Analysis
    
    3.3 box spread
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



    

