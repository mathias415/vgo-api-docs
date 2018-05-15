# API Interfaces

* [IAuth](IAuth)
* [ICase](ICase) - all VGo keys and VGo cases stuff
* [ICaseSite](ICaseSite) - All endpoints that a vcase website needs to use, except creating their initial user.
* [IItem](IItem)
* [ISecurity](ISecurity)
* [ITest](ITest)
* [ITrade](ITrade) - p2p trading
* [IUser](IUser)

## VGo Item Standard Output
TBD

## OpenedCase standard output

```json
{
  "id": 1,
  "status": 3,
  "status_text": "Opened",
  "case_id": 1,
  "case_site_trade_offer_id": null,
  "item": (Item Object)
}
```
```
    const STATE_ERROR = 1;
    const STATE_PENDING = 2;
    const STATE_OPENED = 3;
```
