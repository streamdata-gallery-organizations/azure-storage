{
  "info": {
    "name": "Azure Storage API Jobs Delete",
    "_postman_id": "4f06e1f6-d159-4a3b-aaa8-72883d5edf87",
    "description": "Deletes an existing import/export job. Only import/export jobs in the Creating or Completed states can be deleted.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "jobs",
      "item": [
        {
          "id": "049ebef4-5c13-4a4b-b8e2-fefb04b5e9ab",
          "name": "Jobs_Delete",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ImportExport/jobs/:jobName"
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
            "method": "DELETE",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an existing import/export job"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7844c9a0-5e82-480c-b7b4-8a518ea95267"
            }
          ]
        }
      ]
    }
  ]
}