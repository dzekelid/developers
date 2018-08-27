---
swagger: "2.0"
x-collection-name: Apigee
x-complete: 0
info:
  title: Apigee Edge Get Organizations Name Developers
  description: Gets the developer profile by registered date.
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