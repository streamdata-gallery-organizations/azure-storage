{
  "info": {
    "name": "Azure Storage API Jobs List By Resource Group",
    "_postman_id": "0e5f1fd9-dbe4-465b-86e2-d89b310f6767",
    "description": "Returns all active and completed import/export jobs in a resource group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "jobs resource group",
      "item": [
        {
          "id": "91ec73cf-e788-4ac8-98e8-ef98d4697e19",
          "name": "Jobs_ListByResourceGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ImportExport/jobs"
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
                },
                {
                  "id": "resourceGroupName",
                  "value": "resourceGroupName",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns all active and completed import/export jobs in a resource group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bb855c00-665e-404d-b7de-f34142b89857"
            }
          ]
        }
      ]
    }
  ]
}