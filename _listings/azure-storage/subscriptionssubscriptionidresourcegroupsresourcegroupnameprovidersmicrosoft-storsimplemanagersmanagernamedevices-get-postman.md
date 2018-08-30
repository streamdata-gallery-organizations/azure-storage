{
  "info": {
    "name": "Azure Storage API Devices List By Manager",
    "_postman_id": "06514837-4482-41ce-955f-4e6d3bba5c8a",
    "description": "Returns the list of devices for the specified manager.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "devices",
      "item": [
        {
          "id": "d774db98-bbbc-41a3-94aa-1d6256ca058a",
          "name": "Devices_ListByManager",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.StorSimple/managers/:managerName/devices"
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
            "description": "Returns the list of devices for the specified manager"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b575fc58-af08-4641-b976-55fa65acb876"
            }
          ]
        }
      ]
    }
  ]
}