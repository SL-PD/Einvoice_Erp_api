# Query process status of invoices

The query upload status here refers to the status of the invoice upload to the integrated service platform by the e-Invoice value center.

Query multiple invoice upload status \(using Http Post\)  
  
\*\*Attention：Name is difference. Single is Invoice, Multiple is Invoices

### Example:

```
{"CompanyID":"12345678","InvoiceID":"CA89430001"}
```

### Description

* CompanyID : Seller's Company Tax ID \(Must be the e-Invoice customer\)
* InvoiceID : Invoice number

ReturnsvalueisInterrupted,Processing,Uploadfailed,tobeconfirmed,Uploadcompleted.Whentheinvoiceisuploadedtothee-Invoiceonehourlater,Thequeryresultisnot'Uploadcompleted'.Youcouldtaketheinitiativetonotifye-Invoicetohelp。Iftheinvoiceuploadfails，e-Invoicewillnotifyyoutocorrectthecontentsoftheinvoiceandre-uploadit。

### ReturnFieldAppendStatus：

N：Invoice is not exist.  
P：Invoice is exist.  
U：Invoice was uploaded to the integrated service platform.  
C：Invoice was uploaded to the integrated service platform and the integrated service platform had confirmed.

