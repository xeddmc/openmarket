
==================


[OpenMarket]() &mdash; A free, decentralized marketplace.
==========
![asdf](http://img.shields.io/version/0.0.2.png?color=green)

**Currently alpha testing**

[OpenMarket]() is an open-source, decentralized marketplace, like amazon or etsy, where you can sell anything in exchange for bitcoin. The network and website is hosted by any seller running software installed from this page, and accessible by any of the running network nodes that keep a complete copy of the database.

It comes with a local-only, integrated [BitcoinJ](https://github.com/bitcoinj/bitcoinj)-based [Bitcoin wallet](http://github.com/tchoulihan/bitmerchant) so you can immediately start accepting payments without having to go through an intermediary service like coinbase or bitpay. 

To see what its all about, check out [a sample OpenMarket website]()


## Features include
* A complete web store including product reviews, ratings, wishlists, shipping tracking urls, feedback, categories, etc.
* A decentrally hosted database, built atop [rqlite](https://github.com/otoolep/rqlite). 
* A fully portable webservice and website built with java [Spark](https://github.com/perwendel/spark). *No web server required*
* An offline bitcoin [wallet](http://github.com/tchoulihan/bitmerchant) that uses [BIP70](https://github.com/bitcoin/bips/blob/master/bip-0070.mediawiki). 
* A [network page]() showing the connected nodes.


## Screenshots:
<img src="http://i.imgur.com/dwqxaaL.png">
<img src="http://i.imgur.com/5BX8h5R.png">
<img src="http://i.imgur.com/xd40ucL.png">
<img src="http://i.imgur.com/ckDwi77.png">
<img src="http://i.imgur.com/0c584RB.png">


## Installation
### Requirements
- Java 8
- Go (version at least 1.4) 
  - [GVM](https://github.com/moovweb/gvm) is the best way to install.
- If behind a router, make sure ports 4566-4570 are correctly forwarded to your local ip address.

Download the jar, located [here]()

To help test, use this command to join an existing test node that uses the bitcoin testnet:
<pre>java -jar openmarket.jar -testnet -join 96.28.13.51:4570</pre>

<pre>java -jar openmarket.jar [parameters]</pre>
<pre>parameters:
 -deleteDB     : Delete the sqlite DB before running.(Warning, this deletes
                 your wallets too)
 -join VAL     : Startup OpenMarket joining a master nodeIE, 127.0.0.1:4001
 -loglevel VAL : Sets the log level [INFO, DEBUG, etc.]
 -port N       : Startup your webserver on a different port(default is 4567)
 -testnet      : Run using the Bitcoin testnet3, and a test DB
 -uninstall    : Uninstall OpenMarket.(Warning, this deletes your wallets too)

</pre>

Then access this URL from your browser, and go through the signup process
http://localhost:4567/

## Building from scratch

To build OpenMarket, run the following commands:
```
git clone https://github.com/tchoulihan/openmarket
cd openmarket
chmod +x deploy.sh
./deploy.sh -testnet -join 96.28.13.51:4570
```

and access



## Support 
If you'd like to contribute to the project, you can either post bounties for desired features [here](https://www.bountysource.com/trackers/9805417-tchoulihan-bitmerchant), or click [this link](http://tchoulihan.github.io/bitmerchant/support.html).

## Bugs and feature requests
Have a bug or a feature request? If your issue isn't [already listed](https://github.com/tchoulihan/openmarket/issues/), then [open a new issue here](https://github.com/tchoulihan/openmarket/issues/new).

## Thanks
* Special thanks to Mike Hearn and Andreas Schildbach for their assistance with BIP70 and refunding orders.

## Feature requests / todos
* 
