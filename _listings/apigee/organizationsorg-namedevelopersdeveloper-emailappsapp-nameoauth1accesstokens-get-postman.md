{
  "info": {
    "name": "Apigee Edge Get Organizations Name Developers Developer Email Apps App Name Oauth1accesstokens",
    "_postman_id": "c2d8c702-c5c4-481f-aa6c-80557c8ff141",
    "description": "Get count of OAuth 1.0 access tokens for a developer's app.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizations",
      "item": [
        {
          "id": "3a163772-9e40-4050-a044-ad3f3b9078fb",
          "name": "getOrganizationsOrgNameDevelopersDeveloperEmailAppsAppNameOauth1accesstokens",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.enterprise.apigee.com",
              "path": [
                "v1",
                "organizations/:org_name/developers/:developer_email/apps/:app_name/oauth1accesstokens"
              ],
              "variable": [
                {
                  "id": "app_name",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "developer_email",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "org_name",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get count of OAuth 1.0 access tokens for a developer's app."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "15f3fdd3-0fb0-4a8f-b9e3-a8828dd8e4bc"
            }
          ]
        }
      ]
    }
  ]
}