# Objects, in the Citrix.PVS.SnapIn Namespace

## PvsADAccount

Read-Only Fields

string Domain: Domain the account is a member of.

string DomainController: The name of the DC used to create the host's computer account.

string Name: Name of the Device for the account.

string Sid: The value of the objectSID AD attribute of the same name for the Device's computer account.

## PvsAuditAction

Read-Only Fields

Guid Guid or AuditActionId: GUID of the action.

Guid ObjectId: GUID of the object of the action.

string ObjectName: Name of the object of the action. Max Length=1000

string Path: Path of the object of the action. An example is Site\\Collection for a Device. Default="" Max Length=101

Guid SiteId: GUID of the Site for the object of the action. 00000000-0000-0000-0000-000000000000 when not valid. Default=00000000-0000-0000-0000-000000000000

Guid SubId: GUID of the Collection or Store of the action. 00000000-0000-0000-0000-000000000000 when not valid. Default=00000000-0000-0000-0000-000000000000

uint Type: Type of object that action was performed on. Values are: 1 (AuthGroup), 2 (Collection), 3 (Device), 4 (Disk), 5 (DiskLocator), 6 (Farm), 7 (FarmView), 8 (Server), 9 (Site), 10 (SiteView), 11 (Store), 12 (System), and 13 (UserGroup)

## PvsAuditActionParameter

Read-Only Fields

Guid AuditActionId: GUID of the Audit Action used for Get and Set.

string Name or AuditParameterName: Name of the parameter. Max Length=50

string Value: Value of the parameter. Max Length=1000

## PvsAuditActionProperty

Read-Only Fields

Guid AuditActionId: GUID of the Audit Action used for Get and Set.

string Name or AuditPropertyName: Name of the property. Max Length=50

string NewValue: New value of the Property. Default="" Max Length=1000

string OldValue: Previous value of the Property. Default="" Max Length=1000

## PvsAuditTrail

Read-Only Fields

uint Action: Name of the action taken. This is a number that is converted to a string for display. Values are: 1 (AddAuthGroup), 2 (AddCollection), 3 (AddDevice), 4 (AddDiskLocator), 5 (AddFarmView), 6 (AddServer), 7 (AddSite), 8 (AddSiteView), 9 (AddStore), 10 (AddUserGroup), 11 (AddVirtualHostingPool), 12 (AddUpdateTask), 13 (AddDiskUpdateDevice), 1001 (DeleteAuthGroup), 1002 (DeleteCollection), 1003 (DeleteDevice), 1004 (DeleteDeviceDiskCacheFile), 1005 (DeleteDiskLocator), 1006 (DeleteFarmView), 1007 (DeleteServer), 1008 (DeleteServerStore), 1009 (DeleteSite), 1010 (DeleteSiteView), 1011 (DeleteStore), 1012 (DeleteUserGroup), 1013 (DeleteVirtualHostingPool), 1014 (DeleteUpdateTask), 1015 (DeleteDiskUpdateDevice), 1016 (DeleteDiskVersion), 2001 (RunAddDeviceToDomain), 2002 (RunApplyAutoUpdate), 2003 (RunApplyIncrementalUpdate), 2004 (RunArchiveAuditTrail), 2005 (RunAssignAuthGroup), 2006 (RunAssignDevice), 2007 (RunAssignDiskLocator), 2008 (RunAssignServer), 2009 (RunWithReturnBoot), 2010 (RunCopyPasteDevice), 2011 (RunCopyPasteDisk), 2012 (RunCopyPasteServer), 2013 (RunCreateDirectory), 2014 (RunCreateDiskCancel), 2015 (RunDisableCollection), 2016 (RunDisableDevice), 2017 (RunDisableDeviceDiskLocator), 2018 (RunDisableDiskLocator), 2019 (RunDisableUserGroup), 2020 (RunDisableUserGroupDiskLocator), 2021 (RunWithReturnDisplayMessage), 2022 (RunEnableCollection), 2023 (RunEnableDevice), 2024 (RunEnableDeviceDiskLocator), 2025 (RunEnableDiskLocator), 2026 (RunEnableUserGroup), 2027 (RunEnableUserGroupDiskLocator), 2028 (RunExportOemLicenses), 2029 (RunImportDatabase), 2030 (RunImportDevices), 2031 (RunImportOemLicenses), 2032 (RunMarkDown), 2033 (RunWithReturnReboot), 2034 (RunRemoveAuthGroup), 2035 (RunRemoveDevice), 2036 (RunRemoveDeviceFromDomain), 2037 (RunRemoveDirectory), 2038 (RunRemoveDiskLocator), 2039 (RunResetDeviceForDomain), 2040 (RunResetDatabaseConnection), 2041 (RunRestartStreamingService), 2042 (RunWithReturnShutdown), 2043 (RunStartStreamingService), 2044 (RunStopStreamingService), 2045 (RunUnlockAllDisk), 2046 (RunUnlockDisk), 2047 (RunServerStoreVolumeAccess), 2048 (RunServerStoreVolumeMode), 2049 (RunMergeDisk), 2050 (RunRevertDiskVersion), 2051 (RunPromoteDiskVersion), 2052 (RunCancelDiskMaintenance), 2053 (RunActivateDevice), 2054 (RunAddDiskVersion), 2055 (RunExportDisk), 2056 (RunAssignDisk), 2057 (RunRemoveDisk), 2058 (RunDiskUpdateStart), 2059 (RunDiskUpdateCancel), 2060 (RunSetOverrideVersion), 2061 (RunCancelTask), 2062 (RunClearTask), 2063 (RunForceInventory), 2064 RunUpdateBDM, 2065 (RunStartDeviceDiskTempVersionMode), 2066 (RunStopDeviceDiskTempVersionMode), 3001 (RunWithReturnCreateDisk), 3002 (RunWithReturnCreateDiskStatus), 3003 (RunWithReturnMapDisk), 3004 (RunWithReturnRebalanceDevices), 3005 (RunWithReturnCreateMaintenanceVersion), 3006 (RunWithReturnImportDisk), 4001 (RunByteArrayInputImportDevices), 4002 (RunByteArrayInputImportOemLicenses), 5001 (RunByteArrayOutputArchiveAuditTrail), 5002 (RunByteArrayOutputExportOemLicenses), 6001 (SetAuthGroup), 6002 (SetCollection), 6003 (SetDevice), 6004 (SetDisk), 6005 (SetDiskLocator), 6006 (SetFarm), 6007 (SetFarmView), 6008 (SetServer), 6009 (SetServerBiosBootstrap), 6010 (SetServerBootstrap), 6011 (SetServerStore), 6012 (SetSite), 6013 (SetSiteView), 6014 (SetStore), 6015 (SetUserGroup), 6016 SetVirtualHostingPool, 6017 SetUpdateTask, 6018 SetDiskUpdateDevice, 7001 (SetListDeviceBootstraps), 7002 (SetListDeviceBootstrapsDelete), 7003 (SetListDeviceBootstrapsAdd), 7004 (SetListDeviceCustomProperty), 7005 (SetListDeviceCustomPropertyDelete), 7006 (SetListDeviceCustomPropertyAdd), 7007 (SetListDeviceDiskPrinters), 7008 (SetListDeviceDiskPrintersDelete), 7009 (SetListDeviceDiskPrintersAdd), 7010 (SetListDevicePersonality), 7011 (SetListDevicePersonalityDelete), 7012 (SetListDevicePersonalityAdd), 7013 (SetListDiskLocatorCustomProperty), 7014 (SetListDiskLocatorCustomPropertyDelete), 7015 (SetListDiskLocatorCustomPropertyAdd), 7016 (SetListServerCustomProperty), 7017 (SetListServerCustomPropertyDelete), 7018 (SetListServerCustomPropertyAdd), 7019 (SetListUserGroupCustomProperty), 7020 (SetListUserGroupCustomPropertyDelete), and 7021 (SetListUserGroupCustomPropertyAdd)

uint Attachments: An or'ed value that indicates if there are any details for this action. A value of 15 indicates that there are Children, Sibling, Parameters and Properties for the action. Values are: 0 (None), 1 (Children), 2 (Sibling), 4 (Parameters), and 8 (Properties) Default=0

Guid Guid or AuditActionId: GUID of the action.

string Domain: Domain of the user that performed the action. Max Length=255

Guid ObjectId: GUID of the object of the action. Default=00000000-0000-0000-0000-000000000000

string ObjectName: Name of the object of the action. Default="" Max Length=1000

Guid ParentId: GUID of the parent action (one that triggered this action) if one exists. 00000000-0000-0000-0000-000000000000 when not valid. Default=00000000-0000-0000-0000-000000000000

string Path: Path of the object of the action. An example is Site\\Collection for a Device. Default="" Max Length=101

Guid RootId: GUID of the root action (one that triggered this group of actions) if one exists. 00000000-0000-0000-0000-000000000000 when not valid. Default=00000000-0000-0000-0000-000000000000

Guid SiteId: GUID of the Site for the object of the action. 00000000-0000-0000-0000-000000000000 when not valid. Default=00000000-0000-0000-0000-000000000000

Guid SubId: GUID of the Collection or Store of the action. 00000000-0000-0000-0000-000000000000 when not valid. Default=00000000-0000-0000-0000-000000000000

DateTime Time: Date/Time the action occurred down to the millisecond. Has the date and time including milliseconds. Default=Empty

uint Type: Type of object that action was performed on. Values are: 0 (Many), 1 (AuthGroup), 2 (Collection), 3 (Device), 4 (Disk), 5 (DiskLocator), 6 (Farm), 7 (FarmView), 8 (Server), 9 (Site), 10 (SiteView), 11 (Store), 12 (System), and 13 (UserGroup)

string UserName: User that performed the action. Max Length=255

## PvsAuthGroup

Read/Write Fields

string Name or AuthGroupName: Name of the Active Directory or Windows Group. Max Length=450

string Description: User description. Default="" Max Length=250

Read-Only Fields

Guid Guid or AuthGroupId: Read-only GUID that uniquely identifies this AuthGroup.

uint Role: Role of the AuthGroup for a Collection. role can only be used with CollectionId or CollectionName. 300 is Collection Administrator, and 400 is Collection Operator. Default=999

## PvsAuthGroupUsage

Read-Only Fields

Guid Guid or Id: GUID of the item. The item can be a Farm, Site or Collection. It will be 00000000-0000-0000-0000-000000000000 for Farm.

string Name: Name of the item. The item can be a Farm, Site or Collection.

uint Role: Role of the AuthGroup for the item. 100 is Farm Administrator, 200 is Site Administrator, 300 is Collection Administrator, and 400 is Collection Operator. Default=999

## PvsCeipData

Read/Write Fields

uint Enabled: 1 if CEIP is enabled, otherwise 0. Min=0, Max=1

uint InProgress: 1 if an upload is currently in progress, otherwise 0. Default=0

DateTime NextUpload: Date and time next CEIP upload is due if enabled is 1. Default=Empty

uint OneTimeUpload: 1 to perform a one time upload. Default=0

Guid ServerId: ID of server that is currently uploading, null if InProgress is 0. Default=00000000-0000-0000-0000-000000000000

Read-Only Field

Guid Uuid: CEIP UUID.

## PvsCisData

Read/Write Fields

string Password: Password of the user required to obtain the token. This is required only by Set and Add

string Path: Path where the last problem report bundle was saved Default="" Max Length=255

string UserName: Username used to obtain the token Default="" Max Length=255

Read-Only Fields

Guid Guid or CisDataId: CIS UUID

string UploadToken: Token for uploading bundles to CIS Default="" Max Length=10

## PvsCollection

Read/Write Fields

uint AutoAddNumberLength: The maximum length of the Device Number for Auto Add. This length plus the AutoAddPrefix length plus the AutoAddSuffix length must be less than 16. Required that ((lenautoAddPrefix+lenautoAddSuffix)+AutoAddNumberLength)<=15. Min=3, Max=9, Default=4

string AutoAddPrefix: The string put before the Device Number for Auto Add. Default="" ASCII computer name characters no end digit Max Length=12

string AutoAddSuffix: The string put after the Device Number for Auto Add. Default="" ASCII computer name characters no begin digit Max Length=12

bool AutoAddZeroFill: True when zeros be placed before the Device Number up to the AutoAddNumberLength for Auto Add, false otherwise. Default=true

string Name or CollectionName: Name of the Collection. It is unique within the Site. Max Length=50

string Description: User description. Default="" Max Length=250

bool Enabled: True when Devices in the Collection can be booted, false otherwise. Default=true

uint LastAutoAddDeviceNumber: The Device Number of the last Auto Added Device. Default=0

Guid TemplateDeviceId: GUID of a Device in the Collection whose settings are used for initial values of new Devices. Not used with templateDeviceName. Default=00000000-0000-0000-0000-000000000000

string TemplateDeviceName: Name of a Device in the Collection whose settings are used for initial values of new Devices. Not used with TemplateDeviceId. Default=""

Read-Only Fields

uint ActiveDeviceCount: Read-only count of active Devices in this Collection. Default=0

Guid Guid or CollectionId: Read-only GUID that uniquely identifies this Collection.

uint DeviceCount: Read-only count of Devices in this Collection. Default=0

uint DeviceWithPVDCount: Read-only count of Devices with Personal vDisk in this Collection. Default=0

uint MakActivateNeededCount: Read-only count of active Devices that need MAK activation in this Collection. Default=0

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, 200 is Site Administrator, 300 is Collection Administrator, and 400 is Collection Operator. Default=999

Guid SiteId: GUID of the Site that this Collection is a member of. It is not used with SiteName.

string SiteName: Name of the Site that this Collection is a member of. It is not used with SiteId.

## PvsConnection

Read/Write Fields

string Domain: Domain name to use for Authentication. If it has a value, it will be \*\*\*\*\*. Default=""

string Password: Password to use for Authentication. If it has a value, it will be \*\*\*\*\*. Default=""

string Persist: True when the connection settings should be, for Set, or have been, for Get, saved to the registry.

string Port: The Port to use to connect. Default=54321

string Name or Server: Name or IP of the Server to connect to. Default=localhost

string User: User name to use for Authentication. If it has a value, it will be \*\*\*\*\*. Default=""

Read-Only Field

string Connected: True when the Citrix.PVS.SnapIn is currently connected to the SoapServer with the settings in this PvsConnection.

PvsConnection can be created or modified using methods below:

New-Object Citrix.PVS.SnapIn.PvsConnection: Creates default Server=localhost, Port=54321, and no authentication.

New-Object Citrix.PVS.SnapIn.PvsConnection(Citrix.PVS.SnapIn copyFrom): Creates with settings of the copyFrom Citrix.PVS.SnapIn.

SetServerToLocalHostDefaultSettings: Server=localhost, Port=54321, and no authentication.

Copy(Citrix.PVS.SnapIn copyFrom): Modifies the settings to match the copyFrom Citrix.PVS.SnapIn.

Equals(Citrix.PVS.SnapIn compareTo): Returns true when the settings match what is in the compareTo.

## PvsDevice

Read/Write Fields

string AdPassword: The Active Directory machine account password. Do not set this field, it is only set internally by PVS. Default="" ASCII Max Length=256

uint AdSignature: The signature of the Active Directory machine account password. Do not set this field, it is only set internally by PVS. Default=0

uint AdTimestamp: The time the Active Directory machine account password was generated. Do not set this field, it is only set internally by PVS. Default=0

uint Authentication: Device log in authentication. Choices are 0 for none, 1 for User Name/Password, and 2 for Extern. This cannot be Set for a Device with Personal vDisk. Min=0, Max=2, Default=0

bool BdmBoot: Use PXE boot when set to false, BDM boot when set to true. Default is PXE Default=false

DateTime BdmCreated: Timstamp when BDM device was created  Default=Empty

uint BdmFormat: 1 use VHD for BDMboot, 2 use ISO, 3 use USB. Default=0

uint BdmType: Use PXE boot when set to 0, BDM (Bios) boot when set to 1 and BDM (Uefi) boot when set to 2.  Default=0

DateTime BdmUpdated: Timestamp of the last BDM boot disk update. Default=Empty

uint BootFrom: Device to boot from. Choices are 1 for vDisk, 2 for Hard Disk, and 3 for Floppy. This cannot be Set for a Device with Personal vDisk. Min=1, Max=3, Default=1

string ClassName: Used by Automatic Update feature to match new versions of Disks to a Device. This cannot be Set for a Device with Personal vDisk. Default="" Max Length=41

string Description: User description. Default="" Max Length=250

PvsPhysicalAddress DeviceMac: Ethernet address can have the form XX-XX-XX-XX-XX-XX. Uniquely identifies the Device.

string Name or DeviceName: Computer name with no spaces. ASCII computer name characters Max Length=15

string DomainControllerName: The name of the DC used to create the host's computer account. Do not set this field, it is only set internally by PVS. Default="" Max Length=4000

string DomainName: Fully qualified name of the domain that the Device belongs to. Do not set this field, it is only set internally by PVS. Default="" Max Length=255

string DomainObjectSID: The value of the objectSID AD attribute of the same name for the Device's computer account. Do not set this field, it is only set internally by PVS. Default="" Max Length=186

DateTime DomainTimeCreated: The time that the computer account was created. Has the date and time including milliseconds. Do not set this field, it is only set internally by PVS. Default=Empty

bool Enabled: True when it can be booted, false otherwise. This cannot be Set for a Device with Personal vDisk. Default=true

bool LocalDiskEnabled: If there is a local disk menu choice for the Device, this is true. This cannot be Set for a Device with Personal vDisk. Default=false

uint LocalWriteCacheDiskSize: The size in GB to format the Device cache file disk. If the value is 0, then the disk is not formatted. Min=0, Max=2048, Default=0

uint LogLevel: Level to perform logging at. Values are: 0 (None), 1 (Fatal), 2 (Error), 3 (Warning), 4 (Info), 5 (Debug), and 6 (Trace). Min=0, Max=6, Default=0

string Password: Password of user to authenticate before the boot process continues. This cannot be Set for a Device with Personal vDisk. Default="" ASCII Max Length=100

uint Port: UDP port to use with Stream Service. Min=1025, Max=65534, Default=6901

uint Type: 1 when it performs test of Disks, 2 when it performs maintenance on Disks, 3 when it has a Personal vDisk, 4 when it has a Personal vDisk and performs tests, 0 otherwise. A Device with type 0 - 3 can only be Set to 0 - 3, and a Device with type 3 - 4 can only be Set to 3 - 4. Min=0, Max=4, Default=0

string User: Name of user to authenticate before the boot process continues. This cannot be Set for a Device with Personal vDisk. Default="" ASCII Max Length=20

Guid XsPvsProxyUuid: UUID of XenServer PVS\_proxy Default=00000000-0000-0000-0000-000000000000

Read-Only Fields

bool Active: True if the Device is currently active, false otherwise. Default=false

Guid CollectionId: GUID of the Collection this Device is to be a member of. It is not used with CollectionName.

string CollectionName: Name of the Collection this Device is to be a member of. SiteName or SiteId must also be used.

Guid Guid or DeviceId: Read-only GUID that uniquely identifies this Device.

string HypVmId: Hypervisor VM ID for HCL Default="" Max Length=250

string PvdDriveLetter: Read-only Personal vDisk Drive letter. Range is E to U and W to Z. Default="" Max Length=1

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, 200 is Site Administrator, 300 is Collection Administrator, and 400 is Collection Operator. Default=999

Guid SiteId: GUID of the Site the CollectionName is to be a member of. This or SiteName is used with CollectionName.

string SiteName: Name of the Site the CollectionName is to be a member of. This or SiteId is used with CollectionName.

bool Template: True if the Device is the template in its Collection, false otherwise. Default=false

bool TemporaryVersionSet: Read-only true when temporary version is set. Default=false

Guid VirtualHostingPoolId: GUID that uniquely identifies the Virtual Hosting Pool for a VM. This is needed when Adding a VM device. Default=00000000-0000-0000-0000-000000000000

## PvsDeviceBootstrap

Read-Only Fields

Guid Guid or DeviceId: GUID of the Device.

PvsDeviceBootstrapList: Each one of these has these 2 fields:

string Name or Bootstrap: Name of the bootstrap file. Max Length=259

string MenuText: Text that is displayed in the Boot Menu. If this field has no value, the bootstrap value is used. Default="" ASCII Max Length=64

PvsDeviceBootstrapList\[\] DeviceBootstrap: List of objects that can be changed with the methods below.

Methods

Add(string bootstrap, string menuText): Used to add a PvsDeviceBootstrapList to the end of the array.

Insert(int position, string bootstrap, string menuText): Used to insert a PvsDeviceBootstrapList array item at position. The position is 0 based.

Remove(int position): Used to remove a PvsDeviceBootstrapList array item at position. The position is 0 based.

Set(int position, string menuText): Used to set a PvsDeviceBootstrapList array item MenuText at position. The position is 0 based.

Reorder(int oldPosition, int newPosition): Used to move a PvsDeviceBootstrapList array item from the oldPosition to the newPosition. The oldPosition and newPosition are 0 based.

## PvsDeviceBootstrapList

Read/Write Fields

string Name or Bootstrap: Name of the bootstrap file. Max Length=259

string MenuText: Text that is displayed in the Boot Menu. If this field has no value, the bootstrap value is used. Default="" ASCII Max Length=64

## PvsDeviceDiskTempVersion

Read-Only Fields

Guid Guid or DeviceId: Read-only GUID that uniquely identifies the Device with temporary version.

string Name or DeviceName: Read-only Computer name that uniquely identifies the Device with temporary version. ASCII computer name characters

Guid DiskLocatorId: Read-only GUID that uniquely identifies then Disk Locator with temporary version.

string DiskLocatorName: Read-only Name of the Disk Locator File with temporary version. It is unique within the Store. ASCII

Guid SiteId: Read-only GUID of the Site the Device and DiskLocator are a member of.

string SiteName: Read-only Name of the Site the Device and DiskLocator are a member of.

Guid StoreId: Read-only GUID of the Store that the Disk Locator is a member of.

string StoreName: Read-only Name of the Store that the Disk Locator is a member of.

uint Version: Read-only Disk version the temporary is for.

## PvsDeviceInfo

Read-Only Fields

bool Active: True if the Device is currently active, false otherwise. Default=false

string AdPassword: The Active Directory machine account password. Do not set this field, it is only set internally by PVS. Default="" ASCII Max Length=256

uint AdSignature: The signature of the Active Directory machine account password. Do not set this field, it is only set internally by PVS. Default=0

uint AdTimestamp: The time the Active Directory machine account password was generated. Do not set this field, it is only set internally by PVS. Default=0

uint Authentication: Device log in authentication. Choices are 0 for none, 1 for User Name/Password, and 2 for Extern. This cannot be Set for a Device with Personal vDisk. Min=0, Max=2, Default=0

bool BdmBoot: Use PXE boot when set to false, BDM boot when set to true. Default is PXE Default=false

DateTime BdmCreated: Timstamp when BDM device was created  Default=Empty

uint BdmFormat: 1 use VHD for BDMboot, 2 use ISO, 3 use USB. Default=0

uint BdmType: Use PXE boot when set to 0, BDM (Bios) boot when set to 1 and BDM (Uefi) boot when set to 2.  Default=0

DateTime BdmUpdated: Timestamp of the last BDM boot disk update. Default=Empty

uint BootFrom: Device to boot from. Choices are 1 for vDisk, 2 for Hard Disk, and 3 for Floppy. This cannot be Set for a Device with Personal vDisk. Min=1, Max=3, Default=1

string ClassName: Used by Automatic Update feature to match new versions of Disks to a Device. This cannot be Set for a Device with Personal vDisk. Default="" Max Length=41

Guid CollectionId: GUID of the Collection this Device is to be a member of. It is not used with CollectionName.

string CollectionName: Name of the Collection this Device is to be a member of. SiteName or SiteId must also be used.

string Description: User description. Default="" Max Length=250

Guid Guid or DeviceId: Read-only GUID that uniquely identifies this Device.

PvsPhysicalAddress DeviceMac: Ethernet address can have the form XX-XX-XX-XX-XX-XX. Uniquely identifies the Device.

string Name or DeviceName: Computer name with no spaces. ASCII computer name characters Max Length=15

string DiskFileName: Name of the Disk File including the extension. It is equal to "" if the Device is not active.

Guid DiskLocatorId: Read-only GUID of the Disk Locator that the Device is using. It is equal to 00000000-0000-0000-0000-000000000000 if the Device is not active.

string DiskLocatorName: Read-only name of the Disk Locator File that the Device is using. It is equal to the list of Disk Locator names for the Device if the Device is not active.

uint DiskVersion: Read-only version of the Disk Locator File that the Device is using. It is equal to 0 if the Device is not active. Default=0

uint DiskVersionAccess: State of the Disk Version. Values are: 0 (Production), 1 (Maintenance), 2 (MaintenanceHighestVersion), 3 (Override), 4 (Merge), 5 (MergeMaintenance), 6 (MergeTest), and 7 (Test). It is equal to 0 if the Device is not active. Default=0

string DomainControllerName: The name of the DC used to create the host's computer account. Do not set this field, it is only set internally by PVS. Default="" Max Length=4000

string DomainName: Fully qualified name of the domain that the Device belongs to. Do not set this field, it is only set internally by PVS. Default="" Max Length=255

string DomainObjectSID: The value of the objectSID AD attribute of the same name for the Device's computer account. Do not set this field, it is only set internally by PVS. Default="" Max Length=186

DateTime DomainTimeCreated: The time that the computer account was created. Has the date and time including milliseconds. Do not set this field, it is only set internally by PVS. Default=Empty

bool Enabled: True when it can be booted, false otherwise. This cannot be Set for a Device with Personal vDisk. Default=true

string HypVmId: Hypervisor VM ID for HCL Default="" Max Length=250

System.Net.IPAddress Ip: Read-only IP of the Device. It is equal to 0.0.0.0 if the Device is not active.

uint License: Oem Only: Read-only type of the license. Values are 0 when None, 1 or 2 when Desktop. It is equal to 0 if the Device is not active. Default=0

uint LicenseType: 0 when None, 1 for Desktop, 2 for Server, 5 for OEM SmartClient, 6 for XenApp, 7 for XenDesktop. It is equal to 0 if the Device is not active. Default=0

bool LocalDiskEnabled: If there is a local disk menu choice for the Device, this is true. This cannot be Set for a Device with Personal vDisk. Default=false

uint LocalWriteCacheDiskSize: The size in GB to format the Device cache file disk. If the value is 0, then the disk is not formatted. Min=0, Max=2048, Default=0

uint LogLevel: Level to perform logging at. Values are: 0 (None), 1 (Fatal), 2 (Error), 3 (Warning), 4 (Info), 5 (Debug), and 6 (Trace). Min=0, Max=6, Default=0

uint MakLicenseActivated: Read-only indicator if MAK licensing is being used and is activated. Values are: 0 (MAK not used), 1 (Not Activated), 2 (Activated). It is equal to 0 if the Device is not active. Default=0

string Model: Oem Only: Read-only model of the computer. Values are OptiPlex 745, 755, 320, 760, FX160, or Default. It is equal to "" if the Device is not active.

string Password: Password of user to authenticate before the boot process continues. This cannot be Set for a Device with Personal vDisk. Default="" ASCII Max Length=100

uint Port: UDP port to use with Stream Service. Min=1025, Max=65534, Default=6901

string PvdDriveLetter: Read-only Personal vDisk Drive letter. Range is E to U and W to Z. Default="" Max Length=1

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, 200 is Site Administrator, 300 is Collection Administrator, and 400 is Collection Operator. Default=999

Guid ServerId: Read-only GUID of the Server that the Device is using. It is equal to 00000000-0000-0000-0000-000000000000 if the Device is not active.

System.Net.IPAddress ServerIpConnection: Read-only IP of the Server that the Device is using. It is equal to 0.0.0.0 if the Device is not active.

string ServerName: Read-only Name of the Server that the Device is using. It is equal to "" if the Device is not active.

uint ServerPortConnection: Read-only Port of the Server that the Device is using. It is equal to 0 if the Device is not active. Default=0

Guid SiteId: GUID of the Site the CollectionName is to be a member of. This or SiteName is used with CollectionName.

string SiteName: Name of the Site the CollectionName is to be a member of. This or SiteId is used with CollectionName.

string Status: 1 or 2 numbers in the format n,n. They are the number of retries and if ram cache is being used, ram cache percent used. It is equal to "" if the Device is not active.

bool Template: True if the Device is the template in its Collection, false otherwise. Default=false

bool TemporaryVersionSet: Read-only true when temporary version is set. Default=false

uint Type: 1 when it performs test of Disks, 2 when it performs maintenance on Disks, 3 when it has a Personal vDisk, 4 when it has a Personal vDisk and performs tests, 0 otherwise. Min=0, Max=4, Default=0

string User: Name of user to authenticate before the boot process continues. This cannot be Set for a Device with Personal vDisk. Default="" ASCII Max Length=20

Guid VirtualHostingPoolId: GUID that uniquely identifies the Virtual Hosting Pool for a VM. This is needed when Adding a VM device. Default=00000000-0000-0000-0000-000000000000

Guid XsPvsProxyUuid: UUID of XenServer PVS\_proxy Default=00000000-0000-0000-0000-000000000000

## PvsDevicePersonality

Read-Only Fields

Guid Guid or DeviceId: GUID of the Device.

PvsDevicePersonalityList: Each one of these has these 2 fields:

string Name: Name of the Device personality item. Max Length=250

string Value: Value for the Device personality item. Max Length=1000

PvsDevicePersonalityList\[\] DevicePersonality: List of objects that can be changed with the methods below.

Methods

Add(string name, string value): Used to add a PvsDevicePersonalityList to the end of the array.

Insert(int position, string name, string value): Used to insert a PvsDevicePersonalityList array item at position. The position is 0 based.

Remove(int position): Used to remove a PvsDevicePersonalityList array item at position. The position is 0 based.

Set(int position, string value): Used to set a PvsDevicePersonalityList array item Value at position. The position is 0 based.

Reorder(int oldPosition, int newPosition): Used to move a PvsDevicePersonalityList array item from the oldPosition to the newPosition. The oldPosition and newPosition are 0 based.

## PvsDevicePersonalityList

Read/Write Fields

string Name: Name of the Device personality item. Max Length=250

string Value: Value for the Device personality item. Max Length=1000

## PvsDeviceStatus

Read-Only Fields

Guid Guid or DeviceId: Read-only GUID of the Device. Can be used with Get Device.

string Name or DeviceName: Read-only Name of the Device. Can be used with Get Device.

string DiskFileName: Name of the Disk File including the extension.

Guid DiskLocatorId: Read-only GUID of the Disk Locator that the Device is using.

string DiskLocatorName: Read-only name of the Disk Locator File that the Device is using.

uint DiskVersion: Read-only version of the Disk Locator File that the Device is using. Default=0

uint DiskVersionAccess: State of the Disk Version. Values are: 0 (Production), 1 (Maintenance), 2 (MaintenanceHighestVersion), 3 (Override), 4 (Merge), 5 (MergeMaintenance), 6 (MergeTest), and 7 (Test) Default=0

System.Net.IPAddress Ip: Read-only IP of the Device.

uint LicenseType: 0 when None, 1 for Desktop, 2 for Server, 5 for OEM SmartClient, 6 for XenApp, 7 for XenDesktop. Default=0

uint MakLicenseActivated: Read-only indicator if MAK licensing is being used and is activated. Values are: 0 (MAK not used), 1 (Not Activated), 2 (Activated). Default=0

Guid ServerId: Read-only GUID of the Server that the Device is using.

System.Net.IPAddress ServerIpConnection: Read-only IP of the Server that the Device is using.

string ServerName: Read-only Name of the Server that the Device is using.

uint ServerPortConnection: Read-only Port of the Server that the Device is using. Default=0

string Status: 1 or 2 numbers in the format n,n. They are the number of retries and if ram cache is being used, ram cache percent used.

## PvsDisk

Read/Write Fields

bool AccelerateOfficeActivation: Run script to activate office automatically.

bool ActivationDateEnabled: Use activation date to activate image when set to true. Default false

DateTime ActiveDate: Date to activate the disk if AutoUpdateEnabled and activationDateEnabled are true. Has the date. Empty when the AutoUpdateEnabled or activationDateEnabled are false.

bool AdPasswordEnabled: Enable AD password management when set to true.

string Author: User defined author. Max Length=40

bool AutoUpdateEnabled: Automatically update this image for matching Devices when set to true. Default false

UInt64 Build: User defined build number. Min=0, Max=4294967295, Default=0

string Class: Class of the Disk. Max Length=40

string ClearCacheDisabled: Clear cached secrets disabled.

string Company: User defined company. Max Length=40

string Date: User defined date. Max Length=40

bool VHDX: If VHDX is true, the format of the image is VHDX. Otherwise it is VHD. Default=false

bool HaEnabled: Enable HA when set to true.

string HardwareTarget: User defined hardware target. Max Length=127

string ImageType: Type of this image (software type). Max Length=40

string InternalName: User defined name. Max Length=63

uint LicenseMode: 0 (None), 1 (Multiple Activation Key), or 2 (Key Management Service). Min=0, Max=2, Default=0

string LongDescription: Description of the Disk. Max Length=399

UInt64 MajorRelease: User defined major release number. Min=0, Max=4294967295, Default=0

UInt64 MinorRelease: User defined minor release number. Min=0, Max=4294967295, Default=0

string OperatingSystem: Operating System of Disk. Max Length=250

string OriginalFile: User defined original file. Max Length=127

string OsType: Operating System Type of Disk. Max Length=40

bool PrinterManagementEnabled: Invalid printers will be deleted from the Device when set to true.

string SerialNumber: User defined serial number. Max Length=36

string Title: User defined title. Max Length=40

UInt64 WriteCacheSize: RAM cache size (MB). Not 0 when used with Cache in Device RAM, and Cache in Device RAM with Overflow on Hard Disk. A value of 0 will disable the RAM use for Cache in Device RAM with Overflow on Hard Disk. Min=0, Max=131072, Default=0

uint WriteCacheType: 0 (Private), 1 (Cache on Server), 3 (Cache in Device RAM), 4 (Cache on Device Hard Disk), 7 (Cache on Server, Persistent), 9 (Cache in Device RAM with Overflow on Hard Disk), 10 (Private async), 11(Server persistent async), 12 (Cache in Device RAM with Overflow on Hard Disk async) Min=0, Max=12, Default=0

Read-Only Fields

Guid Guid or DiskLocatorId: GUID of the DiskLocator used for Get and Set.

UInt64 DiskSize: Read-only size of the image. The value is 0 when it is not available. Default=0

string LogicalSectorSize: Logical Sector Size. Values are: 512, 4096, Default=512

uint VhdBlockSize: Block size in KB. For VHD it is only used with Dynamic type. Tested sizes for VHD are 512, 2048, and 16384. VHD Min=512, Max=16384, Default=2048. For VHDX it is used for all types. Tested size for VHDX is 32768. VHDX Min=1024, Max= 262144, Default=32768. Default=0

## PvsDiskInfo

Read-Only Fields

bool AccelerateOfficeActivation: Run script to activate office automatically.

bool ActivationDateEnabled: Use activation date to activate image when set to true. Default false

bool Active: True if the DiskLocator is currently active, false otherwise. Default=false

DateTime ActiveDate: Date to activate the disk if AutoUpdateEnabled and activationDateEnabled are true. Has the date. Empty when the AutoUpdateEnabled or activationDateEnabled are false.

bool AdPasswordEnabled: Enable AD password management when set to true.

string Author: User defined author. Max Length=40

bool AutoUpdateEnabled: Automatically update this image for matching Devices when set to true. Default false

UInt64 Build: User defined build number. Min=0, Max=4294967295, Default=0

string Class: Class of the Disk. Max Length=40

string ClearCacheDisabled: Clear cached secrets disabled.

string Company: User defined company. Max Length=40

string Date: User defined date. Max Length=40

string Description: User description. Default="" Max Length=250

uint DeviceCount: Read-only count of Devices. Default=0

Guid Guid or DiskLocatorId: Read-only GUID that uniquely identifies this Disk Locator.

string Name or DiskLocatorName: Name of the Disk Locator File. It is unique within the Store. ASCII Max Length=52

UInt64 DiskSize: Read-only size of the image. The value is 0 when it is not available. Default=0

Guid DiskUpdateDeviceId: GUID of the DiskUpdateDevice that is used when updates are performed. Default=00000000-0000-0000-0000-000000000000

string DiskUpdateDeviceName: Name of the DiskUpdateDevice that is used when updates are performed. Default=""

bool Enabled: True when this disk can be booted, false otherwise. Default=true

bool EnabledForDevice: True when this disk is enabled for the Device specified, false otherwise. This is only returned when a Device is specified. Default=true

bool VHDX: If VHDX is true, the format of the image is VHDX. Otherwise it is VHD. Default=false

bool HaEnabled: Enable HA when set to true.

string HardwareTarget: User defined hardware target. Max Length=127

string ImageType: Type of this image (software type). Max Length=40

string InternalName: User defined name. Max Length=63

uint LicenseMode: 0 (None), 1 (Multiple Activation Key), or 2 (Key Management Service). Min=0, Max=2, Default=0

bool Locked: True if the Disk is currently locked, false otherwise. Default=false

string LogicalSectorSize: Logical Sector Size. Values are: 512, 4096, Default=512

string LongDescription: Description of the Disk. Max Length=399

UInt64 MajorRelease: User defined major release number. Min=0, Max=4294967295, Default=0

bool Mapped: True if the Disk is currently mapped, false otherwise. Default=false

string MenuText: Text that is displayed in the Boot Menu. If this field has no value, the name value is used. Default="" ASCII Max Length=64

UInt64 MinorRelease: User defined minor release number. Min=0, Max=4294967295, Default=0

string OperatingSystem: Operating System of Disk. Max Length=250

string OriginalFile: User defined original file. Max Length=127

string OsType: Operating System Type of Disk. Max Length=40

bool PrinterManagementEnabled: Invalid printers will be deleted from the Device when set to true.

bool RebalanceEnabled: True when this Server can automatically rebalance Devices, false otherwise. Default=false

uint RebalanceTriggerPercent: Percent over fair load that triggers a dynamic Device rebalance. Min=5, Max=5000, Default=25

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, 200 is Site Administrator, 300 is Collection Administrator, and 999 is read-only. Default=999

string SerialNumber: User defined serial number. Max Length=36

Guid ServerId: GUID of the single Server that this Disk Locator is assigned to. It is not used with ServerName. Default=00000000-0000-0000-0000-000000000000

string ServerName: Name of the single Server that this Disk Locator is assigned to. It is not used with ServerId. Default=""

Guid SiteId: GUID of the Site this DiskLocator is to be a member of. It is not used with SiteName.

string SiteName: Name of the Site this DiskLocator is to be a member of. It is not used with SiteId.

Guid StoreId: GUID of the Store that this Disk Locator is a member of. SiteName or SiteId must also be used. It is not used with StoreName.

string StoreName: Name of the Store that this Disk Locator is a member of. SiteName or SiteId must also be used. It is not used with StoreId.

uint SubnetAffinity: Qualifier for subnet affinity when assigning a Server. 0=None, 1=Best Effort, 2=Fixed. Min=0, Max=2, Default=0

bool TemporaryVersionSet: Read-only true when temporary version(s) are set. Default=false

string Title: User defined title. Max Length=40

uint VhdBlockSize: Block size in KB. For VHD it is only used with Dynamic type. Tested sizes for VHD are 512, 2048, and 16384. VHD Min=512, Max=16384, Default=2048. For VHDX it is used for all types. Tested size for VHDX is 32768. VHDX Min=1024, Max= 262144, Default=32768. Default=0

UInt64 WriteCacheSize: RAM cache size (MB). Not 0 when used with Cache in Device RAM, and Cache in Device RAM with Overflow on Hard Disk. A value of 0 will disable the RAM use for Cache in Device RAM with Overflow on Hard Disk. Min=0, Max=131072, Default=0

uint WriteCacheType: 0 (Private), 1 (Cache on Server), 3 (Cache in Device RAM), 4 (Cache on Device Hard Disk), 7 (Cache on Server, Persistent), 9 (Cache in Device RAM with Overflow on Hard Disk), 10 (Private async), 11(Server persistent async), 12 (Cache in Device RAM with Overflow on Hard Disk async) Min=0, Max=12, Default=0

## PvsDiskInventory

Read-Only Fields

string Active: 1 if the Server is currently active, 2 if unknown, and 0 otherwise.

Guid Guid or DiskLocatorId: GUID of the DiskLocator used for Get and Set.

string FilePath: Path used to access the disk version from the Server. Empty if the information is not available.

DateTime FileTime: Date/Time of the date version file. Has the date and time without milliseconds. Empty if the information is not available.

DateTime PropertiesTime: Date/Time of the disk properties. Has the date and time without milliseconds. Empty if the information is not available.

Guid ServerId: GUID of the Server that the Disk Version Inventory is being reported about.

string ServerName: Name of the Server that the Disk Version Inventory is being reported about.

string State: The number code of the inventory state. Values are: 0 (Up to date), 1 (version file is missing), 2 (version file is out of date), 3 (properties are missing), 4 (properties are out of date), 5 (server is not reachable).

string Version: Version number. The base disk is version 0, the other version numbers are in part of the file name.

## PvsDiskLocator

Read/Write Fields

string Description: User description. Default="" Max Length=250

bool Enabled: True when this disk can be booted, false otherwise. Default=true

string MenuText: Text that is displayed in the Boot Menu. If this field has no value, the name value is used. Default="" ASCII Max Length=64

bool RebalanceEnabled: True when this Server can automatically rebalance Devices, false otherwise. Default=false

uint RebalanceTriggerPercent: Percent over fair load that triggers a dynamic Device rebalance. Min=5, Max=5000, Default=25

Guid ServerId: GUID of the single Server that this Disk Locator is assigned to. It is not used with ServerName. Default=00000000-0000-0000-0000-000000000000

string ServerName: Name of the single Server that this Disk Locator is assigned to. It is not used with ServerId. Default=""

uint SubnetAffinity: Qualifier for subnet affinity when assigning a Server. 0=None, 1=Best Effort, 2=Fixed. Min=0, Max=2, Default=0

Read-Only Fields

bool Active: True if the DiskLocator is currently active, false otherwise. Default=false

Guid Guid or DiskLocatorId: Read-only GUID that uniquely identifies this Disk Locator.

string Name or DiskLocatorName: Name of the Disk Locator File. It is unique within the Store. ASCII Max Length=52

Guid DiskUpdateDeviceId: GUID of the DiskUpdateDevice that is used when updates are performed. Default=00000000-0000-0000-0000-000000000000

string DiskUpdateDeviceName: Name of the DiskUpdateDevice that is used when updates are performed. Default=""

bool EnabledForDevice: True when this disk is enabled for the Device specified, false otherwise. This is only returned when a Device is specified. Default=true

bool Mapped: True if the Disk is currently mapped, false otherwise. Default=false

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, 200 is Site Administrator, 300 is Collection Administrator, and 999 is read-only. Default=999

Guid SiteId: GUID of the Site this DiskLocator is to be a member of. It is not used with SiteName.

string SiteName: Name of the Site this DiskLocator is to be a member of. It is not used with SiteId.

Guid StoreId: GUID of the Store that this Disk Locator is a member of. SiteName or SiteId must also be used. It is not used with StoreName.

string StoreName: Name of the Store that this Disk Locator is a member of. SiteName or SiteId must also be used. It is not used with StoreId.

bool TemporaryVersionSet: Read-only true when temporary version(s) are set. Default=false

## PvsDiskLocatorLock

Read-Only Fields

Guid DeviceId: GUID of the Device that has the lock, will be 00000000-0000-0000-0000-000000000000 if a Server has the lock.

string DeviceName: Name of the Device that has the lock, will not be included if a Server has the lock.

bool Exclusive: True when the lock is exclusive, false when it is shared. Default=false

bool ReadOnly: True when lock is because file system is read only, false when file system is read write Default=false

Guid ServerId: GUID of the Server that has the lock, will be 00000000-0000-0000-0000-000000000000 if a Device has the lock.

string ServerName: Name of the Server that has the lock, will not be included if a Device has the lock.

## PvsDiskUpdateDevice

Read/Write Fields

string AdPassword: The Active Directory machine account password. Do not set this field, it is only set internally by PVS. Default="" Max Length=256

uint AdSignature: The signature of the Active Directory machine account password. Do not set this field, it is only set internally by PVS. Default=0

uint AdTimestamp: The time the Active Directory machine account password was generated. Do not set this field, it is only set internally by PVS. Default=0

string Description: User description. Default="" Max Length=250

string DomainControllerName: The name of the DC used to create the host's computer account. Do not set this field, it is only set internally by PVS. Default="" Max Length=4000

string DomainName: Fully qualified name of the domain that the Device belongs to. Do not set this field, it is only set internally by PVS. Default="" Max Length=255

string DomainObjectSID: The value of the objectSID AD attribute of the same name for the Device's computer account. Do not set this field, it is only set internally by PVS. Default="" Max Length=186

DateTime DomainTimeCreated: The time that the computer account was created. Has the date and time including milliseconds. Do not set this field, it is only set internally by PVS. Default=Empty

uint LogLevel: Level to perform logging at. Values are: 0 (None), 1 (Fatal), 2 (Error), 3 (Warning), 4 (Info), 5 (Debug), and 6 (Trace). Min=0, Max=6, Default=0

uint Port: UDP port to use with Stream Service. Min=1025, Max=65534, Default=6901

Read-Only Fields

bool Active: True if the Device is currently active, false otherwise. Default=false

Guid Guid or DeviceId: Read-only GUID that uniquely identifies this Device.

PvsPhysicalAddress DeviceMac: Ethernet address can have the form XX-XX-XX-XX-XX-XX. Uniquely identifies the Device.

string Name or DeviceName: Computer name with no spaces. ASCII computer name characters Max Length=15

Guid DiskLocatorId: GUID of the Disk Locator to update with this Device.

string DiskLocatorName: Name of the Disk Locator File to update with this Device.

uint DiskVersion: Read-only version of the Disk Locator File that the Device is using. It is equal to 0 if the Device is not active. Default=0

System.Net.IPAddress Ip: Read-only IP of the Device. It is equal to 0.0.0.0 if the Device is not active.

uint License: Oem Only: Read-only type of the license. Values are 0 when None, 1 or 2 when Desktop. It is equal to 0 if the Device is not active. Default=0

uint LicenseType: 0 when None, 1 for Desktop, 2 for Server, 5 for OEM SmartClient, 6 for XenApp, 7 for XenDesktop. It is equal to 0 if the Device is not active. Default=0

uint MakLicenseActivated: Read-only indicator if MAK licensing is being used and is activated. Values are: 0 (MAK not used), 1 (Not Activated), 2 (Activated). It is equal to 0 if the Device is not active. Default=0

string Model: Oem Only: Read-only model of the computer. Values are OptiPlex 745, 755, 320, 760, FX160, or Default. It is equal to "" if the Device is not active.

Guid ServerId: Read-only GUID of the Server that the Device is using. It is equal to 00000000-0000-0000-0000-000000000000 if the Device is not active.

System.Net.IPAddress ServerIpConnection: Read-only IP of the Server that the Device is using. It is equal to 0.0.0.0 if the Device is not active.

string ServerName: Read-only Name of the Server that the Device is using. It is equal to "" if the Device is not active.

uint ServerPortConnection: Read-only Port of the Server that the Device is using. It is equal to 0 if the Device is not active. Default=0

Guid SiteId: GUID of the Site this Disk Update Device is to be a member of.

string SiteName: Name of the Site this Disk Update Device is to be a member of.

string Status: 1 or 2 numbers in the format n,n. They are the number of retries and if ram cache is being used, ram cache percent used. It is equal to "" if the Device is not active.

Guid StoreId: GUID of the Store that the Disk Locator is a member of.

string StoreName: Name of the Store that the Disk Locator is a member of.

Guid VirtualHostingPoolId: GUID of the Virtual Hosting Pool. It is not used with VirtualHostingPoolName. Default=00000000-0000-0000-0000-000000000000

string VirtualHostingPoolName: Name of the Virtual Hosting Pool.

## PvsDiskUpdateStatus

Read-Only Fields

uint CurrentStatus: Current status of the update. Values are: 0 (Ready), 1 (Update Pending), 2 (Preparing Image), 3 (Starting VM), 4 (Update In Progress), 5 (Stopping VM), 6 (Submitting Image), 7 (Reverting Image), 8 (Invalid), 9 (Aborted), 10 (Completed Successfully), 11 (No Updates) Min=0, Max=11, Default=0

string CurrentStatusMessage: Message string that includes the results of the run. Default="" Max Length=255

string Description: User description of the Update Task.

Guid DeviceId: GUID that Device being used to do the update.

string DeviceName: Name of the Device being used to do the update.

Guid DiskLocatorId: GUID of the Disk Locator to update.

string Name or DiskLocatorName: Name of the Disk Locator File to update.

Guid Guid or DiskUpdateTaskId: GUID that uniquely identifies this Update Task and Device relationship.

uint PreviousResult: Status of the last run. Values are: 0 (Ready), 1 (Update Pending), 2 (Preparing Image), 3 (Starting VM), 4 (Update In Progress), 5 (Stopping VM), 6 (Submitting Image), 7 (Reverting Image), 8 (Invalid), 9 (Aborted), 10 (Completed Successfully), 11 (No Updates) Min=0, Max=11, Default=0

string PreviousResultMessage: Message string that includes the results of the last run. Default="" Max Length=255

Guid SiteId: GUID of the Site that this Update Task Name is a member of.

string SiteName: Name of the Site that this Update Task Name is a member of.

Guid StoreId: GUID of the Store that the Disk Locator is a member of.

string StoreName: Name of the Store that the Disk Locator is a member of.

Guid UpdateTaskId: GUID that uniquely identifies the Update Task.

string UpdateTaskName: Name of the Update Task.

Guid VirtualHostingPoolId: GUID of the Virtual Hosting Pool being used for the update.

string VirtualHostingPoolName: Name of the Virtual Hosting Pool being used for the update.

## PvsDiskVersion

Read/Write Fields

string Description: User description. Default="" Max Length=250

DateTime ScheduledDate: Date/Time that the Disk Version is scheduled to become available. Has the date, hour and minute. Empty when the disk version is made available immediately. Default=Empty

Read-Only Fields

uint Access: Read-only access of the Disk Version. Values are: 0 (Production), 1 (Maintenance), 2 (MaintenanceHighestVersion), 3 (Override), 4 (Merge), 5 (MergeMaintenance), 6 (MergeTest), and 7 (Test) Min=0, Max=7, Default=0

bool CanDelete: Read-only true when the version can be deleted. Default=false

bool CanMerge: Read-only true when the version can be update merged. Will be set for the highest version number. Default=false

bool CanMergeBase: Read-only true when the version can be base merged. Will be set for the highest version number. Default=false

bool CanOverride: Read-only true when the version can be set as the Override. Default=false

bool CanPromote: Read-only true when the version can be promoted. Default=false

bool CanRevertMaintenance: Read-only true when the version can be reverted to Maintenance Access. Default=false

bool CanRevertTest: Read-only true when the version can be reverted to Test Access. Default=false

bool CanSetScheduledDate: Read-only true when the version can have the scheduled date modified. Default=false

string CreateDate: Read-only Date/Time that the Disk Version was created. Default=getdate

bool DeleteWhenFree: Read-only true if the Disk Version is no longer needed because of a merge. If not current booted by a Device, it can be deleted. Default=false

uint DeviceCount: Read-only count of Devices. Default=0

string Name or DiskFileName: Name of the Disk File including the extension. Default=""

Guid Guid or DiskLocatorId: GUID of the DiskLocator used for Get and Set.

bool GoodInventoryStatus: True when the up to date file is accessible by all Servers, false otherwise. Default=false

bool IsPending: Read-only true when the version ScheduledDate has not occurred. Default=false

uint TaskId: When a Merge is occurring, this will be set with the task number of the process that is occurring. Default=""

bool TemporaryVersionSet: Read-only true when temporary version(s) are set. Some changes cannot be made to the version when this is set. Default=false

uint Type: Read-only type of the Disk Version. Values are: 0 (Base), 1 (Manual), 2 (Automatic), 3 (Merge), and 4 (MergeBase) Min=0, Max=4, Default=0

uint Version: Read-only version number. The base disk is version 0, the other version numbers are in part of the file name. Default=0

## PvsFarm

Read/Write Fields

bool AuditingEnabled: True when Auditing is enabled, false otherwise. Default=false

bool AutoAddEnabled: True when Auto Add is enabled, false otherwise. Default=false

bool AutomaticMergeEnabled: True when Automatic Merge is enabled, false otherwise. If the number of versions becomes more than the MaxVersions value, a merge will occur at the end of PromoteDiskVersion. Default=true

Guid DefaultSiteId: GUID of the Site to place new Devices into automatically. Not used with defaultSiteName. Default=00000000-0000-0000-0000-000000000000

string DefaultSiteName: Name of the Site to place new Devices into automatically. Not used with DefaultSiteId. Default=""

string Description: User description. Default="" Max Length=250

string Name or FarmName: Name of the Farm. Default="" Max Length=50

DateTime LastAuditArchiveDate: Last date of Audit Trail data that was Archived. Has the date. Default=Empty

string LicenseServer: License server name. Default="" Max Length=255

uint LicenseServerPort: License server port. Min=1025, Max=65534, Default=27000

uint LicenseSKU: LicenseSKU. 0 for on-premises, 1 for cloud. Min=0, Max=1, Default=0

bool LicenseTradeUp: License server trade up, when set to true. Default=false

uint MaxVersions: Maximum number a versions of a Disk that can exist before a merge will automatically occur. Min=3, Max=50, Default=5

uint MergeMode: Mode to place the version in after a merge has occurred. Values are: 0 (Production), 1 (Test) and 2 (Maintenance). Min=0, Max=2, Default=2

bool OfflineDatabaseSupportEnabled: True when Offline Database Support is enabled, false otherwise. Default=false

Read-Only Fields

bool AdGroupsEnabled: Active Directory groups are used for authorization, when set to true. Windows groups are used when set to false. Default=false

string DatabaseInstanceName: Read-only name of the database instance.

string DatabaseName: Read-only name of the database.

string DatabaseServerName: Read-only name of the database server.

string FailoverPartnerInstanceName: Read-only name of the database server instance.

string FailoverPartnerServerName: Read-only name of the database server.

Guid Guid or FarmId: Read-only GUID that uniquely identifies this Farm.

string MultiSubnetFailover: Read-only Database MultiSubnetFailover value

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, and 999 is read-only. Default=999

## PvsFarmView

Read/Write Fields

string Description: User description. Default="" Max Length=250

string Name or FarmViewName: name of the Farm View. Max Length=50

Read-Only Fields

uint ActiveDeviceCount: Read-only count of active Devices in this Farm View. Default=0

uint DeviceCount: Read-only count of Devices in this Farm View. Default=0

Guid Guid or FarmViewId: Read-only GUID that uniquely identifies this Farm View.

uint MakActivateNeededCount: Read-only count of active Devices that need MAK activation in this Farm View. Default=0

## PvsGroup

Read-Only Fields

Guid Guid: GUID of the Active Directory group. 00000000-0000-0000-0000-000000000000 for Windows groups.

string Name: Name of the Group.

## PvsLocalServer

Read-Only Field

string Name or LocalServer: NetBios name of local server.

## PvsNewDiskVersion

Read-Only Fields

string Name: Name of the disk file without the extension.

uint Status: Status of the disk file. Values are: 0 (Valid), 1 (Missing Properties File), 2 (Access Denied), 3 (Access Denied and Missing Properties File), 4 (Invalid Disk File), 5 (Manifest Invalid)

## PvsPhysicalAddress

Derived from System.Net.NetworkInformation.PhysicalAddress. GetString() returns a - delimited MAC address.

## PvsServer

Read/Write Fields

uint AdMaxPasswordAge: Number of days before a password expires. Min=1, Max=30, Default=7

bool AdMaxPasswordAgeEnabled: Age the password, when set to true. Default=false

uint BootPauseSeconds: Number of seconds that a Device will pause during login if its server busy. Min=1, Max=60, Default=10

uint BuffersPerThread: Number of buffers per worker thread. Min=1, Max=128, Default=24

uint BusyDbConnectionRetryCount: Number of times a failed database connection will be retried. Min=0, Max=32767, Default=2

uint BusyDbConnectionRetryInterval: Interval, in number of milliseconds, the server should wait before retrying to connect to a database. Min=0, Max=10000, Default=25

string Description: User description. Default="" Max Length=250

bool EventLoggingEnabled: Enable event logging, when set to true. Default=false

uint FirstPort: Number of the first UDP port for use by the Stream Service, First and Last must allow at least 5 ports. Min=1025, Max=65534, Default=6910

uint InitialQueryConnectionPoolSize: Initial size of database connection pool for non-transactional queries. Min=1, Max=1000, Default=50

uint InitialTransactionConnectionPoolSize: Initial size of database connection pool for transactional queries. Min=1, Max=1000, Default=50

uint IoBurstSize: Number of bytes read/writes can send in a burst of packets. Required that IoBurstSize/(MaxTransmissionUnits-76)<=32. Min=4096, Max=61440, Default=32768

System.Net.IPAddress\[\] Ip: One or more streaming ip addresses.

DateTime LastBugReportAttempt: Time that this server last attempted to upload or generate a bug report bundle. Default=Empty

string LastBugReportResult: Status of the last bug report on this server. Default="" Max Length=4000

string LastBugReportStatus: Status of the last bug report on this server. Default="" Max Length=250

string LastBugReportSummary: Summary of the last bug report on this server. Default="" Max Length=250

DateTime LastCeipUploadAttempt: Time that this server last attempted a CEIP upload. Default=Empty

uint LastPort: Number of the last UDP port for use by the Stream Service, First and Last must allow at least 5 ports. Min=1025, Max=65534, Default=6930

uint LicenseTimeout: Amount of seconds before a license times out. Min=15, Max=300, Default=30

uint LocalConcurrentIoLimit: Maximum concurrent IO transactions it performs for vDisks that are local. A value of 0 disables the feature. Min=0, Max=128, Default=4

uint LogFileBackupCopiesMax: Maximum number of log file backups. Min=1, Max=50, Default=4

uint LogFileSizeMax: Maximum size log files can reach in Megabytes. Min=1, Max=50, Default=5

uint LogLevel: Level to perform logging at. Values are: 0 (None), 1 (Fatal), 2 (Error), 3 (Warning), 4 (Info), 5 (Debug), and 6 (Trace). Min=0, Max=6, Default=4

uint MaxBootDevicesAllowed: Maximum number of Devices allowed to boot simultaneously. Min=1, Max=1000, Default=500

uint MaxBootSeconds: Maximum number of seconds for a Device to boot. Min=10, Max=900, Default=60

uint MaxQueryConnectionPoolSize: Maximum size of database connection pool for non-transactional queries. Min=1, Max=32767, Default=1000

uint MaxTransactionConnectionPoolSize: Maximum size of database connection pool for transactional queries. Min=1, Max=32767, Default=1000

uint MaxTransmissionUnits: Ethernet maximum transmission unit size for the protocol for use for Server and Device. Required that IoBurstSize/(MaxTransmissionUnits-76)<=32. Min=502, Max=16426, Default=1506

bool NonBlockingIoEnabled: Use non-Blocking IO, when set to true. Default=true

float PowerRating: A strictly relative rating of this Server's capabilities when compared to other Servers in the Store(s) it belongs too; can be used to help tune load balancing. Min=0.1, Max=1000, Default=1

uint RefreshInterval: Interval, in number of seconds, the server should wait before refreshing settings. If set to 0, unused database connections are never released. Min=0, Max=32767, Default=300

uint RemoteConcurrentIoLimit: Maximum concurrent IO transactions it performs for vDisks that are remote. A value of 0 disables the feature. Min=0, Max=128, Default=4

uint ServerCacheTimeout: Number of seconds to wait before considering another Server is down. Min=5, Max=60, Default=8

string Name or ServerName: Computer name with no spaces. ASCII computer name characters Max Length=21

uint ThreadsPerPort: Number of worker threads per IO port. Required that (threadPerPort \* numberPorts \* numberIPs) <= 1000. Min=1, Max=60, Default=8

uint UnusedDbConnectionTimeout: Interval, in number of seconds, a connection should go unused before it is to be released. Min=0, Max=32767, Default=300

uint VDiskCreatePacing: VDisk create time pacing in milliseconds. Min=0, Max=5, Default=0

Read-Only Fields

uint Active: 1 if the Server is currently active, 2 if unknown, and 0 otherwise. Min=0, Max=2, Default=0

System.Net.IPAddress ManagementIp: IP address used for management communications between Servers. Default=0.0.0.0

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, and 200 is Site Administrator. Default=999

string ServerFqdn: Read-only fully qualified domain name. Default="" Max Length=1024

Guid Guid or ServerId: Read-only GUID that uniquely identifies this Server.

Guid SiteId: GUID of the Site this Server is to be a member of. It is not used with SiteName.

string SiteName: Name of the Site this Server is to be a member of. It is not used with SiteId.

## PvsServerBiosBootstrap

Read/Write Fields

bool BootFromHdOnFail: For network recovery reboot to hard drive when set to true, restore network connection when set to false. Default=false

System.Net.IPAddress Bootserver1\_Ip: 1st boot server IP. Only used when Lookup is false.

uint Bootserver1\_Port: 1st boot server port. Only used when Lookup is false. Min=1025, Max=65536, Default=6910

System.Net.IPAddress Bootserver2\_Ip: 2nd boot server IP. Only used when Lookup is false. Default=0.0.0.0

uint Bootserver2\_Port: 2nd boot server port. Only used when Lookup is false. Min=1025, Max=65536, Default=6910

System.Net.IPAddress Bootserver3\_Ip: 3rd boot server IP. Only used when Lookup is false. Default=0.0.0.0

uint Bootserver3\_Port: 3rd boot server port. Only used when Lookup is false. Min=1025, Max=65536, Default=6910

System.Net.IPAddress Bootserver4\_Ip: 4th boot server IP. Only used when Lookup is false. Default=0.0.0.0

uint Bootserver4\_Port: 4th boot server port. Only used when Lookup is false. Min=1025, Max=65536, Default=6910

bool DhcpEnabled: Use DHCP to retrieve target device IP when set to true, otherwise use the static domain, dnsIpAddresstrue and dnsIpAddress2 settings. Default=true

System.Net.IPAddress DnsIpAddress1: Primary DNS server IP. Only used when DhcpEnabled is false.

System.Net.IPAddress DnsIpAddress2: Secondary DNS server IP. Only used when DhcpEnabled is false.

string Domain: Domain of the primary and secondary DNS servers. Only used when DhcpEnabled is false.

bool Enabled: Automatically update the BIOS on the target device with these setting when set to true, otherwise do not use these settings. Default=false

uint GeneralTimeout: Login general timeout in milliseconds. Min=1000, Max=60000, Default=5000

bool InterruptSafeMode: Interrupt safe mode (use if target device hangs during boot) when set to true. Default=false

bool Lookup: Use DNS to find the Server when set to true with the ServerName host value, otherwise use the bootservertrue\_Ip, bootservertrue\_Port, bootserver2\_Ip, bootserver2\_Port, bootserver3\_Ip, bootserver3\_Port, bootserver4\_Ip, and bootserver4\_Port settings. Default=true

bool PaeMode: PAE mode (use if PAE enabled in boot.ini of target device) when set to true. Default=false

uint PollingTimeout: Login polling timeout in milliseconds. Min=1000, Max=60000, Default=5000

uint RecoveryTime: When bootFromHdOnFail is 1, this is the number of seconds to wait before reboot to hard drive. Min=10, Max=60000, Default=50

string Name or ServerName: Host to use for DNS lookup. Only used when Lookup is true. Default=IMAGESERVER1

bool VerboseMode: Display verbose diagnostic information when set to true. Default=false

Read-Only Field

Guid Guid or ServerId: GUID of the Server used for Get and Set.

## PvsServerBootstrap

Read/Write Fields

bool BootFromHdOnFail: For network recovery reboot to hard drive when set to true, restore network connection when set to false. Default=false

System.Net.IPAddress Bootserver1\_Gateway: 1st boot server gateway. Default=0.0.0.0

System.Net.IPAddress Bootserver1\_Ip: 1st boot server IP.

System.Net.IPAddress Bootserver1\_Netmask: 1st boot server netmask. Default=0.0.0.0

uint Bootserver1\_Port: 1st boot server port. Min=1025, Max=65536, Default=6910

System.Net.IPAddress Bootserver2\_Gateway: 2nd boot server gateway. Default=0.0.0.0

System.Net.IPAddress Bootserver2\_Ip: 2nd boot server IP. Default=0.0.0.0

System.Net.IPAddress Bootserver2\_Netmask: 2nd boot server netmask. Default=0.0.0.0

uint Bootserver2\_Port: 2nd boot server port. Min=1025, Max=65536, Default=6910

System.Net.IPAddress Bootserver3\_Gateway: 3rd boot server gateway. Default=0.0.0.0

System.Net.IPAddress Bootserver3\_Ip: 3rd boot server IP. Default=0.0.0.0

System.Net.IPAddress Bootserver3\_Netmask: 3rd boot server netmask. Default=0.0.0.0

uint Bootserver3\_Port: 3rd boot server port. Min=1025, Max=65536, Default=6910

System.Net.IPAddress Bootserver4\_Gateway: 4th boot server gateway. Default=0.0.0.0

System.Net.IPAddress Bootserver4\_Ip: 4th boot server IP. Default=0.0.0.0

System.Net.IPAddress Bootserver4\_Netmask: 4th boot server netmask. Default=0.0.0.0

uint Bootserver4\_Port: 4th boot server port. Min=1025, Max=65536, Default=6910

uint GeneralTimeout: Login general timeout in milliseconds. Min=1000, Max=60000, Default=5000

bool InterruptSafeMode: Interrupt safe mode (use if target device hangs during boot) when set to true. Default=false

bool PaeMode: PAE mode (use if PAE enabled in boot.ini of target device) when set to true. Default=false

uint PollingTimeout: Login polling timeout in milliseconds. Min=1000, Max=60000, Default=5000

uint RecoveryTime: When bootFromHdOnFail is 1, this is the number of seconds to wait before reboot to hard drive. Min=10, Max=60000, Default=50

bool VerboseMode: Display verbose diagnostic information when set to true. Default=false

Read-Only Fields

string Name: Name of the bootstrap file used to Get and Set.

Guid Guid or ServerId: GUID of the Server used for Get and Set.

## PvsServerBootstrapName

Read-Only Field

string Name: Bootstrap file name.

## PvsServerInfo

Read-Only Fields

uint Active: 1 if the Server is currently active, 2 if unknown, and 0 otherwise. Min=0, Max=2, Default=0

uint AdMaxPasswordAge: Number of days before a password expires. Min=1, Max=30, Default=7

bool AdMaxPasswordAgeEnabled: Age the password, when set to true. Default=false

uint BootPauseSeconds: Number of seconds that a Device will pause during login if its server busy. Min=1, Max=60, Default=10

uint BuffersPerThread: Number of buffers per worker thread. Min=1, Max=128, Default=24

uint BusyDbConnectionRetryCount: Number of times a failed database connection will be retried. Min=0, Max=32767, Default=2

uint BusyDbConnectionRetryInterval: Interval, in number of milliseconds, the server should wait before retrying to connect to a database. Min=0, Max=10000, Default=25

System.Net.IPAddress ContactIp: Read-only contact IP for the Server.

string ContactPort: Read-only contact port for the Server.

string Description: User description. Default="" Max Length=250

uint DeviceCount: Read-only count of Devices. Default=0

bool EventLoggingEnabled: Enable event logging, when set to true. Default=false

uint FirstPort: Number of the first UDP port for use by the Stream Service, First and Last must allow at least 5 ports. Min=1025, Max=65534, Default=6910

uint InitialQueryConnectionPoolSize: Initial size of database connection pool for non-transactional queries. Min=1, Max=1000, Default=50

uint InitialTransactionConnectionPoolSize: Initial size of database connection pool for transactional queries. Min=1, Max=1000, Default=50

uint IoBurstSize: Number of bytes read/writes can send in a burst of packets. Required that IoBurstSize/(MaxTransmissionUnits-76)<=32. Min=4096, Max=61440, Default=32768

System.Net.IPAddress\[\] Ip: One or more streaming ip addresses.

DateTime LastBugReportAttempt: Time that this server last attempted to upload or generate a bug report bundle. Default=Empty

string LastBugReportResult: Status of the last bug report on this server. Default="" Max Length=4000

string LastBugReportStatus: Status of the last bug report on this server. Default="" Max Length=250

string LastBugReportSummary: Summary of the last bug report on this server. Default="" Max Length=250

DateTime LastCeipUploadAttempt: Time that this server last attempted a CEIP upload. Default=Empty

uint LastPort: Number of the last UDP port for use by the Stream Service, First and Last must allow at least 5 ports. Min=1025, Max=65534, Default=6930

uint LicenseTimeout: Amount of seconds before a license times out. Min=15, Max=300, Default=30

uint LocalConcurrentIoLimit: Maximum concurrent IO transactions it performs for vDisks that are local. A value of 0 disables the feature. Min=0, Max=128, Default=4

uint LogFileBackupCopiesMax: Maximum number of log file backups. Min=1, Max=50, Default=4

uint LogFileSizeMax: Maximum size log files can reach in Megabytes. Min=1, Max=50, Default=5

uint LogLevel: Level to perform logging at. Values are: 0 (None), 1 (Fatal), 2 (Error), 3 (Warning), 4 (Info), 5 (Debug), and 6 (Trace). Min=0, Max=6, Default=4

System.Net.IPAddress ManagementIp: IP address used for management communications between Servers. Default=0.0.0.0

uint MaxBootDevicesAllowed: Maximum number of Devices allowed to boot simultaneously. Min=1, Max=1000, Default=500

uint MaxBootSeconds: Maximum number of seconds for a Device to boot. Min=10, Max=900, Default=60

uint MaxQueryConnectionPoolSize: Maximum size of database connection pool for non-transactional queries. Min=1, Max=32767, Default=1000

uint MaxTransactionConnectionPoolSize: Maximum size of database connection pool for transactional queries. Min=1, Max=32767, Default=1000

uint MaxTransmissionUnits: Ethernet maximum transmission unit size for the protocol for use for Server and Device. Required that IoBurstSize/(MaxTransmissionUnits-76)<=32. Min=502, Max=16426, Default=1506

bool NonBlockingIoEnabled: Use non-Blocking IO, when set to true. Default=true

float PowerRating: A strictly relative rating of this Server's capabilities when compared to other Servers in the Store(s) it belongs too; can be used to help tune load balancing. Min=0.1, Max=1000, Default=1

uint RefreshInterval: Interval, in number of seconds, the server should wait before refreshing settings. If set to 0, unused database connections are never released. Min=0, Max=32767, Default=300

uint RemoteConcurrentIoLimit: Maximum concurrent IO transactions it performs for vDisks that are remote. A value of 0 disables the feature. Min=0, Max=128, Default=4

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, and 200 is Site Administrator. Default=999

uint ServerCacheTimeout: Number of seconds to wait before considering another Server is down. Min=5, Max=60, Default=8

string ServerFqdn: Read-only fully qualified domain name. Default="" Max Length=1024

Guid Guid or ServerId: Read-only GUID that uniquely identifies this Server.

string Name or ServerName: Computer name with no spaces. ASCII computer name characters Max Length=21

Guid SiteId: GUID of the Site this Server is to be a member of. It is not used with SiteName.

string SiteName: Name of the Site this Server is to be a member of. It is not used with SiteId.

uint ThreadsPerPort: Number of worker threads per IO port. Required that (threadPerPort \* numberPorts \* numberIPs) <= 1000. Min=1, Max=60, Default=8

uint UnusedDbConnectionTimeout: Interval, in number of seconds, a connection should go unused before it is to be released. Min=0, Max=32767, Default=300

uint VDiskCreatePacing: VDisk create time pacing in milliseconds. Min=0, Max=5, Default=0

## PvsServerStatus

Read-Only Fields

uint DeviceCount: Read-only count of Devices. Default=0

System.Net.IPAddress Ip: Read-only contact IP for the Server.

uint Port: Read-only contact port for the Server.

Guid Guid or ServerId: Read-only GUID of the Server. Can be used with Get Server.

string Name or ServerName: Read-only Name of the Server. Can be used with Get Server.

uint Status: Status of the server, 0 if down, 1 if up and 2 if unknown. Default=0

## PvsServerStore

Read/Write Fields

string\[\] CachePath: Cache path(s) that the Server uses with the Store. If none are specified the caches will be placed in the Store cachePath. Default=None

string Path: Directory path that the Server uses to access the Store. Default="" Max Length=255

Read-Only Fields

Guid ServerId: GUID of the server that uses the Store. ServerName can be used instead.

string ServerName: Name of the server that uses the Store. ServerId can be used instead.

Guid StoreId: GUID of the Store. StoreName can be used instead.

string StoreName: Name of the Store. StoreId can be used instead.

## PvsSite

Read/Write Fields

Guid DefaultCollectionId: GUID of the Collection to place new Devices into automatically. Not used with defaultCollectionName. Default=00000000-0000-0000-0000-000000000000

string DefaultCollectionName: Name of the Collection to place new Devices into automatically. Not used with DefaultCollectionId. Default=""

string Description: User description. Default="" Max Length=250

Guid DiskUpdateServerId: GUID of the Disk Update Server for the Site. Not used with DiskUpdateServerName. Default=00000000-0000-0000-0000-000000000000

string DiskUpdateServerName: Name of the Disk Update Server for the Site. Not used with DiskUpdateServerId. Default=""

bool EnableDiskUpdate: True when Disk Updated is enabled for the Site, false otherwise. Default=false

uint InventoryFilePollingInterval: The number of seconds between polls for Disk changes in the Stores. Min=1, Max=600, Default=60

string MakPassword: User password used for MAK activation. Default="" Max Length=64

string MakUser: User name used for MAK activation. Default="" Max Length=64

string Name or SiteName: Name of the Site. Max Length=50

Read-Only Fields

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, 200 is Site Administrator, and 999 is read-only. Default=999

Guid Guid or SiteId: Read-only GUID that uniquely identifies this Site.

## PvsSiteView

Read/Write Fields

string Description: User description. Default="" Max Length=250

string Name or SiteViewName: Name of the Site View. Max Length=50

Read-Only Fields

uint ActiveDeviceCount: Read-only count of active Devices in this Site View. Default=0

uint DeviceCount: Read-only count of Devices in this Site View. Default=0

uint DeviceWithPVDCount: Read-only count of Devices with Personal vDisk in this Site View. Default=0

uint MakActivateNeededCount: Read-only count of active Devices that need MAK activation in this Site View. Default=0

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, and 200 is Site Administrator. Default=999

Guid SiteId: GUID of the Site this View is to be a member of. It is not used with SiteName.

string SiteName: Name of the Site this View is to be a member of. It is not used with SiteId.

Guid Guid or SiteViewId: Read-only GUID that uniquely identifies this Site View.

## PvsStore

Read/Write Fields

string\[\] CachePath: Default Cache path(s) that the Servers use with this Store. If none are specified the caches will be placed in the WriteCache subdirectory of the Store path. Default=None

string Description: User description. Default="" Max Length=250

string Path: Default directory path that the Servers use to access this Store. Max Length=255

Guid SiteId: GUID of the Site where Administrators of that Site can change this Store. Not used for Farm Stores. SiteName can be used instead. Default=00000000-0000-0000-0000-000000000000

string SiteName: Name of the Site where Administrators of that Site can change this Store. Not used for Farm Stores. SiteId can be used instead. Default=""

string Name or StoreName: Name of the Store. Max Length=50

Read-Only Fields

string PathType: Read-only field indicating if the vdisks are on a server's local hard disk or on a remote share.

uint Role: Read-only Role of the user for this item. 100 is Farm Administrator, 200 is Site Administrator, and 999 is read-only. Default=999

Guid Guid or StoreId: Read-only GUID that uniquely identifies this Store.

## PvsStoreSharedOrServerPath

Read-Only Fields

string Path: Directory path that the Servers use to access this Store.

Guid StoreId: GUID of the Store.

string StoreName: Name of the Store.

## PvsTask

Read-Only Fields

string Command: Command being processed. Default="" Max Length=50

string CommandType: Type of the command. Values are: Add, Delete, Get, Info, Run, RunWithReturn, Set and SetList. Default="" Max Length=13

DateTime ExpirationTime: Time the task record may be removed from the database if the task does not complete. Has the date and time without milliseconds.

uint Handle: Handle to a running function.

System.Net.IPAddress Ip: IP Address of the remote host.

string MapiException: Exception result in XML format. Default=""

uint Port: Port number of the remote service.

string Results: Result in XML format. Default=""

string ServerFqdn: Qualified name of the server. Default="" Max Length=1024

Guid SiteId: GUID of the Site that this Task is being processed in. Default=00000000-0000-0000-0000-000000000000

string SiteName: Name of the Site that that this Task is being processed in.

DateTime StartTime: Time the task was started. Has the date and time without milliseconds.

uint State: State of the Task. Values are: 0 (Processing), 1 (Cancelled), and 2 (Complete). Min=0, Max=2

uint TaskId: Unique ID of the task.

## PvsUndefinedDisk

Read-Only Fields

bool VHDX: If VHDX is true, the format of the image is VHDX. Otherwise it is VHD. Default=false

string Name: Name of the disk file without the extension.

uint Status: Status of the disk file. Values are: 0 (Valid), 1 (Missing Properties File), 2 (Access Denied), 3 (Access Denied and Missing Properties File), 4 (Invalid Disk File), 5 (Manifest Missing or Invalid), 6 (Both VHD and VHDX)

## PvsUpdateTask

Read/Write Fields

uint\[\] Date: Days of the month. Numbers from 1-31 are the only valid values. This is used with Monthly Date recurrence. Default="" Max Length=83

uint DayMask: Days selected values. 1 = Monday, 2 = Tuesday, 4 = Wednesday, 8 = Thursday, 16 = Friday, 32 = Saturday, 64 = Sunday, 128 = Day. Default=0. This is used with Weekly and Monthly Type recurrence. Min=1, Max=255, Default=4

string Description: User description. Default="" Max Length=250

string Domain: Domain to add the Disk Update Device(s) to. If not included, the first Domain Controller found on the Server is used. Default="" Max Length=255

bool Enabled: True when it will be processed, false otherwise. Default=true

string EsdType: Esd to use. Valid values are SCCM or WSUS. If no value, a custom script is run on the client. Default="" Max Length=50

uint Hour: The hour of the day to perform the task. Min=0, Max=23, Default=0

uint Minute: The minute of the hour to perform the task. Min=0, Max=59, Default=0

uint MonthlyOffset: When to happen monthly. 0 = None, 1 = First, 2 = Second, 3 = Third, 4 = Forth, 5 = Last. This is used with Monthly Type recurrence. Min=0, Max=5, Default=3

string OrganizationUnit: Organizational Unit to add the Disk Update Device(s) to. This parameter is optional. If it is not specified, the device is added to the built in Computers container. Child OU's should be delimited with forward slashes, e.g. "ParentOU/ChildOU". Special characters in an OU name, such as '"', '#', '+', ',', ';', '>', '=', must be escaped with a backslash. For example, an OU called "commaIn,TheMiddle" must be specified as "commaIn\\,TheMiddle". The old syntax of delimiting child OU's with a comma is still supported, but deprecated. Note that in this case, the child OU comes first, e.g. "ChildOU,ParentOU". Default="" Max Length=255

uint PostUpdateApprove: Access to place the version in after the update has occurred. 0 = Production, 1 = Test, 2 = Maintenance. Min=0, Max=2, Default=0

string PostUpdateScript: Script file to run after the update finishes. Default="" Max Length=255

string PostVmScript: Script file to run after the VM is unloaded. Default="" Max Length=255

string PreUpdateScript: Script file to run before the update starts. Default="" Max Length=255

string PreVmScript: Script file to run before the VM is loaded. Default="" Max Length=255

uint Recurrence: The update will reoccur on this schedule. 0 = None, 1 = Daily, 2 = Every Weekday, 3 = Weekly, 4 = Monthly Date, 5 = Monthly Type. Min=0, Max=5, Default=0

string Name or UpdateTaskName: Name of the Update Task. It is unique within the Site. Max Length=50

Read-Only Fields

Guid SiteId: GUID of the Site that this Update Task is a member of. It is not used with SiteName.

string SiteName: Name of the Site that this Update Task is a member of. It is not used with SiteId.

Guid Guid or UpdateTaskId: Read-only GUID that uniquely identifies this Update Task.

## PvsVersion

Read-Only Fields

string DbEdition: Edition of the database. If 'Express Edition', monitor dbSize.

uint DbSize: Size of the database in MB. Monitor this value if the edition is 'Express Edition' and this value is close to reaching the 4000 MB maximum. Default=0

uint DbVersion: Version of the database schema as a number. Default=0

string MapiVersion: Version of the system in major.minor.point.build format.

uint MapiVersionNumber: Internal version number of the system. It is a number that is increaed by 100 for each major and minor release. Point releases are the numbers between each 100. Value is 0 when the system does not support MapiVersionNumber. Default=0

string SdkVersion: Version of the SDK in major.minor.build format.

uint Type: Type of system. Values are 0 (Normal), 1 (OROM), and 2 (Secure). Default=0

## PvsVirtualHostingPool

Read/Write Fields

string Datacenter: Datacenter of the Virtual Hosting Pool. Default="" Max Length=250

string Description: User description. Default="" Max Length=250

string Password: Password to use when logging into the Server.

string PlatformVersion:  Hypervisor Host Version  Default="" Max Length=250

uint Port: Port of the Host Server. Min=80, Max=65534, Default=80

bool PrepopulateEnabled: Enable prepopulate when set to true Default=false

string Server: Name or IP of the Host Server. Max Length=255

uint ShutdownTimeout: Timeout for shutdown. Min=2, Max=30, Default=10

uint Type: Type of the Virtual Hosting Pool. 0 = Citrix XenServer, 1 = Microsoft SCVMM/Hyper-V, 2 = VMWare vSphere/ESX. Min=0, Max=3, Default=0

uint UpdateLimit: Number of updates at the same time. Min=2, Max=1000, Default=1000

uint UpdateTimeout: Timeout for updates. Min=2, Max=240, Default=60

string UserName: Name to use when logging into the Server.

string Name or VirtualHostingPoolName: Name of the Virtual Hosting Pool. It is unique within the Site. Max Length=50

string XdHcCustomProperties: Custom Properties for HCL Connection Details object Default="" Max Length=250

string XdHcHypervisorConnectionName: Hypervisor Connection Name for HCL Connection Details object Default="" Max Length=250

string XdHcHypervisorConnectionUid: Hypervisor Connection Uid for HCL Connection Details object Default="" Max Length=250

string XdHcRevision: Revision for HCL Connection Details object Default="" Max Length=250

string XdHcSslThumbprints: Ssl Thumbprints for HCL Connection Details object Default="" Max Length=250

Guid XdHostingUnitUuid: UUID of XenDesktop Hosting Unit Default=00000000-0000-0000-0000-000000000000

Guid XsPvsSiteUuid: UUID of XenServer PVS\_site  Default=00000000-0000-0000-0000-000000000000

Read-Only Fields

Guid SiteId: GUID of the Site that this Virtual Hosting Pool is a member of. It is not used with SiteName.

string SiteName: Name of the Site that this Virtual Hosting Pool is a member of. It is not used with SiteId.

Guid Guid or VirtualHostingPoolId: Read-only GUID that uniquely identifies this Virtual Hosting Pool.

## PvsXDSite

Read/Write Field

string\[\] ConfigServices: XenDesktop Server addresses. Max Length=2000

Read-Only Field

Guid Guid or XdSiteId: GUID of the XenDesktop Site.