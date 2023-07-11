# Get support city pairs

According to the document each company will have specific fares. So before searching flights we have to figure out which agency the user who making request belong to.

**URL** : `api/agencies`

**Method** : `GET`

**Auth required** : Yes

**Permissions required** : ?

**Support for** : ?

## Success Response

**Code** : `200 OK`

**Content examples**

The content example below is copy exactly from document. But I can't understanding why they return a list of agencies. I guess, maybe one user can belong to many agencies at the same time.

> **_NOTE:_**  `agencyAccount.company.key` is the company key that will be using in the request params of get travel options api.

```json
[
  {
    "href": "https://vietjet-api.intelisystraining.ca/RESTv1/agencies/BvNQq3NaJxlsd3QTXIF%C6%92CPjY3PX3CV2%C6%92joj%C6%92hZK1VyI=",
    "key": "BvNQq3NaJxlsd3QTXIFƒCPjY3PX3CV2ƒjojƒhZK1VyI=",
    "agencyType": {
      "href": "https://vietjet-api.intelisystraining.ca/RESTv1/agencyTypes/gA4c%C6%92Qh4VvgOUqQX0%C2%A57Wc5gBHpmBPOG%C6%92WJlhgrW9s4s=",
      "key": "gA4cƒQh4VvgOUqQX0¥7Wc5gBHpmBPOGƒWJlhgrW9s4s=",
      "name": "API AGENCY",
      "identifier": null,
      "prePaid": null,
      "protected": null,
      "timestamp": null
    },
    "iataNumber": "34000012",
    "name": "GOBUDGETTAIR.COM PTE LTD",
    "status": {
      "active": true,
      "inactive": false,
      "denied": null,
      "historical": null,
      "pending": null
    },
    "masterParentAgency": null,
    "directParentAgency": null,
    "specifiedTaxConfiguration": {
      "overridden": false,
      "taxConfiguration": null
    },
    "address": {
      "address1": "",
      "address2": "",
      "city": "",
      "location": {
        "country": {
          "href": "https://vietjet-api.intelisystraining.ca/RESTv1/countries/NA",
          "code": "NA",
          "name": "NA",
          "provinces": null,
          "timestamp": null
        },
        "province": {
          "href": "https://vietjet-api.intelisystraining.ca/RESTv1/countries/NA/provinces/NA",
          "code": "NA",
          "name": "NA",
          "timestamp": null
        }
      },
      "postalCode": "       "
    },
    "contactInformation": {
      "name": null,
      "phoneNumber": "",
      "mobileNumber": null,
      "faxNumber": "",
      "extension": null,
      "email": ""
    },
    "notes": "MR HUAN ICT RQS TAO NGAY 19JUL17-LOAN",
    "markupCommission": null,
    "specifiedHoldTime": {
      "overridden": false,
      "holdTime": null
    },
    "specifiedGroupBookingCount": {
      "overridden": false,
      "groupBookingCount": null
    },
    "agencyAccount": {
      "key": "Ivig1gKzil3UmXOgsxyuvnJkTtWNG3gvrclIuNQAm10=",
      "agencyAccount": true,
      "gdsAccount": false,
      "company": {
        "href": "https://vietjet-api.intelisystraining.ca/RESTv1/companies/gnt6BDjgabZCjtIaspQrFIHHPScEOLoWn3bHu%C2%A54jGYo=",
        "key": "gnt6BDjgabZCjtIaspQrFIHHPScEOLoWn3bHu¥4jGYo=",
        "identifier": null,
        "name": null,
        "status": null,
        "specifiedTaxConfiguration": null,
        "taxLicense1": null,
        "taxLicense2": null,
        "purchaseOrderRequired": null,
        "address": null,
        "contactInformation": null,
        "notes": null,
        "account": {
          "accountNumber": "34000012",
          "creditLimit": 0,
          "creditAvailable": 7000261297.36,
          "currency": {
            "href": "https://vietjet-api.intelisystraining.ca/RESTv1/currencies/USD",
            "code": "USD",
            "description": "US Dollar",
            "baseCurrency": false,
            "currentExchangeRate": 0,
            "format": null
          }
        },
        "startDate": null,
        "endDate": null,
        "lastInvoiceDate": null,
        "privateFares": null,
        "timestamp": null
      }
    },
    "gdsAccount": null,
    "timestamp": null
  }
]
```

## References

1. [https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query](https://support.vietjetair.com/en/blog/getting-the-required-information-for-the-travel-options-query)