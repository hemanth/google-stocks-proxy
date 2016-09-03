# google-finace-proxy.
> proxy for undocumented Google Finance API.

## DEMO

Currenlty this is [hosted on heroku](https://google-stocks.herokuapp.com/), feel free to use it! 

## Features

* [X] responses in JSON format
* [X] CORS support

## API:

HTTP GET on the end point `https://google-stocks.herokuapp.com/?code=GOOG` with `code` query param. 

`code` might be:

* Just the the stock key like: `GOOG`

* Or it be the stock market : stock code -> `NSE:JKTYRE`

```
fetch('https://google-stocks.herokuapp.com/?code=GOOG')
  .then(console.log)
  .then(console.error)

/*

Would log something like:

[
  {
    "id": "4458694",
    "t": "JKTYRE",
    "e": "NSE",
    "l": "147.40",
    "l_fix": "147.40",
    "l_cur": "&#8377;147.40",
    "s": "0",
    "ltt": "3:51PM GMT+5:30",
    "lt": "Sep 2, 3:51PM GMT+5:30",
    "lt_dts": "2016-09-02T15:51:00Z",
    "c": "+13.60",
    "c_fix": "13.60",
    "cp": "10.16",
    "cp_fix": "10.16",
    "ccol": "chg",
    "pcls_fix": "133.8"
  }
]

P.S: next version will mostly get meanifuly attributes! 
Currently it's just the spatting out what the API returns.

*/
```
