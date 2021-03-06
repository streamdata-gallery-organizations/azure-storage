---
swagger: "2.0"
x-collection-name: Azure Storage
x-complete: 0
info:
  title: Azure Storage API Devices Deactivate
  version: 1.0.0
  description: Deactivates the device.
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
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{accountName}/regenerateKey
  : post:
      summary: Storage Accounts Regenerate Key
      description: Regenerates one of the access keys for the specified storage account.
      operationId: StorageAccounts_RegenerateKey
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountnameregeneratekey-post
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      - in: body
        name: regenerateKey
        description: Specifies name of the key which should be regenerated -- key1
          or key2
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Regenerate Key
  /subscriptions/{subscriptionId}/providers/Microsoft.Storage/usages:
    get:
      summary: Usage List
      description: Gets the current usage count and the limit for the resources under
        the subscription.
      operationId: Usage_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-storageusages-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Usage
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{accountName}/ListAccountSas
  : post:
      summary: Storage Accounts List Account SAS
      description: List SAS credentials of a storage account.
      operationId: StorageAccounts_ListAccountSAS
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountnamelistaccountsas-post
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters to provide to list SAS credentials for the storage
          account
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Account Sas
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{accountName}/ListServiceSas
  : post:
      summary: Storage Accounts List Service SAS
      description: List service SAS credentials of a specific resource.
      operationId: StorageAccounts_ListServiceSAS
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storagestorageaccountsaccountnamelistservicesas-post
      parameters:
      - in: path
        name: accountName
        description: The name of the storage account within the specified resource
          group
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The parameters to provide to list service SAS credentials
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Storage Accounts Service Sas
  /providers/Microsoft.ImportExport/locations:
    get:
      summary: List Locations
      description: Returns a list of locations to which you can ship the disks associated
        with an import or export job. A location is a Microsoft data center region.
      operationId: ListLocations
      x-api-path-slug: providersmicrosoft-importexportlocations-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Locations
  /providers/Microsoft.ImportExport/locations/{locationName}:
    get:
      summary: Get Location
      description: Gets a location to which you can ship the disks associated with
        an import or export job. A location is an Azure region.
      operationId: GetLocation
      x-api-path-slug: providersmicrosoft-importexportlocationslocationname-get
      parameters:
      - in: path
        name: locationName
        description: The name of the location
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Location
  /subscriptions/{subscriptionId}/providers/Microsoft.ImportExport/jobs:
    get:
      summary: Jobs List
      description: Gets all the active and completed import/export jobs in a subscription.
      operationId: Jobs_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-importexportjobs-get
      parameters:
      - in: query
        name: $filter
        description: Can be used to restrict the results to certain conditions
      - in: query
        name: $top
        description: An integer value that specifies how many jobs at most should
          be returned
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ImportExport/jobs:
    get:
      summary: Jobs List By Resource Group
      description: Returns all active and completed import/export jobs in a resource
        group.
      operationId: Jobs_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-importexportjobs-get
      parameters:
      - in: query
        name: $filter
        description: Can be used to restrict the results to certain conditions
      - in: query
        name: $top
        description: An integer value that specifies how many jobs at most should
          be returned
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs Resource Group
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ImportExport/jobs/{jobName}:
    get:
      summary: Jobs Get
      description: Gets information about an existing import/export job.
      operationId: Jobs_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-importexportjobsjobname-get
      parameters:
      - in: path
        name: jobName
        description: The name of the import/export job
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs
    patch:
      summary: Jobs Update
      description: Updates specific properties of the import/export job. You can call
        this operation to notify the Import/Export service that the hard drives comprising
        the import or export job have been shipped to the Microsoft data center. It
        can also be used to cancel an existing job.
      operationId: Jobs_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-importexportjobsjobname-patch
      parameters:
      - in: path
        name: jobName
        description: The name of the import/export job
      - in: body
        name: jobProperties
        description: Import/export job properties that need to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs
    put:
      summary: Jobs Create Or Update
      description: Creates a new import/export job or updates an existing import/export
        job in the specified subscription.
      operationId: Jobs_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-importexportjobsjobname-put
      parameters:
      - in: path
        name: jobName
        description: The name of the import/export job
      - in: body
        name: jobProperties
        description: Properties of the import/export job that need to be specified
          during creation
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs
    delete:
      summary: Jobs Delete
      description: Deletes an existing import/export job. Only import/export jobs
        in the Creating or Completed states can be deleted.
      operationId: Jobs_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-importexportjobsjobname-delete
      parameters:
      - in: path
        name: jobName
        description: The name of the import/export job
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ImportExport/moveResources:
    post:
      summary: Jobs Move
      description: Moves the specified import/export jobs from the resource group
        to a target resource group. The target resource group may be in a different
        subscription.
      operationId: Jobs_Move
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-importexportmoveresources-post
      parameters:
      - in: body
        name: MoveJobsParameters
        description: Parameters to be provided to move a job from one resource group
          to another
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ImportExport/jobs/{jobName}/listBitLockerKeys
  : get:
      summary: Jobs List Bit Locker Keys
      description: Lists the BitLocker keys for all drives in the specified import/export
        job.
      operationId: Jobs_ListBitLockerKeys
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-importexportjobsjobnamelistbitlockerkeys-get
      parameters:
      - in: path
        name: jobName
        description: The name of the import/export job
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Jobs
  /providers/Microsoft.ImportExport/operations:
    get:
      summary: List Supported Operations
      description: Returns the list of operations supported by the import/export resource
        provider.
      operationId: ListSupportedOperations
      x-api-path-slug: providersmicrosoft-importexportoperations-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Supported Operations
  /providers/Microsoft.StorSimple/operations:
    get:
      summary: Operations List
      description: Lists all of the available REST API operations of the Microsoft.Storsimple
        provider
      operationId: Operations_List
      x-api-path-slug: providersmicrosoft-storsimpleoperations-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Operations
  /subscriptions/{subscriptionId}/providers/Microsoft.StorSimple/managers:
    get:
      summary: Managers List
      description: Retrieves all the managers in a subscription.
      operationId: Managers_List
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-storsimplemanagers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Managers
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers:
    get:
      summary: Managers List By Resource Group
      description: Retrieves all the managers in a resource group.
      operationId: Managers_ListByResourceGroup
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Managers Resource Group
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}:
    get:
      summary: Managers Get
      description: Returns the properties of the specified manager name.
      operationId: Managers_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagername-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Managers
    put:
      summary: Managers Create Or Update
      description: Creates or updates the manager.
      operationId: Managers_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagername-put
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The manager
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Managers
    delete:
      summary: Managers Delete
      description: Deletes the manager.
      operationId: Managers_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagername-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Managers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}/configureDevice
  : post:
      summary: Devices Configure
      description: Complete minimal setup before using the device.
      operationId: Devices_Configure
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernameconfiguredevice-post
      parameters:
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: The minimal properties to configure a device
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Devices
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}/devices:
    get:
      summary: Devices List By Manager
      description: Returns the list of devices for the specified manager.
      operationId: Devices_ListByManager
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernamedevices-get
      parameters:
      - in: query
        name: $expand
        description: Specify $expand=details to populate additional fields related
          to the device
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Devices
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}/devices/{deviceName}
  : get:
      summary: Devices Get
      description: Returns the properties of the specified device.
      operationId: Devices_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernamedevicesdevicename-get
      parameters:
      - in: query
        name: $expand
        description: Specify $expand=details to populate additional fields related
          to the device
      - in: path
        name: deviceName
        description: The device name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Devices
    delete:
      summary: Devices Delete
      description: Deletes the device.
      operationId: Devices_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernamedevicesdevicename-delete
      parameters:
      - in: path
        name: deviceName
        description: The device name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Devices
    patch:
      summary: Devices Update
      description: Patches the device.
      operationId: Devices_Update
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernamedevicesdevicename-patch
      parameters:
      - in: path
        name: deviceName
        description: The device Name
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Patch representation of the device
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Devices
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}/devices/{deviceName}/deactivate
  : post:
      summary: Devices Deactivate
      description: Deactivates the device.
      operationId: Devices_Deactivate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-storsimplemanagersmanagernamedevicesdevicenamedeactivate-post
      parameters:
      - in: path
        name: deviceName
        description: The device name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Devices
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