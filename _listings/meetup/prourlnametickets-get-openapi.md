---
swagger: "2.0"
x-collection-name: Meetup
x-complete: 0
info:
  title: Meetup Search Issued Pro Tickets
  description: Redeemed chapter, redeemed member, status, and timestamp for tickets
    belonging to Pro organization.
  version: 1.0.0
host: api.meetup.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /pro/:urlname/tickets:
    get:
      summary: Search Issued Pro Tickets
      description: Redeemed chapter, redeemed member, status, and timestamp for tickets
        belonging to Pro organization.
      operationId: pro
      x-api-path-slug: prourlnametickets-get
      parameters:
      - in: query
        name: chapters
        description: 'Comma delimited positive integers: ids of redeemed chapters'
        type: string
      - in: query
        name: chapter_name
        description: 'String: partial or full name of the redeemed chapter'
        type: string
      - in: query
        name: country
        description: 'String: two-letter country code of the redeemed chapters'
        type: string
      - in: query
        name: status
        description: 'Comma delimited strings: ticket status, among the following:
          inactive, available, claimed, redeemed'
        type: string
      - in: query
        name: ticket_key
        description: 'String: full matching string of an issued ticket key'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Events
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