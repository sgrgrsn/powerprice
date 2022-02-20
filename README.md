# Power Price

## Authenticate

POST: https://api.obviux.dk/v2/authenticate

Headers:
```
Content-Type: application/json
Accept: application/json
X-Customer-Ip: 8.8.8.8
```

Body:
```
{
  "customer": "{email}",
  "password": "{password}"
}
```

Response:
```
{
  "external_id": "596F7572-5F45-7874-6572-6E616C5F4964",
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c"
}
```

## Load prices

GET: https://prod.copi.obviux.dk/pricePage/{external_id}

Headers:
```
Content-Type: application/json
Accept: application/json
Authorization: {token}
```

Response:
```
{
  "prices": [
    {
      "valid_from": "2022-02-20 23:00:00",
      "grid_area": "DK2",
      "price": 13.73875,
      "COPI": {
        "xAxisLabel": "23",
        "pricePrefix": "Kl. 23-00, søndag den 20. februar er prisen",
        "priceExcludingTransport": 0.1373875,
        "priceDisplayExcludingTransport": "0.14",
        "priceIncludingTransport": 1.6980875,
        "priceDisplayIncludingTransport": "1.70",
        "unit": "kr."
      }
    },
    {
      "valid_from": "2022-02-20 22:00:00",
      "grid_area": "DK2",
      "price": 37.39125,
      "COPI": {
        "xAxisLabel": "22",
        "pricePrefix": "Kl. 22-23, søndag den 20. februar er prisen",
        "priceExcludingTransport": 0.3739125,
        "priceDisplayExcludingTransport": "0.37",
        "priceIncludingTransport": 1.9346125,
        "priceDisplayIncludingTransport": "1.93",
        "unit": "kr."
      }
    }
  ]
}
```
