# Futures Endpoints

## Futures Wallet

```GET /future/wallet```

> Response

```json
{
  "data": [
    {
      "symbol": "USDT",
      "total_wallet_balance": 20.911789292484,
      "total_margin_balance": 20.911789292484,
      "total_available_balance": 20.911789292484,
      "total_unpnl": 0,
      "position": []
    }
  ],
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


## Futures Market Trades

```GET /future/market/trade```

> Response

```json
{
  "data": [
    {
      "ticker": "BTCUSDT",
      "price": "26467.1000000000000000",
      "qty": "1.1230000000000000",
      "value": "29722.5533000000000000",
      "position": 0,
      "traded_time": 1692371062979
    },
    {
      "ticker": "BTCUSDT",
      "price": "26467.1000000000000000",
      "qty": "8.4680000000000000",
      "value": "224123.4028000000000000",
      "position": 0,
      "traded_time": 1692366377010
    },
    ...
  ],
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name   | Type   | Required | Description   |
|--------|--------|----------|---------------|
| symbol | String | Yes      |               |
| size   | int    | No       | Default : 100 |


## Futures Market

```GET /future/market```

> Response

```json
{
  "data": {
    "pk": "01H2VFYH7YX5WC0NXKF9EB2V55",
    "ticker": "BTCUSDT",
    "base_price": 26138.4,
    "high_price": 26662.6,
    "low_price": 21102.9,
    "last_price": 26059.2,
    "mark_price": 25965.8276571,
    "index_price": 25964.82729,
    "funding_fee_rate": -1.0E-4,
    "funding_time": 1686700800000,
    "remaining_funding_time": 1384997,
    "change_price": -79.2,
    "change_rate": -0.303,
    "total_qty": 224772.239,
    "total_value": 5.880733979646818E9,
    "last_updated_time": 1686706615003
  },
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name   | Type   | Required | Description   |
|--------|--------|----------|---------------|
| symbol | String | Yes      |               |


## Futures OrderBook

```GET /future/market/orderbook```

> Response

```json
{
  "data": {
    "sell": [
      {
        "payload": null,
        "price": "26554.3",
        "pk": "01H2EXD7FNF2ZA4FNERPB7YED0",
        "ticker": "BTCUSDT",
        "amount": "982.5091",
        "qty": "0.037",
        "total": 2.02958114595E7,
        "total_qty": 764.522,
        "position": "1",
        "scale": "0",
        "updated_time": "1686275268083",
        "mode": "add"
      },
      {
        "payload": null,
        "price": "26554.2",
        "pk": "01H2EXCQQYMD23N3GMZQWV1NC5",
        "ticker": "BTCUSDT",
        "amount": "451.4214",
        "qty": "0.017",
        "total": 2.02948289504E7,
        "total_qty": 764.485,
        "position": "1",
        "scale": "0",
        "updated_time": "1686275451456",
        "mode": "add"
      }
      ...
    ],
    "buy": [
      {
        "payload": null,
        "price": "26538.8",
        "pk": "01H2FD9XHBBZ9AZQ36135CF1FW",
        "ticker": "BTCUSDT",
        "amount": "10468548.1256",
        "qty": "394.462",
        "total": 1.04685481256E7,
        "total_qty": 394.462,
        "position": "0",
        "scale": "0",
        "updated_time": "1686291965027",
        "mode": "add"
      },
      {
        "payload": null,
        "price": "26538.7",
        "pk": "01H2FDA4T0N9PDZXT6ZDWYAAX3",
        "ticker": "BTCUSDT",
        "amount": "101537.0662",
        "qty": "3.826",
        "total": 1.05700851918E7,
        "total_qty": 398.288,
        "position": "0",
        "scale": "0",
        "updated_time": "1686291960645",
        "mode": "add"
      }
      ...
    ]
  },
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name   | Type   | Required | Description  |
|--------|--------|----------|--------------|
| ticker | String | Yes      |              |
| size   | int    | No       | default : 50 |


## Futures Position

```GET /future/position```

> Response

```json
{
  "data": [
    {
      "id": 535,
      "position": 0,
      "entry_price": 26617.03674876,
      "margin_gap": 0.0,
      "status": 0,
      "liquid_price": 25764.30575663,
      "close_fee": 20.8125511,
      "member_id": 79010,
      "ticker": "BTCUSDT",
      "bankruptcy_price": 25631.22057289,
      "take_profit_price": 0.0,
      "entry_time": "2023-06-09T10:21:46",
      "coin_symbol": "BTC",
      "initial_margin": 2001.20683703,
      "close_time": null,
      "base_symbol": "USDT",
      "maintenance_margin": 270.16292299,
      "stop_loss_price": 0.0,
      "ticker_id": 1,
      "leverage": 27,
      "liquid_margin": 852.73099213,
      "adl": 0.0,
      "margin_mode": 0,
      "qty": 2.03,
      "position_margin": 2022.01938813,
      "return_liquid_margin": null,
      "value": 54032.5846,
      "extra_margin": 0.0
    }
  ],
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name   | Type   | Required | Description                                           |
|--------|--------|----------|-------------------------------------------------------|
| ticker | String | Yes      | If blank, then query all <br> position that user have |


## Futures Position Close All

Close All Positions On That Ticker Or Close All Positions On All Tickers

```POST /future/position/close/all```

> Response

```json
{
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name   | Type   | Required | Description                               |
|--------|--------|----------|-------------------------------------------|
| ticker | String | Yes      | all : close all positions on all tickers  |


## Futures Leverage

```POST /future/leverage```

> Response

```json
{
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name      | Type   | Required | Description |
|-----------|--------|----------|-------------|
| ticker    | String | Yes      |             |
| leverage  | int    | Yes      | 1 ~ 125     |


## Futures Order

```POST /future/order```

> Response

```json
{
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name                         | Type    | Required                                  | Description                                                      |
|------------------------------|---------|-------------------------------------------|------------------------------------------------------------------|
| ticker                       | String  | Yes                                       |                                                                  |
| direction                    | int     | Yes                                       | 0 : OPEN <br> 1 : CLOSE                                          |
| margin_mode                  | int     | Yes                                       | 0 : ISOLATED                                                     |
| position                     | int     | Yes                                       | 0 : BUY(Long)<br> 1 : SELL(Short)  <br> close : on the other way |
| order_type                   | int     | Yes                                       | 0 : MARKET <br> 1 : LIMIT                                        |
| order_price                  | String  | Yes                                       |                                                                  |
| order_qty                    | String  | Yes                                       |                                                                  |
| is_reduce_only               | boolean | No                                        |                                                                  |
| is_post_only                 | boolean | No                                        |                                                                  |
| is_take_profit               | boolean | No                                        |                                                                  |
| take_profit_trigger_type     | int     | No (is_take_profit = true : Yes )         | 1 : MARK <br/> 2 : LAST                                          |
| take_profit_trigger_price    | String  | No (is_take_profit = true : Yes )         |                                                                  |
| take_profit_order_type       | int     | No (is_take_profit = true : Yes )         | 0 : MARKET <br> 1 : LIMIT                                        |
| take_profit_order_price      | String  | No (take_profit_order_type = true : Yes ) |                                                                  |
| is_stop_loss                 | boolean | No (is_stop_loss = true : Yes )           |                                                                  |
| stop_loss_trigger_type       | int     | No (is_stop_loss = true : Yes )           | 1 : MARK <br/> 2 : LAST                                          |
| stop_loss_trigger_price      | String  | No (is_stop_loss = true : Yes )           |                                                                  |
| stop_loss_order_type         | int     | No (is_stop_loss = true : Yes )           | 0 : MARKET <br> 1 : LIMIT                                        |
| stop_loss_order_price        | String  | No (stop_loss_order_type = true : Yes )   |                                                                  |


## Futures Open Order

```GET /future/order```

> Response

```json
{
  "data": [
    {
      "id": 277419,
      "ticker_id": 1,
      "member_id": 79010,
      "order_id": "F7901016863067195812430",
      "margin_mode": 0,
      "direction": 0,
      "position": 0,
      "order_type": 1,
      "status": 0,
      "tif_mode": 0,
      "trigger_type": 0,
      "trigger_direction": 0,
      "ticker": "BTCUSDT",
      "coin_symbol": "BTC",
      "base_symbol": "USDT",
      "leverage": 27,
      "order_price": 26607.1,
      "order_qty": 1.0,
      "traded_price": 0.0,
      "traded_qty": 0.0,
      "traded_value": 0.0,
      "left_qty": 1.0,
      "is_post_only": false,
      "is_reduce_only": false,
      "is_price_protected": false,
      "trigger_id": null,
      "trigger": null,
      "order_time": "2023-06-09T10:32:00",
      "filled_time": null,
      "cancel_time": null
    }
  ],
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name       | Type    | Required  | Description               |
|------------|---------|-----------|---------------------------|
| ticker     | String  | No        | If blank, then query all  |
| start_time | String  | No        | unix timestamp            |
| size       | int     | No        | default : 50              |


## Futures Order Cancel

```POST /future/order/cancel/{orderId}```

> Response

```json
{
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### PathValue:

| Name       | Type    | Required | Description |
|------------|---------|----------|-------------|
| orderId    | String  | Yes      |             |


## Futures Order Cancel All

```POST /future/order/cancel/all```

> Response

```json
{
  "code": 0,
  "message": "success"
}
```

### Headers:

| Name           | Type   | Required | Description              |
|----------------|--------|----------|--------------------------|
| Authorization  | String | Yes      | Auth Key (type = Bearer) |
| x-api-token    | String | Yes      | API key                  |


### Parameter:

| Name   | Type    | Required | Description                               |
|--------|---------|----------|-------------------------------------------|
| ticker | String  | Yes      | all : cancel all positions on all tickers |
