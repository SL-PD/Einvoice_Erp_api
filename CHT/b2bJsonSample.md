B2B存證發票範本

```
{
     "CompanyID":"89430377",
     "InvoiceID":"AA12345678",
     "InvoiceDateTime":"2016-10-27T16:27:34",
     "InvoiceFor":"B",
     "BuyerID":"26089959",
     "BuyerInvoiceTitle":"矽聯科技股份有限公司南區營業所"
     "BuyerName":"Nestor Huang",
     "BuyerTelNo":"077190888",         
     "BuyerAddress":"高雄市鳳山區光遠路226號B1",         
     "BuyerEmail":"nestor@systemlead.com",
     "CheckNumber":"8943",
     "RelateNumber":"OD2017032801",
     "PrintMark":"N",
     "TaxType":"1",
     "SalesAmount":5238,
     "TaxAmount":262,
     "TotalAmount":5500,
     "Details":[
         {
             "DetailID":"001",
             "ProductID":"P1234",
             "ProductName":"產品名稱",
             "Quantity":5.0,
             "UnitPrice":95.238,
             "SubTotal":476.19
         },
         {
             "DetailID":"002",
             "ProductID":"P2345",
             "ProductName":"長度256個字",
             "Quantity":2.0,
             "UnitPrice":476.1904,
             "SubTotal":952.3808
         },
         {
             "DetailID":"003",
             "ProductID":"P3456",
             "ProductName":"明細編號3碼",
             "Quantity":4.0,
             "UnitPrice":952.3809,
             "SubTotal":3809.5236,
             "Remark":"貨品缺1件候補"
         }]
}
```

回傳結果範例：

```
[
  { // 成功上傳
    "InvoiceID":"CA89430015",
    "InvoiceDateTime":"2017-06-12T12:34:56",
    "AuthCode":"113B2C2E-81E3-41B5-B77F-656598B8BAEF"
  },
  { // 上傳失敗
    "InvoiceID":"CA89430016",
    "InvoiceDateTime":"2017-06-12T12:34:34",,
    "Message":,"Append Inovice Error!!"
  },
  { // 驗證錯誤
    "InvoiceID":"CA89430017",
    "InvoiceDateTime":"2017-06-12T12:34:34",,
    "Message":,"簽章驗證錯誤"  
  }
]
```



