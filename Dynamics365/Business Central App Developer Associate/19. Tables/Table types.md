>[!summary]
>[[Business Central]] data is stored in [[Table extensions|tables]], which are categorized by their implementation and their functional use

>[!info] By implementation

- **Database**. Most common tables. 
>	Customer
>	Vendor
>	Item
- System. Necessary for the system to function.
>	Company
>	Profile
>	Permission
- Virtual. Read-only tables. The data is created at runtime; not stored in the database.
>	Active session
- Temporary. Only exists in memory. Has no data by itself. Keeps a copy of another table.
>	Routines
>	Document reports

>[!info] Functional use

- **Master**.  Hold the most important information.
>	Customer
>	Vendor
>	Item
- **Supplemental**. Additional information that complements the master table.
>	Currency
>	Language
- **Setup**. Configuration data for the modules.
>	G/L Setup
>	Sales & Receivables Setup
- **Ledger**. Transactional information of its related functional domain.
>	Cust. Ledger Entry
>	Item Ledger Entry
- **Register**. Historical and transactional data related to their ledger tables
>	G/L Register
>	Item Register
- **Subsidiary**. Combined information from master and/or supplemental tables.
>	Item Vendor
>	FA Depreciation Book
- **Journal**. It's the primary transactional table. Transactions are booked through journals.
>	General Journal
>	Item Journal
- **Document**. Secondary transactional tables. Always built out of two tables: header and line details, like sales order header and sales order lines.
>	Sales Orders
>	Sales Quotes
- **Document history**. Historical version of Document tables.