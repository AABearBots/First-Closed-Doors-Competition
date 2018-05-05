**[<< Previous: Launching Your Algobot](./3-LaunchingYourAlgobot.md)**



# Launching Your Algobot

Now that your bot is ready and you are happy with its behavior, it is time to release it under the AGPL license, register your Algobot Team and bots in the AAPlatform and eventually run it in the cloud. Running in the cloud is not that different from running the bot locally.

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

### Configure Algobot Team and Bots in the Web Platform

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
    }, # <– ADD THIS COMMA AND CHANGE YOUR INFO BELOW
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
      },  # <– ADD THIS COMMA AND CHANGE YOUR INFO BELOW
      {
        "devTeam": "AAYourOrganization",
        "bot": "AAYourBot",
        "release": "1.0.0"
      }
```

Modify the pasted code to incorporate the details of your own GitHub organization and your own bot. Create a pull request and wait for someone at our end to review it.


<hr>
### Support

[Join the Advanced Algos Telegram Channel](https://t.me/advancedalgos)

### Feedback

We hope your participation is fun and educational and we'd love to make it better. Please submit any issues you experience during the competition in the [issues section](https://github.com/AAArena/First-Closed-Doors-Competition/issues) of this repository. Please also submit **any** suggestions or other feedback you might have to enhance future experiences via email to feedback at advancedalgos dot org. 



<hr>
[Terms of Service](../Terms.md)  &bull;  [Disclaimer](../Disclaimer.md)

<hr>
**Table of Contents:** [Basic Definitions](../README.md/#basic-definitions) | [About The Competition](../TheCompetition.md) | [The AAPlatform](../AAPlatform.md) | [Setting Up Your Development Environment](./0-Setup.md) | [Trading Algobots](./1-TradingAlgobots.md) | [Starting Out Your Own Algobot](./2-YourOwnAlgobot.md) | [Launching Your Algobot](./3-LaunchingYourAlgobot.md)
