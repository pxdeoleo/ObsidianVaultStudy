>[!summary]
Understanding dataset design patterns in Microsoft Dynamics 365 Business Central reports is crucial for creating efficient and effective report layouts. Properly structuring data items and using properties like DataItemLink and PrintOnlyIfDetail ensures accurate and useful datasets without unnecessary information.

#### Definitions
- **Dataset Design**: The process of organizing data items in a report to determine how records are added to the runtime dataset.
- **DataItemLink Property**: Establishes relationships between data items to avoid incorrect joins and large datasets.
- **PrintOnlyIfDetail Property**: Ensures only parent data items with child data output are included in the report.

>[!example] Unlinked Data Items Example
- **Code**:
    ```al
    dataitem(Customer; Customer)
    {
        column(CustomerNo; "No.")
        {
        }
        column(CustomerName; Name)
        {
        }
    }
    dataitem(Vendor; Vendor)
    {
        column(VendorNo; "No.")
        {
        }
        column(VendorName; Name)
        {
        }
    }
    ```
- **Result**: Both Customer and Vendor records are added separately, each in their respective columns.

>[!example] Indented Data Items without Links Example
- **Code**:
    ```al
    dataset
    {
        dataitem(Customer; Customer)
        {
            column(CustomerNo; "No.")
            {
            }
            column(CustomerName; Name)
            {
            }
            dataitem(CustomerLedgers;"Cust. Ledger Entry")
            {
                column(CustomerLedgersCustomerNo;"Customer No.")
                {
                }
                column(CustomerLedgersAmountLCY;"Amount (LCY)")
                {
                }
            }
        }
    }
    ```
- **Result**: Incorrect dataset due to cross join, resulting in a large number of irrelevant records.

>[!example] Indented Data Items with DataItemLink Example
- **Code**:
    ```al
    dataitem(Customer; Customer)
    {
        column(CustomerNo; "No.")
        {
        }
        column(CustomerName; Name)
        {
        }
        dataitem(CustomerLedgers; "Cust. Ledger Entry")
        {
            DataItemLinkReference = Customer;
            DataItemLink = "Customer No." = field("No.");
            column(CustomerLedgersCustomerNo; "Customer No.")
            {
            }
            column(CustomerLedgersAmountLCY; "Amount (LCY)")
            {
            }
        }
    }
    ```
- **Result**: Correctly linked customer and customer ledger entry records. However, customers without ledger entries are still included.

>[!example] Using PrintOnlyIfDetail Property Example
- **Code**:
    ```al
    dataitem(Customer; Customer)
    {
        PrintOnlyIfDetail = true;
        column(CustomerNo; "No.")
        {
        }
        column(CustomerName; Name)
        {
        }
        dataitem(CustomerLedgers; "Cust. Ledger Entry")
        {
            DataItemLinkReference = Customer;
            DataItemLink = "Customer No." = field("No.");
            column(CustomerLedgersCustomerNo; "Customer No.")
            {
            }
            column(CustomerLedgersAmountLCY; "Amount (LCY)")
            {
            }
        }
    }
    ```
- **Result**: Dataset includes only customers with ledger entries, excluding those without.

#### Tags
#datasetdesign #businesscentral #reportdesign #dataitems #bestpractices