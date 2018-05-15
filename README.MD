# API Interfaces

* [IAuth](IAuth.md)
* [ICase](ICase.md) - all VGo keys and VGo cases stuff
* [ICaseSite](ICaseSite.md) - All endpoints that a vcase website needs to use, except creating their initial user.
* [IItem](IItem.md)
* [ITest](ITest.md)
* [ITrade](ITrade.md) - p2p trading
* [IUser](IUser.md)

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
