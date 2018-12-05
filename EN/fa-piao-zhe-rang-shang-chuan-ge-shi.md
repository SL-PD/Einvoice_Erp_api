# Discount Invoice Upload Format

### Example

```
{
  "AllowanceNumberPrefix": "2017061314",
  "SellerID": "12345678",
  "BuyerID": "87654321",
  "AllowanceType": "2",
  "TaxAmount": 40,
  "TotalAmount": 800,
  "Details": [
    {
      "InvoiceNumber": "AA12345678",
      "SequenceNumber": "003",
      "Amount": 300,
      "Quantity": 1,
      "UnitPrice": 300,
      "Tax": 15
    },
    {
      "InvoiceNumber": "AA12345678",
      "SequenceNumber": "005",
      "Amount": 500,
      "Quantity": 2,
      "UnitPrice": 250,
      "Tax": 25
    }
  ]
}
```

### Description

#### Discount Invoice Header

* AllowanceNumberPrefix: Prefix discount number\(Suggest no more than 10 chars\)
* SellerID: Seller's company tax ID\(Must be the e-Invoice customer\)
* BuyerID: Buyer's company tax ID
* AllowanceType: Discount type: The default code is 2; Code Description 1. (Buyer uploads a discount) 2. (Seller uploads a discount)
* TaxAmount: Discounted amount of tax
* TotalAmount: Discounted amount of no tax
* Details: Discounted invoice details

#### Discount Invoice Detail
* InvoiceNumber: Discount invoice number
* SequenceNumber: the original serial number of the discount invoice
* Amount: Discount amount
* Quantity: Discount quantity
* UnitPrice: Discounted unit price of no tax
* Tax: Discounted tax



