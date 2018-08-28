---
swagger: "2.0"
x-collection-name: AWS Route 53
x-complete: 0
info:
  title: AWS Route 53 API Get Checker Ip Ranges
  version: 1.0.0
  description: GetCheckerIpRanges still works, but we recommend that you download
    ip-ranges.json, which includes IP address ranges for all AWS services. For more
    information, see IP Address Ranges of Amazon Route 53 Servers in the Amazon Route
    53 Developer Guide.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/checkeripranges:
    get:
      summary: Get Checker Ip Ranges
      description: GetCheckerIpRanges still works, but we recommend that you download
        ip-ranges.json, which includes IP address ranges for all AWS services. For
        more information, see IP Address Ranges of Amazon Route 53 Servers in the
        Amazon Route 53 Developer Guide.
      operationId: getcheckeripranges
      x-api-path-slug: 20130401checkeripranges-get
      responses:
        200:
          description: OK
      tags:
      - IP Ranges
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