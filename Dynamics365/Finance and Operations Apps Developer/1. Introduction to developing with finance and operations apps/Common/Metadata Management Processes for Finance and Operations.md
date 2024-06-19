**1. Purpose of Metadata:**

- **Definition and Search:** Metadata is used to define and locate elements within finance and operations applications.

**2. Accessing Metadata Search:**

- **Navigation:** Visual Studio > Dynamics 365 > Metadata search.
- **Usage:** Allows searching for elements like forms, tables, and code snippets.

**3. Practical Use Case:**

- **Example Scenario:** Searching for a table with partial name known ("cust").
- **Method:** Use metadata search to find tables incorporating "cust" in their names.

**4. Search Parameters:**

- **Syntax for Searches:** `*<filter_1>:<filter_1_value> [<filter_2>:<filter_2_value>... <filter_N>:<filter_N_value>]*`
- **Searchable Attributes:**
    - **Name:** Default filter; use commas for multiple names.
    - **Type:** Specify element or sub-element types.
    - **Model:** Search by model name, comma-separated for multiple models.
    - **Property:** Targets specific properties on forms.
    - **Code:** Search within code snippets, encapsulated in quotes.

**5. Visual Tools:**

- **Screenshot:** Provides a visual guide to metadata search in Visual Studio.