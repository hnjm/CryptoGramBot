# THIS PROJECT IS NO LONGER MAINTAINED - CryptoGramBot



A telegram bot that sends your balance updates from coinigy, send trade notifications from Poloniex and Bittrex and creates you a trade export for your own spreadsheet magicary.

### Donations Welcome
* **BTC**: 1LVtLb6Vo79nyPBp252GSJVDMPToGvjFN6
* **DASH**: XoQepSjoTEriBV7bLo1bdTVjbdy1AJW11B
* **ETH**: 0x20A660DB0Abb84f62c532E5881C90e0Ef0e29638
* **LTC**: LYGuFsyHSYFpmEiW4SKPedt6KsvL2ZqeEW

## Installation
* Pre-requisites:
[.Net Core SDK](https://www.microsoft.com/net/core#windowscmd) version 2.0.3 or higher. 

1. Get your Bot ID, you need to chat to the BotFather. See [here](https://core.telegram.org/bots#3-how-do-i-create-a-bot) and [here](https://core.telegram.org/bots#6-botfather) 
2. Open a new chat to your bot and talk to him. Say hi. He won't respond just yet. 

3. If you would like to add commands, do this now. See Bot Commands below. Note they will only show on a new chat with the bot or by clearing history and clicking "/start"
4. Open a chat to this [bot](https://t.me/MyTelegramID_bot). This should show you your chat id.
5. Download the lastest version of the zip from [here](https://github.com/mehtadone/CryptoGramBot/releases) and unzip to a folder. Download CryptoGramBot.zip and not the source files if you want to run without building. 
6. Fill in your config in appsettings.json. Bot ID is WITHOUT Bot and choose whether you want enable each service (true or false).  NOTE: Create a new API key at your exchange, do not use an existing API key.
7. Give CryptoGramBot the correct execute permissions via chmod if on linux
8. Start on command line with "dotnet CryptoGramBot.dll"

## Bot Commands
To add bot commands so they pop up when you type /, you need to let the BotFather know of the commands. You will need to make sure the commands correspond with what you have enabled on the appsettings.json file as clicking "/total_coinigy" when you do not have coinigy enabled will not do anything. 

1. Open a chat to the [BotFather](https://telegram.me/botfather) again
2. Type /mybots
3. Click the bot you created for CryptoGramBag
4. Click "Edit Bot"
5. Click "Edit Commands"
6. Paste a selection from the following below you want commands for: 

```
trade_export - an excel export of all trades
profit - profit information for pair

list_coinigy_accounts - list coinigy account names
total_coinigy - total balance from all acounts

upload_bittrex_trades - upload bittrex order export
trex_balance - bittrex account summary

polo_balance - poloniex account summary
polo_reset_trades - reset trades database from poloniex

```
7. Clear history on your telegram bot to pick up the commands

## Upgrade
* Stop your bot
* Copy everything over in the new zip EXCEPT logs, database and appsettings.json
* Check to see if there are any new properties in the new appsettings.json and add then to your existing one. 
* Start your bot

## Usage
* Type /help when the bot is running

## Tips

This app needs to be run all the time to have the bot running. I might look at creating a windows service for this for windows users. For linux, there are a couple of options. 

* I use screen. Type "screen -S telegram" to create a new screen. Run the bot like above and CTRL-A-D to dettach from the screen. "screen -r telegram" to reattach. [Screen cheatsheet](http://aperiodic.net/screen/quick_reference)
* Another option is tmux. "tmux start session" then start the bot. Ctrl+b+d to dettach. [tmux cheatsheet](http://www.dayid.org/comp/tm.html)

## Done
* Use a combination of bittrex, poloniex and/or Coinigy
* Coinigy 24 hour PnL with profit and loss in BTC and USD
* Bittrex Trade notifications with % profit if a sell 
* Poloniex Trade notifications with % profit if a sell
* Bittrex balance information
* Bittrex wallet information and % change since bought.
* Bittrex csv order export upload
* Excel trade history export
* Price drop notifications when a balance drops more than 30%. Used for bag management. Runs 4 times a day.
* Dust notifications
* Pair profit 
* Open order notifications
* Deposit and withdrawal notification
* Low BTC notifications
* Reset polo trades through a command

## Todo
* Show deposits and withdrawals to show accurate profit and loss. 
* Profit calculations are wrong on a sell if we don't have the data in the database. 

## Support
* Join the [telegram group](https://goo.gl/4nY9Ug)

## Screenshots

![Screenshot 1](https://github.com/mehtadone/CryptoGramBot/blob/master/CryptoGramBot/images/screenshot.png?raw=true)
![Screenshot 1](https://github.com/mehtadone/CryptoGramBot/blob/master/CryptoGramBot/images/screenshot-1.png?raw=true)
