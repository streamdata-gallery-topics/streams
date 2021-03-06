---
swagger: "2.0"
info:
  title: Azure Automation API Test Job Streams Get
  version: 1.0.0
  description: Retrieve a test job streams identified by runbook name and stream id.
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Automation/automationAccounts/{automationAccountName}/runbooks/{runbookName}/draft/testJob/streams/{jobStreamId}
  : get:
      summary: Test Job Streams Get
      description: Retrieve a test job streams identified by runbook name and stream
        id
      operationId: TestJobStreams_Get
      parameters:
      - in: path
        name: automationAccountName
        description: The automation account name
      - in: path
        name: jobStreamId
        description: The job stream id
      - in: query
        name: No Name
      - in: path
        name: runbookName
        description: The runbook name
      responses:
        200:
          description: OK
      tags:
      - test
      - job
      - streams
definitions:
  ActivityParameter:
    properties: []
x-collection-name: Azure Automation
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