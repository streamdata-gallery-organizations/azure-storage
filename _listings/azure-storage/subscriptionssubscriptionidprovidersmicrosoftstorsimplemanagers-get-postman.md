{
  "info": {
    "name": "Azure Storage API Managers List",
    "_postman_id": "efba942a-0790-4146-b07b-25311dc8e1ef",
    "description": "Retrieves all the managers in a subscription.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Managers",
      "item": [
        {
          "id": "bf3110b6-1164-42a2-b54f-010465e18a30",
          "name": "Managers_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.StorSimple/managers"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Retrieves all the managers in a subscription."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "660afa56-fe18-4bc9-bdc8-e46260c05e4d"
            }
          ]
        }
      ]
    }
  ]
}