>[!summary]  
Document Sending Profiles in Business Central allow you to define how sales and purchase documents are sent to customers and vendors, reducing the need to select sending options each time. Profiles can include options for printing, emailing, saving to disk, or sending as electronic documents.
#### Definitions
- **Document Sending Profile**: A set of preferences defining how documents are sent to customers and vendors.
- **Default Profile**: The sending profile used for all customers and vendors unless specified otherwise.

>[!info] Setting Up Document Sending Profiles

1. **Open Document Sending Profile**:
    - Select the search icon, enter "document sending profile," and select the related link.

2. **Create New Profile**:
    - On the Document Sending Profile page, select the New action.
    - Fill in the required fields:
        - **Code**: A unique identifier for the profile.
        - **Description**: A brief description of the profile.
        - **Default**: Specify if this profile should be the default for all customers except those with a different profile.

3. **Configure Profile Options**:
    - **Printer**: Select if and how the document is printed. Options include "Yes (Prompt for Settings)" for manual configuration during each send.
    - **Email**: Select if and how the document is attached as a PDF to an email. Options include:
        - **Yes (Prompt for Settings)**: Manually configure each send.
        - **Yes (Use Default Settings)**: Automatically use predefined settings.
    - **Combine PDF Documents**: Merge selected documents into a single PDF when sending.
    - **Disk**: Specify if the document is saved as a PDF or created as an electronic document.
    - **Electronic Document**: Send the document as an electronic file that the customer can import into their system. Requires configuration of the Electronic Format field.

4. **Assign Profiles to Customers/Vendors**:
    - Set the Document Sending Profile field on the customer or vendor card to the appropriate profile.
#### Key Points

- **Default Profile Usage**: Customers and vendors without an assigned profile will use the default profile.
- **Profile Customization**: Customize profiles to suit different sending needs, ensuring consistent document handling.
- **Post and Send Action**: The Post and Send Confirmation dialog box shows the sending options used, allowing for last-minute changes.