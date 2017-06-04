# BitCypher™
A new approach to Bitcoin tumbling and secure wallets; you can locally host it on your pc or privately host it on your server(s).  
  
Documentation is provided for setup and issues will be promptly responded to; feel free to contribute updates (contact me)!  
  
# Windows Usage
First, you'll need to install PHP for Windows: http://windows.php.net/download/  
Then you can use the scripts with passed information as arguments via cmd:   http://php.net/manual/en/install.windows.legacy.index.php#install.windows.legacy.commandline  
For those that are inexperienced, we suggest you get secure web hosting and use the .index we provide.  
  
# Hosting Usage  
After uploading it to your server, simply run 'setup.php' and add your details, then delete 'setup.php' and have fun!  
You can use 'manage.php' to change settings, afterward, but it will require you to retain the encryption details from setup.

*Note: since the first library we will implement is Block.io, your PHP setup will require:  
GMP: http://php.net/manual/en/gmp.installation.php
cURL: http://php.net/manual/en/curl.installation.php
mCrypt: http://php.net/manual/en/mcrypt.installation.php

# How does it work?  
This is both a wallet solution and tumbler, built to function together; rather than trying to simply pass bitcoins through multiple addresses and then send them to a single location (making it easier to see where they came from) --- our tumbling works by taking timed steps and phases to split the coins into multiple addresses within the wallet. When you send coins from your account to another address, it uses them at random to send the specified amount and network fee. Setting a higher network fee for faster processing is also an option.

We will use the wallet API of well-known providers only (adding more on request) so that you can also download an automatically generated offline wallet or access your bitcoins through their websites in the form of withdrawals from your account - not just being stuck with this project if you chose to create your own or modify things in the future. It's your money, so freedom and full control is a must.

MD5, PGP, and other encryption methods are also available for account information so that in the event of a hacking attempt nothing would be gained from it and each account would be separately encrypted based on that user's chosen id and password for account login.
