# Purpose of the Verba Volant Scripta Manent (VVSM)

VVSM is just a POC of how a distributed app (dapp) running on the Tezos Virtual Machine (TVM) can store securely and consistently with the flexibility required by business users.

In this case we will build a periodic maintenance book where we will record a vehicle maintenance history

The features of VVSM will be as follow:

### MVP:
* The contract will contain data structures called _Items_, which will contain information concerning the represented _item_ (e.g.: A motorcycle or other vehicle)
* The contract will contain informations regarding ownership of the _items_ (_Items_ will be owned by _Owners_)
* _Owners_ will be able to subscribe to the smart contract
* The item will have a history of _events_, that may contain a string or a number as value and will have a timestamp of when they were inserted
* No history _event_ will be deletable
* No Item will be deletable
* _Items_ ownership will be transferable
* Only an _Item owner_ will be able to add an _Event_ to an owned _item_, and only with a valid subscription

### Possible further features:
* Enrich _item_'s info with a picture
* Encrypt _Owners_ information
* Add special data structures for service points, that are able to add events to an Item wothout being owners of said items
* Make _Service points_ able to edit an _Item_ only after the _Item's Owner_ has given them access to the item history
* Allow private _Items/history_ visible only to _Owners_ and authorized _Service points_
* Regulate an _Item_ transfer in exchange of money, having the smart contract act as Escrow
  * Taxes/fees?