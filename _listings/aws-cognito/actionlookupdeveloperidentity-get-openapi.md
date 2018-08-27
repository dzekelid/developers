---
swagger: "2.0"
x-collection-name: AWS Cognito
x-complete: 0
info:
  title: AWS Cognito API Lookup Developer Identity
  version: 1.0.0
  description: |-
    Retrieves the IdentityID associated with a
                DeveloperUserIdentifier or the list of
             DeveloperUserIdentifiers associated with an IdentityId for an
             existing identity.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=GetOpenIdTokenForDeveloperIdentity:
    get:
      summary: Get Open Id Token For Developer Identity
      description: |-
        Registers (or retrieves) a Cognito IdentityId and an OpenID Connect
                 token for a user authenticated by your backend authentication process.
      operationId: getOpenIdTokenForDeveloperIdentity
      x-api-path-slug: actiongetopenidtokenfordeveloperidentity-get
      parameters:
      - in: query
        name: IdentityId
        description: A unique identifier in the format REGION:GUID
        type: string
      - in: query
        name: IdentityPoolId
        description: An identity pool ID in the format REGION:GUID
        type: string
      - in: query
        name: Logins
        description: A set of optional name-value pairs that map provider names to
          provider tokens
        type: string
      - in: query
        name: TokenDuration
        description: The expiration time of the token, in seconds
        type: string
      responses:
        200:
          description: OK
      tags:
      - Open ID Token for Developer Identities
  /?Action=LookupDeveloperIdentity:
    get:
      summary: Lookup Developer Identity
      description: |-
        Retrieves the IdentityID associated with a
                    DeveloperUserIdentifier or the list of
                 DeveloperUserIdentifiers associated with an IdentityId for an
                 existing identity.
      operationId: lookupDeveloperIdentity
      x-api-path-slug: actionlookupdeveloperidentity-get
      parameters:
      - in: query
        name: DeveloperUserIdentifier
        description: A unique ID used by your backend authentication process to identify
          a user
        type: string
      - in: query
        name: IdentityId
        description: A unique identifier in the format REGION:GUID
        type: string
      - in: query
        name: IdentityPoolId
        description: An identity pool ID in the format REGION:GUID
        type: string
      - in: query
        name: MaxResults
        description: The maximum number of identities to return
        type: string
      - in: query
        name: NextToken
        description: A pagination token
        type: string
      responses:
        200:
          description: OK
      tags:
      - Developer Identities
  /?Action=MergeDeveloperIdentities:
    get:
      summary: Merge Developer Identities
      description: |-
        Merges two users having different IdentityIds, existing in the same
                 identity pool, and identified by the same developer provider.
      operationId: mergeDeveloperIdentities
      x-api-path-slug: actionmergedeveloperidentities-get
      parameters:
      - in: query
        name: DestinationUserIdentifier
        description: User identifier for the destination user
        type: string
      - in: query
        name: DeveloperProviderName
        description: The domain by which Cognito will refer to your users
        type: string
      - in: query
        name: IdentityPoolId
        description: An identity pool ID in the format REGION:GUID
        type: string
      - in: query
        name: SourceUserIdentifier
        description: User identifier for the source user
        type: string
      responses:
        200:
          description: OK
      tags:
      - Developer Identities
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---