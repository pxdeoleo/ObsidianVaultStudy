>[!summary] 
>[[Business Central]] has many properties that act like metadata for tables. These allow to identify the tables easily for end users, and identify behavior for developers.

>[!info] ID and Name

**ID**. Number value. Must be within the range Microsoft provides when becoming a Dynamics 365 Business Central partner.

**Name**. Every table name must be singular; customer, not customers. It is recommended to use prefix/suffix to make table name unique.

>[!Caption property]

Text displayed in the title bar of the window.

AL table definition:
```AL
table 50100 Car
{
	Caption = 'Car';

	fields
	{
		field(1; "No."; Code[20])
		{
		}
	}
}
```

>[!info] DataPerCompany property

Even in a multicompany environment, the data in a table will be kept unique for each company. That's the role of the **DataPerCompany** field, which is set to **Yes** by default.
When it is set to **No**, the data will be available to all companies, which might have significant consequences.

>[!info] DataClassification property

States the classification of the data. Can be used to adhere to security, compliance and privacy requirements.
Example classification options:
- **ToBeClassified**. Default option. Data has no yet been given a classification.
- **AccountData**. Related to customer billing information.
- **EndUserIdentifiableInformation**. User data, such as IP Address or user principle name.
This property is provided by Microsoft as a matter of convenience. The responsibility on its usage lies on the partner.
>[!info] LookupPageId and DrillDownPageId properties

**LookUpPageId** links to the page that will be used to show the records of the table from a [[lookup action]].
**DrillDownPageId** links to a page that will be used to show the records of the table from a [[drill-down action]], which shows only details for a certain field.

>[!info] ObsoleteState, ObsolteReason, ObsoleteTag

These properties let other developers know if an object or feature is, or is soon to be obsolete.



