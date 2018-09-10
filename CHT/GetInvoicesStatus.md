# 查詢發票處理狀態

此處查詢處理狀態指的是發票在e首發票加值中心的最後處理作業的狀態
查詢多筆發票處理狀態 (使用 Http Post) <br />

### 範例格式：
```
{"CompanyID":"12345678","InvoiceID":"CA89430001"}
```
### 欄位說明
* CompanyID 公司統編
* InvoiceID 發票號碼

### 回傳結果：
InvoiceID：發票號
ProcessStatus：處理狀態