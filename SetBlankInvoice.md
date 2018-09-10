# Update the blank invoice number

If the invoice number is obtained by e-Invoice,the e-Invoice would help upload blank invoice number \(not used\).

### Exmple for Single Data

```
{"CompanyID":"89430377","Word":"FF","StageYear":"2016","StageMonth":"12","StartNumber":"00000000","EndNumber":"00000499","NextNumber":"00000412"}
```

### Field Description

* CompanyID: Seller's Company Tax ID \(Must be the e-Invoice customer\)
* Word: Invoice Track
* StageYear: Year of Invoice Period. yyyy: 2016
* StageMonth: Even Month of Invoice Period; 例如 11-12月，就填 12
* StartNumber: the start number of the period
* EndNumber: the last number of the period
* NextNumber: the next use number of the period. If use finished, it will be equivalent to the end number. Such as the creating of the last one for is 00000411, then the next number is 00000412

### Return Value

```
[
    {
        "ErrorMessage": null,                 //Error Message
        "COMPANY_ID": "89430377",             //Company Tax ID
        "YearMonth": "10512",                 //Year of the Republic and Period (Even Month)
        "InvoiceWord": "FF",                  //Invoice Track
        "BlankInvoiceBeginNo": "00000412",    //Blank Invoice Start Number
        "BlankInvoiceEndNo": "00000499"       //Blank Invoice End Number
    }
]
```



