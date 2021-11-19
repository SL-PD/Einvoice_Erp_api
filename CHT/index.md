# e首發票發票版 API 說明文件 (此為 發票版本 API，前端系統完成取號開立時使用)

此文件 說明 e首發票 API 相關欄位說明文件。 實際使用仍以最新釋出版本為主。

* 拋入已開立發票由e首發票進行後續整合作業\(發票版\)

```
  採用的是HTTP POST的方式傳送，以 SHA256簽章值 驗證
  發票版e首發票 API 測試區串接位置：
  https://webapi.systemlead.com/terpapi 
  其版本與正式區相符，惟正式區網址，待測試區測通後，將由業務人員提供。
```

### 查詢授權e首發票下載之發票字軌與期號 

```
POST /Inquire/GetInvoiceIDList
```
[傳送格式說明](getinvoiceidlist.md)

### 上傳空白發票號
```
POST /Append/TrackBlank
```
[傳送格式說明](trackblank)

### 更新空白發票號
```
POST /Update/SetBlankInvoiceID
```
[傳送格式說明](setblankinvoice)

### 單筆訂單上傳(訂單版)
```
POST /Append/Order
```
[傳送格式說明](receipt)

### 訂單批次上傳(訂單版)
```
POST /Append/Orders
```
[傳送格式說明](receipt)

### 發票批次上傳(發票版)
```
POST /Append/Invoices
```
[傳送格式說明](receipt)

### 多筆發票批次更新
```
POST /Update/Invoices
```
<font color="red">
注意: 
1.發票號為鍵值，除發票號與發票開立日期外其餘欄位皆可異動
2.發票若已啟動上傳將無法更新發票
</font>
[傳送格式說明](receipt)

### 新增發票並列印
```
POST /Append/PrintInvoices
```
[傳送格式說明](receipt)

### 查詢多筆發票最新處理狀態
```
POST /Inquire/GetInvoicesStatus
```
[傳送格式說明](getinvoicesstatus)

### 查詢多筆發票上傳狀態
```
POST /Inquire/GetInvoicesAppendStatus
```
[傳送格式說明](getinvoicesappendstatus)

### 批次作廢發票
```
POST /Update/CancelInvoices
```
[傳送格式說明](cancelinvoice)

### 批次作廢空白發票(發票號跳號用)
```
POST /Append/BlankCancel
```
[傳送格式說明](cancelinvoice)

### 批次開立折讓單
```
POST /Update/AllowanceInvoice
```
[傳送格式說明](insertallowance)

### 批次作廢折讓單
```
POST /Update/CancelAllowances
```
[傳送格式說明](cancelallowance)

