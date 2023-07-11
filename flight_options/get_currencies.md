# Get support city pairs

// Todo: Add more description.
Retrieves a list of the currently configured currencies.

**URL** : `api/currencies`

**Method** : `GET`

**Auth required** : ?

**Permissions required** : ?

**Support for** : ?

## Success Response

**Code** : `200 OK`

**Content examples**

As you can see the example content is a little different from official viet jet air [document](https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query). It is logical to return a list of currencies instead of an currency object.

```json
[
    {
    "href": "https://vietjet-api.intelisystraining.ca/RESTv1/currencies/VND",
    "code": "VND",
    "description": "Vietnam Dong",
    "baseCurrency": true,
    "currentExchangeRate": 1,
    "format": "#,##0 VND"
    },
    ...
]
```

## References

1. [https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query](https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query)