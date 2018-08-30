{
  "info": {
    "name": "Azure Storage API Jobs List Bit Locker Keys",
    "_postman_id": "3e735288-413d-47d4-a384-59f0b4ad6a68",
    "description": "Lists the BitLocker keys for all drives in the specified import/export job.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "jobs",
      "item": [
        {
          "id": "5239e484-b410-4c45-9ed1-1387fb6fb6d5",
          "name": "Jobs_ListBitLockerKeys",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ImportExport/jobs/:jobName/listBitLockerKeys"
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
                  "id": "jobName",
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
            "description": "Lists the BitLocker keys for all drives in the specified import/export job"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "044ca9b2-32d2-48ec-a420-45b9cc350efe"
            }
          ]
        }
      ]
    }
  ]
}