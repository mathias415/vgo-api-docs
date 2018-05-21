- [IItem](#iitem)
  * [GenerateTestItem (v1)](#generatetestitem-v1)
  * [GetWearTierMapping (v1)](#getweartiermapping-v1)
  * [GetWearTierIndex (v1)](#getweartierindex-v1)
  * [GetItems (v1)](#getitems-v1)
  * [GetItemsById (v1)](#getitemsbyid-v1)
  * [RedeemForEth (v1)](#redeemforeth-v1)

# IItem

Interface used for VgoItem class


## GenerateTestItem (v1)

Only available on dev/staging environments.

`POST http://api.vgo.test/IItem/GenerateTestItem/v1/`

#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
sku | int | - | Which item definition to generate.  If not provided, one will be randomly selected.
wear | float | - | What wear value the item should have.  Range 0-1 inclusive.  If not provided, one will be randomly selected.
pattern_index | int | - | What pattern index the item should have.  Range: 0-1000 inclusive.  If not provided, one will be randomly selected.

#### Output Example
```json
{
    "status": 1,
    "time": 1526416984,
    "response": {
        "items": [
            {
                "id": 29,
                "sku": 20,
                "wear": 0.6879568,
                "pattern_index": 864,
                "preview_urls": null,
                "eth_inspect": null,
                "wear_tier": "Battle-Scarred",
                "name": "AK-47 | Case Hardened",
                "category": "Classified Rifle",
                "color": "D2D2D2",
                "image": "https://vgo.gg/img/item/sku+wear_tier",
                "suggested_price": 1099
            }
        ]
    }
}
```


## GetWearTierMapping (v1)

`GET http://api.vgo.gg/IItem/GetWearTierMapping/v1?key=z`

#### The output for this endpoint will always be the same, the values will never change.

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


## GetItemsById (v1)


#### Input Descriptions

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
item_id| int-csv | - | item id filter, separated with comma

#### Output Example

```json
{
    "status": 1,
    "time": 1526930137,
    "response": {
        "items": [
            {
                "id": "61",
                "sku": "20",
                "wear": "0.88152909278869630",
                "pattern_index": "596",
                "fast_field_inspection_id": null,
                "full_field_inspection_id": null,
                "eth_txn": null,
                "create_time": "1526913466",
                "flags": "0"
            },
            {
                "id": "62",
                "sku": "20",
                "wear": "0.94740200042724610",
                "pattern_index": "42",
                "fast_field_inspection_id": null,
                "full_field_inspection_id": null,
                "eth_txn": null,
                "create_time": "1526913467",
                "flags": "0"
            }
        ]
    }
}
```
