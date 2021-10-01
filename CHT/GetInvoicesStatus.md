# 查詢發票處理狀態

此處查詢處理狀態指的是發票在e首發票加值中心的最後處理作業的狀態
查詢多筆發票處理狀態 (使用 Http Post) <br />

### 範例格式：
```
{
  "CompanyID":"12345678",
  "InvoiceID":"CA89430001"
}
```
### 欄位說明
* CompanyID 公司統編
* InvoiceID 發票號碼

### 回傳格式
```
{
  "InvoiceID": "CA89430001",
  "ProcessStatus": "I9",
  "ProcessStatusMessage": "開立上傳完成"
}
```

### 回傳結果：
InvoiceID：發票號 <br />
ProcessStatus：處理狀態 <br />
ProcessStatusMessage: 處理狀態訊息 <br />

### 狀態說明
## 發票開立
|ProcessStatus|ProcessStatusMessage|
|---|---|
|I0|開立新增|
|I1|開立待上傳|
|I2|開立上傳待確認|
|I9|開立上傳完成|
|IP|開立暫停上傳|

## 發票作廢
|ProcessStatus|ProcessStatusMessage|
|---|---|
|C0|作廢新增|
|C1|作廢待上傳|
|C2|作廢上傳待確認|
|C9|作廢上傳完成|
|CP|作廢暫停上傳|

## 折讓單開立
|ProcessStatus|ProcessStatusMessage|
|---|---|
|A0|折讓新增|
|A1|折讓待上傳|
|A2|折讓上傳待確認|
|A9|折讓上傳完成|
|AP|折讓暫停上傳|

## 折讓單作廢
|ProcessStatus|ProcessStatusMessage|
|---|---|
|D0|折讓作廢新增|
|D1|折讓作廢待上傳|
|D2|折讓作廢上傳待確認|
|D9|折讓作廢上傳完成|
|DP|折讓作廢暫停上傳|
