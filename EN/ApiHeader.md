# API Delivery Format:

Attention: Before uploading the created invoice, need to confirm **the account has been created** with the business staff firstly. And, getting **a set of exclusive encryption salt** for subsequent upload operations.

### URL of Test Location

```
(after 2019-02-22)
https://webapi.systemlead.com/terpapi
```

### Example

The sending data format description uses a single data Json as an example.

```
{
    "CompanyID":"89430377",
    "Timestamp":"1477585655",
    "Signature":"89C480C1E4ACD1FD06C08D364404D74C014EEEDCDD8FE026EA2018B311A96D16",
    "Data":{[Sending Data]}
}
```

The sending data format description uses multiple data Json as an example.

```
[
    {
        "CompanyID":"89430377",
        "Timestamp":"1477585655",
        "Signature":"89C480C1E4ACD1FD06C08D364404D74C014EEEDCDD8FE026EA2018B311A96D16",
        "Data":{[Sending Data 1]}
    },
    {
        "CompanyID":"89430377",
        "Timestamp":"1477585655",
        "Signature":"89C480C1E4ACD1FD06C08D364404D74C014EEEDCDD8FE026EA2018B311A96D16",
        "Data":{[Sending Data 2]}
    },

]
```

\*Attention:The sending data needs to be wrapped within the API delivery format。

### Field Description

| Field | Name | Description | DataType | Length | Condition |
| :--- | :--- | :--- | :--- | :--- | :--- |
|  | CompanyID | Seller's Company Tax ID | Char | 8 | Mustbee-Invoicebusiness |
|  | Timestamp | Timestamp | String |  | Reference: \[[http://www.epochconverter.com/](http://www.epochconverter.com/)\] |
|  | Signature | Signature verification value | String |  | Reference:[Signature verification code](Signature.html) |
|  | Data | SendindData | String |  | Reference:[e-Invoice API List](InvoiceApiList.html) |



