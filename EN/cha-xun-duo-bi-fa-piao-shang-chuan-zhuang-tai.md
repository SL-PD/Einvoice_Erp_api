# Query process status of invoices

The query upload status here refers to the status of the invoice upload to the integrated service platform by the e-Invoice value center.

Query multiple invoice upload status (using Http Post) <br />
**Attention：Name is difference. Single is Invoice, Multiple is Invoices

### Example:
```
{"CompanyID":"12345678","InvoiceID":"CA89430001"}
```
### Description
* CompanyID : Seller's Company Tax ID \(Must be the e-Invoice customer\)
* InvoiceID : Invoice number

Returns value is Interrupted, Processing, Upload failed, to be confirmed, Upload completed. When the invoice is uploaded to the e-Invoice one hour later, The query result is not 'Upload completed'. You could take the initiative to notify e-Invoice to help。If the invoice upload fails，e-Invoice will notify you to correct the contents of the invoice and re-upload it。

### Return Field AppendStatus ：
N：Invoice is not exist.
P：Invoice is exist.
U：Invoice was uploaded to the integrated service platform.
C：Invoice was uploaded to the integrated service platform and the integrated service platform had confirmed.