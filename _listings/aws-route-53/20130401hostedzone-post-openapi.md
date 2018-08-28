---
swagger: "2.0"
x-collection-name: AWS Route 53
x-complete: 0
info:
  title: AWS Route 53 API Create Hosted Zone
  version: 1.0.0
  description: Creates a new public hosted zone, used to specify how the Domain Name
    System (DNS)routes traffic on the Internet for a domain, such as example.com,
    and its subdomains. ImportantPublic hosted zones can't be converted to a private
    hosted zone or vice versa.Instead, create a new hosted zone with the same name
    and create new resource recordsets.Send a POST request to the /2013-04-01/hostedzone
    resource. The request body must include a documentwith a CreateHostedZoneRequest
    element. The response returns theCreateHostedZoneResponse element containing metadata
    about the hostedzone.Fore more information about charges for hosted zones, see
    Amazon Route 53 Pricing.Note the following:You can't create a hosted zone for
    a top-level domain (TLD).Amazon Route 53 automatically creates a default SOA record
    and four NS records for the zone.For more information about SOA and NS records,
    see NS and SOA Records that Amazon Route 53 Creates for a Hosted Zone in the Amazon
    Route 53 Developer Guide.If your domain is registered with a registrar other than
    Amazon Route 53, you must update thename servers with your registrar to make Amazon
    Route 53 your DNS service. For more information, seeConfiguring Amazon Route 53
    as your DNSService in the Amazon Route 53 Developer's Guide.After creating a zone,
    its initial status is PENDING. This means that itis not yet available on all DNS
    servers. The status of the zone changes to INSYNCwhen the NS and SOA records are
    available on all Amazon Route 53 DNS servers. When trying to create a hosted zone
    using a reusable delegation set, specify anoptional DelegationSetId, and Amazon
    Route 53 would assign those 4 NS records for the zone, instead ofallotting a new
    one.
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
  /2013-04-01/healthcheck/HealthCheckId:
    delete:
      summary: Delete Health Check
      description: Deletes a health check. Send a DELETE request to the/2013-04-01/healthcheck/health
        check ID            resource.ImportantAmazon Route 53 does not prevent you
        from deleting a health check even if the health check isassociated with one
        or more resource record sets. If you delete a health check and you don'tupdate
        the associated resource record sets, the future status of the health check
        can't bepredicted and may change. This will affect the routing of DNS queries
        for your DNS failoverconfiguration. For more information, see Replacing and
        Deleting Health Checks in the Amazon Route 53 Developer Guide.
      operationId: deletehealthcheck
      x-api-path-slug: 20130401healthcheckhealthcheckid-delete
      parameters:
      - in: path
        name: HealthCheckId
        description: The ID of the health check that you want to delete
        type: string
      responses:
        200:
          description: OK
      tags:
      - Checks
      - Health
    get:
      summary: Get Health Check
      description: Gets information about a specified health check. Send a GET request
        to the/2013-04-01/healthcheck/health check ID             resource. Formore
        information about using the console to perform this operation, see Amazon
        Route 53 Health Checks and DNS Failover in theAmazon Route 53 Developer Guide.
      operationId: gethealthcheck
      x-api-path-slug: 20130401healthcheckhealthcheckid-get
      parameters:
      - in: path
        name: HealthCheckId
        description: The identifier that Amazon Route 53 assigned to the health check
          when you created it
        type: string
      responses:
        200:
          description: OK
      tags:
      - Checks
      - Health
    post:
      summary: Update Health Check
      description: Updates an existing health check.Send a POST request to the /2013-04-01/healthcheck/health
        check ID             resource. Therequest body must include a document with
        an UpdateHealthCheckRequestelement. For more information about updating health
        checks, see Creating, Updating, and DeletingHealth Checks in the Amazon Route
        53 Developer Guide.
      operationId: updatehealthcheck
      x-api-path-slug: 20130401healthcheckhealthcheckid-post
      parameters:
      - in: body
        name: AlarmIdentifier
        description: A complex type that identifies the CloudWatch alarm that you
          want Amazon Route 53 health checkers touse to determine whether this health
          check is healthy
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: ChildHealthChecks
        description: A complex type that contains one ChildHealthCheck element for
          each healthcheck that you want to associate with a CALCULATED health check
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: EnableSNI
        description: Specify whether you want Amazon Route 53 to send the value ofFullyQualifiedDomainName
          to the endpoint in the client_hellomessage during TLS negotiation
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: FailureThreshold
        description: The number of consecutive health checks that an endpoint must
          pass or fail for Amazon Route 53 tochange the current status of the endpoint
          from unhealthy to healthy or vice versa
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: FullyQualifiedDomainName
        description: Amazon Route 53 behavior depends on whether you specify a value
          for IPAddress
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: HealthCheckId
        description: The ID for the health check for which you want detailed information
        type: string
      - in: body
        name: HealthCheckVersion
        description: A sequential counter that Amazon Route 53 sets to 1 when you
          create a health checkand increments by 1 each time you update settings for
          the health check
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: HealthThreshold
        description: The number of child health checks that are associated with a
          CALCULATEDhealth that Amazon Route 53 must consider healthy for the CALCULATED
          health check to beconsidered healthy
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: InsufficientDataHealthStatus
        description: 'When CloudWatch has insufficient data about the metric to determine
          the alarm state, the status that you want Amazon Route 53 to assign to the
          health check:                        Healthy: Amazon Route 53 considers
          the health check to be healthy'
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Inverted
        description: Specify whether you want Amazon Route 53 to invert the status
          of a health check, for example, toconsider a health check unhealthy when
          it otherwise would be considered healthy
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: IPAddress
        description: The IPv4 or IPv6 IP address for the endpoint that you want Amazon
          Route 53 to perform health checks on
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Port
        description: The port on the endpoint on which you want Amazon Route 53 to
          perform health checks
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Regions
        description: A complex type that contains one Region element for each region
          from which you wantAmazon Route 53 health checkers to check the specified
          endpoint
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: ResourcePath
        description: The path that you want Amazon Route 53 to request when performing
          health checks
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: SearchString
        description: If the value of Type is HTTP_STR_MATCH orHTTP_STR_MATCH, the
          string that you want Amazon Route 53 to search for in the responsebody from
          the specified resource
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: UpdateHealthCheckRequest
        description: Root level tag for the UpdateHealthCheckRequest parameters
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Checks
      - Health
  /2013-04-01/hostedzone:
    post:
      summary: Create Hosted Zone
      description: Creates a new public hosted zone, used to specify how the Domain
        Name System (DNS)routes traffic on the Internet for a domain, such as example.com,
        and its subdomains. ImportantPublic hosted zones can't be converted to a private
        hosted zone or vice versa.Instead, create a new hosted zone with the same
        name and create new resource recordsets.Send a POST request to the /2013-04-01/hostedzone
        resource. The request body must include a documentwith a CreateHostedZoneRequest
        element. The response returns theCreateHostedZoneResponse element containing
        metadata about the hostedzone.Fore more information about charges for hosted
        zones, see Amazon Route 53 Pricing.Note the following:You can't create a hosted
        zone for a top-level domain (TLD).Amazon Route 53 automatically creates a
        default SOA record and four NS records for the zone.For more information about
        SOA and NS records, see NS and SOA Records that Amazon Route 53 Creates for
        a Hosted Zone in the Amazon Route 53 Developer Guide.If your domain is registered
        with a registrar other than Amazon Route 53, you must update thename servers
        with your registrar to make Amazon Route 53 your DNS service. For more information,
        seeConfiguring Amazon Route 53 as your DNSService in the Amazon Route 53 Developer's
        Guide.After creating a zone, its initial status is PENDING. This means that
        itis not yet available on all DNS servers. The status of the zone changes
        to INSYNCwhen the NS and SOA records are available on all Amazon Route 53
        DNS servers. When trying to create a hosted zone using a reusable delegation
        set, specify anoptional DelegationSetId, and Amazon Route 53 would assign
        those 4 NS records for the zone, instead ofallotting a new one.
      operationId: createhostedzone
      x-api-path-slug: 20130401hostedzone-post
      parameters:
      - in: body
        name: CallerReference
        description: A unique string that identifies the request and that allows failedCreateHostedZone
          requests to be retried without the risk of executing theoperation twice
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: CreateHostedZoneRequest
        description: Root level tag for the CreateHostedZoneRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Default
        description: None
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: DelegationSetId
        description: If you want to associate a reusable delegation set with this
          hosted zone, the ID thatAmazon Route 53 assigned to the reusable delegation
          set when you created it
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: HostedZoneConfig
        description: (Optional) A complex type that contains an optional comment about
          your hosted zone
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Name
        description: The name of the domain
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Parent
        description: CreatedHostedZoneRequest
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: VPC
        description: The VPC that you want your hosted zone to be associated with
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Hosted Zones
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