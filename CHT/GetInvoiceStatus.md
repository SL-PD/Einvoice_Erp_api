# 查詢單筆發票上傳狀態

此處查詢上傳狀態指的是由e首發票加值中心將發票上傳至整合服務平台的狀態

### 範例格式
```
GET api/einv/GetInvoiceStatus?InvoiceID=AA12345678
```
### 欄位說明
* InvoiceID 發票號碼

如果回傳為NULL則表示尚未進行上傳動作。(測試區皆會回傳NULL)

