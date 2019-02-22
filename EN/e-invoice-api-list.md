### Inquiry authorization invoice track and period number 

```
(after 2019-02-22)
POST Inquire/GetInvoiceIDList
```
<font color="red">Please use the new test location to test API。</font>

[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/inquiry-authorization-invoice-track-and-period-number)

### Upload the blank invoice number
```
(after 2019-02-22)
POST Append/TrackBlank
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/upload-the-blank-invoice-number)

### Update the blank invoice number
```
(after 2019-02-22)
POST Update/SetBlankInvoiceID
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/update-the-blank-invoice-number)

### Batch upload for multiple invoice
```
(after 2019-02-22)
POST Append/Invoices
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/batch-upload-for-multiple-invoice)
### Batch update for multiple invoice
```
(after 2019-02-22)
POST Update/Invoices
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/batch-upload-for-multiple-invoice)
### Upload multiple invoice and Print
```
(after 2019-02-22)
POST Append/PrintInvoices
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/batch-upload-for-multiple-invoice)
### Query multiple invoice upload status
```
(after 2019-02-22)
POST Inquire/GetInvoicesAppendStatus
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/cha-xun-duo-bi-fa-piao-shang-chuan-zhuang-tai)
### Batch void invoice
```
(after 2019-02-22)
POST Update/CancelInvoices
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/fa-piao-zuo-fei-shang-chuan-ge-shi)
### Batch void blank invoice 
##### (Used when the invoice number is not sequential and produces a blank number)
```
(after 2019-02-22)
POST Append/BlankCancel
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/fa-piao-zuo-fei-shang-chuan-ge-shi)
### Invoice discount
```
(after 2019-02-22)
POST Update/AllowanceInvoice
```
[Sending Data Description](https://slproject.gitbook.io/sl-einv-project/en/fa-piao-zhe-rang-shang-chuan-ge-shi)
