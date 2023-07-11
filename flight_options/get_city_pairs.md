# Get support city pairs

As I understanding viet jet air only support a limit city pairs. So whenerver we search flights we have to provide a valid pairs (ex: SGN-HAN).

**URL** : `api/CityPairs`

**Method** : `GET`

**Auth required** : ?

**Permissions required** : ?

**Support for** : ?

## Success Response

**Code** : `200 OK`

**Content examples**

As you can see the example content is a little different from official viet jet air [document](https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query). It is logical to return a list of city pairs instead of an city pairs object.

```json
[
  {
    "href": "https://vietjet-api.intelisystraining.ca/RESTv1/cityPairs/SGN-HAN",
    "identifier": "SGN-HAN",
    "departure": {
        "airport": {
        "href": "https://vietjet-api.intelisystraining.ca/RESTv1/airports/SGN",
        "code": "SGN",
        "name": "Ho Chi Minh",
        "latitude": null,
        "longitude": null,
        "timezone": null,
        "utcOffset": null,
        "secure": null
        }
    },
    "arrival": {
        "airport": {
        "href": "https://vietjet-api.intelisystraining.ca/RESTv1/airports/HAN",
        "code": "HAN",
        "name": "Ha Noi",
        "latitude": null,
        "longitude": null,
        "timezone": null,
        "utcOffset": null,
        "secure": null
        }
    },
    "validConnectionAirports": null,
    "fareStatuses": null,
    "chargeStatuses": null,
    "taxConfiguration": null,
    "loyaltyPointsEarned": 0,
    "groupBookingCount": null,
    "routeType": null,
    "travelOptionCriteria": null,
    "fares": null,
    "charges": null,
    "timestamp": null
  },
  ...
]
```

## References

1. [https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query](https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query)