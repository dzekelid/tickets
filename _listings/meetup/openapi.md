---
swagger: "2.0"
x-collection-name: Meetup
x-complete: 1
info:
  title: Meetup
  description: the-meetup-api-provides-simple-restful-http-and-streaming-interfaces-for-exploring-and-interacting-meetup-platform-from-your-own-apps--the-api-is-a-set-of-core-methods-and-a-common-request-format--these-are-combined-to-form-a-url-that-returns-the-information-you-want--
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
---