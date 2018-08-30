{
  "info": {
    "name": "Azure Storage API Storage Accounts List Keys",
    "_postman_id": "b4c28570-5b0b-491c-a195-0fb9259a4970",
    "description": "Lists the access keys for the specified storage account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "storage accounts keys",
      "item": [
        {
          "id": "08b811b8-fffe-46fb-b0b2-9af3080865c7",
          "name": "StorageAccounts_ListKeys",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.Storage/storageAccounts/:accountName/listKeys"
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Lists the access keys for the specified storage account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0225a278-850a-4783-ba72-8d424cc8faec"
            }
          ]
        }
      ]
    }
  ]
}