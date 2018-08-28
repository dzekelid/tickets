---
swagger: "2.0"
x-collection-name: Eventbrite
x-complete: 0
info:
  title: Eventbrite Get User List Tickets
  description: This method lists the tickets purchased by the authenticated user.
    Each transaction is an order in our system and an order may contain one or more
    tickets. Tickets to free events are included.
  version: 1.0.0
host: www.eventbrite.com
basePath: /%7Bdata-type%7D/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /user_list_tickets:
    get:
      summary: Get User List Tickets
      description: This method lists the tickets purchased by the authenticated user.
        Each transaction is an order in our system and an order may contain one or
        more tickets. Tickets to free events are included.
      operationId: Get_user_list_tickets_
      x-api-path-slug: user-list-tickets-get
      parameters:
      - in: query
        name: data-type
        description: xml or json data-types are supported
      responses:
        200:
          description: OK
      tags:
      - User
      - List
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