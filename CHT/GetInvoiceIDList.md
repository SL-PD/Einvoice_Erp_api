# 查詢發票字軌與期號

此功能僅提供查詢客戶授權e首發票下載之發票字軌及期號

### 查詢範例格式:

```
[{ //正確查詢
  "CompanyID":"12345678",
  "Timestamp":"1496339450",
  "Signature":"FC6EB21ECDBCC95682450BC376C88C100A6ED7D01925BA9B93FCAA1F5D560606",
  "Data":
  {
     "CompanyID":"12345678",
     "StageYear":"2017"
	}
},
{ //查無資訊
  "CompanyID":"12345678",
  "Timestamp":"1496339450",
  "Signature":"FC6EB21ECDBCC95682450BC376C88C100A6ED7D01925BA9B93FCAA1F5D560606",
  "Data":
  {
     "CompanyID":"34567890",
     "StageYear":"2017",
     "StageMonth":"8"
	}
},
{ //簽章驗證錯誤
  "CompanyID":"12345678",
  "Timestamp":"1496339450",
  "Signature":"FC6EB21ECDBCC95682450BC376C88C100A6ED7D01925BA9B93FCAA1F5D560607",
  "Data":
  {
     "CompanyID":"34567890",
     "StageYear":"2017"
	}
}]
```

#### 查詢單一期別

```
{"CompanyID":"12345678","StageYear":"2017","StageMonth":"2"}
```

#### 查詢一整年度

```
{"CompanyID":"12345678","StageYear":"2017"}
```

### 欄位說明:

* CompanyID: 賣方統編\(必須為e首發票客戶\)
* StageYear: 查詢年度
* StageMonth: 查詢期別\(偶數月\)

### 回覆範例值

```
[{ //正確查詢
 "IDList": [
            {
                "IDKey": "1234567810606HC1234000000",
                "CompanyID": "12345678",
                "Word": "HC",
                "StageYear": "2017",
                "StageMonth": 6,
                "BeginNumber": "12340000",
                "EndNumber": "12349999"
                "Details": [
                    {
                        "Code": "01",
                        "StartNumber": "12340000",
                        "EndNumber": "12342999",
                        "CurrentNumber": "12340000",
                        "SplitBooklet": 60,
                        "BeginBooklet": 1,
                        "EndBooklet": 60,
                        "InvoiceCount": 3000,
                        "LastUseDate": NULL,
                        "RowStatus": "A",
                        "UseFor": "U1",
                        "Note": ""
                    },
                    {
                        "Code": "02",
                        "StartNumber": "12343000",
                        "EndNumber": "12344999",
                        "CurrentNumber": "12340000",
                        "SplitBooklet": 40,
                        "BeginBooklet": 61,
                        "EndBooklet": 100,
                        "InvoiceCount": 2000,
                        "LastUseDate": NULL,
                        "RowStatus": "A",
                        "UseFor": "U1",
                        "Note": ""
                    }
                ]
            }
        ],
        "CompanyID": "12345678",
        "StageYear": "2017"
    },
    { //查無資訊
        "IDList": [],
        "CompanyID": "34567890",
        "StageYear": "2017",
        "StageMonth": "8"
    },
    { //簽章驗證錯誤
        "Message": "簽章驗證錯誤",
        "CompanyID": "34567890",
        "StageYear": "2017"
    }
]
```


