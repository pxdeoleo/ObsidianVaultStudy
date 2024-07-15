> [!summary] 
> Page parts are used on FactBoxes and document pages to display extra information about the currently selected record, such as latest purchases on a customer card or invoice lines on a sales document.
 
#### Definitions
- **[[Pages Overview|Page]] parts**: Components used on FactBoxes and document pages to display additional information related to the current record.
- **FactBox**: An area of the page used to display additional details related to the main content, like latest purchases or unpaid invoices.
- **Document page**: A page used to display documents such as sales orders, often linked to header and line tables.

> [!info] Use of Page Parts
- On a customer card, they can show latest purchases or unpaid invoices.
- On document pages, they typically display lines, like sales invoice lines linked to a sales header.

> [!tip] Defining a Page Part
To define a page part:
1. Use the `tpart` snippet.
2. Structure: `part(PartName; PartSource)`
3. Provide the control name and the page to be loaded, usually a ListPart or CardPart.

> [!code] Example
```al
part(CustomerSalesInvoices; "Customer Sales Invoice ListPart")
```

> [!info] SubPageLink and SubPageView Properties
- **SubPageLink**: Links the main page to the page part, showing part details based on the main page record. Allows linking multiple fields between tables.
- **SubPageView**: Applies additional filters and sorting to the linked records in the page part.

#### Usage
- **SubPageLink Example**:
  ```al
  SubPageLink = "Customer No." = FIELD("No.");
  ```
- **SubPageView Example**:
  ```al
  SubPageView = SORTING("Invoice Date");
  ```

#### Tags
#pageparts #FactBoxes #documentpages #ALcoding #SubPageLink #SubPageView