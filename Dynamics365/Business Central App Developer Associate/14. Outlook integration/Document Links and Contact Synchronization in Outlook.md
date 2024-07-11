>[!summary]
>The [[Business Central]] Document Links add-in provides quick access to documents mentioned in email messages, while contact synchronization ensures consistent contact information across Business Central and Outlook.

#### Document Links Add-in
- Available if a document number is recognized in an email body.
- Quick access to documents, such as sales quotes, from Outlook.
- Modify and take actions on documents within the add-in.

>[!info] Accessing Documents
1. In Outlook, choose the Document Links button above the email body.
2. In Outlook Web App, select the document number text in the email.

>[!example] Example Document Access
- Email mentions S-QUO100.
- Business Central identifies and allows access to the sales quote.

>[!important] Contact Synchronization
- Sync contacts between Business Central and Outlook for consistency.
- Use the Exchange Sync Setup page to configure synchronization.
- Set up filters to sync specific contacts.

>[!tip] Synchronization Setup
1. Ensure your user profile specifies your Microsoft 365 email account.
2. Validate Exchange connection in the Exchange Sync Setup page.
3. Start synchronization on the Contact Sync Setup page.
4. Optionally, set filters for which contacts to sync.

>[!info] Manual and Automatic Sync
- Manually start synchronization from the Contacts list using Sync with Microsoft 365.
- Optionally adjust filters before syncing.
- Automatic synchronization can be scheduled for regular updates.
>[!todo] Sync Methods
- **Sync with Microsoft 365:** Faster, syncs changes based on the last modified date.
- **Full Sync with Microsoft 365:** Syncs all contacts regardless of last sync date.

>[!warning] Required Fields for Sync
- Contacts must have Name, Email address, and be of type Person.
- Business Central is the master of contact information, resolving duplicates.