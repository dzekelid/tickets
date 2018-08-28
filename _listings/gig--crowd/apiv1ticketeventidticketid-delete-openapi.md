---
swagger: "2.0"
x-collection-name: GIG & CROWD
x-complete: 0
info:
  title: GIGANDCROWD Delete Ticket Eventid Ticketid
  version: 1.0.0
  description: Delete ticket eventid ticketid.
host: gigandcrowd.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/ticket/{ticketId}:
    get:
      summary: Get Ticket Ticketid
      description: Get ticket ticketid.
      operationId: getApiV1TicketTicket
      x-api-path-slug: apiv1ticketticketid-get
      parameters:
      - in: header
        name: Authorization
      - in: path
        name: ticketId
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Ticketid
  /api/v1/ticket/{eventId}/{ticketId}:
    delete:
      summary: Delete Ticket Eventid Ticketid
      description: Delete ticket eventid ticketid.
      operationId: deleteApiV1TicketEventTicket
      x-api-path-slug: apiv1ticketeventidticketid-delete
      parameters:
      - in: header
        name: Authorization
      - in: path
        name: eventId
      - in: path
        name: ticketId
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Eventid
      - Ticketid
  /api/v1/ticket/{eventId}:
    get:
      summary: Get Ticket Eventid
      description: Get ticket eventid.
      operationId: getApiV1TicketEvent
      x-api-path-slug: apiv1ticketeventid-get
      parameters:
      - in: header
        name: Authorization
      - in: path
        name: eventId
      - in: query
        name: from
      - in: query
        name: to
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Eventid
  /api/v1/ticket/{eventId}/export:
    get:
      summary: Get Ticket Eventid Export
      description: Get ticket eventid export.
      operationId: getApiV1TicketEventExport
      x-api-path-slug: apiv1ticketeventidexport-get
      parameters:
      - in: header
        name: Authorization
      - in: path
        name: eventId
      - in: query
        name: from
      - in: query
        name: to
      responses:
        200:
          description: OK
      tags:
      - Ticket
      - Eventid
      - Export
  /api/v1/Ticket:
    get:
      summary: Get Ticket
      description: Get ticket.
      operationId: getApiV1Ticket
      x-api-path-slug: apiv1ticket-get
      parameters:
      - in: header
        name: Authorization
      - in: query
        name: from
      - in: query
        name: to
      responses:
        200:
          description: OK
      tags:
      - Ticket
    post:
      summary: Post Ticket
      description: Post ticket.
      operationId: postApiV1Ticket
      x-api-path-slug: apiv1ticket-post
      parameters:
      - in: header
        name: Authorization
      - in: body
        name: request
        description: ','
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Ticket
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