# 發票折讓上傳格式

### 範例格式

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

### 欄位說明

#### 折讓單頭

* AllowanceNumberPrefix: 折讓單號的前置碼\(建議不超過10碼\)
* SellerID: 賣方統編\(必須為e首發票客戶\)
* BuyerID: 買方統編
* AllowanceType: 折讓類型: 預設為2; 1.\(買方上傳折讓\) 2.\(賣方上傳折讓\)
* TaxAmount: 折讓稅額合計
* TotalAmount: 折讓未稅金額合計
* Details: 折讓發票明細
  #### 折讓單身
* InvoiceNumber: 折讓發票號
* SequenceNumber: 折讓發票原始序號
* Amount: 折讓金額
* Quantity: 折讓數量
* UnitPrice: 折讓未稅單價
* Tax: 折讓稅額



