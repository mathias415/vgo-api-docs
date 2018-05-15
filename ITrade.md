## ITrade

Endpoints which allow users to trade items between VGo accounts via their On-Site Inventories.
- [ITrade/AcceptOffer](ITrade/AcceptOffer.md)
- [ITrade/CancelOffer](ITrade/CancelOffer.md)
- [ITrade/GetOffer](ITrade/GetOffer.md)
- [ITrade/GetOffers](ITrade/GetOffers.md)
- [ITrade/GetTradeUrl](ITrade/GetTradeUrl.md)
- [ITrade/GetUserInventory](ITrade/GetUserInventory.md)
- [ITrade/GetUserInventoryFromSteamId](ITrade/GetUserInventoryFromSteamId.md)
- [ITrade/RegenerateTradeUrl](ITrade/RegenerateTradeUrl.md)
- [ITrade/SendOffer](ITrade/SendOffer.md)
- [ITrade/SendOfferToSteamId](ITrade/SendOfferToSteamId.md)


### Offer states constants:
- STATE_ACTIVE = 2;                             /** The offer is active and the recipient can accept it to exchange the items */
- STATE_ACCEPTED = 3;                           /** The recipient accepted the offer and items were exchanged */
- STATE_EXPIRED = 5;                            /** The offer expired from inactivity */
- STATE_CANCELED = 6;                           /** The sender canceled the offer */
- STATE_DECLINED = 7;                           /** The recipient declined the offer */
- STATE_INVALID_ITEMS = 8;                      /** One of the items in the offer is no longer available/eligible so the offer was canceled automatically */
