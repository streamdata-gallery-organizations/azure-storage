{
  "info": {
    "name": "Azure Storage API Storage Accounts Delete",
    "_postman_id": "491e4b8f-c5b7-4b0c-a0d9-b91ecbf8fb13",
    "description": "Deletes a storage account in Microsoft Azure.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "storage accounts",
      "item": [
        {
          "id": "fe70cff4-93e9-49e0-b7cf-1322f56e4557",
          "name": "StorageAccounts_Delete",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Storage/storageAccounts/:accountName"
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
                  "id": "accountName",
                  "value": "{}",
                  "type": "string"
                },
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a storage account in Microsoft Azure"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "38c65438-9e12-46d5-9d5b-b48d1b68c7db"
            }
          ]
        }
      ]
    }
  ]
}