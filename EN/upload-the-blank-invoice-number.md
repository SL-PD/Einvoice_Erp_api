# Upload the Blank Invoice Number

If you have invoice numbers obtained through the e-invoice, you can also use the e-invoice to upload the blank invoice numbers.

### Example:

{

```
"HeadBan":"12345678",

"BranchBan":"12345678",

"InvoiceType":"07",

"YearMonth":"10706",

"InvoiceTrack":"AA",

"Items": [{

"InvoiceBeginNo":"12340005",

"InvoiceEndNo":"12340003"

},

{

"InvoiceBeginNo":"12340002",

"InvoiceEndNo":"12340003"

},

{

"InvoiceBeginNo":"12340002",

"InvoiceEndNo":"12340003"

}]
```

}

### Description

\* HeadBan: Tax number of head office \(Must be e-Invoice customer\)

\* BranchBan: Tax number of branch office\(Must be e-Invoice customer\) Note: No division is the same as the head office

\* InvoiceType: 07:General tax rate electronic invoice 08:Special tax rate electronic invoice

\* YearMonth: Invoice period: the year of Republic of China+Even months yyyMM; E.g 10608 Said 106 year 07-08 Current period

\* InvoiceTrack: the track of invoice

\* Items: Blank invoice number group \(In the same period and the same track can be multiple blank numbers.\)

\* InvoiceBeginNo: Blank number interval start number

\* InvoiceEndNo: Blank number interval end number \(If the single number is the same as the blank number interval start number\)

### Notice:

If the branch company to be uploaded by the head office on behalf of the blank invoice must apply \(the application for the tax platform\).

\#\#\# Return value

\`\`\`

\[

```
{

"HeadBan": "12345678",

"BranchBan": "12345678",

"InvoiceType": "07",

"YearMonth": "10706",

"InvoiceTrack": "AA",

"Items": [

    {

    "InvoiceBeginNo": "12340005",

    "InvoiceEndNo": "12340003",

    "Message": "發票迄號必須大於或等於起號",

    "Status": "E"

    },

    {

    "InvoiceBeginNo": "12340002",

    "InvoiceEndNo": "12340003",

    "Message": "空白發票新增失敗，請確認是否有輸入相同區間",

    "Status": "E"

    },

    {

    "InvoiceBeginNo": "12340002",

    "InvoiceEndNo": "12340003",

    "Message": "空白發票新增成功",

    "Status": "C"

    }]

}
```

\]

\`\`\`

