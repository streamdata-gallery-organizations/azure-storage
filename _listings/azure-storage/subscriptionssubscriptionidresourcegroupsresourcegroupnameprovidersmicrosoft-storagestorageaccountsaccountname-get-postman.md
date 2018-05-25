{
  "info": {
    "name": "Azure Storage API Storage Accounts Get Properties",
    "_postman_id": "ae6db021-066c-41a3-a05b-43195cef6f59",
    "description": "Returns the properties for the specified storage account including but not limited to name, SKU name, location, and account status. The ListKeys operation should be used to retrieve storage keys.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "storage accounts properties",
      "item": [
        {
          "id": "24d2fbe3-4e52-4a53-9535-0c88212810e4",
          "name": "StorageAccounts_GetProperties",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the properties for the specified storage account including but not limited to name, SKU name, location, and account status"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "88157799-42d3-43ba-a7ad-0ff58bbcf1bf"
            }
          ]
        }
      ]
    }
  ]
}