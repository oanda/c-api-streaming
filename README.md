c-api-streaming
================

A sample C application that connects to OANDA's HTTP based events stream.

### Compiling and Running

Make sure you have the correct dev package for the curl library.
> apt-get install libcurl4-gnutls-dev

Open streaming.c and change the domain, access-token and accountIds.

Compile the file through terminal using the GCC compiler by typing:
> make

Run the output file using the following command.
> ./streaming

Outputs to standard output.

    {"heartbeat":{"time":"2014-08-21T13:43:14.000000Z"}}
    {"transaction":{"id":654877414,"accountId":8703506,"time":"2014-08-21T13:43:24.000000Z","type":"STOP_LOSS_FILLED","tradeId":654877021,"instrument":"EUR_USD","units":1,"side":"sell","price":1.32678,"pl":-0.0002,"interest":0,"accountBalance":99677.3601}}
    {"transaction":{"id":654877419,"accountId":8703506,"time":"2014-08-21T13:43:25.000000Z","type":"STOP_LOSS_FILLED","tradeId":654877314,"instrument":"SPX500_USD","units":1,"side":"sell","price":1987.6,"pl":-0.5477,"interest":0,"accountBalance":99676.8124}}
    {"heartbeat":{"time":"2014-08-21T13:43:29.000000Z"}}
    {"heartbeat":{"time":"2014-08-21T13:43:44.000000Z"}}
    {"transaction":{"id":654877474,"accountId":8703506,"time":"2014-08-21T13:43:46.000000Z","type":"TAKE_PROFIT_FILLED","tradeId":654877239,"instrument":"JP225_USD","units":1,"side":"sell","price":15585.6,"pl":-9.7492,"interest":-0.001,"accountBalance":99667.0622}}
    {"heartbeat":{"time":"2014-08-21T13:43:59.000000Z"}}
    {"heartbeat":{"time":"2014-08-21T13:44:14.000000Z"}}
    {"heartbeat":{"time":"2014-08-21T13:44:29.000000Z"}}
    {"transaction":{"id":654877597,"accountId":8703506,"time":"2014-08-21T13:44:40.000000Z","type":"STOP_LOSS_FILLED","tradeId":654877443,"instrument":"SGD_HKD","units":1,"side":"buy","price":6.20101,"pl":-0.0003,"interest":0,"accountBalance":99667.0619}}

### More Information

[http://developer.oanda.com/](http://developer.oanda.com/docs/v1/stream/#events-streaming)
