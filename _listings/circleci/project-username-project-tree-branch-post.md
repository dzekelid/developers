---
swagger: "2.0"
info:
  title: CircleCI
  description: The CircleCI API is a RESTful, fully-featured API that allows you to
    do almost anything in CircleCI. You can access all information and trigger all
    actions. The only thing we don&rsquo;t provide access to is billing functions,
    which must be done from the CircleCI web UI.
  version: 1.0.0
host: circleci.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /project/{username}/{project}/tree/{branch}:
    post:
      summary: ""
      description: Triggers a new build, returns a summary of the build
      operationId: triggers-a-new-build-returns-a-summary-of-the-buildoptional-build-parameters-can-be-set-using-an-exp
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - ""
definitions:
  Artifact:
    properties:
      node_index:
        description: This is a default description.
        type: post
      path:
        description: This is a default description.
        type: post
      pretty_path:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  Aws:
    properties:
      keypair:
        description: This is a default description.
        type: post
  Build:
    properties:
      body:
        description: This is a default description.
        type: post
      branch:
        description: This is a default description.
        type: post
      build_time_millis:
        description: This is a default description.
        type: post
      build_url:
        description: This is a default description.
        type: post
      committer_email:
        description: This is a default description.
        type: post
      committer_name:
        description: This is a default description.
        type: post
      dont_build:
        description: This is a default description.
        type: post
      queued_at:
        description: This is a default description.
        type: post
      reponame:
        description: This is a default description.
        type: post
      retry_of:
        description: This is a default description.
        type: post
  BuildDetail:
    properties:
      compare:
        description: This is a default description.
        type: post
      job_name:
        description: This is a default description.
        type: post
      node:
        description: This is a default description.
        type: post
      retries:
        description: This is a default description.
        type: post
      ssh_enabled:
        description: This is a default description.
        type: post
      timedout:
        description: This is a default description.
        type: post
      usage_queued_at:
        description: This is a default description.
        type: post
  BuildSummary:
    properties:
      added_at:
        description: This is a default description.
        type: post
      build_num:
        description: This is a default description.
        type: post
      pushed_at:
        description: This is a default description.
        type: post
  CommitDetail:
    properties:
      author_date:
        description: This is a default description.
        type: post
      author_email:
        description: This is a default description.
        type: post
      author_login:
        description: This is a default description.
        type: post
      author_name:
        description: This is a default description.
        type: post
      body:
        description: This is a default description.
        type: post
      commit_url:
        description: This is a default description.
        type: post
      committer_date:
        description: This is a default description.
        type: post
      committer_email:
        description: This is a default description.
        type: post
      committer_login:
        description: This is a default description.
        type: post
      committer_name:
        description: This is a default description.
        type: post
  Envvar:
    properties:
      name:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
  Key:
    properties:
      fingerprint:
        description: This is a default description.
        type: post
      preferred:
        description: This is a default description.
        type: post
      public_key:
        description: This is a default description.
        type: post
      time:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  PreviousBuild:
    properties:
      build_num:
        description: This is a default description.
        type: post
      build_time_millis:
        description: This is a default description.
        type: post
  Project:
    properties:
      branches:
        description: This is a default description.
        type: post
      compile:
        description: This is a default description.
        type: post
      default_branch:
        description: This is a default description.
        type: post
      dependencies:
        description: This is a default description.
        type: post
      extra:
        description: This is a default description.
        type: post
      feature_flags:
        description: This is a default description.
        type: post
      followed:
        description: This is a default description.
        type: post
      has_usable_key:
        description: This is a default description.
        type: post
      hipchat_notify_prefs:
        description: This is a default description.
        type: post
      language:
        description: This is a default description.
        type: post
  Tests:
    properties:
      tests:
        description: This is a default description.
        type: post
  User:
    properties:
      admin:
        description: This is a default description.
        type: post
      all_emails:
        description: This is a default description.
        type: post
      analytics_id:
        description: This is a default description.
        type: post
      avatar_url:
        description: This is a default description.
        type: post
      basic_email_prefs:
        description: This is a default description.
        type: post
      bitbucket:
        description: This is a default description.
        type: post
      bitbucket_authorized:
        description: This is a default description.
        type: post
      containers:
        description: This is a default description.
        type: post
      created_at:
        description: This is a default description.
        type: post
      days_left_in_trial:
        description: This is a default description.
        type: post
x-collection-name: CircleCI
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