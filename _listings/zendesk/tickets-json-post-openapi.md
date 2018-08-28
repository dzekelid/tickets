---
swagger: "2.0"
x-collection-name: Zendesk
x-complete: 0
info:
  title: Zendesk createTicket
  version: 1.0.0
  description: Create Ticket
host: '{host}.zendesk.com'
basePath: /api/v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tickets.json:
    post:
      summary: createTicket
      description: Create Ticket
      operationId: TicketsJsonPost
      x-api-path-slug: tickets-json-post
      parameters:
      - in: body
        name: ticket
        description: Ticket
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Support
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