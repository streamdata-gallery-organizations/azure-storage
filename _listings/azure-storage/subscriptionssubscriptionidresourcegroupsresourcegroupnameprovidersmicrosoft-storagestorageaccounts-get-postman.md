{
  "info": {
    "name": "Azure Storage API Storage Accounts List By Resource Group",
    "_postman_id": "a7304717-2097-4219-afab-21b49bd5b18f",
    "description": "Lists all the storage accounts available under the given resource group. Note that storage keys are not returned; use the ListKeys operation for this.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "storage accounts resource group",
      "item": [
        {
          "id": "28084a78-c0b0-489d-834f-151eb90ab933",
          "name": "StorageAccounts_ListByResourceGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Storage/storageAccounts"
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
            "description": "Lists all the storage accounts available under the given resource group"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e0d22d63-2fef-46f6-8b04-260da0b3c929"
            }
          ]
        }
      ]
    }
  ]
}