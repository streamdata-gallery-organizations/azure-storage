{
  "info": {
    "name": "Azure Storage API Devices Get",
    "_postman_id": "b32c4852-1cd0-46ba-a518-3a927650ce07",
    "description": "Returns the properties of the specified device.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "devices",
      "item": [
        {
          "id": "f374f819-7a22-4207-8872-c15297e28c1a",
          "name": "Devices_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.StorSimple/managers/:managerName/devices/:deviceName"
              ],
              "query": [
                {
                  "key": "$expand",
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
                  "id": "deviceName",
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
                },
                {
                  "id": "managerName",
                  "value": "managerName",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the properties of the specified device"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b83ced6e-58c7-44aa-9657-30ec5f3d217a"
            }
          ]
        }
      ]
    }
  ]
}