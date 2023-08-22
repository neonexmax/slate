# General Info

## General API information
- Base API URL
  - ```https://api.bitmusa.com```
- Root Endpoint
  - ```/api/v1```
- All endpoints return either a JSON object or array.
- Users can use the Open API provided by BitMusa to develop the following functions for
  trading.

  - [Spot API] 
      - Spot Wallet
      - Spot Market
      - Spot OrderBook
      - Spot Market Trades
      - Spot Open Order
      - Spot Order history
      - Spot Trade history
      - Spot Order
      - Spot Order cancel
      - Spot Order Cancel All
      - Spot Current Kline
      - Spot Kline History
  - [Futures API]
      - Futures Wallet
      - Futures Market Trades
      - Futures Market
      - Futures OrderBook
      - Futures Position
      - Futures Position Close All
      - Futures Leverage
      - Futures Order(Open/Close)
      - Futures Open Order
      - Futures Order Cancel
      - Futures Order Cancel All

## Endpoint Security Type
- Auth Key, API Key are passed into the Rest API via the ```Authorization``` , ```x-api-key``` header.

## Limit of requests
- All APIs we provide are limited to 8 times per second and 200 times per minute to ensure
  smooth service.
