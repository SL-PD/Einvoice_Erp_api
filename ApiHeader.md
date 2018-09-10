# API Delivery Format:

Attention: Before uploading the created invoice, need to confirm **the account has been created** with the business staff firstly. And, getting **a set of exclusive encryption salt** for subsequent upload operations.

### URL of Test Location
```
http://tserv.youshop.com.tw/
```
<font color="red"> Notice: the URL of test location will be changed in late June 2017. Related transaction will be notified by the business side。</font>

URL of New test location

```
https://teinv.systemlead.com/
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
<font color="red">*Attention:The sending data needs to be wrapped within the API delivery format。</font>

### Field Description
|Field Name|Description|Data Type|Length|Condition|
|--:|--|--|--|--|
|CompanyID|Seller's Company Tax ID|Char|8|Must be e-Invoice business|
|Timestamp|Timestamp|String||Reference: [[http://www.epochconverter.com/](http://www.epochconverter.com/)]|
|Signature|Signature verification value|String||Reference:[Signature verification code](Signature.html)|
|Data|Sendind Data|String||Reference:[e-Invoice API List](InvoiceApiList.html)|












