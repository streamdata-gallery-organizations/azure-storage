{
  "info": {
    "name": "Azure Storage API Managers List By Resource Group",
    "_postman_id": "d1fb5991-5a5b-4cff-98d1-9af37c29373e",
    "description": "Retrieves all the managers in a resource group.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Managers",
      "item": [
        {
          "id": "9d0e22ee-accb-451d-b90f-6a99b8a67678",
          "name": "Managers_List",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/providers/Microsoft.StorSimple/managers"
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
            "description": "Retrieves all the managers in a subscription."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7bf1c7e9-d6c1-4cc2-b26d-8e56923f2c7b"
            }
          ]
        }
      ]
    },
    {
      "name": "Managers Resource Group",
      "item": [
        {
          "id": "6ab0aa3b-681a-48f4-9dc0-a3b888d18885",
          "name": "Managers_ListByResourceGroup",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.StorSimple/managers"
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
            "description": "Retrieves all the managers in a resource group."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "05fc764e-3002-4a3f-a578-f6366b3ce57b"
            }
          ]
        }
      ]
    }
  ]
}