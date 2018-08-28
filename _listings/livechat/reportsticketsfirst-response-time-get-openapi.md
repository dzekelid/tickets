---
swagger: "2.0"
x-collection-name: LiveChat
x-complete: 0
info:
  title: LiveChat Tickets first response time
  description: Shows the time of the first response to the tickets that were responded
    to for the first time during the specified period.
  version: 1.0.0
host: api.livechatinc.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /reports/tickets/new_tickets:
    get:
      summary: New tickets
      description: Shows the number of the tickets created during the specified period.
      operationId: ReportsTicketsNewTicketsGet
      x-api-path-slug: reportsticketsnew-tickets-get
      parameters:
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: query
        name: group_by
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - New
      - Tickets
  /reports/tickets/first_response_time:
    get:
      summary: Tickets first response time
      description: Shows the time of the first response to the tickets that were responded
        to for the first time during the specified period.
      operationId: ReportsTicketsFirstResponseTimeGet
      x-api-path-slug: reportsticketsfirst-response-time-get
      parameters:
      - in: query
        name: agent
      - in: query
        name: date_from
      - in: query
        name: date_to
      - in: header
        name: X-API-Version
      responses:
        200:
          description: OK
      tags:
      - Tickets
      - First
      - Response
      - Time
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