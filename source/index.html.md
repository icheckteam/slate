---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to Ichain API!

Ichain is a blockchain based on tendermint. Ichain makes deploying, multiple networks connection and run supply chain application easier.



# Keys

## Get All Keys

```shell
curl "http://example.com/keys"
```

> The above command returns JSON structured like this:

```json
[
  {
    "name": "name",
    "type": "local",
    "address": "cosmosaccaddr1w3s4aad6fu84k2h72q9uwacxcu4snpuyee068l",
    "pub_key": "cosmosaccpub1addwnpepqgx2cfgj3z72e0s6xz2jk5kuzlksv2uat75c3skr2jax7azfcc356zak5tu"
  },
  {
    "name": "name2",
    "type": "local",
    "address": "cosmosaccaddr14ut4fk2ayc2umd08m83xgp6jjsl22lglkv9sa5",
    "pub_key": "cosmosaccpub1addwnpepqgwxz7k87w2j68ak6v3xufxeqfk9evdf09wn6t5qejchwu6w6ffw6jan895"
  },
]
```

This endpoint retrieves all keys.

### HTTP Request

`GET http://example.com/api/keys`

## Get a Specific Key

```shell
curl "http://example.com/api/keys/name"
```

> The above command returns JSON structured like this:

```json
{
  "name": "name2",
  "type": "local",
  "address": "cosmosaccaddr14ut4fk2ayc2umd08m83xgp6jjsl22lglkv9sa5",
  "pub_key": "cosmosaccpub1addwnpepqgwxz7k87w2j68ak6v3xufxeqfk9evdf09wn6t5qejchwu6w6ffw6jan895"
}
```

This endpoint retrieves a specific key.
### HTTP Request

`GET http://example.com/keys/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The Name of the key to retrieve

## Get a Specific Seed 

```shell
curl "http://example.com/api/keys/seed"
```


This endpoint retrieve a seed.

### HTTP Request

`GET http://example.com/keys/seed`

> The above command returns string like this:

```text
okay glow divert sketch review offer lens repeat win shop define yellow begin invite ship direct loan example humble rookie loan become wedding broccoli
```


## Add new a Key

```shell
curl "http://example.com/api/keys"
  -H "Accept: application/json"
  -X POST -d '{"name": "name", "password": "password", "seed": "seed"}'
```


This endpoint add a key.

### HTTP Request

`POST http://example.com/keys`



## Update a Key

```shell
curl "http://example.com/api/keys/name"
  -H "Accept: application/json"
  -X PUT -d '{"name": "name", "new_password": "new_password", "old_password": "new_password"}'
```


This endpoint update a key.

### HTTP Request

`PUT http://example.com/keys/<NAME>`


### URL Parameters

Parameter | Description
--------- | -----------
NAME | The Name of the key to update



## Delete a Specific Key

```shell
curl "http://example.com/api/keys/2"
  -H "Accept: application/json"
  -X DELETE -d {"password": "password"}
```


This endpoint deletes a specific key.

### HTTP Request

`DELETE http://example.com/keys/<NAME>`

### URL Parameters

Parameter | Description
--------- | -----------
NAME | The Name of the key to delete




# Blocks

## Get a Specific Block

```shell
curl "http://example.com/blocks/4740"
```

> The above command returns JSON structured like this:

```json
{  
   "block_meta":{  
      "block_id":{  
         "hash":"1DF1475AEE438C5A5B399613AB07E50D61EA6007",
         "parts":{  
            "total":"1",
            "hash":"DEFF970568C53319FAFC9383F29BB4B4198094EC"
         }
      },
      "header":{  
         "chain_id":"ichain",
         "height":"4740",
         "time":"2018-07-23T13:59:08.275071951Z",
         "num_txs":"0",
         "last_block_id":{  
            "hash":"11632066EC317A46D9EBA35D1573EE00017DFEE6",
            "parts":{  
               "total":"1",
               "hash":"CFC647ED8AE7B87CCEED2DE9C125344DD649804E"
            }
         },
         "total_txs":"27",
         "last_commit_hash":"043B21882D2363F685739666497EB636960DA5AC",
         "data_hash":"",
         "validators_hash":"995E231510D36111D879576B43BDB78D16112508",
         "consensus_hash":"D6B74BB35BDFFD8392340F2A379173548AE188FE",
         "app_hash":"2524B608CC48BD53A86CF653F10C41363144614B",
         "last_results_hash":"",
         "evidence_hash":""
      }
   },
   "block":{  
      "header":{  
         "chain_id":"ichain",
         "height":"4740",
         "time":"2018-07-23T13:59:08.275071951Z",
         "num_txs":"0",
         "last_block_id":{  
            "hash":"11632066EC317A46D9EBA35D1573EE00017DFEE6",
            "parts":{  
               "total":"1",
               "hash":"CFC647ED8AE7B87CCEED2DE9C125344DD649804E"
            }
         },
         "total_txs":"27",
         "last_commit_hash":"043B21882D2363F685739666497EB636960DA5AC",
         "data_hash":"",
         "validators_hash":"995E231510D36111D879576B43BDB78D16112508",
         "consensus_hash":"D6B74BB35BDFFD8392340F2A379173548AE188FE",
         "app_hash":"2524B608CC48BD53A86CF653F10C41363144614B",
         "last_results_hash":"",
         "evidence_hash":""
      },
      "data":{  
         "txs":null
      },
      "evidence":{  
         "evidence":null
      },
      "last_commit":{  
         "block_id":{  
            "hash":"11632066EC317A46D9EBA35D1573EE00017DFEE6",
            "parts":{  
               "total":"1",
               "hash":"CFC647ED8AE7B87CCEED2DE9C125344DD649804E"
            }
         },
         "precommits":[  
            {  
               "validator_address":"710D9B6973ABE416C13D631148A059CA885F6F77",
               "validator_index":"0",
               "height":"4739",
               "round":"0",
               "timestamp":"2018-07-23T13:55:54.034392147Z",
               "type":2,
               "block_id":{  
                  "hash":"",
                  "parts":{  
                     "total":"0",
                     "hash":""
                  }
               },
               "signature":{  
                  "type":"tendermint/SignatureEd25519",
                  "value":"O59p8zq6py9hEwEy5eUsQ3YANWeZlrMsBf9BEhOaEy/SA6fyqnsW8a66eQTJ20RV0sLxE8tRMk0Cdw/LHIhZDA=="
               }
            },
            {  
               "validator_address":"8C55528FF497863988D40C393B3A90911CD41A10",
               "validator_index":"1",
               "height":"4739",
               "round":"0",
               "timestamp":"2018-07-23T13:55:53.93455219Z",
               "type":2,
               "block_id":{  
                  "hash":"11632066EC317A46D9EBA35D1573EE00017DFEE6",
                  "parts":{  
                     "total":"1",
                     "hash":"CFC647ED8AE7B87CCEED2DE9C125344DD649804E"
                  }
               },
               "signature":{  
                  "type":"tendermint/SignatureEd25519",
                  "value":"AGF3UDO8/tL31HvpZPDy7LZLv1kJDiUOwqx10KHo985VQnxIu20+ptNQfk0+jCzJpPZpmXCrcM9mrRjeTu7EBA=="
               }
            },
            {  
               "validator_address":"96DEFA0A335F29D30C5CD2D20B184446D3FAFDDC",
               "validator_index":"2",
               "height":"4739",
               "round":"0",
               "timestamp":"2018-07-23T13:55:54.034618887Z",
               "type":2,
               "block_id":{  
                  "hash":"",
                  "parts":{  
                     "total":"0",
                     "hash":""
                  }
               },
               "signature":{  
                  "type":"tendermint/SignatureEd25519",
                  "value":"xnSOLEvlrt3PDNYR/c37FttSI6+W9fmTgqBzojlikx1giLi2v0rJCU6flZwI2vFsDxvrqEF0LsY3/SsvFRqhBg=="
               }
            },
            {  
               "validator_address":"9D1157AC58F42A33814BBDB21D1BCC5F3CFE1733",
               "validator_index":"3",
               "height":"4739",
               "round":"0",
               "timestamp":"2018-07-23T13:55:54.034446254Z",
               "type":2,
               "block_id":{  
                  "hash":"",
                  "parts":{  
                     "total":"0",
                     "hash":""
                  }
               },
               "signature":{  
                  "type":"tendermint/SignatureEd25519",
                  "value":"q2kEnenOGo+SCjfxLO3IGxoxujE5WxRbjfH1U89H6D0yUYz+r2IioCcVwm/ru84nE1fqc+f+41i87DfxSYcxCA=="
               }
            },
            {  
               "validator_address":"FF2A2D94D12E68BD8F649EE5E4C53F809855FCAD",
               "validator_index":"4",
               "height":"4739",
               "round":"0",
               "timestamp":"2018-07-23T13:59:03.025907572Z",
               "type":2,
               "block_id":{  
                  "hash":"11632066EC317A46D9EBA35D1573EE00017DFEE6",
                  "parts":{  
                     "total":"1",
                     "hash":"CFC647ED8AE7B87CCEED2DE9C125344DD649804E"
                  }
               },
               "signature":{  
                  "type":"tendermint/SignatureEd25519",
                  "value":"vfp8YMErGymmef+XPULRwpUHhUX1ZTfg8lmavB40NSg7ag2qtmTBKHNTCsgLmxz+z5LT2UrXM4Kb1Ah5yyQeDw=="
               }
            }
         ]
      }
   }
}
```

This endpoint retrieves specific block.

### HTTP Request

`GET http://example.com/api/blocks/<height>`


### URL Parameters

Parameter | Description
--------- | -----------
height | The height of the block to retrieve





# Txs


## Search all Txs
```shell
curl "http://example.com/txs?tag=sender='address'"
```
> The above command returns JSON structured like this:

```json
[{  
   "hash":"802CF829C55E83A7942B7B01F8D89578AA7128C5",
   "height":"32342",
   "tx":{  
      "type":"auth/StdTx",
      "value":{  
         "msg":[  
            {  
               "type":"identity/SetCerts",
               "value":{  
                  "certifier":"cosmosaccaddr1wkwv3tl5v8t3rzdymkhmurag55k4psudpkvw2r",
                  "recipient":"cosmosaccaddr146t7xjmqsjswl6nt9c383z3xpxwfs0p8ar99ka",
                  "values":[  
                     {  
                        "id":"",
                        "context":"",
                        "property":"livestock_certificate.vietgap",
                        "data":{  
                           "company_address":"Hoang Liet Hoang Mai",
                           "company_name":"324234",
                           "effective_date":"1532503877",
                           "email":"thangn.1411@gmail.com",
                           "end_date":"",
                           "phone":"977465849",
                           "predictive_production":"212121",
                           "product_or_group":"12121",
                           "registration_id":"12121",
                           "total_production_area":"21212",
                           "website":"http://icheckcorp.com/"
                        },
                        "confidence":true,
                        "expires":"0",
                        "revocation":{  
                           "id":"",
                           "type":""
                        }
                     }
                  ]
               }
            }
         ],
         "fee":{  
            "amount":[  
               {  
                  "denom":"",
                  "amount":"0"
               }
            ],
            "gas":"50000"
         },
         "signatures":[  
            {  
               "pub_key":{  
                  "type":"tendermint/PubKeySecp256k1",
                  "value":"A3vmPuikkyMxpPG7xq0YW5OpEth13P+Y2vHjtHdwM8bv"
               },
               "signature":{  
                  "type":"tendermint/SignatureSecp256k1",
                  "value":"MEQCICyw6jWICmqgykRFR7IK/o7qfwSLQo08zv3CTqB5ute0AiAuO1bHnr1Qiba4F81f50JqS5hxe8xOgmcM3x6dH9x3vA=="
               },
               "account_number":"2",
               "sequence":"3"
            }
         ],
         "memo":""
      }
   },
   "result":{  
      "log":"Msg 0: ",
      "gas_used":"5321",
      "fee":{  

      }
   },
   "time":"0"
}]
```
This endpoint retrieves specific tx.

### HTTP Request

`GET http://example.com/txs/?tag=<tag>`


### URL Parameters

Parameter | Description
--------- | -----------
tag | The tag of the tx to retrieve




## Get a Specific Tx

```shell
curl "http://example.com/txs/802CF829C55E83A7942B7B01F8D89578AA7128C5"
```

> The above command returns JSON structured like this:

```json
{  
   "hash":"802CF829C55E83A7942B7B01F8D89578AA7128C5",
   "height":"32342",
   "tx":{  
      "type":"auth/StdTx",
      "value":{  
         "msg":[  
            {  
               "type":"identity/SetCerts",
               "value":{  
                  "certifier":"cosmosaccaddr1wkwv3tl5v8t3rzdymkhmurag55k4psudpkvw2r",
                  "recipient":"cosmosaccaddr146t7xjmqsjswl6nt9c383z3xpxwfs0p8ar99ka",
                  "values":[  
                     {  
                        "id":"",
                        "context":"",
                        "property":"livestock_certificate.vietgap",
                        "data":{  
                           "company_address":"Hoang Liet Hoang Mai",
                           "company_name":"324234",
                           "effective_date":"1532503877",
                           "email":"thangn.1411@gmail.com",
                           "end_date":"",
                           "phone":"977465849",
                           "predictive_production":"212121",
                           "product_or_group":"12121",
                           "registration_id":"12121",
                           "total_production_area":"21212",
                           "website":"http://icheckcorp.com/"
                        },
                        "confidence":true,
                        "expires":"0",
                        "revocation":{  
                           "id":"",
                           "type":""
                        }
                     }
                  ]
               }
            }
         ],
         "fee":{  
            "amount":[  
               {  
                  "denom":"",
                  "amount":"0"
               }
            ],
            "gas":"50000"
         },
         "signatures":[  
            {  
               "pub_key":{  
                  "type":"tendermint/PubKeySecp256k1",
                  "value":"A3vmPuikkyMxpPG7xq0YW5OpEth13P+Y2vHjtHdwM8bv"
               },
               "signature":{  
                  "type":"tendermint/SignatureSecp256k1",
                  "value":"MEQCICyw6jWICmqgykRFR7IK/o7qfwSLQo08zv3CTqB5ute0AiAuO1bHnr1Qiba4F81f50JqS5hxe8xOgmcM3x6dH9x3vA=="
               },
               "account_number":"2",
               "sequence":"3"
            }
         ],
         "memo":""
      }
   },
   "result":{  
      "log":"Msg 0: ",
      "gas_used":"5321",
      "fee":{  

      }
   },
   "time":"0"
}
```
This endpoint retrieves specific tx.

### HTTP Request

`GET http://example.com/txs/<hash>`


### URL Parameters

Parameter | Description
--------- | -----------
hash | The hash of the tx to retrieve

# Account Certificates
## Get All Certificates

```shell
curl "http://example.com/accounts/cosmosaccaddr146t7xjmqsjswl6nt9c383z3xpxwfs0p8ar99ka/certs"
```
> The above command returns JSON structured like this:

```json
[  
   {  
      "id":"",
      "context":"",
      "property":"entity.person",
      "certifier":"cosmosaccaddr178r5xtw82ethyzyn82wa8yry76nnmyr26m79ww",
      "owner":"cosmosaccaddr16y6p2v",
      "trust":true,
      "data":{  
         "address_line_1":"Hoang Liet Hoang Mai",
         "address_line_2":"",
         "city":"Hanoi",
         "country":"",
         "effective_date":"1532344605",
         "end_date":"",
         "first_name":"Thang",
         "last_name":"Nguyen",
         "org_type":"",
         "postal_code":"",
         "province":"Hà Nội"
      },
      "confidence":true,
      "expires":"0",
      "created_at":"1532328402",
      "revocation":{  
         "id":"",
         "type":""
      }
   }
]
```

This endpoint retrieves certificates.

### HTTP Request

`GET http://example.com/accounts/<addr>/certs`


### URL Parameters

Parameter | Description
--------- | -----------
addr | The address of the account to retrieve


### Query String

Parameter | Description
--------- | -----------
trust | Only retrieve trust certificate
certifier | The address of the certifier
property | The property of the certificate

## Issue/Revokcation Certificate

```shell
curl "http://example.com/accounts/cosmosaccaddr146t7xjmqsjswl6nt9c383z3xpxwfs0p8ar99ka/certs"
  -H "Accept: application/json"
  -X POST -d '{
    "base_req": {
      "name": "name",
      "password": "password",
      "account_number": "account_number",
      "sequence": "sequence",
      "gas": "10000",
      "chain_id": "chain_id"
    },
    "values": [
      {
        "property": "company",
        "data": {"demo": "demo"},
        "confidence": true
      }
    ]
  }'

```

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint issue certificate.

### HTTP Request

`POST http://example.com/accounts/<addr>/certs`

### URL Parameters

Parameter | Description
--------- | -----------
addr | The address of the account to receive

# Trust

## Add Trust
```shell
curl "http://example.com/accounts/cosmosaccaddr146t7xjmqsjswl6nt9c383z3xpxwfs0p8ar99ka/trusts"
  -H "Accept: application/json"
  -X POST -d '{
    "base_req": {
      "name": "name",
      "password": "password",
      "account_number": "account_number",
      "sequence": "sequence",
      "gas": "10000",
      "chain_id": "chain_id"
    },
    "trust": true
  }'

```

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint add trust.

### HTTP Request

`POST http://example.com/accounts/<addr>/trusts`

### URL Parameters

Parameter | Description
--------- | -----------
addr | The address of the account to receive

## Get All Trusts
```shell
curl "http://example.com/accounts/cosmosaccaddr146t7xjmqsjswl6nt9c383z3xpxwfs0p8ar99ka/trusts"
  -H "Accept: application/json"

```

> The above command returns JSON structured like this:

```json
[
  {
    "trustor": "1212",
    "trusting": "12121",
    "trust": 1,
  }
]
```

This endpoint retrieves all  trusts.

### HTTP Request

`POST http://example.com/accounts/<addr>/trusts`

### URL Parameters

Parameter | Description
--------- | -----------
addr | The address of the account to receive



# Assets

## Get All Assets

## Create Asset Record

```shell
curl "http://example.com/assets"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      },
      "name": "test",
      "asset_id": "test",
      "quantity": "100",
      "unit": "kg",
      "parent": "1",
      "properties": [
        {"name": "size", "type": "4", "number_value": "50"}
      ]
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint issue certificate.

### HTTP Request

`POST http://example.com/assets`

## Add Quantity

```shell
curl "http://example.com/assets/id/add"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      },
      "quantity": "10"
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint add quantity

### HTTP Request

`POST http://example.com/assets/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to add


## Subtract Quantity

```shell
curl "http://example.com/assets/id/subtract"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      },
      "quantity": "10"
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint subtract quantity

### HTTP Request

`POST http://example.com/assets/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to subtract

## Add Materials

```shell
curl "http://example.com/assets/id/materials"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      },
      "amount": [
        {"denom": "test", "amount": "5"}
      ]
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint add quantity

### HTTP Request

`POST http://example.com/assets/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to add

## Update Properties

```shell
curl "http://example.com/assets/id/properties"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      },
      "properties": [
        {"name": "size", "type": "4", "number_value": "50"}
      ]
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint update properties

### HTTP Request

`POST http://example.com/assets/<ID>/properties`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to update

## Finalize

```shell
curl "http://example.com/assets/id/finalize"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      }
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint finalize

### HTTP Request

`POST http://example.com/assets/<ID>/finalize`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to finalize

## Create Proposal

```shell
curl "http://example.com/assets/id/proposals"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      },
      "recipient": "%s",
      "properties": ["size"],
      "role": "1"
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint create proposal

### HTTP Request

`POST http://example.com/assets/<ID>/proposals`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to create 

## Answer Proposal

```shell
curl "http://example.com/assets/id/proposals/3434/answer"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      },
      "response": "1"
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint answer proposal

### HTTP Request

`POST http://example.com/assets/<ID>/proposals/<ADDRESS>/answer`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to answer
ADDRESS | The recipient address 


## Revoke Reporter

```shell
curl "http://example.com/assets/id/reporters/3434/revoke"
  -H "Accept: application/json"
  -X POST -d '
    {
      "base_req": {
        "name": "name",
        "password": "password",
        "account_number": "account_number",
        "sequence": "sequence",
        "gas": "10000",
        "chain_id": "chain_id"
      }
    }
  '
``` 

> The above command returns JSON structured like this:

```json
{
  "check_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "delive_tx": {
    "code": "1",
    "data": "",
    "log": "",
    "info": "",
    "gas_wanted": "1000",
    "gas_used": "100",
    "tags": [],
    "fee": {},
  },
  "hash": "2391391391",
  "height": "1212"
}
```

This endpoint revoke reporter

### HTTP Request

`POST http://example.com/assets/<ID>/reporters/<ADDRESS>/revoke`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The id of the asset to answer
ADDRESS | The recipient address



# Accounts

## Get Account

```shell
curl "http://example.com/accounts/cosmosaccaddr14ut4fk2ayc2umd08m83xgp6jjsl22lglkv9sa5"
  -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
{  
   "type":"ichain/Account",
   "value":{  
      "BaseAccount":{  
         "address":"cosmosaccaddr14ut4fk2ayc2umd08m83xgp6jjsl22lglkv9sa5",
         "coins":[  
            {  
               "denom":"tomato",
               "amount":"100000"
            }
         ],
         "public_key":{  
            "type":"tendermint/PubKeySecp256k1",
            "value":"AhxhesfzlS0fttMibiTZAmxcsal5XT0ugMyxd3NO0lLt"
         },
         "account_number":"8",
         "sequence":"3"
      },
      "name":""
   }
}
```


This endpoint retrieve account

### HTTP Request

`POST http://example.com/accounts/<ADDRESS>`

### URL Parameters

Parameter | Description
--------- | -----------
ADDRESS | the address

## Get All Assets
```shell
curl "http://example.com/accounts/aac/assets"
  -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "id",
    "name": "name"
  }
]
```

This endpoint retrieves assets

### HTTP Request

`POST http://example.com/accounts/<ADDRESS>/assets`

### URL Parameters

Parameter | Description
--------- | -----------
ADDRESS | the address


## Get All Report Assets
```shell
curl "http://example.com/accounts/acc/report-assets"
  -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": "id",
    "name": "name"
  }
]
```

This endpoint retrieves assets

### HTTP Request

`POST http://example.com/accounts/<ADDRESS>/report-assets`

### URL Parameters

Parameter | Description
--------- | -----------
ADDRESS | the address

## Get All Proposals
```shell
curl "http://example.com/accounts/acc/proposals"
  -H "Accept: application/json"
```

> The above command returns JSON structured like this:

```json
[
  {
    "role": "id",
    "status": "name",
    "properties": [""],
    "issuer": "issuer",
    "recipient": "string"
  }
]
```

This endpoint retrieves proposals

### HTTP Request

`POST http://example.com/accounts/<ADDRESS>/proposals`

### URL Parameters

Parameter | Description
--------- | -----------
ADDRESS | the address

