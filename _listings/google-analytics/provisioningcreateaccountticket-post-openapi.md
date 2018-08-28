---
swagger: "2.0"
x-collection-name: Google Analytics
x-complete: 0
info:
  title: Google Analytics Create Account Ticket
  description: Creates an account ticket.
  contact:
    name: Google
    url: https://google.com
  version: v3
host: www.googleapis.com
basePath: /analytics/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /provisioning/createAccountTicket:
    post:
      summary: Create Account Ticket
      description: Creates an account ticket.
      operationId: analytics.provisioning.createAccountTicket
      x-api-path-slug: provisioningcreateaccountticket-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Tickets
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