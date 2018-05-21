{
  "info": {
    "name": "Azure Storage API Jobs List",
    "_postman_id": "48207089-814f-4c5a-86af-42c1ba6f2f91",
    "description": "Gets all the active and completed import/export jobs in a subscription.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "jobs",
      "item": [
        {
          "id": "0b0459c3-b6d6-42e8-b909-977dccd28315",
          "name": "Jobs_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.ImportExport/jobs"
              ],
              "query": [
                {
                  "key": "$filter",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "$top",
                  "value": "%7B%7D",
                  "disabled": false
                },
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
            "description": "Gets all the active and completed import/export jobs in a subscription"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fb0cdd04-3b81-43a0-8ad4-15d915a5d17e"
            }
          ]
        }
      ]
    }
  ]
}