### Inquiry authorization invoice track and period number 

```
POST /api/Inquire/GetInvoiceIDList
```
<font color="red">Please use the new test location to test API。</font>
[Sending Data Description](GetInvoiceIDList.html)

### Update the blank invoice number
```
POST api/eInv/SetBlankInvoiceID
```
[Sending Data Description](SetBlankInvoice.html)

### Batch upload for multiple invoice
```
POST api/einv/AppendInvoices
```
[Sending Data Description](Receipt.html)
### Query single invoice upload status
```
GET api/einv/GetInvoiceStatus
```
[Sending Data Description](GetInvoiceStatus.html)
### Query multiple invoice upload status
```
POST api/einv/GetInvoicesStatus
```
[Sending Data Description](GetInvoicesStatus.html)
### Batch void invoice
```
POST api/einv/CancelInvoices
```
[Sending Data Description](CancelInvoice.html)
### Invoice discount
```
GET api/einv/AllowanceInvoice
```
[Sending Data Description](InsertAllowance.html)




