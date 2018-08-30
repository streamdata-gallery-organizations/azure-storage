---
swagger: "2.0"
info:
  title: StorSimpleSeries8000ManagementClient
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.StorSimple/managers/{managerName}/listPublicEncryptionKey
  : post:
      summary: Managers Get Public Encryption Key
      description: Returns the symmetric encrypted public encryption key of the manager
      operationId: Managers_GetPublicEncryptionKey
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - managers public encryption key
definitions:
  StorageAccountCheckNameAvailabilityParameters:
    properties:
      name:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  CheckNameAvailabilityResult:
    properties:
      nameAvailable:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
  Sku:
    properties:
      name:
        description: This is a default description.
        type: post
      tier:
        description: This is a default description.
        type: post
  CustomDomain:
    properties:
      name:
        description: This is a default description.
        type: post
      useSubDomain:
        description: This is a default description.
        type: post
  EncryptionService:
    properties:
      enabled:
        description: This is a default description.
        type: post
      lastEnabledTime:
        description: This is a default description.
        type: post
  EncryptionServices:
    properties: []
  Encryption:
    properties:
      keySource:
        description: This is a default description.
        type: post
  StorageAccountPropertiesCreateParameters:
    properties:
      accessTier:
        description: This is a default description.
        type: post
      supportsHttpsTrafficOnly:
        description: This is a default description.
        type: post
  StorageAccountCreateParameters:
    properties:
      kind:
        description: This is a default description.
        type: post
      location:
        description: This is a default description.
        type: post
      tags:
        description: This is a default description.
        type: post
  Endpoints:
    properties:
      blob:
        description: This is a default description.
        type: post
      queue:
        description: This is a default description.
        type: post
      table:
        description: This is a default description.
        type: post
      file:
        description: This is a default description.
        type: post
  StorageAccountProperties:
    properties:
      provisioningState:
        description: This is a default description.
        type: post
      primaryLocation:
        description: This is a default description.
        type: post
      statusOfPrimary:
        description: This is a default description.
        type: post
      lastGeoFailoverTime:
        description: This is a default description.
        type: post
      secondaryLocation:
        description: This is a default description.
        type: post
      statusOfSecondary:
        description: This is a default description.
        type: post
      creationTime:
        description: This is a default description.
        type: post
      accessTier:
        description: This is a default description.
        type: post
      supportsHttpsTrafficOnly:
        description: This is a default description.
        type: post
  StorageAccount:
    properties:
      kind:
        description: This is a default description.
        type: post
  StorageAccountKey:
    properties:
      keyName:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
      permissions:
        description: This is a default description.
        type: post
  StorageAccountListResult:
    properties:
      value:
        description: This is a default description.
        type: post
  StorageAccountListKeysResult:
    properties:
      keys:
        description: This is a default description.
        type: post
  StorageAccountRegenerateKeyParameters:
    properties:
      keyName:
        description: This is a default description.
        type: post
  StorageAccountPropertiesUpdateParameters:
    properties:
      accessTier:
        description: This is a default description.
        type: post
      supportsHttpsTrafficOnly:
        description: This is a default description.
        type: post
  StorageAccountUpdateParameters:
    properties:
      tags:
        description: This is a default description.
        type: post
  UsageName:
    properties:
      value:
        description: This is a default description.
        type: post
      localizedValue:
        description: This is a default description.
        type: post
  Usage:
    properties:
      unit:
        description: This is a default description.
        type: post
      currentValue:
        description: This is a default description.
        type: post
      limit:
        description: This is a default description.
        type: post
  UsageListResult:
    properties:
      value:
        description: This is a default description.
        type: post
  Resource:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      location:
        description: This is a default description.
        type: post
      tags:
        description: This is a default description.
        type: post
  AccountSasParameters:
    properties:
      signedServices:
        description: This is a default description.
        type: post
      signedResourceTypes:
        description: This is a default description.
        type: post
      signedPermission:
        description: This is a default description.
        type: post
      signedIp:
        description: This is a default description.
        type: post
      signedProtocol:
        description: This is a default description.
        type: post
      signedStart:
        description: This is a default description.
        type: post
      signedExpiry:
        description: This is a default description.
        type: post
      keyToSign:
        description: This is a default description.
        type: post
  ListAccountSasResponse:
    properties:
      accountSasToken:
        description: This is a default description.
        type: post
  ServiceSasParameters:
    properties:
      canonicalizedResource:
        description: This is a default description.
        type: post
      signedResource:
        description: This is a default description.
        type: post
      signedPermission:
        description: This is a default description.
        type: post
      signedIp:
        description: This is a default description.
        type: post
      signedProtocol:
        description: This is a default description.
        type: post
      signedStart:
        description: This is a default description.
        type: post
      signedExpiry:
        description: This is a default description.
        type: post
      signedIdentifier:
        description: This is a default description.
        type: post
      startPk:
        description: This is a default description.
        type: post
      endPk:
        description: This is a default description.
        type: post
  ListServiceSasResponse:
    properties:
      serviceSasToken:
        description: This is a default description.
        type: post
  SupportedOperationsListResult:
    properties:
      value:
        description: This is a default description.
        type: get
  BitLockerKeysListResult:
    properties:
      value:
        description: This is a default description.
        type: get
  MoveJobParameters:
    properties:
      targetResourceGroup:
        description: This is a default description.
        type: get
      resources:
        description: This is a default description.
        type: get
  LocationsListResult:
    properties:
      value:
        description: This is a default description.
        type: get
  ErrorBase:
    properties:
      code:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      target:
        description: This is a default description.
        type: get
  ErrorInfo:
    properties:
      details:
        description: This is a default description.
        type: get
  ErrorResponse:
    properties: []
  MutableJobProperties:
    properties:
      cancelRequested:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      logLevel:
        description: This is a default description.
        type: get
      backupDriveManifest:
        description: This is a default description.
        type: get
  MutableJob:
    properties:
      tags:
        description: This is a default description.
        type: get
  JobListResult:
    properties:
      nextLink:
        description: This is a default description.
        type: get
      value:
        description: This is a default description.
        type: get
  JobProperties:
    properties:
      storageAccountId:
        description: This is a default description.
        type: get
      containerSas:
        description: This is a default description.
        type: get
      jobType:
        description: This is a default description.
        type: get
      diagnosticsPath:
        description: This is a default description.
        type: get
      logLevel:
        description: This is a default description.
        type: get
      backupDriveManifest:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      cancelRequested:
        description: This is a default description.
        type: get
      percentComplete:
        description: This is a default description.
        type: get
      incompleteBlobListUri:
        description: This is a default description.
        type: get
  Job:
    properties: []
  OperationDisplayInformation:
    properties:
      provider:
        description: This is a default description.
        type: get
      resource:
        description: This is a default description.
        type: get
      operation:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
  Operation:
    properties:
      name:
        description: This is a default description.
        type: get
  LocationProperties:
    properties:
      recipientName:
        description: This is a default description.
        type: get
      streetAddress1:
        description: This is a default description.
        type: get
      streetAddress2:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      stateOrProvince:
        description: This is a default description.
        type: get
      postalCode:
        description: This is a default description.
        type: get
      countryOrRegion:
        description: This is a default description.
        type: get
      phone:
        description: This is a default description.
        type: get
      supportedCarriers:
        description: This is a default description.
        type: get
      alternateLocations:
        description: This is a default description.
        type: get
  Location:
    properties:
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  ReturnAddress:
    properties:
      recipientName:
        description: This is a default description.
        type: get
      streetAddress1:
        description: This is a default description.
        type: get
      streetAddress2:
        description: This is a default description.
        type: get
      city:
        description: This is a default description.
        type: get
      stateOrProvince:
        description: This is a default description.
        type: get
      postalCode:
        description: This is a default description.
        type: get
      countryOrRegion:
        description: This is a default description.
        type: get
      phone:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
  ReturnShipping:
    properties:
      carrierName:
        description: This is a default description.
        type: get
      carrierAccountNumber:
        description: This is a default description.
        type: get
  ShippingInformation:
    properties:
      name:
        description: This is a default description.
        type: get
      address:
        description: This is a default description.
        type: get
  PackageInfomation:
    properties:
      carrierName:
        description: This is a default description.
        type: get
      trackingNumber:
        description: This is a default description.
        type: get
      driveCount:
        description: This is a default description.
        type: get
      shipDate:
        description: This is a default description.
        type: get
  Drive:
    properties:
      driveId:
        description: This is a default description.
        type: get
      bitLockerKey:
        description: This is a default description.
        type: get
      manifestFile:
        description: This is a default description.
        type: get
      manifestHash:
        description: This is a default description.
        type: get
  DriveStatus:
    properties:
      state:
        description: This is a default description.
        type: get
      copyStatus:
        description: This is a default description.
        type: get
      percentComplete:
        description: This is a default description.
        type: get
      verboseLogUri:
        description: This is a default description.
        type: get
      errorLogUri:
        description: This is a default description.
        type: get
      manifestUri:
        description: This is a default description.
        type: get
  Export:
    properties:
      blobListblobPath:
        description: This is a default description.
        type: get
  AsymmetricEncryptedSecret:
    properties:
      value:
        description: This is a default description.
        type: post
      encryptionCertThumbprint:
        description: This is a default description.
        type: post
      encryptionAlgorithm:
        description: This is a default description.
        type: post
  AsymmetricEncryptedSecretList:
    properties:
      value:
        description: This is a default description.
        type: post
  AvailableProviderOperation:
    properties:
      name:
        description: This is a default description.
        type: post
      origin:
        description: This is a default description.
        type: post
  AvailableProviderOperationDisplay:
    properties:
      provider:
        description: This is a default description.
        type: post
      resource:
        description: This is a default description.
        type: post
      operation:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
  AvailableProviderOperationList:
    properties:
      value:
        description: This is a default description.
        type: post
      nextLink:
        description: This is a default description.
        type: post
  AvailableProviderOperationProperties:
    properties: []
  BaseModel:
    properties:
      id:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  ConfigureDeviceRequest:
    properties: []
  ConfigureDeviceRequestProperties:
    properties:
      friendlyName:
        description: This is a default description.
        type: post
      currentDeviceName:
        description: This is a default description.
        type: post
      timeZone:
        description: This is a default description.
        type: post
  Device:
    properties: []
  DeviceDetails:
    properties:
      endpointCount:
        description: This is a default description.
        type: post
      volumeContainerCount:
        description: This is a default description.
        type: post
  DeviceList:
    properties:
      value:
        description: This is a default description.
        type: post
  DevicePatch:
    properties: []
  DevicePatchProperties:
    properties:
      deviceDescription:
        description: This is a default description.
        type: post
  DeviceProperties:
    properties:
      friendlyName:
        description: This is a default description.
        type: post
      activationTime:
        description: This is a default description.
        type: post
      culture:
        description: This is a default description.
        type: post
      deviceDescription:
        description: This is a default description.
        type: post
      deviceSoftwareVersion:
        description: This is a default description.
        type: post
      friendlySoftwareName:
        description: This is a default description.
        type: post
      deviceConfigurationStatus:
        description: This is a default description.
        type: post
      targetIqn:
        description: This is a default description.
        type: post
      modelDescription:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  EncryptionSettings:
    properties: []
  EncryptionSettingsProperties:
    properties:
      encryptionStatus:
        description: This is a default description.
        type: post
      keyRolloverStatus:
        description: This is a default description.
        type: post
  Key:
    properties:
      activationKey:
        description: This is a default description.
        type: post
  Manager:
    properties:
      etag:
        description: This is a default description.
        type: post
  ManagerExtendedInfo:
    properties:
      etag:
        description: This is a default description.
        type: post
  ManagerExtendedInfoProperties:
    properties:
      version:
        description: This is a default description.
        type: post
      integrityKey:
        description: This is a default description.
        type: post
      encryptionKey:
        description: This is a default description.
        type: post
      encryptionKeyThumbprint:
        description: This is a default description.
        type: post
      portalCertificateThumbprint:
        description: This is a default description.
        type: post
      algorithm:
        description: This is a default description.
        type: post
  ManagerIntrinsicSettings:
    properties:
      type:
        description: This is a default description.
        type: post
  ManagerList:
    properties:
      value:
        description: This is a default description.
        type: post
  ManagerProperties:
    properties:
      provisioningState:
        description: This is a default description.
        type: post
  ManagerSku:
    properties:
      name:
        description: This is a default description.
        type: post
  NetworkInterfaceData0Settings:
    properties:
      controllerZeroIp:
        description: This is a default description.
        type: post
      controllerOneIp:
        description: This is a default description.
        type: post
  PublicKey:
    properties:
      key:
        description: This is a default description.
        type: post
  SecondaryDNSSettings:
    properties:
      secondaryDnsServers:
        description: This is a default description.
        type: post
  SymmetricEncryptedSecret:
    properties:
      value:
        description: This is a default description.
        type: post
      valueCertificateThumbprint:
        description: This is a default description.
        type: post
      encryptionAlgorithm:
        description: This is a default description.
        type: post
x-collection-name: Azure Storage
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