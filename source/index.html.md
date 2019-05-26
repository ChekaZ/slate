---
title: Coinkit Wiki

language_tabs: # must be one of https://git.io/vQNgJ
  - shell: Twitter
  - ruby: Telegram
  - python: Slack
  - javascript: Discord

toc_footers:
  - <a href='#'>The Future of Tipping</a>
  - <a href='https://coinkit.de'>CoinKit</a>

search: true
---

# Getting Started

Welcome to the CoinKit Documentation! We are happy that you are using CoinKit, this Documentation should include all information to tip your favorite CryptoCurrency!

## Installation

CoinKit needs to be in your Channel to assist you with Tipping! So if CoinKit isnt present yet, please install/add it with the links below. Twitter is enabled by default, to get started there, just click the link.

Twitter: <a href='https://twitter.com/messages/compose?recipient_id=1111599216126820354&welcome_message_id=1125897988113600517'>Start</a>
Slack: <a href='https://slack.com/oauth/authorize?client_id=226325165126.378800172996&scope=commands,bot,users.profile:write,users:write,reactions:write,reactions:read,users.profile:read,users:read,users:read.email,usergroups:write,usergroups:read,groups:read,emoji:read,chat:write:bot,channels:read,channels:history,links:read,links:write,mpim:read,channels:write,team:read'> Install </a>
Telegram: <a href='https://t.me/coinkitbot'>Start</a>
Discord: <a href='https://discordapp.com/api/oauth2/authorize?client_id=546463922287411230&permissions=522304&scope=bot'>Install</a>

# Commands

Coinkit has a lot of functions which will be explained in this section.

## Tiphelp

Command: Tiphelp

Tiphelp will always help you out as it lists all Commands CoinKit has.
<aside class="notice">
To prevent spamming this Command is only available in private chat with CoinKit.
</aside>

## Coins

Command: Coins

Will display all integrated and usable Coins.

> Deposit Usage:

```Twitter

<code>coins</code>

Example:
 - coins
```
```Slack

<code>/coins</code>

Example:
 - /coins
```
```Telegram

<code>/coins</code>

Example:
 - /coins
```
```Discord

<code>/coins</code>

Example:
 - /coins
```

## ChangeCoin

Command: changecoin <coin>

This Command changes the Coin you or your Channel is using. It has two usecases:
- Set a default Coin for a Channel (Slack, Telegram, Discord), this can only be done by an Admin or ChannelOwner (Telegram).
- Change to your desired Coin in PrivateChat with CoinKit. ( Telegram, Discord, Twitter )

The Integration will be changed to the Coin and all other Commands will be using this Set Coin.

> Changecoin Usage:

```Twitter

<code>changecoin <coin></code>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```
```Slack

<code>/changecoin <coin></code>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```
```Telegram

<code>/changecoin <coin></code>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```
```Discord

<code>/changecoin <coin></code>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```

## Deposit

Command: Deposit

To be able to tip people, you first have to load up your wallet with a desired amount of Coins. With this command your personal deposit address will be created, so the Coins you transfer there will be assigned to you. Now you can get started.

> Deposit Usage:

```Twitter

<code>deposit <coin></code>

Example:
 - deposit
```
```Slack

<code>/deposit <coin></code>

Example:
 - /deposit
```
```Telegram

<code>/deposit<coin></code>

Example:
 - /deposit
```
```Discord

<code>/deposit <coin></code>

Example:
 - /deposit
```


## Balance

Command: Balance

Balance will show your Confirmed and Unconfirmed Balance. After you have deposited Coins to your Deposit-Address, you need to wait for Confirmations, Confirmations depend on the Coin you are using and it may take up to a few minutes until they are confirmed. Unconfirmed Coins are shown in round brackets.
When your Coins are confirmed, you are ready to tip!

> Balance Usage:

```Twitter

<code>balance <coin></code>

Example:
 - balance
```
```Slack

<code>/balance <coin></code>

Example:
 - /balance
```
```Telegram

<code>/balance<coin></code>

Example:
 - /balance
```
```Discord

<code>/balance <coin></code>

Example:
 - /balance
```

## Tipping

Your Coins are confirmed? Now you are ready for Tipping!
This Section is all about Tipping, Single-Tips, Multi-Tips and Coingiveaways.

### Single-Tip

Command: tip @<username> <amount> <message>

This Tip is designed to Tip a single person. You can also add a nice message to the Tip what may be the reason for the Tip.


> Tip Usage:

```Twitter

<code>Post a Status with '@coinkit_ tip @user1 <amount> [#|$]<coin>'</code>

Example:
 - @coinkit_ tip @elonmusk 10 tzc
 - @coinkit_ tip @elonmusk 10 #nxs
 - @coinkit_ tip @elonmusk 10 $tzc
 - @coinkit_ tip @elonmusk 10 #TUBE
 <aside class="warning"> Remember to add the Coin you want to Tip on Twitter!</aside>
```

```Slack

<code>/tip @Username <amount>></code>

Example:
 - /tip @GrumpyCat 10
```

```Telegram

<code>/tip @Username <amount>></code>

Example:
 - /tip @GrumpyCat 10
```

```Discord

<code>/tip @Username <amount>></code>

Example:
 - /tip @GrumpyCat 10
```

### Reply-Tip

Command: tip <amount> <message>

With this function you can directly tip the person in a reply without the need of an extra mention!

> Reply Usage:

```Twitter

<code>Reply to a Post/Comment '@coinkit_ tip @user1 <amount> [#|$]<coin>'</code>

Example:
 - @coinkit_ tip 10 tzc
 <aside class="warning"> 
 Be careful, you will tip everyone who is Quoted in your reply!</aside>
```

```Slack

<code>/tip <amount>></code>

Example:
 - /tip 10
```

```Telegram

<code>/tip <amount>></code>

Example:
 - /tip 10
```

```Discord

<code>/tip <amount>></code>

Example:
 - /tip 10
```

### Multi-Tips

This Feature is designed to spread the love even more! You can tip as many people as you like in your Channel, default is 10. We have implemented two ways of tipping the crowd, Channel-Tip and Rain.
On top of that CoinKit Multi-Tips are based on activity, who hasnt been active, is idle, AFK or offline will not get tipped. So, be active!

### Channel-Tip

Command: tip @channel <amount> [user-amount]

Tipping a whole Channel, doesnt that sound like fun? - Channel-Tip makes that possible, but we have set the default to 10 people, so if you forget to insert the additional parameter only 10 people will get tipped.
The amount choosen on this command will be tipped to all people, so every person will get the amount you have inserted, it wont get split between them!


> Channel-Tip Usage:

```Twitter

On Twitter we have no channels, to tip a bunch of people, just chain the usernames in your post.

<code>Post a Status with '@coinkit_ tip @user1 [@user.. @userN] <amount> [#|$]<coin>'</code>

Example:
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #nxs
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 $tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #TUBE
 <aside class="warning"> Remember to add the Coin you want to Tip on Twitter!</aside>
```

```Slack

<code>/tip @channel <amount> [10|userAmount]></code>

Example:
 - /tip @channel 10 
 # Tips 10 people 10 Coins, so 100 Coins in Total

 - /tip @channel 10 20
 # Tips 20 people 10 Coins, so 200 Coins in Total

 - /tip @channel 10 5
 # Tips 5 people 10 Coins, so 50 Coins in Total
```

```Telegram

<code>/tip @channel <amount> [10|userAmount]></code>

Example:
 - /tip @channel 10 
 # Tips 10 people 10 Coins, so 100 Coins in Total

 - /tip @channel 10 20
 # Tips 20 people 10 Coins, so 200 Coins in Total

 - /tip @channel 10 5
 # Tips 5 people 10 Coins, so 50 Coins in Total
```

```Discord

<code>/tip @channel <amount> [10|userAmount]></code>

Example:
 - /tip @channel 10 
 # Tips 10 people 10 Coins, so 100 Coins in Total

 - /tip @channel 10 20
 # Tips 20 people 10 Coins, so 200 Coins in Total

 - /tip @channel 10 5
 # Tips 5 people 10 Coins, so 50 Coins in Total

### Rain

Command: rain <amount> [user-amount]

Rain is a command which is spread accross all Social Channels, mostly used in Discord! - Rain does divide a given amount of Coins to a desired amount of People, so basicly "rain" on them. This Feature is also based on activity as well as having a default size of 10 people.

> Rain Usage:

```Twitter

On Twitter we have no channels, to tip a bunch of people, just chain the usernames in your post.

<code>Post a Status with '@coinkit_ tip @user1 [@user.. @userN] <amount> [#|$]<coin>'</code>

Example:
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #nxs
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 $tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #TUBE
 <aside class="warning"> Remember to add the Coin you want to Tip on Twitter!</aside>
```

```Slack

<code>/rain <amount> [10|userAmount]></code>

Example:
 - /rain 10 
 # Rains 10 Coins on 10 people, 10 Coins in total, each person gets 1 Coin.

 - /rain 10 20
 # Rains 10 Coins on 20 people, 10 Coins in total, each person gets 0.5 Coins.

 - /rain 10 5
 # Rains 10 Coins on 5 people, 5 Coins in total, each person gets 2 Coins.
```

```Telegram

<code>/rain <amount> [10|userAmount]></code>

Example:
 - /rain 10 
 # Rains 10 Coins on 10 people, 10 Coins in total, each person gets 1 Coin.

 - /rain 10 20
 # Rains 10 Coins on 20 people, 10 Coins in total, each person gets 0.5 Coins.

 - /rain 10 5
 # Rains 10 Coins on 5 people, 5 Coins in total, each person gets 2 Coins.
```

```Discord

<code>/rain <amount> [10|userAmount]></code>

Example:
 - /rain 10 
 # Rains 10 Coins on 10 people, 10 Coins in total, each person gets 1 Coin.

 - /rain 10 20
 # Rains 10 Coins on 20 people, 10 Coins in total, each person gets 0.5 Coins.

 - /rain 10 5
 # Rains 10 Coins on 5 people, 5 Coins in total, each person gets 2 Coins.

### Coingiveaway

Command: coingiveaway <amount> [user-amount]

An interesting and unique feature to give away coins is CoinGiveAway! This feature is based on activity, to receive a tip, users have to interact with the giveaway and click a moneybag to be eligible for this type of giveaway.
This Giveaway is time and user limited! - The creator can choose how many people get the opportunity to receive coins. Has the time run out or the limit of people is reached, the giveaway is over and all participants will get rewarded.
Default User amount is 10 and the time-limit is set to 5 minutes.

> Rain Usage:

```Twitter

<aside class="warning">
Right now there is no support for that kind of giveaway on Twitter.
</aside>
```

```Slack

<code>/coingiveaway <amount> [10|userAmount]></code>

Example:
 - /coingiveaway 10 
 # Starts a Giveaway with 10 Coins for 10 people, 100 Coins in total, each person gets 10 Coins.

 - /rain 10 20
 # Starts a Giveaway with 10 Coins for 20 people, 200 Coins in total, each person gets 10 Coins.

 - /rain 10 5
 # Starts a Giveaway with 10 Coins for 5 people, 50 Coins in total, each person gets 10 Coins.
```

```Telegram

<aside class="warning">
Right now there is no support for that kind of giveaway on Telegram.
</aside>
```

```Discord

<code>/coingiveaway <amount> [10|userAmount]></code>

Example:
 - /coingiveaway 10 
 # Starts a Giveaway with 10 Coins for 10 people, 100 Coins in total, each person gets 10 Coins.

 - /rain 10 20
 # Starts a Giveaway with 10 Coins for 20 people, 200 Coins in total, each person gets 10 Coins.

 - /rain 10 5
 # Starts a Giveaway with 10 Coins for 5 people, 50 Coins in total, each person gets 10 Coins.

## Withdraw

Command: withdraw <address> <amount>

All good things come to an end, if you want to withdraw your coins to your local wallet you will have to use our Withdraw function! This command initiates directly a transfer to the given address.

> Withdraw Usage:

```Twitter

<code>withdraw <address> <amount></code>

Example:
 - withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```
```Slack

<code>/withdraw <address> <amount></code>

Example:
 - /withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```
```Telegram

<code>/withdraw <address> <amount></code>

Example:
 - /withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```
```Discord

<code>/withdraw <address> <amount></code>

Example:
 - /withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```

## Price

Command: price <coin>

This Command show the Price of the Coin in BTC,USD,EUR,GBP,KRW. The default coin will be taken if no additional parameter is passed, but it can be applied to all integrated Coins.

> Price Usage:

```Twitter

<code>price <coin></code>

Example:
 - price nxs
 - price tzc
 - price tube
```
```Slack

<code>/price <coin></code>

Example:
 - /price nxs
 - /price tzc
 - /price tube
```
```Telegram

<code>/price <coin></code>

Example:
 - /price nxs
 - /price tzc
 - /price tube
```
```Discord

<code>/price <coin></code>

Example:
 - /price nxs
 - /price tzc
 - /price tube
```

## Convert

Command: convert [amount] <fromCoin> [to|in] <toCoin|usd>

Our Convert feature is designed to calculate the Value of Coins into another Coin or USD.

> Convert Usage:

```Twitter

<code>convert [amount] <fromCoin> [to|in] <toCoin|usd></code>

Example:
 - convert 20 nxs to tzc
 - convert 800 tzc to usd
 - convert 10 tube to pivx
```
```Slack

<code>convert [amount] <fromCoin> [to|in] <toCoin|usd></code>

Example:
 - /convert 20 nxs to tzc
 - /convert 800 tzc to usd
 - /convert 10 tube to pivx
```
```Telegram

<code>convert [amount] <fromCoin> [to|in] <toCoin|usd></code>

Example:
 - /convert 20 nxs to tzc
 - /convert 800 tzc to usd
 - /convert 10 tube to pivx
```
```Discord

<code>convert [amount] <fromCoin> [to|in] <toCoin|usd></code>

Example:
 - /convert 20 nxs to tzc
 - /convert 800 tzc to usd
 - /convert 10 tube to pivx
```

## Audit

Command: auditme

Audit Time! - You will get all information we have about you. These information include Account ID, Addresses of the selected Coin, Confirmed and Unconfirmed Balance.

> Auditme Usage:

```Twitter

<code>auditme </code>

Example:
 - auditme
```
```Slack

<code>/auditme </code>

Example:
 - /auditme
```
```Telegram

<code>/auditme </code>

Example:
 - /auditme
```
```Discord

<code>/auditme </code>

Example:
 - /auditme
```

#Support 

We are happy to receive Bug reports, feedback or suggestions, please use the following commands to send us your thoughts!

## CoinKitSupport

Command: Coinkitsupport

Ooops! Something went wrong? - Please use CoinKit Support if any Bug or error occours which should not happen! This function is only for bug reports, not for personal assisting on how to use the CoinKit ;)

> Coinkitsupport Usage:

```Twitter

<code>coinkitsupport </code>

Example:
 - coinkitsupport
```
```Slack

<code>/coinkitsupport </code>

Example:
 - /coinkitsupport
```
```Telegram

<code>/coinkitsupport </code>

Example:
 - /coinkitsupport
```
```Discord

<code>/coinkitsupport </code>

Example:
 - /coinkitsupport
```

## CoinKitFeedback

Command: Coinkitfeedback <text>

Any suggestions or feedback? - We would love to hear it! Just use this function and we assure you that we will take a close look at it!

> Coinkitfeedback Usage:

```Twitter

<code>coinkitfeedback <text> </code>

Example:
 - coinkitfeedback This is constructive feedback!
```
```Slack

<code>/coinkitfeedback <text> </code>

Example:
 - /coinkitfeedback This is constructive feedback!
```
```Telegram

<code>/coinkitfeedback <text> </code>

Example:
 - /coinkitfeedback This is constructive feedback!
```
```Discord

<code>/coinkitfeedback <text> </code>

Example:
 - /coinkitfeedback This is constructive feedback!
```

