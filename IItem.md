- [IItem](#iitem)
  * [Generate (v1)](#generate-v1.md)
  * [GenerateKey (v1)](#generatekey-v1.md)
  * [GetKeyCount (v1)](#getkeycount-v1.md)
  * [GetWearTierMapping (v1)](#getweartiermapping-v1.md)
  * [GetWearTierIndex (v1)](#getweartierindex-v1.md)
  * [GetItems (v1)](#getitems-v1.md)
  * [RedeemForEth (v1)](#redeemforeth-v1.md)

# IItem

Interface used for VgoItem class

## Generate (v1)

`POST http://api.vgo.gg/IItem/Generate/v1/`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
blockchain_tx | string | + | Blockchain transaction ID
contract_token | string | + | User ID
sku | int | + | SKU of item
pattern_index | int | + |  Pattern index
wear | float | + | Wear float value

#### Output Example
```json
{  
  "status":1,
  "time":1525206480,
  "response":{  
    "item_id":25
  }
}
```

## GetWearTierMapping (v1)

`GET http://api.vgo.gg/IItem/GetWearTierMapping/v1?key=z`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
_none_ | | | 

#### Output Example

```json
{
  "status": 1,
  "time": 1524849064,
  "response": {
    "wear_tier_index_map": {
      "Factory New": 1,
      "Minimal Wear": 2,
      "Field-Tested": 3,
      "Well-Worn": 4,
      "Battle-Scarred": 5
    },
    "wear_tier_value_map": {
      "1": {
        "min": 0,
        "max": 0.06999999999999
      },
      "2": {
        "min": 0.07,
        "max": 0.14999999999999
      },
      "3": {
        "min": 0.15,
        "max": 0.37999999999999
      },
      "4": {
        "min": 0.38,
        "max": 0.44999999999999
      },
      "5": {
        "min": 0.45,
        "max": 1
      }
    }
  }
}
```

## GetWearTierIndex (v1)

`GET http://api.vgo.gg/IItem/GetWearTierIndex/v1?key=z&wear_value=0.25`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
wear_value | float | + | Wear float value

#### Output Example

```json
{
  "status": 1,
  "time": 1524849045,
  "response": {
    "wear_tier_index": 3
  }
}
```


## GetItems (v1)

All enabled items: `GET http://api.vgo.gg/IItem/GetItems/v1?key=z`

Filter by SKU: `GET http://api.vgo.gg/IItem/GetItems/v1?key=z&sku_filter=10`

Filter by SKU & Wear Tier: `GET http://api.vgo.gg/IItem/GetItems/v1?key=z&sku_filter=10&wear_tier_index=1`

Multiple SKU: `GET http://api.vgo.gg/IItem/GetItems/v1?key=z&sku_filter=10,20&wear_tier_index=1`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
sku_filter | int-csv | - | SKU filter, separated with comma
- wear_tier_index | int | - | Optional alongside sku_filter

#### Output Example

```json
{
  "status": 1,
  "time": 1524850074,
  "response": {
    "items": {
      "10": {
        "1": {
          "wear_tier": "Factory New",
          "name": "UMP-45 | Primal Saber",
          "category": "Classified SMG",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 5
        },
        "2": {
          "wear_tier": "Minimal Wear",
          "name": "UMP-45 | Primal Saber",
          "category": "Classified SMG",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 100
        },
        "3": {
          "wear_tier": "Field-Tested",
          "name": "UMP-45 | Primal Saber",
          "category": "Classified SMG",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 200
        },
        "4": {
          "wear_tier": "Well-Worn",
          "name": "UMP-45 | Primal Saber",
          "category": "Classified SMG",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 300
        },
        "5": {
          "wear_tier": "Battle-Scarred",
          "name": "UMP-45 | Primal Saber",
          "category": "Classified SMG",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 400
        }
      },
      "20": {
        "1": {
          "wear_tier": "Factory New",
          "name": "AK-47 | Case Hardened",
          "category": "Classified Rifle",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 1099
        },
        "2": {
          "wear_tier": "Minimal Wear",
          "name": "AK-47 | Case Hardened",
          "category": "Classified Rifle",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 1099
        },
        "3": {
          "wear_tier": "Field-Tested",
          "name": "AK-47 | Case Hardened",
          "category": "Classified Rifle",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 1099
        },
        "4": {
          "wear_tier": "Well-Worn",
          "name": "AK-47 | Case Hardened",
          "category": "Classified Rifle",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 1099
        },
        "5": {
          "wear_tier": "Battle-Scarred",
          "name": "AK-47 | Case Hardened",
          "category": "Classified Rifle",
          "color": "D2D2D2",
          "image": "https://vgo.gg/img/item/sku+wear_tier",
          "suggested_price": 1099
        }
      }
    }
  }
}
```

## RedeemForEth (v1)

`POST http://api.vgo.gg/IItem/RedeemForEth/v1`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
items | int csv | x | Item IDs (keys)
eth_address | string | x | Eth address to send the eth to
twofactor_code | string | x | 2FA code

#### Output Example

```json
{
  "status": 1,
  "time": 1524849045,
  "response": {
    "eth_txn_id": "0xa4daad3e2951522c830ea57f6584f6d629ecb24424a6a693980097dc37536e0b",
    "eth_sent": "0.02103940100000"
  }
}
```
