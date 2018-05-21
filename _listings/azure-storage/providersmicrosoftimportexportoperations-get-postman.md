{
  "info": {
    "name": "Azure Storage API List Supported Operations",
    "_postman_id": "cb4e92cc-618b-4655-b9f8-7b0cedf10c85",
    "description": "Returns the list of operations supported by the import/export resource provider.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "supported operations",
      "item": [
        {
          "id": "a96d7e96-a3b5-4251-bcb2-05074dbb53a1",
          "name": "ListSupportedOperations",
          "request": {
            "url": "http://management.azure.com/providers/Microsoft.ImportExport/operations?No Name=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the list of operations supported by the import/export resource provider"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "92c80f7a-351d-4cef-abb9-77e512b852f2"
            }
          ]
        }
      ]
    }
  ]
}