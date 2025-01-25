```mermaid
erDiagram

   PRODUCT{
    string item
    string model
    string ShoeLine
    string SKU FK
    string description
    float percentOFF
   }
CUSTOMER ||--o{ SALE : places
   CUSTOMER{
    string firstName
    string lastName
    string phone_num PK
   }
SALE }|--|{ PRODUCT : contains
SALE ||--o{INVENTORY : changes
   SALE{
    string SALEnum
    float percentOFF
    string location
    string payment_method
   }
INVENTORY ||--|{ PRODUCT : contains
   INVENTORY{
    int quantity
    int PricePerUnit
    int Returns
    string SKU FK
   }
```

|Entity     |Description     |
| --- | --- |
|PRODUCT   | The product being sold to the customer    |
|CUSTOMER| The customer that buys the products  |
|SALE| The transaction bewteen the business and the customer, the exchange of the products for money|
|INVENTORY| What the business has stored |


|Relationship     |Description     | Significance | 
| --- | --- | --- |
|PRODUCT <=> SALE     | The      | |
|PRODUCT <=> INVENTORY     |     | |
|CUSTOMER <=> SALE| |  |
|SALE <=> INVENTORY| |  |    




