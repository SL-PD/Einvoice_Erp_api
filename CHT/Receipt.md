# 已開立發票資料上傳(單筆訂單上傳)

### 範例格式
B2B存證 [範例](https://slproject.gitbook.io/sl-einv-project/cht/b2bjsonsample)
B2C存證 [範例](https://slproject.gitbook.io/sl-einv-project/cht/b2cjsonsample)

<font color='red'>
若使用的是 /Append/Order <br />
則 不須傳入 <br />
InvoiceID、InvoiceDateTime <br />
但 必須傳入 <br />
RelateNumber 且必須不重複 <br />
</font>

<font color='green'>
若使用的是 /Append/PrintInvoices <br />
則依照原開立發票格式上傳即可 <br />
</font>

### 欄位說明 
---
閱讀說明：

B2B：指的是B2B交易所開立之發票(或三聯式發票)，開立對象為公司行號或機關組織，其中發票內容有計算稅額以供買受人作為進項扣抵。
B2C：指的是B2C交易所開立之發票(或二聯式發票)，開立對象為自然人或機關組織，其中發票內容不計算稅額，僅供買受人做為購買憑證。

B2B與B2C欄位標註說明：
M: 必需提供資料
CM: 條件符合時，必需提供資料
O: 可選擇是否提供資料
CO: 條件符合時，可選擇是否提供資料
X: 不須提供資料

---

#### 發票單頭
|欄位名稱|欄位說明|欄位型態|欄位長度|B2B|B2C|條件說明|
|--|--|--|--|--|--|--|
|CompanyID|Seller BAN|String|10|M|M|賣方統編(必須為e首發票客戶)|
|InvoiceID|Invoice Number|String|10|M|M|發票字軌含流水號例如 QQ12345678|
|InvoiceDateTime|Invoice Create DateTime|DateTime||M|M|發票開立時間(訂單版得不需傳入)，請採用ISO 8601格式傳遞UTC Time 例如：<br /> 2011-07-14T19:43:37|
|InvoiceFor|Invoice For Buyer|String|1|M|M|發票開立對象，使用B2B存證填寫B，使用B2C存證填寫C|
|BuyerID|Buyer BAN|String|10|M|M|買方統編，若為自然人須為 000000000 (10個0)|
|BuyerInvoiceTitle|Buyer Company Name|String|60|M|O|買方公司名稱|
|BuyerName|BuyerName|String|30|O|O|購買人姓名|
|BuyerTelNo|Buyer Telephone Number|string|26|O|O|買方電話號碼，若要傳送簡訊則此欄位填寫行動電話號碼|
|BuyerEmail|Buyer Email|String|80|O|O|買方電子郵件帳號，如果PrintMark=N此欄位與[買方電話號碼]兩者必填其一，否則電子發票通知無法寄送|
|BuyerAddress|Buyer Address|String|100|O|O|如要寄送實體發票，此欄位必填|
|CarrierType|載具類型|String|6|O|O|僅能為手機載具(3J0002)或自然人憑證(CQ0001)|
|CarrierId|載具編號|String|64|O|O||
|CheckNumber|Invoice Check Number|String|4|M|X| 檢查碼，B2B 發票上必須列印四碼檢查碼(隨機四碼)，且檢查碼必須與上傳至整合服務平台相同，若未列印(PrintMark=N)且未傳送此欄位，將由e首發票系統產生|
|RandomNumber|Invoice Random Number|String|4|X|M| 隨機碼，B2C 發票上必須列印四碼隨機碼(隨機四碼)，且隨機碼必須與上傳至整合服務平台相同，若未列印(PrintMark=N)且未傳送此欄位，將由e首發票系統產生|
|RelateNumber|Relate Number|String|20|O|O|關聯號碼，e首發票中可用來帶入關聯的訂單號碼|
|PrintMark|Print Mark|String|1|M|M|是否已列印紙本發票給買受人，是填Y，否填N|
|DonateMark|Donate Mark|String|1|X|M|是否捐贈發票，捐贈為Y，不捐贈為N，若已經列印(PrintMark=Y)則只能為N|
|NPOBAN|NPO BAN|String|7|X|CO|捐贈單位愛心碼，若DonateMark=Y則必須填此欄位|
|TaxType|TaxType|String|1|M|M|課稅別  1:應稅 2:零稅率 3:免稅|
|SalesAmount|Sales Amount|Decimal|(12,0)|CO|CO|銷售未稅總額;(明細小計總額); 如果為應稅時填寫(TaxType=1)|
|TaxAmount|Tax Amount|Decimal|(12,0)|CM|CM|總稅額; 如果為應稅時填寫(TaxType=1)|
|ZeroTaxSalesAmount|Zero Tax Sales Amount|Decimal|(12,0)|CO|CO|零稅銷售總額,如特別關稅; 如果為零稅率時填寫(TaxType=2)|
|CustomsClearanceMark|Customs Clearance Mark|String|1|CM|CM|通關方式 1:非經海關出口 2:經海關出口; 如果為零稅率時填寫(TaxType=2)|
|BondedArea|Bonded Area|String|1|CM|X|零稅率註記 1:符合買受人為保稅區營業人 2:符合買受人為遠洋漁業營業人3:符合買受人為自由貿易港區營業人; 如果為零稅率時填寫(TaxType=2)|
|BuyerRemark|Buyer Remark|String|1|CO|CO|買受人註記 1:得抵扣之進貨及費 2:得抵扣之固定資 3:不得抵扣之進貨及費用 4:不得抵扣之固定資口; 如果為零稅率時填寫(TaxType=2)選填此欄位|
|FreeTaxSalesAmount|Free Tax Sales Amount|Decimal|(12,0)|CM|CM|免稅銷售總額,如農特產品銷售; 如果為免稅時填寫(TaxType=3)|
|TotalAmount|Total Amount|Decimal|(12,0)|M|M|總金額(銷售未稅總額+總稅額);|
|MainRemark|發票備註|String|200|O|O|發票備註|
|UseFor|選擇使用發票組別|String|2|O|O|對應api/Inquire/GetInvoiceIDList中Details內的 UseFor欄位|
|PrinterNo|印表機編號|String|2|O|O|指定列印的印表機號；例如: 00、01|
|PrintWithDetail|選擇是否列印明細|String|1|O|O|2:僅列印發票，3:同時列印發票與明細|
|CutDetail|選擇C類發票明細是否裁斷|Boolen|1|O|X|true(預設):明細裁斷，false:明細不裁|
|Details|發票明細內容|Json Format Object||M|M|單身明細|

#### Details 發票明細內容格式說明

|欄位名稱|欄位說明|欄位型態|欄位長度|B2B|B2C|條件說明|
|--|--|--|--|--|--|--|
|DetailID|Serial Nnmber|String|3|M|M|三碼數字編碼，依序 001 002 不足三碼左邊補 0|
|ProductID|Product ID|String|20|O|O|產品代碼|
|ProductName|Product DEscription|string|256|M|M|產品名稱|
|Quantity|Quantity|Decimal|(12,4)|M|M|數量;|
|UnitPrice|Unit Price|Decimal|(12,4)|M|M|單價; B2B單價未含稅額，B2C單價包含稅額|
|SubTotal|Sub Total|Decimal|(12,4)|M|M|小計; (數量X單價)|
|Remark|明細備註|String|40|O|O|每個明細的備註|



---



