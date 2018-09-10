### Inquiry authorization invoice track and period number 

```
POST api/Inquire/GetInvoiceIDList
```
<font color="red">Please use the new test location to test API。</font>

[Sending Data Description](GetInvoiceIDList.html)

### Upload the blank invoice number
```
POST api/Append/TrackBlank
```
[Sending Data Description](TrackBlank.html)

### Update the blank invoice number
```
POST api/Update/SetBlankInvoiceID
```
[Sending Data Description](SetBlankInvoice.html)

### Batch upload for multiple invoice
```
POST api/Append/Invoices
```
[Sending Data Description](Receipt.html)
### Batch update for multiple invoice
```
POST api/Update/Invoices
```
[Sending Data Description](Receipt.html)
### Upload multiple invoice and Print
```
POST api/Append/PrintInvoices
```
[Sending Data Description](Receipt.html)
### Query multiple invoice upload status
```
POST api/Inquire/GetInvoicesAppendStatus
```
[Sending Data Description](GetInvoicesStatus.html)
### Batch void invoice
```
POST api/Update/CancelInvoices
```
[Sending Data Description](CancelInvoice.html)
### Batch void blank invoice 
##### (Used when the invoice number is not sequential and produces a blank number)
```
POST api/Append/BlankCancel
```
[Sending Data Description](CancelInvoice.html)
### Invoice discount
```
POST api/Update/AllowanceInvoice
```
[Sending Data Description](InsertAllowance.html)




