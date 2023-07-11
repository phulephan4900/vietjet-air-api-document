# Get travel options

Similar to search flights

**URL** : `api/travelOptions`

**URL Parameters** : 

* `cityPair`: Describe the departure and return point. Example: `cityPair=SGN-HAN`
* `departure`: Departure date. Example: `departure=2021-07-28`
* `cabinClass`: Cabin class code. Example: `cabinClass=Y`
* `currency`: Currency code. Example: `currency=VND`
* `adultCount`: Number of adult. Example: `adultCount=1`
* `childCount`: Number of child. Example: `childCount=1`
* `infantCount`: Number of infant. Example: `infantCount=1`
* `return`: Return date. An optional param need when we search travel options for return way. Example: `return=2021-07-30`
* `promoCode`: Promo code, An optional param. Example: `paromoCode=R@ND0MC0D3`
* `companyKey`: Company key related to user that making get travel options (view [Get agencies document](flight_options/agencies.md) for more detail). Example: `companyKey=gnt6BDjgabZCjtIaspQrFIHHPScEOLoWn3bHu%C2%A54jGYo=`

**Method** : `GET`

**Auth required** : Yes

**Permissions required** : ?

## Success Response

**Code** : `200 OK`

**Content examples**

For the sake of simplicity. I have reomved some part but you can view the detail of example response [here](https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query).

The travel options response can potentially be quite large. Each travel option will show basic flight information in the top portion of the response. This will include city pair, flight, and aircraft information. This is followed by the 'fareOptions' portion of the response. This is the portion that contains the information related to booking including applicable charges, fare class information, availability, seat assignment and tax configuration information. The most important piece being the booking key which will be used in the booking request.

The last portion displays promo code information if applicable.
```json
[
    {
    "href": "https://vietjet-api.intelisystraining.ca/RESTv1/travelOptions/KthFU7X4iyUCm6BcvXdobJW%C2%A5QUXXbWvO7m4BNJh9icrNGl5AknIfAKgha6M0QakFRLqgBzqqZ16NhN56pJR5SHwEyfuy3GBlWaFk33sj0kOE4iRDNQK0QWGB1mxpLDQbHN0fikMJqgtkYXoWSIp1r94fUtK63aM9jSRa%C6%92E4XeDDklkvrAMOHHMTn8eYYs62RAmtrJKise06PIOKswXSD%C6%92Q==",
    "key": "KthFU7X4iyUCm6BcvXdobJW¥QUXXbWvO7m4BNJh9icrNGl5AknIfAKgha6M0QakFRLqgBzqqZ16NhN56pJR5SHwEyfuy3GBlWaFk33sj0kOE4iRDNQK0QWGB1mxpLDQbHN0fikMJqgtkYXoWSIp1r94fUtK63aM9jSRaƒE4XeDDklkvrAMOHHMTn8eYYs62RAmtrJKise06PIOKswXSDƒQ==",
    "cityPair": { .. },
    "departureDate": 2021-07-28,
    "enRouteHours": 2.1667,
    "numberOfStops": 1,
    "numberOfChanges": 0,
    "flights": [
        { .... },
        ...
    ]
    "fareOptions": [
        { ... },
        ...
    ]
    "promoCodeApplicability":  { ... }
    },
    ...
]
```

## References

1. [https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query](https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query)