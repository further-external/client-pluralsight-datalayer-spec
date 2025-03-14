# Checkout Started

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Checkout Started",
    "product": [
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
                "sellingPrice": "<sellingPrice>",
                "sku": "<sku>"
            }
        }
    ]
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|product[n].productInfo.billingCycle|string|String set to the user selected billing cycle selection within the b2b cart. \(B2B ONLY\)|Quarterly, Yearly|||||||
|product[n].productInfo.class|string|String representation of the class of the product within the shopping cart. This is being calculated off of the|b2b, b2c|||||||
|product[n].productInfo.duration|string|String representation of the billing duration of the product within the shopping cart|annual, monthly|||||||
|product[n].productInfo.gift|string|String set to yes or no to define if a product is being purchased as a gift or not|"true", "false"|||||||
|product[n].productInfo.listPrice|string|String representation of the price paid prior to coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|||||||
|product[n].productInfo.marketingID|string|String representation of the friendly readable product identifier. Identified as "marketing\_id" within the product catalog.|AI-PLUS-DATA, EVERY-NEW-B2B-A, CL-M-PLUS-FT|||||||
|product[n].productInfo.name|string|Name of the product or offering. Should be unique and 1:1 with productID|Core Tech \(Annual\), Data+ Free Trial \(converts to Annual\), Security + Cloud \(Pilot\)|||||||
|product[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|product[n].productInfo.promo|string|String of the promo code as applied in the shopping cart \(if applicable\)|25FEB30OFFYRCT|||||||
|product[n].productInfo.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|||||||
|product[n].productInfo.sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||




