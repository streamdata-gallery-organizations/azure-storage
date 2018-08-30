{
  "info": {
    "name": "Azure Storage API Managers Get Public Encryption Key",
    "_postman_id": "8ce65415-ac00-47e3-a77f-2875f120bdb6",
    "description": "Returns the symmetric encrypted public encryption key of the manager.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "managers public encryption key",
      "item": [
        {
          "id": "d99a9619-3deb-4c6f-9db0-c31cdb4e7b83",
          "name": "Managers_GetPublicEncryptionKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.StorSimple/managers/:managerName/listPublicEncryptionKey"
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
            "description": "Returns the symmetric encrypted public encryption key of the manager"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ca9d6208-617a-4800-93a6-3340d69150f0"
            }
          ]
        }
      ]
    }
  ]
}