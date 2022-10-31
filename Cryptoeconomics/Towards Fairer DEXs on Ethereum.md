# Towards Fairer DEXs on Ethereum
One price per token per block.

Status: Draft 📝    
Speaker(s): [Felix Leupold](https://app.devcon.org/speakers/CGP99L)  
Date: Day 4 - Oct 14, 2022  
Track: Cryptoeconomics  
Keywords: Mechanism Design,MEV,Batch Auctions  
Video link: https://archive.devcon.org/archive/watch/6/towards-fairer-dexs-on-ethereum/?tab=YouTube
Slides link:

Felix Leupold from CoW Swap

The adoption of decentralized trading (DEX trading) is still a tiny portion of global trading (2B$) compared to 60B$ for digital assets (including centralized exchanges) and 6000B$ Global Forex.

## Brief History of Dex markets

### The Art of Designing Markets

[Alvin Roth](https://en.wikipedia.org/wiki/Alvin_E._Roth), winner of the Nobel Memorial Prize in Economic Sciences, his [essay](https://hbr.org/2007/10/the-art-of-designing-markets) covers the necessary requirements for a market to function. 

Here are the three properties he covers for a market to function:
1. Thickness - brings together a large enough propotion of potential buyers and sellers.
2. Safety - incentivize participants to truthfully reveal their preferences.
3. Overcome congestion - give market participants means to make satisfactory choices when faced with a variety of options. _Importance of [[Ethereum scalability]], better DEX creation will piggyback on that_.

### On-chain Limit Order Book DEXs
Examples of some first DEXs; Etherdelta, Idex, Oasis.

Worked fine for some token pairs ETH/USDC... but had a fundamental flaw, but required participants to update their quotes and bids to keep the market in sync. But with the explosion of tokens this was very hard to create thickness. [[AMM]] came along and solved this problem.  

- Required *active* market making
- Difficult to bootstrapp new pairs 
- High cost for managing orders

### AMMs democratizing market making
Came to solve the limitation of on-chain limit order book DEXs. Based on Logarithmic Market Scoring Rule [Hanson et al. 2002]()

## Building Safety on top of AMMs

### Root Cause
One asset, can have many prices in the same block on Ethereum. 
An example of that is [Block 15673043]() from the most liquid pair on Ethereum ETH/USD was traded 11 times at 8 different prices, the difference between the lowest and the highest price in this block was >1.05%.

> this makes the market unsafe

### Solution

One price per token per block
