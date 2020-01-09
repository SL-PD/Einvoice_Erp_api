# API 資料傳送格式:

注意:上傳已開立發票前，需要先與業務人員**確認帳號已建立完成**，並取得**專屬加密Salt**一組，以便後續上傳作業之進行。

### 測試區URL

```
(2019-02-22 之後)
https://webapi.systemlead.com/terpapi
```

### 範例格式
傳送資料格式說明以單筆資料Josn為例。

```
{
	"CompanyID":"89430377",
	"Timestamp":"1477585655",
	"Signature":"89C480C1E4ACD1FD06C08D364404D74C014EEEDCDD8FE026EA2018B311A96D16",
	"Data":{[傳送資料]}
}
```

傳送資料格式說明以多筆資料Josn為例。

```
[
	{
		"CompanyID":"89430377",
		"Timestamp":"1477585655",
		"Signature":"89C480C1E4ACD1FD06C08D364404D74C014EEEDCDD8FE026EA2018B311A96D16",
		"Data":{[傳送資料1]}
	},
	{
		"CompanyID":"89430377",
		"Timestamp":"1477585655",
		"Signature":"89C480C1E4ACD1FD06C08D364404D74C014EEEDCDD8FE026EA2018B311A96D16",
		"Data":{[傳送資料2]}
	},

]
```
<font color="red">*注意:傳送資料都需要被包裹API傳送格式內。</font>

### 欄位格式說明
|欄位名稱|欄位說明|欄位型態|欄位長度|條件說明|
|--:|--|--|--|--|
|CompanyID|賣方公司統一編號|Char|8|須為e首發票商家|
|Timestamp|時間戳記|String||相關轉換請參考 [[http://www.epochconverter.com/](http://www.epochconverter.com/)]|
|Signature|簽章驗證值|String||產生方法可參閱[簽章驗證碼](https://slproject.gitbook.io/sl-einv-project/cht/signature)說明|
|Data|傳送資料|String||產生方法可參閱[e首發票API清單](https://slproject.gitbook.io/sl-einv-project/cht/invoiceapilist)中各API的格式說明|












