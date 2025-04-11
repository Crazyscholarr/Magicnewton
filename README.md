# MagicNewton Bot - Automated Dice Rolling and Minesweeper Playing

## Introduction
MagicNewton Bot is an automation tool written in Node.js to perform "Roll Dice" and play Minesweeper on the MagicNewton website (https://www.magicnewton.com). This script saves you time by automatically clicking buttons, checking roll status, and playing Minesweeper with simple logic. The bot supports multiple accounts using cookies and proxies, and provides detailed colored logs (green for wins, red for losses).

### Features
- Automatically clicks "Roll now", "Let's roll", and "Throw Dice" for daily rolls.
- Checks roll status to avoid wasting time if already rolled.
- Plays Minesweeper automatically on "EASY" difficulty with a maximum of 3 games per day.
- Supports multiple accounts with cookies and proxies.
- Detailed logs with real-time timestamps and proxy IPs.
- Automatically waits and reruns after cooldown periods.

## Usage Guide

### Requirements
- **Node.js**: Version 16.x or higher.
- **Browser**: Chrome or Firefox (for manual cookie extraction).
- **Configuration Files**: `data.txt` (for cookies) and `proxys.txt` (for proxies).

### Installation
1. **Clone or Download the Repository**:
   ```bash
   git clone <repository_url>
   cd magicnewton-bot
   ```
2. **Install Dependencies**: Run the following command to install required packages:
```bash

npm install puppeteer fs chalk figlet axios
```
3. **Prepare Configuration Files**:
Create a data.txt file and add each account's cookie (one per line).
Create a proxys.txt file and add proxies (if any), format: protocol://username:password@host:port (one per line).
### How to Manually Extract Cookies
1. **Open Browser (Chrome/Firefox)**:
Log in to https://www.magicnewton.com using Gmail or an EVM wallet.
2. **Open DevTools:**
Press `` F12`` to open Developer Tools.
Go to the ``Application`` tab (or ``Storage `` in Firefox).
3. **Find the Cookie:**
Under ``Cookies``, locate ``https://www.magicnewton.com.``
Find the cookie named ``__Secure-next-auth.session-token.``
4. **Copy the Value:**
Copy the value from the "Value" column.
Paste it into ``data.txt``, one cookie per line for each account.
### Running the Program
1. **Start the Bot:** After preparing ``data.txt`` and ``proxys.txt``, run:
```bash
node index.js
```
2. **Monitor Logs:**
    The bot will display detailed logs with account info, proxy IPs, roll scores, and Minesweeper results.
    If rolls or Minesweeper games are exhausted, the bot will fetch the cooldown time and rerun later.
    Example Configuration Files
    ``data.txt:``
```bash
eytoken1abcxyz123
eytoken2defxyz456
```
``    proxys.txt:``
```bash
http://user1:pass1@proxy1.example.com:8080
http://user2:pass2@proxy2.example.com:8080
```

#Notes
Proxies: If the number of proxies is less than the number of accounts, remaining accounts will run without proxies.
Expired Cookies: If a cookie is invalid, the bot will log an error and skip that account.
Cooldown Time: The bot calculates cooldown based on the website's countdown timer.
Debugging: Check logs to troubleshoot issues (e.g., cookie, proxy, or connection problems).
Contact
Telegram:[@Crzscholar](https://t.me/Crzscholar)
Support: [@Crzscholar](https://t.me/Crzscholar)# Magicnewton
