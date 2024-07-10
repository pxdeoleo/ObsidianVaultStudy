>[!summary]
>Programmatically add Business Central tabs in Microsoft Teams channels and chats using the Microsoft Graph API. Ensure the user has access to the Business Central app for Teams for successful execution.

#### Adding Business Central Tabs via Graph API
- Use Microsoft Graph API to create channels, chats, and tabs in Teams.
- Prerequisites: Access to Business Central app for Teams and appropriate permissions.

#### Endpoint and Payload Structure
- **Channels Endpoint:**
```HTTP
POST https://graph.microsoft.com/v1.0/teams/{teamId}/channels/{channelId}/tabs
{
    "displayName": "<tab name>",
    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps/84c2de91-84e8-4bbf-b15d-9ef33245ad29",
    "configuration": {
        "entityId": "<unique id>",
        "contentUrl": "https://businesscentral.dynamics.com/teams?<company and page ID>",
        "websiteUrl": "https://businesscentral.dynamics.com/?<company and page ID>"
    }
}
```
- **Chats Endpoint:**
```HTTP
POST https://graph.microsoft.com/v1.0/chats/{chat-id}/tabs
{
    "displayName": "<tab name>",
    "teamsApp@odata.bind": "https://graph.microsoft.com/v1.0/appCatalogs/teamsApps/84c2de91-84e8-4bbf-b15d-9ef33245ad29",
    "configuration": {
        "entityId": "<unique id>",
        "contentUrl": "https://businesscentral.dynamics.com/teams?<company and page ID>",
        "websiteUrl": "https://businesscentral.dynamics.com/?<company and page ID>"
    }
}
```

#### Key Properties
- **displayName:** Name of the tab in Teams.
- **teamsApp@odata.bind:** Binds the tab to the Business Central app for Teams.
- **entityId:** Unique identifier for the tab.
- **contentUrl:** URL for rendering the Business Central tab content.
- **websiteUrl:** URL for viewing tab contents outside of Teams.

#### Example: Creating a Team and Adding a Tab
- **Create a Team Using Graph Explorer:**
  1. Sign in to Graph Explorer.
  2. Set method to POST and use the following URL:
```HTTP
    https://graph.microsoft.com/v1.0/teams
```
  1. Consent to required permissions.
  2. In the request body, use:
```JSON
    {
        "template@odata.bind": "https://graph.microsoft.com/v1.0/teamsTemplates('standard')",
        "displayName": "Warehouse",
        "description": "Team for communicating with the warehouse personnel"
    }
```
  1. Select Run Query.
  2. Retrieve the team ID from the response headers.

- **Add Business Central Tab:**
  1. Use the retrieved team ID and channel ID to construct the POST request for adding a tab.
  2. Send the request with the appropriate payload to create a tab for page 9305 Sale Orders.