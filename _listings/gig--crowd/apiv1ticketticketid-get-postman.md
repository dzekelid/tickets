{
  "info": {
    "name": "GIGANDCROWD Get Ticket Ticketid",
    "_postman_id": "058c3552-f9d4-42ef-a079-cdb1d22e82cf",
    "description": "Get ticket ticketid.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Ticket",
      "item": [
        {
          "id": "2900776c-5a4c-4847-b2f8-b31d6e41ab78",
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
              "id": "51842c6e-b310-4819-a373-0db9efe0a6c9"
            }
          ]
        }
      ]
    }
  ]
}