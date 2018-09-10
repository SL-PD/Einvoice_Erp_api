# 空白發票號上傳

若透過e首發票取得發票號，亦透過e首發票協助上傳空白發票號\(未使用\)。

### 範例格式\(單筆為例\)

```
{"CompanyID":"89430377","Word":"FF","StageYear":"2016","StageMonth":"12","StartNumber":"00000000","EndNumber":"00000499","NextNumber":"00000412"}
```

### 欄位說明

* CompanyID: 賣方統編\(必須為e首發票客戶\)
* Word: 發票字軌
* StageYear: 發票期別年度 yyyy; 例如 2016
* StageMonth: 發票期別偶數月; 例如 11-12月，就填 12
* StartNumber: 發票該期起始號碼
* EndNumber: 發票該期結束號碼
* NextNumber: 發票該期下一個使用號，如使用完畢就會等同於結束號; 例如開立出去的最後一號為 00000411 ,則 NextNumber設定為 00000412

### 回傳值

```
[
    {
        "ErrorMessage": null,                 //錯誤訊息
        "CompanyID": "89430377",             //公司統編
        "YearMonth": "10512",                 //民國年度與期別
        "InvoiceWord": "FF",                  //發票字軌
        "BlankInvoiceBeginNo": "00000412",    //空白發票起始號
        "BlankInvoiceEndNo": "00000499"       //空白發票結束號
    }
]
```



