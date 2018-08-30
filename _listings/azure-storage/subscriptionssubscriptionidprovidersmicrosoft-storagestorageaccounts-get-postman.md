{
  "info": {
    "name": "Azure Storage API Storage Accounts List",
    "_postman_id": "2ceb3b0d-c4d0-40e9-9ca1-3a8c5fe8f6c4",
    "description": "Lists all the storage accounts available under the subscription. Note that storage keys are not returned; use the ListKeys operation for this.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "storage accounts",
      "item": [
        {
          "id": "e2e93aaf-f22d-45f5-8696-282b3b8f2096",
          "name": "StorageAccounts_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.Storage/storageAccounts"
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
            "description": "Lists all the storage accounts available under the subscription"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "30a0491f-db49-4a78-9acb-af5124af6035"
            }
          ]
        }
      ]
    }
  ]
}