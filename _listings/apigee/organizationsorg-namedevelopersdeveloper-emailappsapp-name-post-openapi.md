---
swagger: "2.0"
x-collection-name: Apigee
x-complete: 0
info:
  title: Apigee Edge Post Organizations Name Developers Developer Email Apps App Name
  description: Revokes a Developer App, disabling access to all API Products .
  version: 1.0.0
host: api.enterprise.apigee.com
basePath: /v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizations/{org_name}/developers:
    get:
      summary: Get Organizations Name Developers
      description: Gets the developer profile by registered date.
      operationId: getOrganizationsOrgNameDevelopers
      x-api-path-slug: organizationsorg-namedevelopers-get
      parameters:
      - in: path
        name: org_name
        description: Mention the organization name
      - in: query
        name: registeredat
        description: Mention the registered date
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
    post:
      summary: Post Organizations Name Developers
      description: Create a developer in an organization .
      operationId: postOrganizationsOrgNameDevelopers
      x-api-path-slug: organizationsorg-namedevelopers-post
      parameters:
      - in: query
        name: Content-Type
        description: Specify the Content Type
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
  /organizations/{org_name}/developers/{developer_name}:
    get:
      summary: Get Organizations Name Developers Developer Name
      description: Get a count of apps by developer email address.
      operationId: getOrganizationsOrgNameDevelopersDeveloperName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-name-get
      parameters:
      - in: path
        name: developer_name
        description: Mention the developer email
      - in: query
        name: entity
        description: Specify the entity
      - in: path
        name: org_name
        description: Mention the organization name
      - in: query
        name: query
        description: Query type count
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
    put:
      summary: Put Organizations Name Developers Developer Name
      description: Update an existing developer profile with new values or additional
        attributes.
      operationId: putOrganizationsOrgNameDevelopersDeveloperName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-name-put
      parameters:
      - in: query
        name: Content-Type
        description: Specify the Content Type
      - in: path
        name: developer_name
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
    post:
      summary: Post Organizations Name Developers Developer Name
      description: Sets the status of a developer.
      operationId: postOrganizationsOrgNameDevelopersDeveloperName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-name-post
      parameters:
      - in: query
        name: action
        description: Set the status
      - in: query
        name: Content-Type
        description: Specify Content Type
      - in: path
        name: developer_name
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
    delete:
      summary: Delete Organizations Name Developers Developer Name
      description: Deletes a developer from an Organization.
      operationId: deleteOrganizationsOrgNameDevelopersDeveloperName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-name-delete
      parameters:
      - in: path
        name: developer_name
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
  /organizations/{org_name}/developers/{developer_email}/apps:
    get:
      summary: Get Organizations Name Developers Developer Email Apps
      description: Provides an expanded view of a developer's collection of apps .
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailApps
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailapps-get
      parameters:
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: query
        name: expand
        description: Mention expand value as true
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - s
    post:
      summary: Post Organizations Name Developers Developer Email Apps
      description: Creates an app associated with a developer.
      operationId: postOrganizationsOrgNameDevelopersDeveloperEmailApps
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailapps-post
      parameters:
      - in: query
        name: Content-Type
        description: Specify the Content Type
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - s
  /organizations/{org_name}/developers/{developer_email}/apps/{app_name}:
    get:
      summary: Get Organizations Name Developers Developer Email Apps App Name
      description: Gets a count of all API resources in the API products accessible
        by a developer app .
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppsAppName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-name-get
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: query
        name: entity
        description: Specify the entity as API resources
      - in: path
        name: org_name
        description: Mention the organization name
      - in: query
        name: query
        description: Set query value to count
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
    put:
      summary: Put Organizations Name Developers Developer Email Apps App Name
      description: Updates the app to get a new set of consumer credentials.
      operationId: putOrganizationsOrgNameDevelopersDeveloperEmailAppsAppName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-name-put
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: query
        name: Content-Type
        description: Specify the Content Type
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
    post:
      summary: Post Organizations Name Developers Developer Email Apps App Name
      description: Revokes a Developer App, disabling access to all API Products .
      operationId: postOrganizationsOrgNameDevelopersDeveloperEmailAppsAppName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-name-post
      parameters:
      - in: query
        name: action
        description: Mention action as revoke
      - in: path
        name: app_name
        description: Mention the app name
      - in: query
        name: Content-Type
        description: Specify Content Type
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
    delete:
      summary: Delete Organizations Name Developers Developer Email Apps App Name
      description: Delete a Developer's App.
      operationId: deleteOrganizationsOrgNameDevelopersDeveloperEmailAppsAppName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-name-delete
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
  /organizations/{org_name}/developers/{developer_email}/apps/{app_name}/keys/{consumer_key}:
    get:
      summary: Get Organizations Name Developers Developer Email Apps App Name Keys
        Consumer Key
      description: Returns details for a consumer key for a developer app .
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameKeysConsumerKey
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-namekeysconsumer-key-get
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: consumer_key
        description: Mention the consumer key
      - in: path
        name: developer_email
        description: Mention the Developer Email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Keys
      - Consumer
      - Key
    post:
      summary: Post Organizations Name Developers Developer Email Apps App Name Keys
        Consumer Key
      description: Revokes a developer app key.
      operationId: postOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameKeysConsumerKey
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-namekeysconsumer-key-post
      parameters:
      - in: query
        name: action
        description: Mention action as revoke
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: consumer_key
        description: Mention the consumer key
      - in: query
        name: Content-Type
        description: Specify Content Type
      - in: path
        name: developer_email
        description: Mention the Developer Email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Keys
      - Consumer
      - Key
    delete:
      summary: Delete Organizations Name Developers Developer Email Apps App Name
        Keys Consumer Key
      description: Deletes a consumer key that belongs to an app.
      operationId: deleteOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameKeysConsumerKey
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-namekeysconsumer-key-delete
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: consumer_key
        description: Mention the consumer key
      - in: path
        name: developer_email
        description: Mention the Developer Email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Keys
      - Consumer
      - Key
  /organizations/{org_name}/developers/{developer_email}/apps/{app_name}/keys/{consumer_key}/apiproducts/{apiproduct_name}:
    post:
      summary: Post Organizations Name Developers Developer Email Apps App Name Keys
        Consumer Key Apiproducts Apiproduct Name
      description: Revokes the association of an API Product with a Developer App's
        consumer key.
      operationId: postOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameKeysConsumerKeyApiproductsApiproductName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-namekeysconsumer-keyapiproductsapiproduct-name-post
      parameters:
      - in: query
        name: action
        description: Mention action as revoke
      - in: path
        name: apiproduct_name
        description: Mention the API Product name
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: consumer_key
        description: Mention the app name
      - in: query
        name: Content-Type
        description: Specify Content Type
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Keys
      - Consumer
      - Key
      - API
      - Products
      - API
      - Productss
    delete:
      summary: Delete Organizations Name Developers Developer Email Apps App Name
        Keys Consumer Key Apiproducts Apiproduct Name
      description: Removes an API product from a developer app key profile, and thereby
        renders the developer app unable to access the URIs defined in the API product
        specified.
      operationId: deleteOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameKeysConsumerKeyApiproductsApiproductNam
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-namekeysconsumer-keyapiproductsapiproduct-name-delete
      parameters:
      - in: path
        name: apiproduct_name
        description: Mention the API Product name
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: consumer_key
        description: Mention the app name
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Keys
      - Consumer
      - Key
      - API
      - Products
      - API
      - Productss
  /organizations/{org_name}/developers/{developer_email}/apps/{app_name}/oauth1accesstokens:
    get:
      summary: Get Organizations Name Developers Developer Email Apps App Name Oauth1accesstokens
      description: Get count of OAuth 1.0 access tokens for a developer's app.
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameOauth1accesstokens
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-nameoauth1accesstokens-get
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization Name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Oauth1accesstokens
  /organizations/{org_name}/developers/{developer_email}/apps/{app_name}/oauth2accesstokens:
    get:
      summary: Get Organizations Name Developers Developer Email Apps App Name Oauth2accesstokens
      description: Get count of    OAuth 2.0 access tokens for a developer's app.
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameOauth2accesstokens
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-nameoauth2accesstokens-get
      parameters:
      - in: query
        name: appName
        description: Mention the app name
      - in: query
        name: developerEmail
        description: Mention the developer email
      - in: query
        name: organizationName
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Oauth2accesstokens
  /organizations/{org_name}/developers/{developer_email}/apps/{app_name}/keys/{consumer_key}/oauth1accesstokens:
    get:
      summary: Get Organizations Name Developers Developer Email Apps App Name Keys
        Consumer Key Oauth1accesstokens
      description: Get count of OAuth 1.0 access tokens for a developer's app key.
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameKeysConsumerKeyOauth1accesstokens
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-namekeysconsumer-keyoauth1accesstokens-get
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: consumer_key
        description: Mention the consumer key
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Keys
      - Consumer
      - Key
      - Oauth1accesstokens
  /organizations/{org_name}/developers/{developer_email}/apps/{app_name}/keys/{consumer_key}/oauth2accesstokens:
    get:
      summary: Get Organizations Name Developers Developer Email Apps App Name Keys
        Consumer Key Oauth2accesstokens
      description: Get count of OAuth 2.0 access tokens for a developer's app key.
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameKeysConsumerKeyOauth2accesstokens
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappsapp-namekeysconsumer-keyoauth2accesstokens-get
      parameters:
      - in: path
        name: app_name
        description: Mention the app name
      - in: path
        name: consumer_key
        description: Mention the consumer key
      - in: path
        name: developer_email
        description: Mention the developer name
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - ""
      - Keys
      - Consumer
      - Key
      - Oauth2accesstokens
  /organizations/{org_name}/companies/{company_name}/developers:
    get:
      summary: Get Organizations Name Companies Company Name Developers
      description: Lists all developers associated with a company.
      operationId: getOrganizationsOrgNameCompaniesCompanyNameDevelopers
      x-api-path-slug: organizationsorg-namecompaniescompany-namedevelopers-get
      parameters:
      - in: path
        name: company_name
        description: Mention the company name
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Companies
      - Companies
      - Developers
    post:
      summary: Post Organizations Name Companies Company Name Developers
      description: Adds a developer to a company.
      operationId: postOrganizationsOrgNameCompaniesCompanyNameDevelopers
      x-api-path-slug: organizationsorg-namecompaniescompany-namedevelopers-post
      parameters:
      - in: path
        name: company_name
        description: Mention the company name
      - in: query
        name: Content-Type
        description: Specify the Content Type
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Companies
      - Companies
      - Developers
  /organizations/{org_name}/companies/{company_name}/developers/{developer_email}:
    delete:
      summary: Delete Organizations Name Companies Company Name Developers Developer
        Email
      description: Removes the association of a Developer with a Company.
      operationId: deleteOrganizationsOrgNameCompaniesCompanyNameDevelopersDeveloperEmail
      x-api-path-slug: organizationsorg-namecompaniescompany-namedevelopersdeveloper-email-delete
      parameters:
      - in: path
        name: company_name
        description: Mention the company name
      - in: query
        name: Developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Companies
      - Companies
      - Developers
      - Developer
      - Email
  /organizations/{org_name}/developers/{developer_email}/appfamilies:
    get:
      summary: Get Organizations Name Developers Developer Email Appfamilies
      description: An expanded list of all app families in an organization, listing
        Apps in the collection
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppfamilies
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappfamilies-get
      parameters:
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - Families
    post:
      summary: Post Organizations Name Developers Developer Email Appfamilies
      description: Creates an app family for developers.
      operationId: postOrganizationsOrgNameDevelopersDeveloperEmailAppfamilies
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappfamilies-post
      parameters:
      - in: query
        name: Content-Type
        description: Specify the content type
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - Families
  /organizations/{org_name}/developers/{developer_email}/appfamilies/{appfamily_name}:
    get:
      summary: Get Organizations Name Developers Developer Email Appfamilies Appfamily
        Name
      description: Gets a list of apps in an appfamily.
      operationId: getOrganizationsOrgNameDevelopersDeveloperEmailAppfamiliesAppfamilyName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappfamiliesappfamily-name-get
      parameters:
      - in: path
        name: appfamily_name
        description: Mention app family name
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - Families
      - Applications
      - family
    post:
      summary: Post Organizations Name Developers Developer Email Appfamilies Appfamily
        Name
      description: Updates an existing app family.
      operationId: postOrganizationsOrgNameDevelopersDeveloperEmailAppfamiliesAppfamilyName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappfamiliesappfamily-name-post
      parameters:
      - in: path
        name: appfamily_name
        description: Mention app family name
      - in: query
        name: Content-Type
        description: Specify the Content Type
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - Families
      - Applications
      - family
    delete:
      summary: Delete Organizations Name Developers Developer Email Appfamilies Appfamily
        Name
      description: Deletes an App Family and all Apps it contains.
      operationId: deleteOrganizationsOrgNameDevelopersDeveloperEmailAppfamiliesAppfamilyName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappfamiliesappfamily-name-delete
      parameters:
      - in: path
        name: appfamily_name
        description: Mention app family name
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - Families
      - Applications
      - family
  /organizations/{org_name}/developers/{developer_email}/appfamilies/{appfamily_name}/apps/{app_name}:
    delete:
      summary: Delete Organizations Name Developers Developer Email Appfamilies Appfamily
        Name Apps App Name
      description: Removes an App from an App Family.
      operationId: deleteOrganizationsOrgNameDevelopersDeveloperEmailAppfamiliesAppfamilyNameAppsAppName
      x-api-path-slug: organizationsorg-namedevelopersdeveloper-emailappfamiliesappfamily-nameappsapp-name-delete
      parameters:
      - in: path
        name: appfamily_name
        description: Mention app family name
      - in: path
        name: app_name
        description: Mention app name
      - in: path
        name: developer_email
        description: Mention the developer email
      - in: path
        name: org_name
        description: Mention the organization name
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Developers
      - Developer
      - Email
      - Applications
      - Families
      - Applications
      - family
      - Applications
      - ""
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