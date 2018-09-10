# Inquiry authorization invoice track and period number

This feature only provides the invoice track and period number for which the customer is authorized to download

### Query the sample format:

```
[{ //Correctly query
  "CompanyID":"12345678",
  "Timestamp":"1496339450",
  "Signature":"FC6EB21ECDBCC95682450BC376C88C100A6ED7D01925BA9B93FCAA1F5D560606",
  "Data":
  {
     "CompanyID":"12345678",
     "StageYear":"2017"
    }
},
{ //No information available
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
{ //Signature verification error
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

#### Query a single period

```
{"CompanyID":"12345678","StageYear":"2017","StageMonth":"2"}
```

#### Query the whole year

```
{"CompanyID":"12345678","StageYear":"2017"}
```

### Field Description:

* CompanyID: Seller's Company Tax ID \(Must be the e-Invoice customer\)
* StageYear: Query year
* StageMonth: Query period \(even months\)

### Reply values

```
[{ //Correctly query
 "IDList": [
            {
                "IDKey": "1234567810606HC1234000000",
                "CompanyID": "12345678",
                "Word": "HC",
                "StageYear": "2017",
                "StageMonth": 6,
                "BeginNumber": "12340000",
                "EndNumber": "12349999"
            }
        ],
        "CompanyID": "12345678",
        "StageYear": "2017"
    },
    { //No information available
        "IDList": [],
        "CompanyID": "34567890",
        "StageYear": "2017",
        "StageMonth": "8"
    },
    { //Signature verification error
        "Message": "簽章驗證錯誤",
        "CompanyID": "34567890",
        "StageYear": "2017"
    }
]
```