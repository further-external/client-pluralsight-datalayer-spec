# Checkout Complete

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Checkout Complete",
    "transaction": {
        "country":"<country>",
        "currency": "<currency>",
        "invoiceID": "<invoiceID>",
        "item": [
            {
                "productInfo": {
                    "billingCycle": "<billingCycle>",
                    "class": "<class>",
                    "duration": "<duration>",
                    "gift": "<gift>",
                    "listPrice": "<listPrice>",
                    "marketingID": "<marketingID>",
                    "name": "<name>",
                    "productID": "<productID>",
                    "promo": "<promo>",
                    "quantity": <quantity>,
                    "sellingPrice": "<sellingPrice>",
                    "sku": "<sku>",
                    "trial": "<trial>"
                }
            }
        ],
        "paymentMethod":"<paymentMethod>",
        "orderTotal": "<orderTotal>",
        "subscriptionID": "<subscriptionID>",
        "transactionID": "<transactionID>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|transaction.country|string|String set to the user selected country value within the account details step|United States, India, Ireland|||||||
|transaction.currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase|USD, CAD, GBP, CHF|||||||
|transaction.invoiceID|string|String set to the invoiceID that is created during the digital cart checkout|8a8aa38094df9b9a0194e0e624561594|||||||
|transaction.item[n].productInfo.billingCycle|string|String set to the user selected billing cycle selection within the b2b cart. \(B2B ONLY\)|String set to the user selected billing cycle selection within the b2b cart. \(B2B ONLY\)|||||||
|transaction.item[n].productInfo.class|string|String representation of the class of the product within the shopping cart.|b2b, b2c|||||||
|transaction.item[n].productInfo.duration|string|String representation of the billing duration of the product within the shopping cart|annual, monthly|||||||
|transaction.item[n].productInfo.gift|string|String set to yes or no to define if a product is being purchased as a gift or not|"true","false"|||||||
|transaction.item[n].productInfo.listPrice|string|String representation of the price paid prior to coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|||||||
|transaction.item[n].productInfo.marketingID|string|String representation of the friendly readable product identifier. Identified as "marketing\_id" within the product catalog.|AI-PLUS-DATA, EVERY-NEW-B2B-A, CL-M-PLUS-FT|||||||
|transaction.item[n].productInfo.name|string|Name of the product or offering. Should be unique and 1:1 with productID|Core Tech \(Annual\), Data+ Free Trial \(converts to Annual\), Security + Cloud \(Pilot\)|||||||
|transaction.item[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|transaction.item[n].productInfo.promo|string|String of the promo code as applied in the shopping cart \(if applicable\)|25FEB30OFFYRCT|||||||
|transaction.item[n].productInfo.quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\). For B2B this value will reflect the quantity of seats selected during checkout and for b2c the value will reflect the number of products in cart.|1, 2, 5, 10, 50|||||||
|transaction.item[n].productInfo.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|||||||
|transaction.item[n].productInfo.sku|string|This is referenced as the legacy\_product\_sku in the product catalog|SECURITY-PLUS-CL, AI-PLUS, IND-EVERYTHING|||||||
|transaction.item[n].productInfo.trial|string|String set to yes or no to define if a product is being purchased as a trial or not|"true", "false"|||||||
|transaction.paymentMethod|string|Describes the payment method selected at the time of checkout|Credit Card,paypal,ACH Direct debit|||||||
|transaction.orderTotal|string|The value of total services purchased|200, 29.99, 50, 0|||||||
|transaction.subscriptionID|string|String set to the subscriptionID that is created during the digital cart checkout|b8307d2582594df9b7a4e0e622dc0109|||||||
|transaction.transactionID|string|Unique identifier of the transaction. Max Length 100. Used as a key for upload of post transaction data. |123e4567-e89b-12d3-a456-426614174000|^[a-zA-Z0-9]{6,100}$|6|100||||




