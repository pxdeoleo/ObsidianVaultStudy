> [!summary] 
> After setting up a new company and completing data migration, opening balances for general ledger, customers, vendors, and items must be transferred using journals for consistency and reliability. Use tables 81 (General Journal Line) and 83 (Item Journal Line) in the configuration package.

#### Definitions

- **General Journal Line (Table 81)**: Used for creating general ledger journal entries.
- **Item Journal Line (Table 83)**: Used for creating item journal entries.

> [!info] Creating Journal Lines

- Use [[Business Central]] functions to prepare journal lines efficiently.
- Functions include:
    - Create G/L Account Journal Lines
    - Create Customer Journal Lines
    - Create Vendor Journal Lines
    - Create Item Journal Lines

> [!example] Steps to Create G/L Account Journal Lines

1. Select the **Search for page** icon in the top-right corner.
2. Enter **Create G/L account journal lines** and select the related link.
3. Fill in the fields on the **Create G/L account journal lines** page.
4. Select **OK**.

> The result is a line for each account in the selected general journal batch.

> [!tip] Manual and Automated Data Entry

- Manually add amounts for each account in the general journal.
- Export table 81 in the configuration worksheet or configuration package to Excel to create a template with lines for each G/L account, customer, vendor, and item.

> [!attention] Consistent Data Entry

- Ensure data consistency and reliability by using journal entries rather than direct ledger entry modifications.

#### Using Excel for Journal Lines

1. Export table 81 or 83 from the configuration package to Excel.
2. Fill in the necessary amounts in the Excel template.
3. Import the filled Excel template back into Business Central.