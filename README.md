# Competition Guidelines

## Introduction

As explained in the documentation offered further down this document, the AA Platform is part of a system that dramatically simplifies the creation and operation of crypto trading bots while hosting trading bots competitions. The platform is still under development, and its use along with registration for bots competitions are free of charge for the time being, while running on alpha testing mode.

The functionality offered at this point in time is rather basic and nowhere near complete. We are very much aware of that and accept that early trading will be rather dumb. The reason for hosting early stage competitions is to help drive alpha testing and to integrate early feedback from developers and traders. We want to make sure the platform evolves with developers' and traders' interests in mind.

In the near future, the AA Platform is set to implement a business model by which end users subscribe to bots to have bots trade on their behalf, paying subscription fees to cover the costs of running the bots in the cloud and to pay Dev Teams fees. Fees will be paid in ALGO tokens, the AA Platform’s native token.

Therefore, participating in early competitions not only offers you the chance to win competition prizes, but also makes you a member of the AA Community and sets you in the track to further monetize your efforts once the platform is launched to the general public.

## Competition Rules

### Dates

The first ever competition starts on **Monday April 2nd 2018** at 00:00:00.000 GMT and ends on **Sunday April 10th** at 23:59:59.999 GMT. 

Subsequent competitions shall be announced and confirmed later on.

### Dev Team Registration

We are launching the first competition on an invite-only basis. If you haven’t been invited and want in, send us an email to feedback@advancedalgos.org.

#### Step 1: Poloniex Account

Make sure you have an account with [Poloniex](https://poloniex.com/). If you don't, move swiftly and open one ASAP, as there may be a waiting period. You can proceed an attempt the verification process, however, you will be able to trade even if you don't.

#### Step 2: Your Own Bots

The next step is creating your own GitHub Organization and your own bots. Follow the [Getting Started Guide](https://github.com/AdvancedAlgos/Documentation/wiki/Overview) to do so.

#### Step 3: Competition Configuration

Next, enter your organization’s and bot’s details in the [competition configuration file](https://github.com/AAArena/First-Closed-Doors-Competition/blob/master/this.competition.config.json). Fork the file, enter your details and submit a pull request. Someone at our end will take care of merging your details.

### About Bots

Each Dev Team is allowed to compete with one trading bot only. You can create as many Indicator Bots as required to implement your strategy. If you find that making calculations within your trading bot’s code instead of creating actual indicator bots is preferrable, feel free to do so.

**Once a bot is released in the competition it cannot be modified.**

> NOTE: The AA Platform is still in its infancy, on alpha stage. It is likely that errors may occur at runtime. Should any unhandled error occur --either at the bot or platform level-- resulting in the bot interrupting its execution, the bot will be considered dead and will not be restarted. This is unfortunate but it is the reality of alpha testing applications.

### Markets

The competition takes place in the **USDT-BTC market in Poloniex**.

For the time being, the platform serves both historic and live trades data. Trades are performed at Dev Team’s accounts at the exchange, thus having an account with Poloniex is a requirement for participating. 

For the time being, we will only be using Poloniex and the USDT-BTC market to do our trading. We will expand the horizon in upcoming competitions.

### Capital

Each Dev Team trades with their own funds within their own accounts at the exchange. Dev Teams are fully responsible for the trading they do.

Each bot is allowed to trade up to 0.001 BTC Initial Capital (roughly equivalent to USD 10). This is in order to minimize risk at this first ever alpha stage competition.

> NOTE: In order to avoid unnecessary risk, we recommend withdrawing excess funds from the exchange  or block them by placing an order at a price you know will not be filled.

#### Partial Profits Trading

Bots are allowed to trade with partial profits. This is the only way in which bots can legally trade with more than the Initial Capital specified above. Thus, the limit is 0.001 BTC + Partial Profits. The platform serves running balances that your bot can check in order to make sure the limit is not exceded.

**Bots trading more than the allowed limit are automatically disqualified.** 

#### Fees

Participating in the competition and running your bots on the AA Platform is free of charge at this point in time.

For your information, Poloniex charges the following fees for every order filled:

| **Maker** | **Taker** |
|-----------|-----------|
| 0.15% | 0.25% |

Poloniex fees are explained [here](https://poloniex.com/fees/).

That said, the competition does NOT take fees into consideration while calculating the ranking and competition results.

### Ranking

The ranking is determined by a very simple performance metric: [Return on Investment (ROI)](https://www.investopedia.com/terms/r/returnoninvestment.asp).

#### Formula

**ROI** = (Gain from Investment - Cost of Investment) / Cost of Investment (expressed as a percentage)

#### Definitions

* **Cost of Investment** = Initial BTC Balance = 0.001 BTC. For the purpose of this competition, this is a constant, meaning that if you use less than 0.001 BTC to do your trading, we will still use 0.001 BTC as the value for this constant.

> NOTE: It doesn’t matter how much BTC you actually have in the exchange. The platform keeps track of your trades and running balances during the competition.

* **Gain from Investment** (or Losses, expressed as negative Gains) = Final BTC Balance

#### Winners

The result of the competition is determined by the position of each bot in the ranking by the end of the competition.

#### Example

**Bot A ends up with 0.0015 BTC**

Bot A ROI = (0.0015 - 0.001) / 0.001 * 100% = 50%

**Bot B ends up with 0.0005 BTC**

Bot B ROI = (0.00075 - 0.001) / 0.001 * 100% = -25%

**Bot C ends up with 0.001 BTC**

Bot B ROI = (0.001 - 0.001) / 0.001 * 100% = 0%

**Final Ranking**

| **Position** | **Bot** | **ROI** |
|:----------|:---------:|----------:|
| 1st | A | 50 % |
| 2nd | C | 0 % |
| 3rd | B | -25 % |

### Prizes

The competition awards 0.5 BTC and 500,000 ALGO (worth USD 5,000 as of this date) as prize money for the top 3 performers during each competition period, with the following caveats:

* BTC Prizes are awarded to bots with ROI >= 10% (10% profits and higher) only.

* ALGO prices are awarded always, even when ROI is negative (loss).

**The prize money is awarded as follows:**

| **Position** | **BTC Prize** | **ALGO Prize** |
|:----------|----------:|----------:|
| 1st | 0.30 | 300,000 |
| 2nd | 0.15 | 150,000 |
| 3rd | 0.05 | 50,000 |

> NOTE: In the [example above](#example), only Bot A would have been awarded the BTC Prize, as it is the only one with a ROI bigger than 10%.

## Term of Service

The information provided in this document is intended for informational purposes only and is subject to change without notice. The AA Project may make improvements and/or changes in the products, pricing and/or the programs described in this information at any time without notice.

## Disclaimer

THE AA PLATFORM AND ITS ASSOCIATED PRODUCTS AND SERVICES ARE PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY, SUITABILITY FOR A PARTICULAR PURPOSE, OR NON-INFRINGEMENT.

IN NO EVENT WILL THE AA PROJECT BE LIABLE TO ANY PARTY FOR ANY DIRECT, INDIRECT, SPECIAL OR OTHER CONSEQUENTIAL DAMAGES FOR ANY USE OF THE AA PLATFORM, OR ANY OTHER ASSOCIATED SERVICE OR WEB SITE, INCLUDING, WITHOUT LIMITATION, ANY LOST PROFITS, BUSINESS INTERRUPTION, LOSS OF FUNDS, PROGRAMS OR OTHER DATA OR OTHERWISE, EVEN IF WE ARE EXPRESSLY ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

# The AA Platform

## Overview

There are three GitHub Organizations you need to be familiar with:

* [Advanced Algos](https://github.com/AdvancedAlgos): Features repositories with the AA Platform code including the bits that run in the cloud (AACloudPlatform) and in the web browser, along with a few other platform-related tools and documentation.

* [AAMasters](https://github.com/AAMasters): Its a showcase GitHub organization similar to the one each Dev Team needs to create for themselves. It features several examples of bots, each in their corresponding repository.

* [AAArena](https://github.com/AAArena): Its another showcase GitHub organization featuring the AA Application hosting the trading bot competition you area about to enter.

## Setting Up a Dev Team Organization

The very first step is setting up a GitHub organization named after your own Dev Team. Make sure the name of the organization starts with “AA”, just like in the above example AAMasters. Also make sure that the phrase “Advanced Algos” is part of the organization’s description.

