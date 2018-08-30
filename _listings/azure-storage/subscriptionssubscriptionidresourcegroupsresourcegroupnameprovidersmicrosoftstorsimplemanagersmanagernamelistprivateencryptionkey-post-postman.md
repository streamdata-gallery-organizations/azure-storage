{
  "info": {
    "name": "Azure Storage API Managers Get Private Encryption Key",
    "_postman_id": "6c8fb15c-708f-4f4f-9b3f-e9173db22a9a",
    "description": "Returns the symmetric encrypted private encryption key of the manager.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "managers private encryption key",
      "item": [
        {
          "id": "939be106-10c4-447a-ac83-2131f3d3ac3e",
          "name": "Managers_GetPrivateEncryptionKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.StorSimple/managers/:managerName/listPrivateEncryptionKey"
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
                },
                {
                  "id": "managerName",
                  "value": "managerName",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the symmetric encrypted private encryption key of the manager"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b1cfb0fe-4124-4f64-bb77-d517f49c0ad8"
            }
          ]
        }
      ]
    }
  ]
}