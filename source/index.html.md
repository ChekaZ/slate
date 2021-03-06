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

Twitter: <a href='https://twitter.com/messages/compose?recipient_id=1111599216126820354&welcome_message_id=1125897988113600517'>Start</a><br/>
Slack: <a href='https://slack.com/oauth/authorize?client_id=226325165126.378800172996&scope=commands,bot,users.profile:write,users:write,reactions:write,reactions:read,users.profile:read,users:read,users:read.email,usergroups:write,usergroups:read,groups:read,emoji:read,chat:write:bot,channels:read,channels:history,links:read,links:write,mpim:read,channels:write,team:read'> Install </a><br/>
Telegram: <a href='https://t.me/coinkitbot'>Start</a><br/>
Discord: <a href='https://discordapp.com/api/oauth2/authorize?client_id=546463922287411230&permissions=522304&scope=bot'>Install</a><br/>

# Commands

Coinkit has a lot of functions which will be explained in this section.

<aside class="warning">
Please Backup your CoinKit Account! Do '/auditme' and link it to the CoinKit Web Wallet <a href='https://wallet.coinkit.de'>CoinKitWallet</a>>
</aside>

## Tiphelp

`Command: Tiphelp`

Tiphelp will always help you out as it lists all Commands CoinKit has.
<aside class="notice">
To prevent spamming this Command is only available in private chat with CoinKit.
</aside>

## Coins

`Command: Coins`

Will display all integrated and usable Coins.

> Coins Usage:

```shell

coins

Example:
 - coins
```
```ruby

/coins

Example:
 - /coins
```
```python

/coins

Example:
 - /coins
```
```javascript

/coins

Example:
 - /coins
```

## ChangeCoin

`Command: changecoin <coin>`

This Command changes the Coin you or your Channel is using. It has two usecases:
- Set a default Coin for a Channel (Slack, Telegram, Discord), this can only be done by an Admin or ChannelOwner (Telegram).
- Change to your desired Coin in PrivateChat with CoinKit. ( Telegram, Discord, Twitter )

The Integration will be changed to the Coin and all other Commands will be using this Set Coin.

> Changecoin Usage:

```shell

changecoin <coin>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```
```python

/changecoin <coin>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```
```ruby

/changecoin <coin>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```
```javascript

/changecoin <coin>

Example:
 - /changecoin tube
 - /changecoin tzc
 - /changecoin nxs
```

## Deposit

`Command: Deposit [number]`

To be able to tip people, you first have to load up your wallet with a desired amount of Coins. With this command your personal deposit address will be created, so the Coins you transfer there will be assigned to you. Now you can get started.

Parameter [number] is only for Lightning invoices.

> Deposit Usage:

```shell

deposit

Example:
 - deposit
```
```python

/deposit

Example:
 - /deposit
```
```ruby

/deposit

Example:
 - /deposit
```
```javascript

/deposit

Example:
 - /deposit
```


## Balance

`Command: Balance`

Balance will show your Confirmed and Unconfirmed Balance. After you have deposited Coins to your Deposit-Address, you need to wait for Confirmations, Confirmations depend on the Coin you are using and it may take up to a few minutes until they are confirmed. Unconfirmed Coins are shown in round brackets.
When your Coins are confirmed, you are ready to tip!



> Balance Usage:

```shell

balance

or

balances (shows all balances > 0)

Example:
 - balance
```
```python

/balance

Example:
 - /balance
```
```ruby

/balance

Example:
 - /balance
```
```javascript

/balance

Example:
 - /balance
```

## Tipping

Your Coins are confirmed? Now you are ready for Tipping!
This Section is all about Tipping, Single-Tips, Multi-Tips and Coingiveaways.

## Single-Tip

`Command: tip @<username> <amount> <message>`

This Tip is designed to Tip a single person. You can also add a nice message to the Tip what may be the reason for the Tip.

<aside class="warning"> Remember to add the Coin you want to Tip on Twitter!</aside>


> Tip Usage:

```shell

Post a Status with '@coinkit_ tip @user1 <amount> [#|$]<coin>'

Example:
 - @coinkit_ tip @elonmusk 10 tzc
 - @coinkit_ tip @elonmusk 10 #nxs
 - @coinkit_ tip @elonmusk 10 $tzc
 - @coinkit_ tip @elonmusk 10 #TUBE
```

```python

tip @Username <amount>

Example:
 - /tip @GrumpyCat 10
```

```ruby

/tip @Username <amount>

Example:
 - /tip @GrumpyCat 10
```

```javascript

/tip @Username <amount>

Example:
 - /tip @GrumpyCat 10
```

### Reply-Tip

`Command: tip <amount> <message>`

With this function you can directly tip the person in a reply without the need of an extra mention!
<aside class="warning"> 
 Be careful, you will tip everyone who is Quoted in your reply!</aside>

> Reply Usage:

```shell

Reply to a Post/Comment '@coinkit_ tip @user1 <amount> [#|$]<coin>'

Example:
 - @coinkit_ tip 10 tzc
 
```

```python

Reply Tip is not available on Slack.

```

```ruby

/tip <amount>

Example:
/tip 10
```

```javascript

/tip <amount>

Example:
Reply Tip is not available on Discord.
```

## Multi-Tips

This Feature is designed to spread the love even more! You can tip as many people as you like in your Channel, default is 10. We have implemented two ways of tipping the crowd, Channel-Tip and Rain.
On top of that CoinKit Multi-Tips are based on activity, who hasnt been active, is idle, AFK or offline will not get tipped. So, be active!

## Channel-Tip

`Command: tip @channel <amount> [user-amount]`

Tipping a whole Channel, doesnt that sound like fun? - Channel-Tip makes that possible, but we have set the default to 10 people, so if you forget to insert the additional parameter only 10 people will get tipped.
The amount choosen on this command will be tipped to all people, so every person will get the amount you have inserted, it wont get split between them!


> Channel-Tip Usage:

```shell

On Twitter we have no channels, to tip a bunch of people, just chain the usernames in your post.

Post a Status with '@coinkit_ tip @user1 [@user.. @userN] <amount> [#|$]<coin>'

Example:
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #nxs
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 $tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #TUBE
```

```python

/tip @channel <amount> [10|userAmount]>

Example:
 - /tip @channel 10 
 # Tips 10 people 10 Coins, so 100 Coins in Total

 - /tip @channel 10 20
 # Tips 20 people 10 Coins, so 200 Coins in Total

 - /tip @channel 10 5
 # Tips 5 people 10 Coins, so 50 Coins in Total
```

```ruby

/tip @channel <amount> [10|userAmount]>

Example:
 - /tip @channel 10 
 # Tips 10 people 10 Coins, so 100 Coins in Total

 - /tip @channel 10 20
 # Tips 20 people 10 Coins, so 200 Coins in Total

 - /tip @channel 10 5
 # Tips 5 people 10 Coins, so 50 Coins in Total
```

```javascript

/tip @channel <amount> [10|userAmount]>

Example:
 - /tip @channel 10 
 # Tips 10 people 10 Coins, so 100 Coins in Total

 - /tip @channel 10 20
 # Tips 20 people 10 Coins, so 200 Coins in Total

 - /tip @channel 10 5
 # Tips 5 people 10 Coins, so 50 Coins in Total
```

## Rain

`Command: rain <amount> [user-amount]`

Rain is a command which is spread accross all Social Channels, mostly used in Discord! - Rain does divide a given amount of Coins to a desired amount of People, so basicly "rain" on them. This Feature is also based on activity as well as having a default size of 10 people.

 <aside class="warning"> Remember to add the Coin you want to Tip on Twitter!</aside>

> Rain Usage:

```shell

On Twitter we have no channels, to tip a bunch of people, just chain the usernames in your post.

Post a Status with '@coinkit_ tip @user1 [@user.. @userN] <amount> [#|$]<coin>'

Example:
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #nxs
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 $tzc
 - @coinkit_ tip @elonmusk @jack @justinbieber @katyperry 10 #TUBE
```

```python

/rain <amount> [10|userAmount]

Example:
 - /rain 10 
 # Rains 10 Coins on 10 people, 10 Coins in total, each person gets 1 Coin.

 - /rain 10 20
 # Rains 10 Coins on 20 people, 10 Coins in total, each person gets 0.5 Coins.

 - /rain 10 5
 # Rains 10 Coins on 5 people, 5 Coins in total, each person gets 2 Coins.
```

```ruby

/rain <amount> [10|userAmount]

Example:
 - /rain 10 
 # Rains 10 Coins on 10 people, 10 Coins in total, each person gets 1 Coin.

 - /rain 10 20
 # Rains 10 Coins on 20 people, 10 Coins in total, each person gets 0.5 Coins.

 - /rain 10 5
 # Rains 10 Coins on 5 people, 5 Coins in total, each person gets 2 Coins.
```

```javascript

/rain <amount> [10|userAmount]

Example:
 - /rain 10 
 # Rains 10 Coins on 10 people, 10 Coins in total, each person gets 1 Coin.

 - /rain 10 20
 # Rains 10 Coins on 20 people, 10 Coins in total, each person gets 0.5 Coins.

 - /rain 10 5
 # Rains 10 Coins on 5 people, 5 Coins in total, each person gets 2 Coins.
```

## Coingiveaway

`Command: coingiveaway <amount> [user-amount]`

An interesting and unique feature to give away coins is CoinGiveAway! This feature is based on activity, to receive a tip, users have to interact with the giveaway and click a moneybag to be eligible for this type of giveaway.
This Giveaway is time and user limited! - The creator can choose how many people get the opportunity to receive coins. Has the time run out or the limit of people is reached, the giveaway is over and all participants will get rewarded.
Default User amount is 10 and the time-limit is set to 5 minutes.

<aside class="warning">
Right now there is no support for that kind of giveaway on Twitter & Telegram.
</aside>

> Rain Usage:

```shell

Right now there is no support for that kind of giveaway on Twitter.

```

```python

/coingiveaway <amount> [10|userAmount]

Example:
 - /coingiveaway 10 
 # Starts a Giveaway with 10 Coins for 10 people, 100 Coins in total, each person gets 10 Coins.

 - /rain 10 20
 # Starts a Giveaway with 10 Coins for 20 people, 200 Coins in total, each person gets 10 Coins.

 - /rain 10 5
 # Starts a Giveaway with 10 Coins for 5 people, 50 Coins in total, each person gets 10 Coins.
```

```ruby
Right now there is no support for that kind of giveaway on Telegram.
```

```javascript

/coingiveaway <amount> [10|userAmount]

Example:
 - /coingiveaway 10 
 # Starts a Giveaway with 10 Coins for 10 people, 100 Coins in total, each person gets 10 Coins.

 - /rain 10 20
 # Starts a Giveaway with 10 Coins for 20 people, 200 Coins in total, each person gets 10 Coins.

 - /rain 10 5
 # Starts a Giveaway with 10 Coins for 5 people, 50 Coins in total, each person gets 10 Coins.
```

## Withdraw

`Command: withdraw <address> <amount>`

All good things come to an end, if you want to withdraw your coins to your local wallet you will have to use our Withdraw function! This command initiates directly a transfer to the given address.

> Withdraw Usage:

```shell

withdraw <address> <amount>

Example:
 - withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```

```python

/withdraw <address> <amount>

Example:
 - /withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```

```ruby

/withdraw <address> <amount>

Example:
 - /withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```

```javascript

/withdraw <address> <amount>

Example:
 - /withdraw 1GanlkaIP9234ANakljra89xDAfajkl 10
 # Withdraws 10 Coins to 1GanlkaIP9234ANakljra89xDAfajkl
```

## Price

`Command: price <coin>`

This Command show the Price of the Coin in BTC,USD,EUR,GBP,KRW. The default coin will be taken if no additional parameter is passed, but it can be applied to all integrated Coins.

> Price Usage:

```shell

price <coin>

Example:
 - price nxs
 - price tzc
 - price tube
```
```python

/price <coin>

Example:
 - /price nxs
 - /price tzc
 - /price tube
```
```ruby

/price <coin>

Example:
 - /price nxs
 - /price tzc
 - /price tube
```
```javascript

/price <coin>

Example:
 - /price nxs
 - /price tzc
 - /price tube
```

## Convert

`Command: convert [amount] <fromCoin> [to|in] <toCoin|usd>`

Our Convert feature is designed to calculate the Value of Coins into another Coin or USD.

> Convert Usage:

```shell

convert [amount] <fromCoin> [to|in] <toCoin|usd>

Example:
 - convert 20 nxs to tzc
 - convert 800 tzc to usd
 - convert 10 tube to ark
```
```python

convert [amount] <fromCoin> [to|in] <toCoin|usd>

Example:
 - /convert 20 nxs to tzc
 - /convert 800 tzc to usd
 - /convert 10 tube to ark
```
```ruby

convert [amount] <fromCoin> [to|in] <toCoin|usd>

Example:
 - /convert 20 nxs to tzc
 - /convert 800 tzc to usd
 - /convert 10 tube to ark
```
```javascript

convert [amount] <fromCoin> [to|in] <toCoin|usd>

Example:
 - /convert 20 nxs to tzc
 - /convert 800 tzc to usd
 - /convert 10 tube to ark
```

## Audit

`Command: auditme`

Audit Time! - You will get all information we have about you. These information include Account ID, Addresses of the selected Coin, Confirmed and Unconfirmed Balance.

> Auditme Usage:

```shell

auditme

Example:
 - auditme
```
```python

/auditme

Example:
 - /auditme
```
```ruby

/auditme

Example:
 - /auditme
```
```javascript

/auditme

Example:
 - /auditme
```

#Giveaway

`Post a Status with '@coinkit_ give <amount> <userAmount> <coin> '`

This Giveaway feature is designed to assist on giveaways with the drawing of eligible users. The user can manually start the drawing at a point he chooses to.

*How does it work?*

Post a status on Twitter, starting with this line:

`@coinkit_ give <amount> <userAmount> <coin> `

Limits: <userAmount> Max = 10


If you did everything correctly, @coinkit_ will retweet and like your status as well as reply with this message: 

`Giveaway is set up for this Tweet! <userAmount> lucky Users will each receive <amount> <coin> once <user> resolves this Giveaway.!`


<aside class="warning">
Entering the giveaway via "retweet" is the default setting. ( Other options will be available at a later point )"
</aside>

*How to draw?*

DM @coinkit_ with `give draw <tweetID> `

You will also get a message which includes this information.

> Tweet Giveaway Usage:

```shell

Post a status on Twitter, starting with this line:

'@coinkit_ give <amount> <userAmount> <coin>'

Example:
 - @coinkit_ give 8 5 tzc
 # Sets up a giveaway for 5 people, each winner gets 8 Coins, total of 40 Coins.
 - @coinkit_ give 500 10 tzc
 # Sets up a giveaway for 10 people, each winner gets 500 Coins, total of 5000 Coins.
 - @coinkit_ give 25 4 tzc
 # Sets up a giveaway for 4 people, each winner gets 25 Coins, total of 100 Coins.
 - @coinkit_ give 50 2 tzc
 # Sets up a giveaway for 2 people, each winner gets 50 Coins, total of 100 Coins.
```

```python

This Feature is not supported on Slack.

```

```ruby

This Feature is not supported on Telegram.

```

```javascript

This Feature is not supported on Discord.

```

#Tweet Monetizing

`Post a Status with '@coinkit_ mon <amount> <userAmount> <coin> <keyword>'`

Monetize your tweets with that feature in a truely unique way. Every retweet will instantly receive the given amount of coins, its fully automated and ends after the amount has been paid out.

*How does it work?*

Post a status on Twitter, starting with this line:

`@coinkit_ mon <amount> <userAmount> <coin> <keyword>`

<aside class="warning">
Avoid multiple times @coinkit_ mentions in your Tweet, otherwise it wont work properly! If you want to talk about CoinKit, please use "#CoinKit".
</aside>

If you did everything correctly, @coinkit_ will retweet and like your status as well as reply with this message: 

`Monetizing is set up for this Tweet! The next <userAmount> Users will receive each <amount> <coin> for their retweet!`

If a Keyword is included:

`Monetizing is set up for this Tweet! The next <amountUsers> Users will receive each <amount> <coin> for their retweet. The keyword is <keyword>`


To be eligible to get Coins when a Keyword is choosen, the tweets needs to get retweeted with a comment, the comment needs to have the keyword included.

<aside class="warning">
Available Coins for Tweet Monetizing: TZC, DOGE, UFO, BNB, QTUM, FTC, DGB, NXS, ARK, BTC, NIM, LTC, XTZ, SMART, DVT, BCH
</aside>

> Tweet Monetization Usage:

```shell

Post a status on Twitter, starting with this line:

'@coinkit_ mon <amount> <userAmount> <coin>'

Example:
 - @coinkit_ mon 10 20 tzc
 # Monetizes a tweet for 20 people, each retweet gets 10 Coins, total of 200 Coins.
 - @coinkit_ mon 500 12 tzc
 # Monetizes a tweet for 12 people, each retweet gets 500 Coins, total of 6000 Coins.
 - @coinkit_ mon 25 10 tzc
 # Monetizes a tweet for 10 people, each retweet gets 25 Coins, total of 250 Coins.
 - @coinkit_ mon 50 50 tzc
 # Monetizes a tweet for 50 people, each retweet gets 50 Coins, total of 2500 Coins.
```

```python

This Feature is not supported on Slack.

```

```ruby

This Feature is not supported on Telegram.

```

```javascript

This Feature is not supported on Discord.

```

##Monetized Tweet Status

`DM @coinkit_ in private with this command:`

'mon status'

Lists all active monetized tweets (tweetId) of your account. You can lookup which tweets these are with https://twitter.com/<YOURUSERNAME>/status/<tweetId>.

##Close Monetized Tweet

To close a monetized tweet manually, you have to go into the DMs with @Coinkit_ and use this command:

`mon end <tweetId>`

This command will close the monetized tweet regardless of how many retweets would be left.

#Tweet Monetizing ( Comment )

`Post a Status with '@coinkit_ com/comment <amount> <userAmount> <coin> [<keyword>]'`

Spread your message with that new unique feature! Users who retweet and comment with the keyword within a sentence, instantly receive the given amount of coins, its fully automated and ends after the amount has been paid out.

If no keyword is choosen, a simple sentence/comment will do it.

*How does it work?*

Post a status on Twitter, starting with this line:

`@coinkit_ com/comment <amount> <userAmount> <coin> [<keyword>]`

If you did everything correctly, @coinkit_ will retweet and like your status as well as reply with this message: 

`Monetizing Comment is set up for this Tweet! The next <userAmount> Users will each receive <amount> <coin> from <user> for retweeting and commenting.`

If a Keyword is included:

`Monetizing Comment is set up for this Tweet! The next <userAmount> Users will each receive <amount> <coin> from Totenfluch for retweeting and commenting. The keyword is <keyword> - Use it in your comment!`

To be eligible to get Coins, you have to retweet AND comment with a sentence with includes the keyword.

<aside class="warning">
Available Coins for Tweet Monetizing (Comment) : TZC, DOGE, UFO, BNB, QTUM, FTC, DGB, NXS, ARK, BTC, NIM, LTC, XTZ, SMART, DVT, BCH, TRON, XBC, WAX
</aside>

> Tweet Monetization Usage:

```shell

Post a status on Twitter, starting with this line:

'@coinkit_ com <amount> <userAmount> <coin>'

Example:
 - @coinkit_ com 10 20 tzc
 # Monetizes a tweet for 20 people, each user gets 10 Coins, total of 200 Coins.
 - @coinkit_ com 500 12 nxs
 # Monetizes a tweet for 12 people, each user gets 500 Coins, total of 6000 Coins.
 - @coinkit_ com 25 10 btc
 # Monetizes a tweet for 10 people, each user gets 25 Coins, total of 250 Coins.
 - @coinkit_ com 50 50 ark
 # Monetizes a tweet for 50 people, each user gets 50 Coins, total of 2500 Coins.
```

```python

This Feature is not supported on Slack.

```

```ruby

This Feature is not supported on Telegram.

```

```javascript

This Feature is not supported on Discord.

```


#MinTips & TxFees

`All Tips are on-chain, so a txfee needs to be included into every tip, here is the list of MinTips & TxFees for each Coin`

<aside class="warning">
Please keep in mind that these "fees" are only withheld, if the txfee is lower at the current point, you will only get deducted the txfee which the network took.
</aside>

*TZC*<br>
Min Tip Amount: 0.5<br>
Monetized Min Amount: 1<br>
Gift Code Min Amount: 5<br>
Default Fee: 0.25<br>

*BNB*<br>
Min Tip Amount: 0.001<br>
Monetized Min Amount: 0.001<br>
Gift Code Min Amount: 0.005<br>
Default Fee: 0.000375<br>

*NXS*<br>
Min Tip Amount: 0.1<br>
Monetized Min Amount: 0.1<br>
Gift Code Min Amount: 0.5<br>
Default Fee: 0.01<br>

*UFO*<br>
Min Tip Amount: 0.2<br>
Monetized Min Amount: 1<br>
Gift Code Min Amount: 50<br>
Default Fee: 0.2<br>

*FTC*<br>
Min Tip Amount: 0.2<br>
Monetized Min Amount: 1<br>
Gift Code Min Amount: 5<br>
Default Fee: 0.2<br>

*DGB*<br>
Min Tip Amount: 0.1<br>
Monetized Min Amount: 0.5<br>
Gift Code Min Amount: 5<br>
Default Fee: 0.01<br>

*DOGE*<br>+
Min Tip Amount: 5<br>
Monetized Min Amount: 5<br>
Gift Code Min Amount: 5<br>
Default Fee: 2.04<br>

*QTUM*<br>
Min Tip Amount: 0.02<br>
Monetized Min Amount: 0.02<br>
Gift Code Min Amount: 0.05<br>
Default Fee: 0.01<br>

*TUBE*<br>
Min Tip Amount: 0.01<br>
Monetized Min Amount: -<br>
Gift Code Min Amount: 5<br>
Default Fee: 0.01<br>

*ARK*<br>
Min Tip Amount: 0.1<br>
Monetized Min Amount: 0.1<br>
Gift Code Min Amount: 0.5<br>
Default Fee: 0.008<br>

*NIM*<br>
Min Tip Amount: 1<br>
Monetized Min Amount: 1<br>
Gift Code Min Amount: 10<br>
Default Fee: 0.005<br>

*LTC*<br>
Min Tip Amount: 0.0005<br>
Monetized Min Amount: 0.0005<br>
Gift Code Min Amount: 0.01<br>
Default Fee: 0.0001<br>

*XTZ*<br>
Min Tip Amount: 0.01<br>
Monetized Min Amount: 0.01<br>
Gift Code Min Amount: 0.1<br>
Default Fee: 0.002<br>
Default Fee to non Burned: 0.257<br>

*SMART*<br>
Min Tip Amount: 0.5<br>
Monetized Min Amount: 1.0<br>
Gift Code Min Amount: 5.0<br>
Default Fee: 0.05<br>

*DVT*<br>
Min Tip Amount: 5<br>
Monetized Min Amount: 5.0<br>
Gift Code Min Amount: 25.0<br>
Default Fee: 1<br>

*TRON*<br>
Min Tip Amount: 0.01<br>
Monetized Min Amount: 0.01<br>
Gift Code Min Amount: 0.1<br>
Default Fee: 0.003<br>

*BCH*<br>
Min Tip Amount: 0.0001<br>
Monetized Min Amount: 0.0001<br>
Gift Code Min Amount: 0.001<br>
Default Fee: 0.00004<br>

*XBC*<br>
Min Tip Amount: 0.001<br>
Monetized Min Amount: 0.001<br>
Gift Code Min Amount: 0.01<br>
Default Fee: 0.0002<br>

*WAX*<br>
Min Tip Amount: 0.01<br>
Monetized Min Amount: 0.01<br>
Gift Code Min Amount: 0.05<br>
Default Fee: 0.000<br>

*BTC (Lightning) Tipping*<br>
Min Tip Amount: 5 sats<br>
Monetized Min Amount: 5 sats<br>
Gift Code Min Amount: 500 sats <br>
Default Fee: 0 sats<br>

*BTC Withdraw/Deposit*<br>
Min Withdraw: 50000 sats<br>
Max Withdraw: 50000000 sats<br>
Default Fee Withdraw: 8000 sats<br>

*BTC (Lightning) Withdraw/Deposit*<br>
Min Withdraw: 5 sats<br>
Max Withdraw: 50000 sats<br>
Default Fee Withdraw: 1 sats<br>

#MinTips & Fees (Token)

`All Tips are on-chain, so a txfee needs to be included into every tip, here is the list of MinTips & TxFees for each Coin`

<aside class="warning">
Please keep in mind that these "fees" are only withheld, if the txfee is lower at the current point, you will only get deducted the txfee which the network took.
</aside>

`TRON TOKENS`

*USDT-TRX*<br>
Min Tip Amount: 0.1<br>
Monetized Min Amount: Not Available<br>
Gift Code Min Amount: Not Available<br>
Default Fee: 5 TRX ( TRON Contract )<br>

*KLV*<br>
Min Tip Amount: 0.1<br>
Monetized Min Amount: Not Available<br>
Gift Code Min Amount: Not Available<br>
Default Fee: 5 TRX ( TRON Contract )<br>


#Gift Codes

Gift Codes are an easy way to get new people introduced to your Coin/Token!
CoinKit has built a mechanism to easily create Gift Codes which can be redeemed in any CoinKit supported Social Channels!

DM @coinkit_ with `giftcode create <redeemValue> <AmountOfRedeems> <coin> [Amount of Codes]`

<aside class="warning">
Creating Gift Codes are also on-chain Transactions, please keep in mind to always have enough funds to cover the on-chain fees!
</aside>

> Gift Codes Usage:

```shell

DM @coinkit_ on Twitter with the following line:

'giftcode create <redeemValue> <AmountOfRedeems> <coin> [Amount of Codes]'

Example:
 - giftcode create 10 20 tzc 2 
 # Creates 2 Gift Codes with the value of 10 TZC which can be redeemed 20 times each. ( Total value of 400 TZC )
 - giftcode create 500 5 tzc
 # Creates 1 Gift Code with the value of 500 TZC which can be redeemed 5 times. ( Total value of 2500 TZC )
 - giftcode create 25 10 tzc 7
 # Creates 7 Gift Codes with the value of 25 TZC which can be redeemed 10 times each. ( Total value of 1750 TZC )
```

```python

This Feature is not supported on Slack.

```

```ruby

This Feature is not supported on Telegram.

```

```javascript

This Feature is not supported on Discord.

```

##Redeem Gift Codes

You can easily redeem that Gift Codes in all our supported Social Channels: Twitter, Discord, Telegram, Slack

Command: `redeem <GiftCode>`

> Gift Codes Usage:

```shell

DM @coinkit_ on Twitter with the following line:

'redeem <GiftCode>'

```

```python

Message CoinKit in private:

'/redeem <GiftCode>'

```

```ruby

Message CoinKit in private:

'/redeem <GiftCode>'

```

```javascript

Message CoinKit in private:

'/redeem <GiftCode>'

```

##Gift Codes Status

Check the status of a Gift Code, see who made it, what the redeem value is and how many redeems are left.

Command: `giftcode status <GiftCode>`

##Gift Code QR

You can easily create a QR code out of the Gift Codes to spread your code more easily!

Command: `giftcode qr <GiftCode>`


#Support 

We are happy to receive Bug reports, feedback or suggestions, please use the following commands to send us your thoughts!

Official CoinKit Discord: <a href='https://discord.coinkit.de'> CoinKit Discord </a>

## CoinKitSupport

`Command: Coinkitsupport`

Ooops! Something went wrong? - Please use CoinKit Support if any Bug or error occours which should not happen! This function is only for bug reports, not for personal assisting on how to use the CoinKit ;)

> Coinkitsupport Usage:

```shell

coinkitsupport

Example:
 - coinkitsupport
```
```python

/coinkitsupport

Example:
 - /coinkitsupport
```
```ruby

/coinkitsupport

Example:
 - /coinkitsupport
```
```javascript

/coinkitsupport

Example:
 - /coinkitsupport
```

## CoinKitFeedback

`Command: Coinkitfeedback <text>`

Any suggestions or feedback? - We would love to hear it! Just use this function and we assure you that we will take a close look at it!

> Coinkitfeedback Usage:

```shell

coinkitfeedback <text>

Example:
 - coinkitfeedback This is constructive feedback!
```
```python

/coinkitfeedback <text>

Example:
 - /coinkitfeedback This is constructive feedback!
```
```ruby

/coinkitfeedback <text>

Example:
 - /coinkitfeedback This is constructive feedback!
```
```javascript

/coinkitfeedback <text>

Example:
 - /coinkitfeedback This is constructive feedback!
```

# Terms of Service

Since we operate on a number of platforms, the respective Terms of Services of the platform naturally apply. 
Nevertheless, we would like to point out that we do not tolerate homophobic, sexist, violence glorifying, discriminating or abusive behaviour in any way.
The first step you should take when you encounter a message that you believe is contrary to these guidelines is to report it according to the policies of the platform you are using.
You can also use the following form to inform us about possible abuse of our bot: <a href='https://forms.gle/2nG6Bvgc9yS4mPFB7'>Report Form</a>
We reserve the right to limit or deny access to our services to users who we believe are in violation of the Terms of Service.

Extended ToS: <a href='https://coinkit.de/terms-of-service.pdf'> Terms-of-Service </a>

