# 空白發票號上傳

若透過e首發票取得發票號，亦透過e首發票協助上傳空白發票號\(未使用\)。

### 範例格式\(單筆為例\)

```
{
     "HeadBan":"12345678",
     "BranchBan":"12345678",
     "InvoiceType":"07",
     "YearMonth":"10706",
     "InvoiceTrack":"AA",
     "Items":[{
       "InvoiceBeginNo":"12340005",         
      "InvoiceEndNo":"12340003"
     },
     {
       "InvoiceBeginNo":"12340002",         
      "InvoiceEndNo":"12340003"
     },
     {
       "InvoiceBeginNo":"12340002",         
      "InvoiceEndNo":"12340003"
     }]
}
```

### 欄位說明

* HeadBan: 總公司統編\(必須為e首發票客戶\)
* BranchBan: 分公司統編\(必須為e首發票客戶\) 說明:無分公司則與總公司相同
* InvoiceType: 發票類型: 07:一般稅率電子發票 08:特種稅率電子發票
* YearMonth: 發票期別: 民國年+偶數月份 yyyMM; 例如 10608 表示106年 07-08 當期
* InvoiceTrack: 字軌
* Items: 空白發票號組(在同期同字軌可以多組空白號)
* InvoiceBeginNo: 空白號區間起始號
* InvoiceEndNo: 空白號區間結束號 (若為單一號碼則與空白號區間起始號相同)

<font color:"red">
注意事項:
分公司若要由總公司代上傳空白發票號必須經過申請。
</font>

### 回傳值

```
[
    {
        "HeadBan": "12345678",
        "BranchBan": "12345678",
        "InvoiceType": "07",
        "YearMonth": "10706",
        "InvoiceTrack": "AA",
        "Items": [
            {
                "InvoiceBeginNo": "12340005",
                "InvoiceEndNo": "12340003",
                "Message": "發票迄號必須大於或等於起號",
                "Status": "E"
            },
            {
                "InvoiceBeginNo": "12340002",
                "InvoiceEndNo": "12340003",
                "Message": "空白發票新增失敗，請確認是否有輸入相同區間",
                "Status": "E"
            },
            {
                "InvoiceBeginNo": "12340002",
                "InvoiceEndNo": "12340003",
                "Message": "空白發票新增失敗，請確認是否有輸入相同區間",
                "Status": "E"
            }
        ]
    }
]
```



