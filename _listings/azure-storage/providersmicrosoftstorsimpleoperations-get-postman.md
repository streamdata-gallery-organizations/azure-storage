{
  "info": {
    "name": "Azure Storage API Operations List",
    "_postman_id": "5e297a14-877a-4371-bfa2-d3eec89fb746",
    "description": "Lists all of the available REST API operations of the Microsoft.Storsimple provider",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "operations",
      "item": [
        {
          "id": "9df04576-f2c6-4058-a296-b54d5fb8bcd6",
          "name": "Operations_List",
          "request": {
            "url": "http://management.azure.com/providers/Microsoft.StorSimple/operations?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all of the available REST API operations of the Microsoft"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c3c9423c-2dcb-4f0b-ba36-52e63f82ec01"
            }
          ]
        }
      ]
    }
  ]
}