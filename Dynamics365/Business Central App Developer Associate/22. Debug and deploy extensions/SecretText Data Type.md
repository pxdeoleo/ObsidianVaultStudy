>[!summary]
The SecretText type in AL code is designed to protect sensitive values like credentials from being exposed during debugging. It ensures security while enabling effective debugging.

#### Definitions
- **SecretText**: A data type in AL code to protect sensitive information from being exposed during debugging.

>[!info] Protection Mechanism

SecretText ensures that sensitive values such as API keys and tokens are not exposed in the AL debugger during both regular and snapshot debugging sessions. Its use is essential for applications handling credentials.

>[!info] Retrieval Methods

Credentials can be retrieved in multiple ways:
- API key through AL HttpClient
- Token via control add-in with authentication provider like OAUTH2
- Custom scenarios creating authentication tokens
- Hardcoded credentials (not recommended)

>[!bug] Vulnerability

Credentials not protected by the NonDebuggable attribute can be exposed during debugging. It's crucial to use SecretText and NonDebuggable attributes to safeguard these values.

>[!example] Code Examples

**RetrieveSessionToken Procedure**

```al
[NonDebuggable]
procedure RetrieveSessionToken(Credential: SecretText; TargetUri: Text): SecretText
var
  Request: HttpRequestMessage;
  Response: HttpResponseMessage;
  Client: HttpClient;
  Headers: HttpHeaders;
begin
  Request.SetRequestUri(TargetUri);
  Request.GetHeaders(Headers);
  Headers.Add('Authorization', SecretStrSubstNo('Bearer %1', Credential));
  Client.Send(Request, Response);
  ParseSessionToken(Response, SessionToken);
  exit;
end;
```

**ParseSessionToken Procedure**

```al
[NonDebuggable]
procedure ParseSessionToken(Response: HttpResponseMessage; var SessionToken: SecretText): Text
begin
  // Parse the response
end;
```

#### Transit

Credentials transit through AL code via:
- Assignments to variables
- Parameters in procedure calls
- Return values of function calls

SecretText guarantees the protection of values during transit, preventing exposure through debuggable types.

#### Consumption

Credentials are consumed in scenarios such as:
- Creating authentication headers for requests
- Adding credentials to request bodies or parameters

Example:

```al
procedure SendAuthenticatedRequestToApi(UriTemplate: Text; BearerToken: SecretText; KeyParameter: SecretText; SecretBody: SecretText)
var
  Client: HttpClient;
  Headers: HttpHeaders;
  SecretHeader: SecretText;
  SecretUri: SecretText;
  RequestMessage: HttpRequestMessage;
begin
  SecretHeader := SecretStrSubstNo('Bearer %1', BearerToken);
  RequestMessage.GetHeaders(Headers);
  Headers.Add('Authorization', SecretHeader);
  SecretUri := SecretStrSubstNo(UriTemplate, KeyParameter);
  RequestMessage.SetSecretRequestUri(SecretUri);
  RequestMessage.Content.WriteFrom(SecretBody);
  SendMessageAndHandleResponse(Client, RequestMessage);
end;

[NonDebuggable]
procedure SendMessageAndHandleResponse(Client: HttpClient; Request: HttpRequestMessage): SecretText
var
  Response: HttpResponseMessage;
begin
  Client.Send(Request, Response);
  Response.Content.ReadAs(CredentialFromResponse);
end;
```

#### Additional Methods

- **Unwrap Method**: Extracts value from SecretText for compatibility, recommended only for .NET interoperability.
- **SecretStrSubstNo Method**: Composes SecretText values without revealing them, similar to StrSubstNo for Text values.

Example:

```al
procedure SecretStrSubstNoExamples()
var
  First: SecretText;
  Second: SecretText;
  Result: SecretText;
begin
  Result := SecretStrSubstNo('%1%2', First, Second);
  Result := SecretStrSubstNo('Bearer %1', First);
  Result := SecretStrSubstNo('%1,%2', First, Second);
end;
```

#### Tags
#SecretText #ALCode #Security #Debugging #CredentialsProtection