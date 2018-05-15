## ITrade

Endpoints which allow users to trade items between VGo accounts via their On-Site Inventories.
- [ITrade/AcceptOffer](ITrade/AcceptOffer)
- [ITrade/CancelOffer](ITrade/CancelOffer)
- [ITrade/GetOffer](ITrade/GetOffer)
- [ITrade/GetOffers](ITrade/GetOffers)
- [ITrade/GetTradeUrl](ITrade/GetTradeUrl)
- [ITrade/GetUserInventory](ITrade/GetUserInventory)
- [ITrade/GetUserInventoryFromSteamId](ITrade/GetUserInventoryFromSteamId)
- [ITrade/RegenerateTradeUrl](ITrade/RegenerateTradeUrl)
- [ITrade/SendOffer](ITrade/SendOffer)
- [ITrade/SendOfferToSteamId](ITrade/SendOfferToSteamId)


### Offer states constants:
- STATE_ACTIVE = 2;                             /** The offer is active and the recipient can accept it to exchange the items */
- STATE_ACCEPTED = 3;                           /** The recipient accepted the offer and items were exchanged */
- STATE_EXPIRED = 5;                            /** The offer expired from inactivity */
- STATE_CANCELED = 6;                           /** The sender canceled the offer */
- STATE_DECLINED = 7;                           /** The recipient declined the offer */
- STATE_INVALID_ITEMS = 8;                      /** One of the items in the offer is no longer available/eligible so the offer was canceled automatically */