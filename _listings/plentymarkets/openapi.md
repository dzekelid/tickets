swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 1
info:
  title: plentymarkets REST-API
  description: the-plentymarkets-rest-api-expands-the-functionality-of-the-plentymarkets-cms-and-allows-access-to-resources-i-e--data-records-via-unique-uri-paths
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/tickets:
    get:
      summary: List tickets by filters
      description: List tickets by filters.
      operationId: getRestTickets
      x-api-path-slug: resttickets-get
      parameters:
      - in: query
        name: confidential
        description: Filter that restricts the search result to tickets of a specific
          confidential value
      - in: query
        name: contactId
        description: Filter that restricts the search result to tickets with a specified
          contact ID
      - in: query
        name: customerClassId
        description: Filter that restricts the search result to tickets with a specified
          customer class ID
      - in: query
        name: deadlineAt
        description: Filter that restricts the search result to tickets with a specified
          deadline
      - in: query
        name: fulltext
        description: Filter that restricts the search result to tickets with full-text
          search
      - in: query
        name: id
        description: Filter that restricts the search result to tickets of a specific
          ticket ID
      - in: query
        name: ownerId
        description: Filter that restricts the search result to tickets with a specified
          owner ID
      - in: query
        name: parentTicketId
        description: Filter that restricts the search result to tickets with a specified
          parent ticket ID
      - in: query
        name: plentyId
        description: Filter that restricts the search result to tickets with a specified
          client (store) ID
      - in: query
        name: priorityId
        description: Filter that restricts the search result to tickets of a specific
          ticket priority ID
      - in: query
        name: progress
        description: Filter that restricts the search result to tickets with a specified
          progress in percent
      - in: query
        name: resubmissionAt
        description: Filter that restricts the search result to tickets with a specified
          resubmission date
      - in: query
        name: roleId
        description: Filter that restricts the search result to tickets with a specified
          role ID
      - in: query
        name: source
        description: Filter that restricts the search result to tickets with a specific
          source value
      - in: query
        name: statusGroupId
        description: Filter that restricts the search result to tickets with a specified
          status group ID
      - in: query
        name: statusId
        description: Filter that restricts the search result to tickets with a specified
          status ID
      - in: query
        name: title
        description: Filter that restricts the search result to tickets with a specified
          phrase in title
      - in: query
        name: typeId
        description: Filter that restricts the search result to tickets of specific
          ticket types
      responses:
        200:
          description: OK
      tags:
      - List
      - Tickets
      - By
      - Filters
    post:
      summary: Create a ticket
      description: Create a ticket.
      operationId: postRestTickets
      x-api-path-slug: resttickets-post
      parameters:
      - in: body
        name: /rest/tickets
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Ticket
  /rest/boards/{boardId}/columns/{columnId}/tasks/{taskId}/references:
    post:
      summary: Creates a new reference from a given task to a contact or a ticket.
      description: Creates a new reference from a given task to a contact or a ticket..
      operationId: postRestBoardsBoardColumnsColumnTasksTaskReferences
      x-api-path-slug: restboardsboardidcolumnscolumnidtaskstaskidreferences-post
      parameters:
      - in: path
        name: boardId
      - in: path
        name: columnId
      - in: query
        name: referenceValue
        description: Reference type followed by foreign ID of the referenced object
      - in: path
        name: taskId
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Reference
      - From
      - Given
      - Task
      - To
      - Contact
      - Ticket
  /rest/tickets/{ticketId}:
    put:
      summary: Update a ticket
      description: Updates a ticket. The ID of the ticket must be specified.
      operationId: putRestTicketsTicket
      x-api-path-slug: restticketsticketid-put
      parameters:
      - in: path
        name: ticketId
      responses:
        200:
          description: OK
      tags:
      - Ticket