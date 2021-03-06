# Telegram-Trade-Copier
Copy Telegram Signal to your Metatrader account MT4 - MT5 for automated trade copying 

Open your Metatrader platform

**Tools => Options => Expert Advisors => Allow Webrequests**

https://api.telegram.org 

# Telegram 
Make a telegram bot by talking to the @botfather within your telegram app. 

Put the access token within the MT5 robot that you get from the botfather. 

Create a N**ew Public Group Chat** and add the telegram bot as **ADMIN with Read Message Access**. 

If you need your chat channel ID or chat Group ID , watch this video 
https://www.youtube.com/watch?v=I-qI6jeLIsI

You may need to use this tool https://github.com/fx4btc/parsesig to send your signals to a **group chat** because two telegrams can not communicate. 

# About
Unlike most of the Telegram trade copier services available, this is a stand alone MetaTrader Robot that does all the copy trading functionality on your hosted trading platform.

# Signal Forwarding
Since you aren't the admin for the provider's telegram group or channel , you will have to forward the signals to your own **PUBLIC GROUP** that you control. This is required because you will need to add a telegram bot to that channel and make that bot an ADMIN therefore the bot has access to the messages. As new messages are forwarded to your channel , the telegram bot will send these messages to the **Telegram Trade Copier** for parsing. 

# Telegram Signal Format

Since the majority of telegram signal providers do not have the same format, you have to format the signal into a format that this **Telegram Trade Copier** can recognize. Please see the examples below for supported format. 

- **Symbol** | Can be upper or lowercase or a mix of both
- **Signal** | BUY, Buy, buy, SELL, Sell, sell
- **TakeProfit** | TP, tp, TAKEPROFIT, TakeProfit, takeprofit
- **StopLoss** | SL, sl, STOPLOSS, StopLoss, stoploss

EURUSD  
BUY 1.12345  
TP 1.23455  
SL 1.01234  

EURUSD  
Buy 1.12345  
tp 1.23455  
sl 1.01234  

EURUSD  
buy 1.12345  
takeprofit 1.23455  
stoploss 1.01234  

# Multiple TakeProfit Values
**Telegram Trade Copier** handles multiple takeprofit targets by entering several positions on the initial signal and giving each position its own takeprofit value. For example a signal with 3 takeprofit values will place 3 positions on your account and each position will have its own takeprofit value. A signal can have up to 4 TakeProfit values. 

EURUSD  
BUY 1.12345  
TP1 1.23455  
TP2 1.34567  
TP3 1.45678  
TP4 1.56789  
SL 1.01234  


# Parameters
- **BrokerageSuffix** | If your broker has a suffix after the symbol, such as EURUSD.lmax , enter ".lmax"
- **TelegramToken** | Your Telegram token , talk to the @BotFather on telegram to create a bot and token 
- **PollingSpeedInSeconds** | How frequently do you want to check the telegram channel or group for a new signal

# License $150

Contact Developer   information on the profile page https://github.com/fx4btc | 1 Week demo available

