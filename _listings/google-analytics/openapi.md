---
swagger: "2.0"
x-collection-name: Google Analytics
x-complete: 1
info:
  title: Google Analytics
  description: views-and-manages-your-google-analytics-data
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
---