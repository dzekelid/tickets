{
  "info": {
    "name": "GIGANDCROWD Get Ticket",
    "_postman_id": "a1c75695-82c6-498f-b4be-a8b4b3b2cd9f",
    "description": "Get ticket.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Ticket",
      "item": [
        {
          "id": "f687774f-8b8b-40e5-93fe-d623692f3647",
          "name": "getApiV1TicketTicket",
          "request": {
            "url": {
              "protocol": "http",
              "host": "gigandcrowd.com",
              "path": [
                "api/v1/ticket/:ticketId"
              ],
              "variable": [
                {
                  "id": "ticketId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get ticket ticketid."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c4a5b873-6acc-4b46-b116-89c116470edc"
            }
          ]
        },
        {
          "id": "e134c18e-3686-40f4-abc6-babc2b6ecbe7",
          "name": "deleteApiV1TicketEventTicket",
          "request": {
            "url": {
              "protocol": "http",
              "host": "gigandcrowd.com",
              "path": [
                "api/v1/ticket/:eventId/:ticketId"
              ],
              "variable": [
                {
                  "id": "eventId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "ticketId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "DELETE",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Delete ticket eventid ticketid."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c5b4c0ec-c965-40a4-8c98-f49b1c42e640"
            }
          ]
        },
        {
          "id": "a897a9c6-9d7c-4af2-a94e-4b19c49e4a05",
          "name": "getApiV1TicketEvent",
          "request": {
            "url": {
              "protocol": "http",
              "host": "gigandcrowd.com",
              "path": [
                "api/v1/ticket/:eventId"
              ],
              "query": [
                {
                  "key": "from",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "eventId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get ticket eventid."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "516240c5-b8dd-4554-85ae-5ad7fcc5fc1c"
            }
          ]
        },
        {
          "id": "2adbcc10-e2f6-4d3d-b189-7520366a17df",
          "name": "getApiV1TicketEventExport",
          "request": {
            "url": {
              "protocol": "http",
              "host": "gigandcrowd.com",
              "path": [
                "api/v1/ticket/:eventId/export"
              ],
              "query": [
                {
                  "key": "from",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "to",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "eventId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get ticket eventid export."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "2baba46b-b410-4841-b7b4-9cf1b3988d97"
            }
          ]
        },
        {
          "id": "25c6d344-212a-4c20-95db-8c8e3e4a375b",
          "name": "getApiV1Ticket",
          "request": {
            "url": "http://gigandcrowd.com/api/v1/Ticket?from=%7B%7D&to=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Authorization",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get ticket."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70e65f54-b112-4561-ba54-cea0ba16b6d6"
            }
          ]
        }
      ]
    }
  ]
}