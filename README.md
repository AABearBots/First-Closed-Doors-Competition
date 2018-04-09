# Introduction

*Welcome to the Advanced Algos Closed-Doors First Bot Competition!* Join us for a dive into the world of crypto-currency trading to collaborate and compete with a select group in the AA Arena hosted on the AA Platform. This marks the beginning of a new community for developers and traders and a chance to cultivate the ultimate open-source crypto-currency trading bot community and ecosystem.

# Contents

[Competition Guidelines](#competition-guidelines)

[The AA Platform](#the-aa-platform)

[Setting up Your Development Environment](#setting-up-your-development-environment)

[Trading Bots](#trading-bots)

[Starting out Your Own Bot](#starting-out-your-own-bot)

[Launching Your Bot](#launching-your-bot)

<hr>

# Competition Guidelines

## The Competition

The AA Arena is an organization built around the competition of crypto-currency bots. The foundation of the Arena is powered by the AA Platform — a system developed by Advanced Algos that dramatically simplifies the creation and operation of crypto-currency bots.

At this point, the AA platform is still in the alpha-stage. A large portion of functionality is still under development and the early generation of bots will be rather dumb. However, hosting early stage competitions will help drive development as well as integrate early feedback and interests from both developers and traders.

In the near future, the AA Platform is set to implement an ecosystem enabling end-users access to subscriptions for bots that trade on their behalf. Subscription fees cover the costs of the bot infrastructure and pay development team fees. Fees will be paid in ALGO tokens, the AA Platform’s native token.

Participating in early competitions not only offers the chance to win competition prizes, but makes you a part of the AA Community and provides increased potential of monetizing your efforts when the platform is released to the general public.

## Competition Rules

### Dates

The first ever competition starts on **Monday April 30th 2018** at 00:00:00.000 GMT and ends on **Sunday May 6th** at 23:59:59.999 GMT.

Subsequent competitions shall be announced and confirmed later on.

### Dev Team Registration

We are launching the first competition on an invite-only basis. If you haven’t been invited and want in, send us an email to feedback at advancedalgos dot org.

### Requirements
#### Step 1: Poloniex Account

Make sure you have an account with [Poloniex](https://poloniex.com/). If you don't, move swiftly and open one ASAP, as there may be a waiting period. You can attempt the verification process, however, you should be able to trade even if you don't verify your account.

#### Step 2: Join Dev's WhatsApp Group

Send us an email to feedback at advancedalgos dot org with your name and phone number. We will add you to a closed WhatsApp Group through which we will offer support.

#### Step 3: Your Own Bots

The next step is creating your own GitHub Organization and your own bots. We will go through the whole process further down this document.

### About Bots

Each Dev Team is allowed to compete with one trading bot only. You can create as many Indicator Bots as required to implement your strategy. If you find that making calculations within your trading bot’s code instead of creating actual indicator bots is preferable, feel free to do so.

**Once a bot is released in the competition it cannot be modified.**

> NOTE: The AA Platform is still in its infancy, on alpha stage. It is likely that errors may occur at runtime. Should any unhandled error occur --either at the bot or platform level-- resulting in the bot interrupting its execution, the bot will be considered dead and will not be restarted. This is unfortunate but it is the reality of alpha testing applications. Execution Logs will be provided for post-mortem analisys.

#### Bots License

The AAMaster bots offered as templates are released under the GNU Affero General Public License (AGPL) to guarantee:

> * the freedom to use the software for any purpose,
> * the freedom to change the software to suit your needs,
> * the freedom to share the software with your friends and neighbors, and
> * the freedom to share the changes you make.
>
> _(Extract from [The Foundations of the GPL](https://www.gnu.org/licenses/quick-guide-gplv3.html))_

It is a policy of Advanced Algos to require all bots running on the AAPlatform to be released under the same license. In order to do that. We will guide you through the process to do just that further down this document.


### Markets

The competition takes place in the **USDT-BTC market in Poloniex**.

For the time being, the platform serves both historic and live trades data. Trades are performed at Dev Team’s accounts at the exchange, thus having an account with Poloniex is a requirement for participating.

For the time being, we will only be using Poloniex and the USDT-BTC market to do our trading. We will expand the horizon in upcoming competitions.

### Capital

Each Dev Team trades with their own funds within their own accounts at the exchange. Dev Teams are fully responsible for the trading they do.

Each bot is allowed to trade up to 0.001 BTC Initial Capital (roughly equivalent to USD 10). This is in order to minimize risk at this first ever alpha stage competition.

> NOTE: In order to avoid unnecessary risk, we recommend withdrawing excess funds from the exchange  or block them by placing an order at a price you know will not be filled.

#### Partial Profits Trading

Bots are allowed to trade with partial profits. This is the only way in which bots can legally trade with more than the Initial Capital specified above. Thus, the limit is 0.001 BTC + Partial Profits. The platform serves available balances that your bot can check in order to make sure the limit is not exceeded.

> Bots attempting to trade more than the allowed limit generate an exception that needs to be handled.

#### Fees

Participating in the competition and running your bots on the AA Platform is free of charge at this point in time.

For your information, Poloniex charges the following fees for every order filled:

| **Maker** | **Taker** |
|-----------|-----------|
| 0.15% | 0.25% |

Poloniex fees are explained [here](https://poloniex.com/fees/).

The competition does take fees into consideration while calculating the ranking and competition results. For that reason, fees are factored in the available balance served by the platform.

### Ranking

The ranking is determined by a very simple performance metric: [Return on Investment (ROI)](https://www.investopedia.com/terms/r/returnoninvestment.asp).

#### Formula

**ROI** = (Gain from Investment - Cost of Investment) / Cost of Investment (expressed as a percentage)

#### Definitions

* **Cost of Investment** = Initial BTC Balance = 0.001 BTC. For the purpose of this competition, this is a constant, meaning that if you use less than 0.001 BTC to do your trading, we will still use 0.001 BTC as the value for this constant.

> NOTE: It doesn’t matter how much BTC you actually have in the exchange. The platform keeps track of your trades and available balances during the competition.

* **Gain from Investment** (or Losses, expressed as negative Gains) = Final BTC Balance

#### Winners

The result of the competition is determined by the position of each bot in the ranking by the end of the competition.

##### _Example_

**Bot A** ends up with 0.0015 BTC

Bot A ROI = (0.0015 - 0.001) / 0.001 * 100% = 50%

**Bot B** ends up with 0.0005 BTC

Bot B ROI = (0.00075 - 0.001) / 0.001 * 100% = -25%

**Bot C** ends up with 0.001 BTC

Bot B ROI = (0.001 - 0.001) / 0.001 * 100% = 0%

_Final Ranking_:

| **Position** | **Bot** | **ROI** |
|:----------|:---------:|----------:|
| 1st | A | 50 % |
| 2nd | C | 0 % |
| 3rd | B | -25 % |

### Prizes

The competition awards 0.5 BTC and up to 800,000 ALGO (worth USD 8,000 as of this date) as prize money for the top performers during each competition period, with the following caveats:

* BTC Prizes are awarded to bots with ROI >= 10% (10% profits and higher) only.

* ALGO prices are awarded always, even when ROI is negative (loss).

**The prize money is awarded as follows:**

| **Position** | **BTC Prize** | **ALGO Prize** |
|:----------|----------:|----------:|
| 1st | 0.30 | 300,000 |
| 2nd | 0.15 | 150,000 |
| 3rd | 0.05 |  50,000 |
| 4th to 15th |      |  25,000 |

> NOTE: In the [example above](#example), only Bot A would have been awarded the BTC Prize, as it is the only one with a ROI bigger than 10%.

## Term of Service

The information provided in this document is intended for informational purposes only and is subject to change without notice. Advanced Algos may make improvements and/or changes in the products, pricing and/or the programs described in this information at any time without notice.

## Disclaimer

THE AACLOUD, THE AA ARENA COMPETITION, THE AA MASTERS BOTS AND THEIR ASSOCIATED PRODUCTS AND SERVICES ARE PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY, SUITABILITY FOR A PARTICULAR PURPOSE, OR NON-INFRINGEMENT.

IN NO EVENT WILL ADVANCED ALGOS BE LIABLE TO ANY PARTY FOR ANY DIRECT, INDIRECT, SPECIAL OR OTHER CONSEQUENTIAL DAMAGES FOR ANY USE OF THE AACLOUD, THE AA ARENA COMPETITION, THE AA MASTERS BOTS, OR ANY OTHER ASSOCIATED SERVICE OR WEB SITE, INCLUDING, WITHOUT LIMITATION, ANY LOST PROFITS, BUSINESS INTERRUPTION, LOSS OF FUNDS, PROGRAMS OR OTHER DATA OR OTHERWISE, EVEN IF WE ARE EXPRESSLY ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

<hr>

# The AA Platform

## Overview

AA Bots are open source projects in Github, programed in JavaScript. The platform calls bots and puts them to run in specific time intervals. Bots consume services from the platform and data from other bots, specially from indicator bots, and at the same time, produce an output that is stored in the cloud (to be consumed by other bots).

There are three GitHub Organizations you need to be familiar with:

* [Advanced Algos](https://github.com/AdvancedAlgos): Features repositories with the AA Platform code including the bits that run in the cloud (AACloud) and in the web browser, along with a few other platform-related configurations and documentation.

* [AAMasters](https://github.com/AAMasters): Its a showcase GitHub organization similar to the one each Dev Team needs to create for themselves. It features several examples of bots, each in their corresponding repository.

* [AAArena](https://github.com/AAArena): Its another showcase GitHub organization featuring the AA Application hosting the trading bot competition you are about to enter.

## Setting Up a Dev Team Organization

The very first step is [setting up a GitHub organization](https://github.com/account/organizations/new) named after your own Dev Team. Make sure the name of the organization starts with “AA”, just like in the above example _AAMasters_. Also make sure that the phrase “_Advanced Algos_” is part of the organization’s description.

<hr>

# Setting up your Development Environment
To setup and develop your own bot, you'll need to pull in several code repositories as well as make a few directories to store configurations. This is a sample view of the final directory structure with important files/folder annotated. Instructions for creating all of this will follow and your directory and file names will differ.
```
.                               # Top level directory located at your choice
├── AACloud		        # Will be cloned from git repository
│   ├── ...                     # A variety of files and folders
│   ├── AACloud.sln             # Used only with VS IDE to launch project
│   └── this.config.json    	# Configure your bot to test and develop in cloud
├── API-Keys                    # Create this dir at same level as AACloud
│   └── AABot.Poloniex.json     # Your Poloniex API Key
├── Connection-Strings          # Create this dir at same level as AACloud
│   └── Production              
│       ├─ .connstring          # A variety of storage connection files to be supplied by Advanced Algos
│       └─ ...  
├── Logs                        # AACloud will output logs here
│            
├── AAPlatform                  # Will be cloned from git repository
│   └── ecosystem.json          # Adding your team and bots to the cloud
│
└── AAYourTeam                  # Directory named after your Dev/Bot Team
    └── AAYourBot-Trading-Bot   # You custom bot repository     
        ├─ Trading-Process
        │    └── User.Bot.js    # Customize your bot logic here
        ├─ AA~Trading-Bot.sln   # Used only with VS IDE to launch project
        └─ this.bot.config.json # Your bot configuration

```

## Step 1: Node.js

Before we start, make sure you have Node.js installed. If you don’t, please [download and install Node.js](https://nodejs.org/en/download/).

![Node.js](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Node-js-01.png)

## Step 2: Azure Storage Explorer

Bots consume and store data in the Microsoft Azure cloud. This tool will allow you to browse and manage data.

### Download, Install, Run

Download and install the [Azure Storage Explorer](https://azure.microsoft.com/en-us/features/storage-explorer/).

The following screen should pop up when you launch Azure Storage Explorer:

![Azure Storage Explorer](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Azure-Storage-Explorer-02.png)

Select _Use a connection string or a shared access signature URI_ and click **Next**.

Select _Use a connection string_ and paste the following connection string in the corresponding field to connect to the testnet storage:

```
DefaultEndpointsProtocol=https;AccountName=aatestnet;AccountKey=rQRuD8KeD0upqcN9532zqZTknKwkYJDpGzkATGptk9lIEovkLchdOGOJVld26cUjpzTA4enxsxpCB33B0pOZRg==;EndpointSuffix=core.windows.net
```

![Azure Storage Explorer](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Azure-Storage-Explorer-03.png)

Click **Next** and **Connect** in the following screen.

> **NOTE**: Please bear in mind that this connection string allows you to browse data in the testnet environment. When you produce your own bot it will store data in its own storage for which you will get your own connection string.

Storage Explorer will load on the following screen:

![Azure Storage Explorer](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Azure-Storage-Explorer-01.png)

## Step 3: Clone the Cloud Platform

Clone the [AACloud](https://github.com/AdvancedAlgos/AACloud) repository in your local machine.

#### Using Git CLI
```
$ git clone https://github.com/AdvancedAlgos/AACloud
```

#### or Using GitHub Desktop

If you are an advanced GitHub user you are probably using Git via the command-line. If you are not, we recommend [downloading and installing the GitHub Desktop](https://desktop.github.com/) application.

If you are not familiar with GitHub at all, we highly recommend you invest the time in learning it, as it is the most popular collaboration and version control system. For further information on how to use GitHub Desktop, please refer to the [Getting Started with GitHub Desktop guide](https://help.github.com/desktop/guides/getting-started-with-github-desktop/) or [watch this video tutorial](https://www.youtube.com/watch?v=GqNAD4XoZ6k).

Once you have launched GitHub Desktop and logged in with your GitHub credentials, this is what you need to do to clone the platform’s repository:

Go to _File > Clone Repository_

![GitHub Desktop](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/GitHub-Desktop-01.png)

Click on the URL tab and paste the repository URL in corresponding field:

```
https://github.com/AdvancedAlgos/AACloud
```

Choose where in your local machine GitHub should copy the files.

![GitHub Desktop](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/GitHub-Desktop-02.png)

Once you clone the repository, GitHub desktop keeps track of the changes that may occur in the files in your local machine and helps synchronize the changes with the online repository via commits and pushes.

<hr>

# Trading Bots

You are almost done with your set up. Let's briefely discuss Trading Bots before actually cloning one to use as a template.

## Overview

At this early stage, the AA Platform and the trading bot templates solve several of the main issues around algorithmic trading:

* Infrastructure to run bots in the cloud;
* Crucial historical and live trades data;
* Connection with exchanges, placement and handling of orders.

This leaves the Dev Team free to focus in the creative side of things: coming up with and implementing a trading strategy.

There are three AACloud modules particularly significant to trading bots:

* _Dependencies_: Your Trading Bot's config file contains a declaration of dependencies. Dependencies exist because trading bots use other bot's datasets, or require certain data to be on a certain state. The dependencies module loads declared dependencies and passes them on to the bot through the Assistant module.

* _Context_: In terms of context, trading bots require the latest status report, the history of what was done on previous runs and the execution context tracking balances, trades, positions and so on. Context is saved in files as outputs of trading bots. The context module reads the last status report, gets the date of the last execution, fetches the corresponding context file and serves it to the Assistant module.

* _Assistant_: The Assistant module processes information available from other modules and serves a digest version to the trading bot. It also serves the datasource with trades, candles, etc. The Assistant module also acts as an interface with the exchange, as it offers methods for placing, closing and moving orders.

In its current version, AACloud provides an object (_platform_) containing several other objects:

* _datasource_: preloads ready-to-consume data comprised of candlesticks and stair patterns;
* _assistant_: opens, closes and moves positions

The overall strategy when working with trading bots can be summarized in the following bullet points:

* Bots are executed every one minute.

* Each time the bot runs, it first needs to understand the context of the current execution. Bots get the context info from the Assitant module.

* Then the bot embarks in the calculations required by its trading strategy. At this point in time, there are very few indicators offering processed information. As a consequence, the bot needs to do all calculations internally. Almost all Technical Analysis indicators are calculated from trades and volume data. Their formulas are in the pubic domain and even code is readily available if you search around. You are free to use open source code within your bot's code.
* Once calculations are performed, the bot decides what to do, and uses the platform to place orders on the exchange.

## Exchanges API

The AA Platform places orders on exchanges through the use of the exchanges' APIs. You will need to create an API Key and configure your bot to use it.

### Creating the API Key

This is how you create an API Key in Poloniex:

Go to the tools menu and select _API KEYS_...

![Poloniex](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Poloniex-API-01.png)

If you have never used the API before, chances are it is disabled at the exchange. So before actually creating an API Key you will need to enable them...

![Poloniex](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Poloniex-API-02.png)

You will need to follow the validation process involving checking your email and confirming your choice. Once that is taken care of, go back to the tools menu and click _API KEY_ again. You should now see a screen offering to create a new key...

![Poloniex](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Poloniex-API-03.png)

Once you create your key, the system will present it as follows...

![Poloniex](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Poloniex-API-04.png)

**Make sure you DO NOT enable withdrawals nor IP access restrictions**.

### Creating an API Key File

Next, you will use the information in the API Key to a create a _.json_ file with the following structure using your own Key and Secret information:

```
{ "Key" : "6HS4YUEB-865UY9W4-KGHEHHJ-GH72ETG1", "Secret" : "1a3529851a05439asdasdw63426378ggd65701ac4a5d53c4859aa3511a8aa65acbd7e713bba755d0b1591ebe3a7618a71393ef4d3d11310628e1db"}
```

Create a folder named _API-Keys_ at the same level of the platform's repository (out of the folder AACloud) and save the file using the following naming convention:

"**AA**" + **BotName** + "**.**" + **ExchangeName** + "**.json**"

e.g.: AAMariam.Poloniex.json

> NOTE: Make sure the folder and file doesn't accidentally end up in GitHub! Your API KEYs should be kept secret!

<hr>

# Starting out Your Own Bot

## Step 1: Using an Existing Bot as a Starting Point

### A: Clone and Rename Bot

We will use Mariam, a Trading Bot within the AAMasters organization as a starting point for creating your own bot. Clone [Mariam's repository](https://github.com/AAMasters/AAMariam-Trading-Bot) and --once in your local machine-- copy and paste the repository’s root folder, renaming it with the name of your new bot.

```
$ git clone https://github.com/AAMasters/AAMariam-Trading-Bot _AAYourBotName-Trading-Bot_
$ cd _AAYourBotName-Trading-Bot_
```

Make sure you follow the naming convention using the following string:

“**AA**”+”**BotName**”+”**-Indicator-Bot**” _or_ “**-Trading-Bot**”

e.g.: _AAMariam-Trading-Bot_

> NOTE: Make sure the bot name is unique. That is, no other bot by any other Dev Team can have the same name. You can find the current list of bots in the _[AAPlatform ecosystem.json file](https://github.com/AdvancedAlgos/AAPlatform/blob/master/ecosystem.json)_.

> NOTE: Having fun is essential; naming your bot offers a good chance to do just that. Feel free to name your bot after a good friend or go crazy with whatever character makes you laugh.

### B: Rename Solution (Optional: VS IDE only)

Now rename the solution using the following syntax: “**AA**”+“**BotName**”+“**-TypeOfBot-**”+“**Bot**”+“**.sln**”

e.g.: _AAMariam-Trading-Bot.sln_

```
$ mv  AAMariam-Trading-Bot.sln _AAYourBotName-Trading-Bot.sln_
```

### C: Remove .git Folder

Next, delete the hidden _.git_ folder to eliminate the relation to the original GitHub repository.

```
$ rm -rf .git
```

### D: Add GitHub Repository

Now is a good time to go to GitHub and add a new local repository within your own organization. Name the repository after your bot (use the exact same name as the root folder). Make sure you include a concise description of what the bot does. Upload the files in your local repository to the GitHub repository so that GitHub takes control of the association between your local files and the ones at GitHub.

#### Using Git CLI:
After creating new empty repository in Github without creating README or other files
```
$ git init
# initialize local repository
$ git add .
# Track all local files
$ git commit -m "Clone bot"
# Make first commit
$ git remote add origin _YourRemoteRepositoryURL
# e.g. https://github.com/YourTeam/AAYourBot-Trading-Bot.git
$ git remote -v
# Verifies the new remote URL
$ git push -u origin master
# Pushes the changes in your local repository up to the remote repository you specified as the origin
```

### E: Request a Storage Account

Bots store data in the cloud. For the time being, the process for opening a storage account for your bot is manual. Please send us a request to open a storage account over WhatsApp; include your bot's name, please. When the request is processed, you will get the following:

#### Your Bot's Connection String

A text string similar to the following one:

```
DefaultEndpointsProtocol=https;AccountName=aayourbot;AccountKey=o1+ImM1zafasYOgf6Npmza+oGDjf7R2dRFEfXv7zF9krgIlgXtUCrNQE+UjAq3DR9u7JdFi684Wl/DWJlLvnwyWT9Q==;EndpointSuffix=core.windows.net
```

Create a folder named _Connection-Strings_ at the same level of the platform's repository (out of the folder AACloud). Inside it, create a subfolder named _Production_.

Open Notepad or any other basic text editor and create a file with the following content, making sure you place the supplied connection string in the appropriate place:

```
{
"useDevelopmentStorage": false,
"connectionString": "PLACE_YOUR_CONNECTION_STRING_HERE",
"accountName": "",
"accountKey": "",
"sas": ""
}
```

Save the file inside _Connection-Strings > Production_ naming it as follows:

"**AA**" + **BotName** + "**.azure.storage**" + **.connstring**"

e.g.: AAMariam.azure.storage.connstring

#### Other Bot's Connection Strings

The bot you cloned --Mariam-- uses datasets that other bots produce, thus, your bot will need connection strings for those other bots. You will get these connection strings in files that you will need to place inside _Connection-Strings > Production_ folders.

#### SAS Token

```
?sv=2017-07-29&ss=f&srt=sco&sp=rl&se=2018-12-31T04:47:12Z&st=2018-03-01T20:47:12Z&spr=https&sig=VFMzqZUyr%2aTEyu53dHV60Zib0hb1PTqzcqEKAl97aLvA%3D
```

You will use the SAS token in the next step.

### F: Configure Your Bot

Open _this.bot.config.json_, a file within your bot's repository. Let's modify the config file segment by segment:

```
{
  "displayName": "Mariam",
  "codeName": "AAMariam",
  "type": "Trading",
  "version": {
    "major": 1,
    "minor": 0,
    "patch": 0
  },
```

You need to update that segment of the config with the following things in mind:

 - *displayName* (your bot's name without the AA prefix)
 - *codeName* (name with the AA prefix; e.g. AAMariam)
 - *version* (start with major:0, minor:1, patch:0 -- increase minor until you release your bot; once you do, change to major:1, minor: 0)

```
  "devTeam": "AAMasters",
  "dataSetVersion": "dataSet.V1",
  "processes": [
    {
      "name": "Trading-Process",
      "description": "Simple trading strategy to be used as a template.",
```

 - *devTeam* (your organization's name including the AA prefix)
 - *dataSetVersion* (different versions of bots may use different versions of datasets)
 - *description* (briefly describe your bot's strategy)
 
```
      "startMode": {
        "allMonths": {
          "run": "false",
          "minYear": "",
          "maxYear": ""
        },
        "oneMonth": {
          "run": "false",
          "year": "",
          "month": ""
        },
        "noTime": {
          "run": "true"
        }
      },
      "normalWaitTime": 60000,
      "retryWaitTime": 10000,
      "sleepWaitTime": 3600000,
      "comaWaitTime": 86400000,
      "dependencies": [
        {
          "devTeam": "AAMasters",
          "bot": "AAMariam",
          "botVersion": {
            "major": 1,
            "minor": 0
          },
          "process": "Trading-Process",
          "dataSetVersion": "dataSet.V1"
        }
      ]
    }
  ],
```

No need to touch the previous segment.

```
  "products": [
    {
      "codeName": "Trading History",
      "displayName": "Mariam Trading History",
      "description": "General information about Mariam trading history.",
      "storageAccount": "aamariam",
      "sets": [
        {
          "codeName": "Oficial History",
          "type": "Single File",
          "validPeriods": [ "24-hs", "12-hs", "08-hs", "06-hs", "04-hs", "03-hs", "02-hs", "01-hs", "45-min", "40-min", "30-min", "20-min", "15-min", "10-min", "05-min", "04-min", "03-min", "02-min", "01-min" ],
          "filePath": "@DevTeam/@Bot.1.0/dataSet.V1/Output/Trading-Process/AACloud.1.0",
          "fileName": "Execution.History.json"
        }
      ],
      "exchangeList": [
        {
          "name": "Poloniex"
        }
      ],
      "plotter": {
        "devTeam": "AAMasters",
        "repo": "Plotters-Trading",
        "moduleName": "History"
      }
    }
  ],
  ```

   - *displayName* (replace "_Example_" with your bot's name)


  ```
    "storage": {
    "sas": "?sv=2017-07-29&ss=f&srt=sco&sp=rl&se=2018-12-31T01:49:13Z&st=2018-03-01T17:49:13Z&spr=https&sig=BGdV3DlytkD6vGr%2FxfXcinqF3xSLFxfIz18lfzFzI6g%3D",
    "fileUri": "https://aayourbot.file.core.windows.net"
  }
}
```

   - *sas* (replace the value with the SAS token we gave you in the [previous step](#sas-token)
   - *fileUri* (replace "_yourbot_" with the actual name of your bot)

Save the file when you are done.

## Step 2: Configure the AACloud

In the AACloud folder, open _this.config.json_, make the changes as explained below and save.

```
{
  "codeName": "AACloud",
  "version": {
    "major": 1,
    "minor": 1,
    "patch": 0
  },
  "executionList": [
    {
      "enabled": "false",
      "botPath": "../Bots/AAMasters/AAMariam-Trading-Bot",	# Enter the path to your bot's project folder
      "process": "Trading-Process"				# up to the last folder only.
    },
    {								# AACloud is prepared to run multiple bots
      "enabled": "false",					# each with it's own processes.
      "botPath": "../Bots/AAMasters/AAOlivia-Indicator-Bot",	# 
      "process": "Multi-Period-Market"				# When you clone AACloud
    },								# you may find different bots
    {								# showing up in the configuration file, 
      "enabled": "false",					# just like the ones here.
      "botPath": "../Bots/AAMasters/AACharly-Extraction-Bot",	#
      "process": "Poloniex-Hole-Fixing"				# You can choose to set "enabled"
    },								# to "false" or simply delete
    {								# the entries you are not using,
      "enabled": "true",					# in which case you will need to 
      "botPath": "../Bots/AAMasters/AABruce-Indicator-Bot",	# delete the comma
      "process": "One-Min-Daily-Candles-Volumes"		# after the first bot.
    }								#
  ],
  "stopGracefully": "true",		# 'false' for continuous run, 'true' for one run only.
  "exchangeSimulationMode": "false",	# 'false' to place real order at the exchange, 'true' to simulate orders.
  "storageConnStringFolder": "Mixed",	# 'Testnet', 'Mixed' or 'Production' indicate which folders to look in for connection strings.
  "maxLogLoops": 10			# The number of loops you wish to log.
}
```

### Path

Change the path to the proper one pointing to your bot in your local machine. Bear in mind the path is relative to where the _AACloud.sln_ is located. Do not include the actual _.sln_ file in the path; only the containing folder is expected.

### Stop Gracefully

When you run a trading bot in your local environment you can configure the AACloud to run it either continuously or only once. This is to avoid the consequences of stopping a trading bot forcefully, which may cause the bot to loose sync with the exchange (open positions may not be taken into account in subsequent runs).

This is where the _stopGracefully_ parameter comes into play. When the value is _false_ the platform will run the bot continuously. When the value is _true_ the platform runs the bot once and stops it afterwards.

If you ran the bot with _"stopGracefully": "false"_ and need to stop the bot, then simply go back to the config, change the parameter to _true_, save the file and wait. Upon the next run, the bot will be stopped.

### Connection String Folders

In addition, the file Run.js allows you to tell the AACloud whether you wish to run your bot againt testnet or production data (or both).

### Configure Which Process to Run

Now we need to tell the platform which process to run. Click on the AACloud node and make sure the value for the Script arguments field is "_Trading-Process_":

![VS](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Visual-Studio-02-TB.png)

## Step 3: Test Run

### Execute

Once running, the process should call the command prompt and start showing some activity:

![VS](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Command-Prompt-01.png)

## Step 4: What to Expect After Execution

Once you run the AACloud and the platform calls the bot and process you just configured, you will not “see” much more than the command prompt popping up, as described earlier. Do not expect any graphics, browser windows or candlestick charts to pop up. The visualization of bots activity over a candlestick chart happens at a different moment. We will get there later. In the meantime, what you can actually see is the dataset generated by the bot in the form of _.json_ files stored in the cloud, the logs stored locally and the orders that may have been placed in your account at the exchange.

### Check Output

As stated above, you should be able to browse the output of the bot using the Azure Storage Explorer with the connection string we provided for your bot earlier (_File Shares > data_).

### Logs

Upon execution, the platform creates a folder named _Logs_ right outside the platform's repository. Thus, you will find the Logs folder in the same directory as the AACloud folder. Each bot stores logs in its own sub-folders.

### Debugging

By now you should be able to run the bot in your local environment and use typical debugging tools and procedures should anything go wrong.

In case you were not able to successfully run the bot, the logs files are the first place to go.

#### A Quick Logs Overview
```
.
├── AACloud              
├── Logs             			# Note: same dir level as AACloud
	└── _Your_Team_ 		# Directory named after your team
	   └── Trading 			# Named after process (e.g. Trading, Indicator, etc)
		   └── _YourBot_ver_    # Named after your Bot
			   └── ...logs 	# See below for details			   
```
**Log name format:** _Date(Yr-Mo-Day-Hr-Min)--RandId--SourceFile.log_
\* _SourceFile_ is the name of the AACloud file to check for associated error or output.

**Selected Log Guide:\***
1.  _~.This.Bot.log:_ Errors and outputs specific to your bot in its repository. All other logs point to CloudPlatform files.
2.  _~.Exchange Api.log:_ Output from exchange API
3.  _~.Assistant.log:_ Trading actions between bot and exchange
4.  _~.Datasource.log:_ Data accessed from storage by your bots
5.  _~File Storage.\_Bot\_.log:_ Data access from storage by listed bot
6. _~.Trading Bot Main Loop.log:_ Best log to narrow down general cloud platform issues

\*_By closest relationship to your bot. Read source code for more detailed comments and to view other files associated with the cloud platform_


If you wish to debug the platform and your bot, open the _IntervalExecutor.js_ module and place a breakpoint in the following line:

```
fileProcessingInterval.start(loopControl);
# line 142
```

Now, run the IDE. When execution halts, press F11 to step into the module _User.Bot.js_ that will be loaded from the configured bot process folder. Once there you can set more breakpoints or debug the module step by step.

## Step 5: Start Coding

Once you have managed to run the bot successfully, you are good to go. We’ve found the following workflow is quite practical:

* The main business logic/solution to edit is in  (_Your-Bot-Repo > Trading-Process > User.Bot.js_). Other types of bots (e.g. indicator or extraction) have different process folder types.
* Your bot will not fully successfully run until there is a balance in your Poloniex account and your bot can make an actual trade. The bot status report will also not be written to your storage account until then. You can use the simulation mode described above (_exchangeSimulationMode_ in the AACloud config) for a temporary workaround until you fund your account.
* Code directly in the bot’s solution until the code is fully implemented.
* Close the bot’s module and go to the cloud platform solution to debug (as explained above). While debugging, the bot’s files will pop up in separate tabs, so that you can edit the code in the process.

<hr>

# Launching Your Bot

Now that your bot is ready and you are happy with its behavior, it is time to release it under the AGPL license, register your Dev Team and bots in the AA Platform and eventually run it in the cloud. Running in the cloud is not that different from running the bot locally.

### Release Under AGPL License

In order to release your bot to the pubic, you need to follow this quick process:

#### Step 1

Go the bot's repository in GitHub and click the _Create new file_ button:

![AGPL License](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Bot-License-01.png)

#### Step 2

Enter the word _LICENSE_ (in all CAPS!) in the text field and click the button _Choose a license template_:

![AGPL License](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Bot-License-02.png)

#### Step 3

Scroll the page and cick the _GNU Affero General Public License v3.0_ link:

![AGPL License](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Bot-License-03.png)

#### Step 4

Click the _Review and submit_ button and follow the rest of the usual steps to commit the changes:

![AGPL License](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Bot-License-04.png)

> NOTE: Make sure you don't modify the license text in any way.

#### Step 5

Go back to your repository root and make sure the AGPL icon has been added to the top right corner of the page, next to the _contributors_ counter:

![AGPL License](https://github.com/AdvancedAlgos/Documentation/blob/master/Media/Dev-Teams-Getting-Sarted-Guide/Bot-License-05.png)

### Configure Dev Team and Bots in the Web Platform

Fork and clone the [AAPlatform](https://github.com/AdvancedAlgos/AAPlatform) repository and open _ecosystem.json_. You will need to locate the following piece of code:

```
    {
      "codeName": "AASpartans",
      "displayName": "AA Spartans",
      "bots": [
        {
          "repo": "AADumbO-Trading-Bot",
          "configFile": "this.bot.config.json"
        }
      ],
      "plotters": []
    }
```

Copy the piece of code and replicate it immediately below the closing key, **adding a comma in between the two segments**:

```
    {
      "codeName": "AASpartans",
      "displayName": "AA Spartans",
      "bots": [
        {
          "repo": "AADumbO-Trading-Bot",
          "configFile": "this.bot.config.json"
        }
      ],
      "plotters": []
    }, # <-- ADD THIS COMMA AND CHANGE YOUR INFO BELOW
    {
      "codeName": "AASpartans",
      "displayName": "AA Spartans",
      "bots": [
        {
          "repo": "AADumbO-Trading-Bot",
          "configFile": "this.bot.config.json"
        }
      ],
      "plotters": []
    }
```

Modify the pasted code to incorporate the details of your own GitHub organization and your own bots:


```
    {
      "codeName": "AASpartans",
      "displayName": "AA Spartans",
      "bots": [
        {
          "repo": "AADumbO-Trading-Bot",
          "configFile": "this.bot.config.json"
        }
      ],
      "plotters": []
    },
    {
      "codeName": "AAYourOrganization",
      "displayName": "AA Your Organization",
      "bots": [
        {
          "repo": "AAYourBot-Trading-Bot",
          "configFile": "this.bot.config.json"
        }
      ],
      "plotters": []
    }
```

#### Git CLI commands for above:
```
$ git clone https://github.com/_Your_Fork_/AAPlatform
$ cd AAPlatform
# Make changes as explained above (e.g. vi ecosystem.json)
$ git add .
$ git commit -m 'Add MyTeam to AAPlatform'
$ git push origin master
# In your browser, go to https://github.com/_Your_Fork_/AAPlatform/compare. Make sure Base fork is AdvancedAlgos/AAPlatform and head fork is yours. You may have to click on 'compare across forks.'
Click 'Create Pull Request' button.
```
Once you are finished, commit the changes and submit a pull request. Someone in the AdvancedAlgos Organization will analyze your request and pull it into the main branch's code if everything looks right.

Once that is done, you will be able to see your bot's activity at http://aawebplatformalpha.azurewebsites.net/

### Competition Configuration

Once your bot is finished and tested, you need to register your bot in the competition's configuration file. Fork and open [_this.competition.config.json_](https://github.com/AAArena/First-Closed-Doors-Competition/blob/master/this.competition.config.json). Locate the following segment:

```
      {
        "devTeam": "AAMasters",
        "bot": "AAMariam",
        "release": "1.0.0"
      }

```

Copy the piece of code and replicate it immediately below the closing key, **adding a comma in between the two segments**:


```
      {
        "devTeam": "AAMasters",
        "bot": "AAMariam",
        "release": "1.0.0"
      },  # <-- ADD THIS COMMA AND CHANGE YOUR INFO BELOW
      {
        "devTeam": "AAYourOrganization",
        "bot": "AAYourBot",
        "release": "1.0.0"
      }
```

Modify the pasted code to incorporate the details of your own GitHub organization and your own bot. Create a pull request and wait for someone at our end to review it.
