---
swagger: "2.0"
x-collection-name: Azure Storage
x-complete: 0
info:
  title: Azure Storage API Storage Accounts List Keys
  version: 1.0.0
  description: Lists the access keys for the specified storage account.
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/providers/Microsoft.Storage/checkNameAvailability:
    post:
      summary: Storage Accounts Check Name Availability
      description: Checks that the storage account name is valid and is not already
        in use.
      operationId: StorageAccounts_CheckNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-storagechecknameavailability-post
      parameters:
      - in: body
        name: accountName
        description: The name of the storage account within the specified resource
          group
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Name Availability
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{accountName}:
    put:
      summary: Storage Accounts Create
      description: Asynchronously creates a new storage account with the specified
        parameters. If an account is already created and a subsequent create request
        is issued with different properties, the account properties will be updated.
        If an account is already created and a subsequent create or update request
        is issued with the exact same set of properties, the request will succeed.
      operationId: StorageAccounts_Create
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountname-put
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters to provide for the created account
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts
    delete:
      summary: Storage Accounts Delete
      description: Deletes a storage account in Microsoft Azure.
      operationId: StorageAccounts_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountname-delete
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts
    get:
      summary: Storage Accounts Get Properties
      description: Returns the properties for the specified storage account including
        but not limited to name, SKU name, location, and account status. The ListKeys
        operation should be used to retrieve storage keys.
      operationId: StorageAccounts_GetProperties
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountname-get
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Properties
    patch:
      summary: Storage Accounts Update
      description: The update operation can be used to update the SKU, encryption,
        access tier, or tags for a storage account. It can also be used to map the
        account to a custom domain. Only one custom domain is supported per storage
        account; the replacement/change of custom domain is not supported. In order
        to replace an old custom domain, the old value must be cleared/unregistered
        before a new value can be set. The update of multiple properties is supported.
        This call does not change the storage keys for the account. If you want to
        change the storage account keys, use the regenerate keys operation. The location
        and name of the storage account cannot be changed after creation.
      operationId: StorageAccounts_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountname-patch
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters to provide for the updated account
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts
  /subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts:
    get:
      summary: Storage Accounts List
      description: Lists all the storage accounts available under the subscription.
        Note that storage keys are not returned; use the ListKeys operation for this.
      operationId: StorageAccounts_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-storagestorageaccounts-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts:
    get:
      summary: Storage Accounts List By Resource Group
      description: Lists all the storage accounts available under the given resource
        group. Note that storage keys are not returned; use the ListKeys operation
        for this.
      operationId: StorageAccounts_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccounts-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Resource Group
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{accountName}/listKeys
  : post:
      summary: Storage Accounts List Keys
      description: Lists the access keys for the specified storage account.
      operationId: StorageAccounts_ListKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountnamelistkeys-post
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Keys
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---