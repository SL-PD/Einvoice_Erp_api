### Inquiry authorization invoice track and period number 

```
POST api/Inquire/GetInvoiceIDList
```
<font color="red">Please use the new test location to test API。</font>

[Sending Data Description](inquiry-authorization-invoice-track-and-period-number)

### Upload the blank invoice number
```
POST api/Append/TrackBlank
```
[Sending Data Description](upload-the-blank-invoice-number)

### Update the blank invoice number
```
POST api/Update/SetBlankInvoiceID
```
[Sending Data Description](update-the-blank-invoice-number)

### Batch upload for multiple invoice
```
POST api/Append/Invoices
```
[Sending Data Description](batch-upload-for-multiple-invoice)
### Batch update for multiple invoice
```
POST api/Update/Invoices
```
[Sending Data Description](batch-upload-for-multiple-invoice)
### Upload multiple invoice and Print
```
POST api/Append/PrintInvoices
```
[Sending Data Description](batch-upload-for-multiple-invoice)
### Query multiple invoice upload status
```
POST api/Inquire/GetInvoicesAppendStatus
```
[Sending Data Description](cha-xun-duo-bi-fa-piao-shang-chuan-zhuang-tai)
### Batch void invoice
```
POST api/Update/CancelInvoices
```
[Sending Data Description](fa-piao-zuo-fei-shang-chuan-ge-shi)
### Batch void blank invoice 
##### (Used when the invoice number is not sequential and produces a blank number)
```
POST api/Append/BlankCancel
```
[Sending Data Description](fa-piao-zuo-fei-shang-chuan-ge-shi)
### Invoice discount
```
POST api/Update/AllowanceInvoice
```
[Sending Data Description](fa-piao-zhe-rang-shang-chuan-ge-shi)
