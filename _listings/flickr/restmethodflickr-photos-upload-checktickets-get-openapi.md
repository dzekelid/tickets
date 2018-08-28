---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 0
info:
  title: Flickr Photos Upload Check Tickets
  description: Checks the status of one or more asynchronous photo upload tickets.
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