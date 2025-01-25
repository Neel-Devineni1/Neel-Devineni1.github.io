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
SALE ||--|{ PRODUCT : contains
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

| Entity      | Description |
| ----------- | ----------- |
| PRODUCT     | Title       |
| CUSTOMER    | Text        |
| SALE        | Title       |
| INVENTORY   | Title       |

| RELATIONSHIP      | Description |
| ----------------- | ----------- |
| PRODUCT            | Title       |
| CUSTOMER           | Text        |
| SALE               | Title       |
| INVENTORY          | Title       |