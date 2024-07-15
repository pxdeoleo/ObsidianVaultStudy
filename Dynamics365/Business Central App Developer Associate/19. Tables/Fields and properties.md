>[!summary] 
>As well as tables, [[Business Central]] fields have their own unique properties. These properties completely change the way the fields hold data.

>[!info] Field No. and Name

Field no. must be within the number ranges provided by Microsoft.
It's important to give fields an english name unique to the table it belongs to.

>[!important] DataType

It's an important property. Determines the data type to be stored in the field.

```AL
feld([number], [name], [datatype])
```

- **Text**
    - Alphanumeric string
    - Max of 250 characters
    - Corresponding SQL data type: NVARCHAR
- **Code**
    - Uppercase alphanumeric string
    - Max of 250 characters
    - Corresponding SQL data type: NVARCHAR
    - Often used as a primary key
- **Decimal**
    - Decimal number
    - From -999,999,999,999,999.99 to +999,999,999,999,999.99
    - Corresponding SQL data type: DECIMAL
- **Integer**
    - Whole number
    - From -2,147,483,647 to 2,147,483,647
    - Corresponding SQL data type: INT
- **BigInteger**
    - 64-bit integer
    - Large whole numbers
    - Corresponding SQL data type: BIGINT
- **Binary**
    - Binary data
    - Corresponding SQL data type: VARBINARY
- **Option**
    - Option string
    - Comma-separated list of strings: valid values of the field
    - Cannot be extended by other extensions
    - Corresponding SQL data type: INT
- **Enum**
    - Linked to an enum object
    - Can be extended by other extensions
    - Corresponding SQL data type: INT
- **Boolean**
    - True or false
    - Formatted: Yes or No
    - Corresponding SQL data type: TINYINT
- **Date**
    - Date value
    - From January 1, 1753 to December 31, 9999
    - Undefined date (default value): 0D
    - Corresponding SQL data type: DATETIME
- **Time**
    - Time value
    - From 00:00:00 to 23:59:59.999
    - Undefined date (default value): 0T
    - Corresponding SQL data type: DATETIME
- **DateFormula**
    - Holds a date formula
    - Ex. 30D, CM+1M, D15 (the fifteenth of each month)
- **DateTime**
    - A point in time, a combined date and time
- **Duration**
    - Difference (ms) between two points in time
- **BLOB**
    - Binary Large Object
    - Store bitmaps and memos
- **Media**
    - Store image
    - Optimized performance to manage images
- **MediaSet**
    - A set of images
    - Manage a collection of images
- **RecordID**
- **TableFilter**
- **GUID**

**Option** data type's actual values are numeric. Its **OptionMembers** property contains the values' names.
Also, it can't be extended by other AL extensions to add values to the **OptionMembers** property.

A viable alternative is the **Enum** type, which requires declaring the enum as a separate object, but can be extensible by other AL extension.
