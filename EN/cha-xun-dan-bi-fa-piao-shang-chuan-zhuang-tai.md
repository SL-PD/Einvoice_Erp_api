# Query upload status of single invoice

The query upload status here refers to the status of the invoice upload to the integrated service platform by the e-Invoice value center.

### Example:
```
GET api/einv/GetInvoiceStatus?InvoiceID=AA12345678
```
### Description
* InvoiceID : Invoice number

If the return is NULL, it means that the upload has not yet been performed.(It always returns NULL in test area.)

