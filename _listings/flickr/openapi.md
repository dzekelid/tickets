---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 1
info:
  title: Flickr
  description: explore-upload-and-organize-photos-on-flickr
  version: 1.0.0
host: api.flickr.com
basePath: /services/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/?method=flickr.photos.upload.checkTickets:
    get:
      summary: Photos Upload Check Tickets
      description: Checks the status of one or more asynchronous photo upload tickets.
      operationId: getRestMethodFlickr.photos.upload.checktickets
      x-api-path-slug: restmethodflickr-photos-upload-checktickets-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      - in: query
        name: tickets
        description: A comma-delimited list of ticket ids
      responses:
        200:
          description: OK
      tags:
      - Photos
      - Upload
      - CheckTickets
---