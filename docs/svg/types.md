  
# Types
  
<br/>
  
- Type aliases
  
  - [Currency](#type-alias-currency)
  - [Size](#type-alias-size)
  - [Language](#type-alias-language)
  - [FontName](#type-alias-fontname)
  - [Data](#interface-data)
  - [Debtor](#interface-debtor)
  - [Creditor](#interface-creditor)
  - [QRBillOptions](#interface-qrbilloptions)
  - [PDFOptions](#interface-pdfoptions)
  - [SVGOptions](#interface-svgoptions)
  
<br/>
  
## Type aliases
  
### Type alias: Currency
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L2C0)  
  
#### Type
  
`"CHF"` | `"EUR"`  
  
<br/>
  
### Type alias: Size
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L3C0)  
  
#### Type
  
`"A4"` | `"A6"` | `"A6/5"`  
  
<br/>
  
### Type alias: Language
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L4C0)  
  
#### Type
  
`"DE"` | `"EN"` | `"FR"` | `"IT"`  
  
<br/>
  
### Type alias: FontName
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L5C0)  
  
#### Type
  
`"Arial"` | `"Frutiger"` | `"Helvetica"` | `"Liberation Sans"`  
  
<br/>
  
### Interface: Data
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L7C0)  
  
- **creditor** [`Creditor`](#interface-creditor) Creditor related data.
- **currency** [`Currency`](#type-alias-currency) The currency to be used. **3 characters.**
- **additionalInformation** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Additional information. **Max 140 characters.**
  
  Bill information contain coded information for automated booking of the payment. The data is not forwarded with the payment. `optional`
- **amount** [`number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) The amount. **Max. 12 digits.** `optional`
- **av1** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Alternative scheme. **Max. 100 characters.**
  
  Parameter character chain of the alternative scheme according to the syntax definition in the [“Alternative scheme” section](https://www.paymentstandards.ch/dam/downloads/ig-qr-bill-en.pdf) `optional`
- **av2** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Alternative scheme. **Max. 100 characters.**
  
  Parameter character chain of the alternative scheme according to the syntax definition in the [“Alternative scheme” section](https://www.paymentstandards.ch/dam/downloads/ig-qr-bill-en.pdf) `optional`
- **debtor** [`Debtor`](#interface-debtor) Debtor related data. `optional`
- **message** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) A message. **Max. 140 characters.**
  
  message can be used to indicate the payment purpose or for additional textual information about payments with a structured reference. `optional`
- **reference** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) A reference number. **Max 27 characters.**
  
  QR-IBAN: Maximum 27 characters. Must be filled if a QR-IBAN is used.
  Creditor Reference (ISO 11649): Maximum 25 characters. `optional`
  
<br/>
  
### Interface: Debtor
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L66C0)  
  
- **address** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Address. **Max 70 characters.**
- **city** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) City. **Max 35 characters.**
- **country** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Country code. **2 characters.**
- **name** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Name. **Max. 70 characters.**
- **zip** [`number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) | [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Postal code. **Max 16 characters.**
- **buildingNumber** [`number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) | [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Building number. **Max 16 characters.** `optional`
  
<br/>
  
### Interface: Creditor
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L99C0)  
  
- **address** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Address. **Max 70 characters.**
- **city** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) City. **Max 35 characters.**
- **country** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Country code. **2 characters.**
- **name** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Name. **Max. 70 characters.**
- **zip** [`number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) | [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Postal code. **Max 16 characters.**
- **buildingNumber** [`number`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) | [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) Building number. **Max 16 characters.** `optional`
- **account** [`string`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) The IBAN. **21 characters.**
  
<br/>
  
### Interface: QRBillOptions
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L107C0)  
  
- **fontName** [`FontName`](#type-alias-fontname) Font used for the QR-Bill.
  Fonts other than Helvetica must be registered in the PDFKit document.  [http://pdfkit.org/docs/text.html#fonts](http://pdfkit.org/docs/text.html#fonts) `optional`
- **language** [`Language`](#type-alias-language) The language with which the bill is rendered. `optional`
- **outlines** [`boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) Whether you want render the outlines. This option may be disabled if you use perforated paper. `optional`
- **scissors** [`boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) Whether you want to show the scissors icons or the text `Separate before paying in` `optional`
  
<br/>
  
### Interface: PDFOptions
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L137C0)  
  
- **fontName** [`FontName`](#type-alias-fontname) Font used for the QR-Bill.
  Fonts other than Helvetica must be registered in the PDFKit document.  [http://pdfkit.org/docs/text.html#fonts](http://pdfkit.org/docs/text.html#fonts) `optional`
- **language** [`Language`](#type-alias-language) The language with which the bill is rendered. `optional`
- **outlines** [`boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) Whether you want render the outlines. This option may be disabled if you use perforated paper. `optional`
- **scissors** [`boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) Whether you want to show the scissors icons or the text `Separate before paying in` `optional`
- **separate** [`boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) Whether you want to show the text `Separate before paying in` `optional`
  
<br/>
  
### Interface: SVGOptions
  
Defined in: [src/shared/types.ts](../../src/shared/types.ts#L148C0)  
  
- **fontName** [`FontName`](#type-alias-fontname) Font used for the QR-Bill.
  Fonts other than Helvetica must be registered in the PDFKit document.  [http://pdfkit.org/docs/text.html#fonts](http://pdfkit.org/docs/text.html#fonts) `optional`
- **language** [`Language`](#type-alias-language) The language with which the bill is rendered. `optional`
- **outlines** [`boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) Whether you want render the outlines. This option may be disabled if you use perforated paper. `optional`
- **scissors** [`boolean`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) Whether you want to show the scissors icons or the text `Separate before paying in` `optional`