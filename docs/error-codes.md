# Error codes

For the Citrix.PVS.SnapIn, if an error occurs, a PvsException will be in the Exception member of the $error.

The members of a PvsException are:

InnerException: The exception that occured. This exception maybe an EAException or other standard Exception.

ToString(): Has the formatted full Message of the InnerException.

If the InnerException GetType().Name equals "EAException", then The members of it are:

returnCode: The number, as shown below in the Error codes. The name of the error, for example "NotImplemented", is not included in the EAException.

Message: The message, as shown below in the Error codes. The \[v1\], \[v2\], \[v3\], \[v4\], and \[v5\] will be replaced with values as required.

Details: Has the Details for the EAException if there are any. OtherException, ManagementInterfaceError and PvsStatusException will have Details.

ToString(): Has the Message as shown below in the Error codes. If there is Details, it will be returned or included, and if partialReturn, they will be included.

partialReturn: Might have a list of EAException objects if any of the items processed during the command had any issues.

Severity: Can have the values Critical, Error, Warning or Duplicate.

Source: Has the value that is displayed in the Console as a Title or Type for the error.

0 Success: The command succeeded.

1 NotImplemented: The \[v1\] feature has not been implemented.

2 InvalidCommand: The \[v1\] command does not exist.

3 InvalidField: The \[v1\] field does not exist.

4 InvalidFieldFormat: The \[v1\] field is not formatted properly, the correct format is \[v2\].

5 InvalidParameter: The \[v1\] parameter is not valid.

6 InvalidParameterFormat: The \[v1\] parameter is not formatted property, the correct format is \[v2\].

7 ReadOnlyField: Unable to change the \[v1\] field because it is read-only.

8 RequiredFieldMissing: The required \[v1\] field is missing.

9 RequiredFieldsMissing: The required \[v1\] or \[v2\] field is missing.

10 RequiredParameterMissing: The required \[v1\] parameter is missing.

11 RequiredParametersMissing: The required \[v1\] or \[v2\] parameter is missing.

12 InternalIdAndNameFieldsMustBeDefined: An internal error occurred. The \[v1\] field is not the next FieldSettings object after the ID.

13 NoFarmAccess: The domain/user does not have access to the Farm.

14 InvalidForeignKeyValue: The \[v1\] field with value \[v2\] is an invalid foreign key.

15 SetupError: The system was not configured correctly.

16 Executing: The \[v1\] command can only be called one at a time. Wait for the command to finish before running again.

17 NoDiskMapped: A vDisk has not yet been mapped.

18 DatabaseError: A database error occurred.

19 DuplicateKey: To avoid creating a duplicate key, the Add or Set command was cancelled.

20 DatabaseErrorMissed: An internal error occurred. An uncaught database error occurred.

21 AddCommandFailed: No objects were added during the last 'Add' command.

22 InsufficientPrivileges: Access denied. The appropriate privileges are not assigned to perform this task.

23 ZeroObjectsAffected: No object was added, updated, or deleted in the last operation.

24 OtherException: An unexpected MAPI error occurred.

25 InvalidFieldLength: The \[v1\] field value is too long, maximum length is \[v2\].

26 InvalidFieldValueMinMax: The \[v1\] field value is invalid, the minimum is \[v2\] and the maximum is \[v3\].

27 InvalidFieldValue: The \[v1\] field can only have values \[v2\] or \[v3\].

28 TooManyParameters: More parameters were specified than permitted.

29 TooFewParameters: Not enough identifying parameters specified.

30 FollowingParametersMissing: To use the \[v1\] parameter, \[v2\] or \[v3\] must also be used.

31 InconsistentData: The action is canceled because the Store directory date/times does not match. Update the Store directories to match.

32 DatabaseOpenFailed: Unable to contact the database server. Ensure Citrix Provisioning server is configured correctly.

33 DatabaseVersionWrong: The wrong database version is being used.  Found version number: \[v1\] Expected version number: \[v2\]

34 DatabaseVersionNotFound: The database version number does not exist or was not found. Ensure Citrix Provisioning server is configured correctly.

35 SomeRequiredParametersMissing: Required parameters are missing.

36 PartialError: The following items failed:

item1 Error message...

item2 Error message...

37 NoItemsToProcess: There are no items to process.

38 NoDefaultCollectionDefined: Unable to add a Device until a default Collection is set.

39 NoDefaultSiteDefined: A default Site is not set, no Devices can be added.

40 InvalidCollection: The specified Collection does not exist.

41 InvalidAuthGroup: The specified AuthGroup does not exist.

42 InvalidGroup: The specified Group does not exist.

43 InvalidDevice: The specified Device does not exist.

44 InvalidDiskLocator: The specified vDisk does not exist.

45 InvalidServer: The specified Server does not exist.

46 InvalidServerSite: Server specified is not in the Site specified.

47 InvalidStoreSite: Store specified is not for the Site specified.

48 InvalidSiteView: The specified Site View does not exist.

49 InvalidSite: The specified Site does not exist.

50 InvalidDeviceDiskLocator: The specified Device or vDisk does not exist.

51 InvalidDeviceImport: Import failed because the file must have Device Name, Mac Address, Site Name, and Collection Name, and they must be tab or comma-delimited.

52 InvalidServerFrom: The Server to copy \[v1\]=\[v2\] was not found.

53 InvalidServerTo: No Server to copy to (\[v1\]=\[v2\]) was found.

54 InvalidDeviceFrom: The Device to copy \[v1\]=\[v2\] was not found.

55 InvalidDeviceTo: No Devices to copy to are found.

56 InvalidDiskFrom: The vDisk to copy \[v1\]=\[v2\] was not found.

57 InvalidDiskTo: No vDisk to copy to (\[v1\]=\[v2\]) was found.

58 InvalidDiskPath: The path '\[v1\]' to the vDisk file is not found.

59 VDiskFileNotFound: \[v1\]: vDisk file was not found.

60 InvalidDiskServer: There is no Server that can serve the vDisk \[v1\] or the Store to which this vDisk belongs. Verify that one or more Servers belonging to the Store are online and that there is sufficient free space for the operation you are attempting.

61 InvalidDiskForServer: Server \[v1\] cannot access all versions of vDisk \[v2\], the vDisk was updated on at least one other Server.

62 SameSiteRequired: Objects within the same Site must be selected.

63 TooFewFields: Not enough fields for a record.

64 ADerrorDC: Unable to connect to the Domain Controller (if any) or the default rootDSE. Error code: \[v1\], message: \[v2\], provider: \[v3\].

65 ADerrorOU: Unable to get the Organizational Unit setting (if any). Error code: \[v1\], message: \[v2\], provider: \[v3\].

66 ADerrorDefaultContainer: Unable to get the default computer accounts container (default location is Active Directory root> Computers). Error code: \[v1\], message: \[v2\], provider: \[v3\].

67 ADerrorCreate: Unable to create the computer account in Active Directory. Ensure the account does not already exist and that the appropriate permissions are available to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

68 ADerrorNewAccount: Unable to get the newly created Active Directory computer account. Error code: \[v1\], message: \[v2\], provider: \[v3\].

69 ADerrorSam: Unable to set the Active Directory samAccountName property. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

70 ADerrorUserAccount: Unable to set the Active Directory userAccountControl property. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

71 ADerrorSave: Unable to save Active Directory change. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

72 ADerrorSetPassword: Unable to set a new password for this user account. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

73 ADerrorAddTrustee: Unable to add trustee (if any). Error code: \[v1\], message: \[v2\], provider: \[v3\].

74 ADerrorEnableAccount: Unable to enable the Active Directory account. Error code: \[v1\], message: \[v3\], provider: \[v2\].

75 ADerrorAlreadyExists: The computer name is already in use. Error code: \[v1\], message: \[v3\], provider: \[v2\]. Select a unique name for this machine.

76 ADerrorGeneral: A general Active Directory error occurred. Error code: \[v1\], message: \[v2\], provider: \[v3\].

77 ADerrorDirectorySearch: Unable to find Active Directory items meeting the search criteria entered. Error code: \[v1\], message: \[v2\], provider: \[v3\].

78 ADerrorSearchComputerAccount: Unable to perform the computer accounts search. Error code: \[v1\], message: \[v2\], provider: \[v3\].

79 ADerrorComputerAccountNotFound: Specified computer account not found. Error code: \[v1\], message: \[v2\], provider: \[v3\].

80 ADerrorComputerAccountHold: This computer account is currently unavailable. Ensure that Active Directory is running properly. Error code: \[v1\], message: \[v2\], provider: \[v3\].

81 ADerrorComputerAccountMove: Failed to move the computer account to the target organizational unit set (also returned if caller lacks permission). Error code: \[v1\], message: \[v2\], provider: \[v3\].

82 ADerrorDelete: Unable to delete this computer account. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

83 ADerrorPasswordGeneration: Unable to generate this password. Ensure the appropriate permissions exist to perform this task.

84 MapDiskNoDriver: Unable to map vDisk because a driver was not found.

85 MapDiskDeniedByServer: Unable to map the vDisk. Mapping was denied by the Server.

86 MapDiskLocalAccessDenied: Unable to map the vDisk. Denied local access.

87 MapDiskMiniportError: Unable to map vDisk because of a Miniport error.

88 UnmapDiskFailed: Failed to unmap a vDisk.

89 DuplicateDisk: The vDisk \[v1\] already exists on \[v2\] at \[v3\].

90 DuplicateDiskLocator: A DiskLocator: \[v1\] already exists on Site: \[v2\].

91 DiskCreationInProgress: The vDisk \[v1\] is being created on \[v2\] at \[v3\].

92 InvalidServerStore: A database integrity error occurred. The Server is not set to deliver vDisks from the Store, but should be.

93 InvalidStore: The specified Store does not exist.

94 InvalidFarmView: Farm View specified does not exist.

95 InvalidStorePath: Store path is empty.

96 ManagementInterfaceError:

Management Interface: Undefined error.

Management Interface: Database interface is inaccessible.

Management Interface: Database interface library is inaccessible.

Management Interface: The database access library is a version incompatible with the Management Server.

Management Interface: Database interface library is invalid.

Management Interface: Database interface could not be created.

Management Interface: Database could not be opened.

Management Interface: Database is in use.

Management Interface: Database error occurred.

Management Interface: Not implemented.

Management Interface: Registry entry was not found.

Management Interface: Request was not created.

Management Interface: Operating System error occurred.

Management Interface: vDisk error.

Management Interface: vDisk header is incomplete.

Management Interface: vDisk footer is incomplete.

Management Interface: vDisk boot record is incomplete.

Management Interface: vDisk boot sector is incomplete.

Management Interface: vDisk size is below the minimum.

Management Interface: vDisk size is above the maximum.

Management Interface: vDisk boot record template is inaccessible.

Management Interface: vDisk boot sector template is inaccessible.

Management Interface: vDisk lock was not found.

Management Interface: vDisk has exclusive lock.

Management Interface: vDisk has shared lock.

Management Interface: vDisk lock error.

Management Interface: vDisk format is incompatible.

Management Interface: vDisk prefooter is incomplete.

Management Interface: vDisk creation is in progress.

Management Interface: vDisk creation information was not found.

Management Interface: vDisk creation cancellation was requested.

Management Interface: vDisk file was not found.

Management Interface: vDisk file path was not found.

Management Interface: vDisk file access was denied.

Management Interface: Cancelled.

Management Interface: Registry key for the product is inaccessible.

Management Interface: Registry key for the installation folder is inaccessible.

Management Interface: Registry key for the management interface is inaccessible.

Management Interface: Registry key for the database path is inaccessible.

Management Interface: Registry key for the management interface IP address is inaccessible.

Management Interface: Buffer size is too small.

Management Interface: Buffer size is too large.

Management Interface: Unknown error.

Management Interface: Remote Server failed to relay a request.

Management Interface: Remote Server is not servicing the Device.

Management Interface: Remote Server or Device refused the request.

Management Interface: Local Server failed to complete a request to a Server or Device.

Management Interface: Local Server failed to complete a request to a Server.

Management Interface: Remote requests were disabled because of an initialization error.

Management Interface: Remote request failed.

Management Interface: Remote request timed out.

Management Interface: Remote request result was not found.

Management Interface: Remote request receiver failed to initialize.

Management Interface: Management command failed for all objects.

Management Interface: Failed to get the preshared key in secure version.

Management Interface: VHD Error.

Management Interface: vDisk properties were lost.

Management Interface: Insufficient Memory.

Management Interface: The network path was not found.

Management Interface: The network name cannot be found.

Management Interface: File already exists.

Management Interface: The geometry of the vDisk is not accessible.

Management Interface: Unable to create the vDisk because the store media is read-only.

Management Interface: vDisk file is being used by another process.

97 ServerTimeout: Server did not respond to a request in time.

98 NotFound: \[v1\] not found.

99 AccountRetrieve: Account information for user \[v1\] was not found.

100 ActiveDevice: The task cannot be performed on active Devices. Shut down the Devices before attempting to perform the task.

101 ActiveDiskLocator: The task cannot be performed on active vDisks. Shut down the Devices that are using the vDisks before attempting to perform the task.

102 AssignedDiskLocator: Unable to delete a vDisk that is currently assigned to a Device. Unassign all Devices, then delete the vDisk.

103 ActiveServer: The task cannot be performed on active Servers. Shut down the Servers before attempting to perform the task.

104 NotEnoughFreeDiskSpace: There is not enough free disk space to create the vDisk.

105 InvalidDiskName: The vDisk name has one or more invalid characters. The invalid characters are < > | " \\ / : \* ?.

106 CannotDeleteLastAuthGroup: Deleting the last Authorization Group causes the system to be inoperable.

107 CannotDeleteUsedAuthGroup: An Authorization Group that is currently in use cannot be deleted.

108 ServerStartFailed: The Server did not start successfully. Ensure the appropriate permissions exist for the service account.

109 ServerStopFailed: The Server did not stop successfully.

110 LockOwnerNotFound: The Device that owns the lock was not found, the vDisk was not unlocked.

111 PossiblySharedVDisk: Unable to delete File \[v1\]. It is possible that the file is being referenced in other Sites or Stores.

112 StorePathInaccessible: The Store path \[v1\] is inaccessible.

113 InvalidAction: The \[v1\] action does not exist.

114 InvalidObjectType: The \[v1\] objectType does not exist.

115 TooManyRecords: The amount of data returned using Get is too large. Use GetFirst and GetNext instead of Get.

116 InvalidUserGroup: The specified UserGroup does not exist.

117 InvalidAuditAction: The specified AuditAction does not exist.

118 LoginFailed: The database login failed. Ensure the appropriate permissions exist to access the database.

119 DatabaseConnectionError: Unable to connect to the database. Restore the connection in order to manage the farm.

120 CreateTriggersParsing: Unable to parse the database script 'CreateTriggers' at: \[v1\]

121 CreateStoredProcParsing: Unable to parse the database script 'CreateStoredProcedures' at: \[v1\]

122 MediaIsReadOnly: Management Interface: Unable to create the vDisk because the store media is read-only.

123 ConnectedDeviceForVirtualHostingPool: Unable to delete this VM from a machine catalog because it is connected to a Delivery Group.

124 ADerrorDN: Unable to get the distinguishedName property. Ensure the appropriate Active Directory permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

125 ADerrorGetSecDes: Unable to get the Active Directory Security Descriptor property. Error code: \[v1\], message: \[v2\], provider: \[v3\].

126 ADerrorSetSecDes: Unable to set the Active Directory Security Descriptor property. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

127 ADerrorDNSHostName: Unable to set the DNS Host Name property (dNSHostName). Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

128 ADerrorDisplayName: Unable to set the displayName property. Error code: \[v1\], message: \[v2\], provider: \[v3\].

129 ADerrorBind: This device was unable to bind to the Domain Controller. Ensure the Domain Controller is running. Error code: \[v1\], message: \[v2\], provider: \[v3\].

130 ADerrorGetSPN: Unable to get an Active Directory Service Principal Name. Error code: \[v1\], message: \[v2\], provider: \[v3\].

131 ADerrorWriteSPN: Unable to write the Active Directory Service Principal Name. Error code: \[v1\], message: \[v2\], provider: \[v3\]

132 ADerrorSearch: Unable to perform the requested Search. Error code: \[v1\], message: \[v2\], provider: \[v3\].

133 ADerrorMoveToOU: Unable to move the Active Directory account to the requested Organizational Unit. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

134 ADerrorDeleteAccount: Unable to delete this computer account. Ensure the appropriate permissions exist to delete accounts.  Error code: \[v1\], message: \[v2\], provider: \[v3\].

135 ADerrorBadParameters: Incorrect parameters sent to Citrix Provisioning from  Studio. Error code: \[v1\], message: \[v2\], provider: \[v3\].

136 VolumeInUse: The volume is being used.

137 VolumeAccessDenied: Volume access is denied.

138 VolumeUnknownVolume: An unknown volume was specified.

139 VolumeGeneralError: An error occured when executing a volume command.

140 MaintenanceServerError: Action cannot be performed, \[v1\] is a maintenance server for \[v2\].

141 NotManagedStore: The action cannot be performed because the store is not managed.

142 PathNotExist: The path does not exist on the given Server.

143 PathNoCreatePermission: The path does not have the appropriate create permissions.

144 PathNoReadPermission: The path does not have the appropriate read permissions.

145 PathNoWritePermission: The path does not have the appropriate write permissions.

146 PathNoDeletePermission: The path does not have the appropriate delete permissions.

147 IPCProtocolError: An internal error occurred. A field is missing from the process communication protocol data.

148 InvalidStoreServer: No active Server can serve the Store \[v1\].

149 ConstraintCheck: A database constraint caused an Add or Update to be stopped.

150 VamtNotFound: The Volume Activation Management Tool cannot be found.

151 ADerrorCannotGetObjectSID: Cannot return objectSID. Error code: \[v1\], message: \[v2\], provider: \[v3\].

152 ADerrorCannotDisableAccount: Cannot disable the Active Directory account at this time. Ensure that all account users are logged off before attempting to disable the account. Error code: \[v1\], message: \[v2\], provider: \[v3\].

153 ADerrorFailedToChangePassword: Unable to reset the machine account password. Ensure the appropriate permissions exist to perform this Active Directory task. Error code: \[v1\], message: \[v2\], provider: \[v3\].

154 ADerrorFailedToCopyDCName: Unable to copy the Domain Controller name. Error code: \[v1\], message: \[v2\], provider: \[v3\].

155 ADerrorDCNameIsTooLong: The Domain Controller name entered exceeds the maximum character length of \[v4\]. Error code: \[v1\], message: \[v2\], provider: \[v3\].

156 SiteMakUserPassword: The Site's makUser and makPassword fields must have values.

157 VamtError: See the log for additional error details.

158 InactiveDevice: Device specified is not active.

159 DiskIsInPrivateMode: This task cannot be performed because the vDisk is in private image mode.

160 AlreadyInChangeMode: Unable to complete this operation, vDisk is already in Maintenance, Merge, or Test mode.

161 CannotCreateMaintenanceDisk: Cannot create maintenance vDisk.

162 CannotEnterMaintenanceMode: To place a vDisk in Maintenance Mode requires using a Server. No Server is available at this time.

163 NotInMaintenanceMode: Unable to perform this action because the vDisk is not in Maintenance Mode.

164 NoVersionForMaintenanceMode: Unable to place this vDisk in Maintenance Mode because the highest version is not found.

165 NoVersionFound: Unable to perform this action because a version record was not found in the database.

166 Obsolete: The \[v1\] feature is obsolete.

167 DatabaseWarning: A database warning occurred.

168 DatabaseSQL: A database SQL error occurred.

169 DatabaseResource: A database resource error occurred.

170 InvalidUpdateTask: The specified UpdateTask does not exist.

171 InvalidVirtualHostingPool: The specified VirtualHostingPool does not exist.

172 RemoteCommand: An exception occurred executing a command on a remote Server.

173 IpcNotConfigured: An internal error occurred. The process communication interface must be configured before executing remote commands.

174 DiskAlreadSetForUpdate: The vDisk is already set for Update with Device \[v1\] in Site \[v2\].

175 InvalidDiskVersion: The vDisk Version specified is not valid.

176 HostResolution: Could not resolve the host name for \[v1\].

177 InProcess: The remote task is taking longer than expected. TaskId: \[v1\]

178 DateMustBeInFuture: The \[v1\] must be in the future.

179 InvalidRemoteReturn: The remote command did not return valid data.

180 InvalidParameterValueMinMax: The \[v1\] parameter value is invalid, the minimum is \[v2\] and the maximum is \[v3\].

181 InvalidParameterNotNumeric: The \[v1\] parameter value is invalid, it is not numeric.

182 InvalidParameterNotGuid: The \[v1\] parameter value is invalid, it is not a GUID.

183 PassThroughMessage: \[v1\]

184 DiskUpdateNotEnabled: The Automatic vDisk Update option must be enabled and the vDisk Update Server must be defined. Set these in the Site properties.

185 PvsStatusException:

Windows API error occurred, number 0xE000FFFF.

SQL error occurred, number 0xE001FFFF.

Manager error occurred. Error number 0xE002FFFF.

StreamProcess error occurred. Error number 0xE003FFFF.

Stream Database error occurred. Error number 0xE004FFFF.

Management error occurred. Error number 0xE005FFFF.

Shutdown in progress; request ignored. Error number 0xE0050001.

CreateDiffDisk: Malformed packet; missing one or more arguments. Error number 0xE0050002.

DeleteDiffDisk: Malformed file name; cannot parse directory and name. Error number 0xE0050003.

DeleteDiffDisk: Malformed packet; missing one or more arguments. Error number 0xE0050004.

IPC: Failed to read mtGetLocks parameters. Error number 0xE0050005.

IPC: Failed to read mtGetLockStatus parameters. Error number 0xE0050006.

IPC: Failed to read mtLock parameters. Error number 0xE0050007.

IPC: Failed to read mtUnlock parameters. Error number 0xE0050008.

MergeDisk event: Malformed packet; unknown message type. Error number 0xE0050009.

MergeDisk event: Unknown target request ID. Error number 0xE005000A.

MergeDisk event: Malformed packet; missing one or more arguments. Error number 0xE005000B.

MergeDisk: Malformed packet; missing one or more arguments. Error number 0xE005000C.

ValidateDisk: Malformed packet; missing one or more arguments. Error number 0xE005000D.

VHD Library error occurred. Error number 0xE006FFFF.

VHD Library: Not implemented. Error number 0xE0060001.

VHD Library: Handle pointer is invalid. Error number 0xE0060002.

VHD Library: Length of the path exceeds the limit of the file system. Error number 0xE0060003.

VHD Library: Name is empty. Error number 0xE0060004.

VHD Library: Length of the name exceeds the limit of the file system. Error number 0xE0060005.

VHD Library: Size of a parameter was too big. Error number 0xE0060006.

VHD Library: Size of a parameter was too small. Error number 0xE0060007.

VHD Library: The media is write protected. Error number 0xE0060008.

VHD Library: Type is invalid. Error number 0xE0060009.

VHD Library: Footer is incomplete. Error number 0xE006000A.

VHD Library: Failed to read or write the entire VHD Header. Error number 0xE006000B.

VHD Library: Failed to read or write the entire VHD Block Allocation Table. Error number 0xE006000C.

VHD Library: Failed to read or write all of the VHD properties. Error number 0xE006000D.

VHD Library: VHD footer is corrupt. Error number 0xE006000E.

VHD Library: VHD header is corrupt. Error number 0xE006000F.

VHD Library: Failed to read or write the VHD objects. Error number 0xE0060010.

VHD Library: Destination string is too small. Error number 0xE0060011.

VHD Library: Destination string pointer is NULL. Error number 0xE0060012.

VHD Library: Source string pointer is NULL. Error number 0xE0060013.

VHD Library: Offset is before the beginning of the VHD data area. Error number 0xE0060014.

VHD Library: Offset is after the end of the VHD data area. Error number 0xE0060015.

VHD Library: Failed to allocate memory because it was unavailable. Error number 0xE0060016.

VHD Library: Caller cancelled the last create request. Error number 0xE0060017.

VHD Library: Failed to read or write all of the data as requested. Error number 0xE0060018.

VHD Library: Failed to create a Universal Unique Identification for a VHD. Error number 0xE0060019.

VHD Library: Failed to find the VHD properties. Error number 0xE006001A.

VHD Library: Failed to read or write the entire sector bitmap within a block. Error number 0xE006001B.

VHD Library: Failed to read or write the entire block. Error number 0xE006001C.

VHD Library: Failed to open the file that represents the VHD. Error number 0xE006001D.

VHD Library: Requested number of bytes exceeds the remainder of bytes in a block. Error number 0xE006001E.

VHD Library: Accessed past end of the VHD file. Error number 0xE006001F.

VHD Library: Differencing VHD Unique ID (UUID) differs to parent VHD Unique ID. Error number 0xE0060020.

VHD Library: Differencing VHD timestamp differs to parent VHD last modified time. Error number 0xE0060021.

VHD Library: Failed to read or write the entire VHD Block Allocation Table Map. Error number 0xE0060022.

IPC error occurred. Error number 0xE007FFFF.

There was an unknown transmission error. Error number 0xE0070001.

No response received for successful send. Error number 0xA0070002.

Message processor timed out. Error number 0xE0070003.

Retry limit exhausted. Error number 0xE0070004.

Message recipient task is not active. Error number 0xE0070005.

Socket send/recv cannot be retried. Error number 0xE0070006.

Port shutdown due to connection opens exhausted. Error number 0xE0070007.

Port shutdown due to flood of junk packets. Error number 0xE0070008.

Port shutdown due to receive retries exhausted. Error number 0xE0070009.

Transport does not support fragmentation. Error number 0xE007000A.

One or more packet fragments are missing. Error number 0xE007000B.

Error sending message. Error number 0xE0070100.

Message acknowledgement timeout. Error number 0xA0070101.

Command timeout. Error number 0xE0070102.

Not implemented. Error number 0xE0070103.

Error verifying message port number, must be >= 0 and <= 65535. Error number 0xE0070104.

Command initialization failed. Error number 0xE0070105.

Start of IPC failed. Error number 0xE0070106.

Stop of IPC failed. Error number 0xE0070107.

Memory allocation failure. Error number 0xE0070108.

Internal error, failure to wait long enough for a communication response to be received. Error number 0xE0070109.

Disk Update error occurred. Error number 0xE008FFFF.

Inventory error occurred. Error number 0xE009FFFF.

Inventory Table: Failed to start thread. Error number 0xE0090001.

Inventory Table: Invalid Entry. Error number 0xE0090002.

Inventory Table: Failed to initialize inventory. Error number 0xE0090003.

Shutdown in progress; request ignored. Error number 0xE0090004.

Get Disk Inventory: Parameters bad. Error number 0xE0090033.

Populate database: Failed offline. Error number 0xE0090065.

Populate database: Server get by name failed. Error number 0xE0090066.

Populate database: Uninitialized. Error number 0xE0090067.

Populate database: Get host name failed. Error number 0xE0090068.

Populate database: Char conversion failed. Error number 0xE0090069.

Populate database: Initialization failed. Error number 0xE009006A.

Populate database: Database open failed. Error number 0xE009006B.

Populate database: Get all disk locators failed. Error number 0xE009006C.

Inventory Table: Not yet implemented. Error number 0xE009006D.

Notifier error occurred. Error number 0xE00AFFFF.

MAPI error occurred. Error number 0xE00BFFFF.

186 TaskCancelled: Task \[v1\] is cancelled and is not running.

187 TaskCompleted: Task \[v1\] has been completed and is not running.

188 TaskInProgress: Task \[v1\] is running and cannot be processed.

189 InvalidTask: The specified Task does not exist.

190 InventoryServerCannotContactDatabase: The Inventory Service cannot contact the database.

191 ServerOffline: The Server is offline.

192 ServerStateUnknown: The Server state is unknown.

193 HighestVersionIsPending: Could not complete this action because the  highest vDisk version is still pending. The scheduled date for the version has not occurred yet.

194 MergeInvalidWithCurrentVersions: Merge is not valid with the current versions that exist.

195 DiskInventoryError: vDisk versions are not up to date on all Servers that access this vDisk. Update all Servers with the latest versions of the vDisk files.

196 VDiskFileNotFoundWarning: \[v1\]: vDisk file was not found because it was deleted.

197 CannotAssignActiveServer: Stop the Server before attempting to assign the Server to a different site.

198 CannotAssignServerWithActiveDevice: Before attempting to assign the Server to a different site, shut down Devices connecting to the Server, then shut down the Server.

199 MappedDiskLocator: The vDisk is mapped and cannot be changed.

200 InvalidTemplateDevice: The Template Device must be a Production Device that does not have a Personal vDisk.

201 DeviceWithPersonalVDiskInvalid: Unable to process a Device that uses a personal vDisk.

202 CreatingDisk: Server is creating a vDisk so change cannot be done.

203 AssignedDiskLocatorToDeviceWithPersonalvDisk: Unable to delete a vDisk if the vDisk is currently assigned to a Device that uses a Personal vDisk. Unassign the Device, then delete the vDisk.

204 InvalidMacAddress: The MAC address for this VM is invalid. Configure the VM with a valid MAC address.

205 CannotGetMacFromHypervisor: The hypervisor did not return the MAC address for this VM: \[v1\]

206 Win32SystemException: A system error occurred.

207 RemoteManagementIpCannotBeResolved: Unable to resolve the management IP for Server \[v1\].

208 LocalManagementIpNotSet: The management IP for local server \[v1\] is not set in registry IPC\\IPv4Address.

209 PerformVolumeMaintenanceTaskPermissions: Ensure the Service Account user has the appropriate 'Perform volume maintenance task' permissions.

210 CannotLoginToVirtualHostingPool: Unable to log on to the virtual hosting pool \[v1\]. Ensure that the hypervisior server is running properly.

211 VirtualHostingPoolNotSetForDevice: The virtualHostingPoolId for device \[v1\] with bdmBoot must be set.

212 ActiveBdmBootDeviceCannotProcess: The Boot Device Manager \[v1\] did not process successfully.

213 CannotMovePvdDeviceToAnotherSite: Personal vDisk Devices cannot be moved to another site.

214 XenDesktopSiteInvalid: Citrix Virtual Desktops Site for Devices is not valid, the Citrix Virtual Desktops Site is: \[v1\]

215 XenDesktopServiceListOutOfDate: Citrix Virtual Desktops Site \[v1\] is not reachable, check that the Citrix PVS Soap Server service user has Citrix Virtual Desktops permissions and network connectivity.

216 NoXenDesktopServiceForPersonalVDiskCapability: No Citrix Virtual Desktops service found for Personal vDisk capability.

217 InsufficientPermissionsToPreparePersonalVDisks: The user account for the Citrix PVS Soap Server has insufficient permissions to prepare Personal vDisks.

218 NotEnoughFreeDiskSpaceForManifest: There is not enough free disk space to create the manifest.

219 OperationCannotBeDoneOnlyPvdDevicesAssigned: Operation cannot be done, only Personal vDisk Devices are assigned.

220 DiskFormatCannotBeSetToVHD: The format cannot be set to VHD since no VHD vDisk file is found in the path, \[v1\], for Server, \[v2\].

221 DiskFormatCannotBeSetToVHDX: The format cannot be set to VHDX since no VHDX vDisk file is found in the path, \[v1\], for Server, \[v2\].

222 TemporaryVersionIsSet: This task cannot be performed because a temporary version is set.

223 DiskIsUsingPersistentCacheOnServer: A temporary version cannot be used for a vDisk that is using persistent cache on server.

224 UploadAlreadyInProgress: An upload is already in progress by Server \[v1\].

225 FieldMustBeNull: Field \[v1\] must be null.

226 DuplicateData: Record already exists in \[v1\] table for Farm.

227 CisUploadTokenGenerateError: Error generating upload token for My Citrix username \[v1\] (\[v2\]).

228 InvalidCredentials: The username or password is incorrect.

229 NoWriteAccessToFolders: No write access to folders \[v1\] or \[v2\].

230 ReportCreationError: Error creating problem report: \[v1\].

231 PvsProxyNotSupported: PVS Proxy not supported on this host

232 CannotCreateRegKey: Cannot create Registry key \[v1\]

4100 ADerrorUnexpectedError: An unexpected Active Directory related error occured. Ensure the appropriate permissions exist to perform this task. Error code: \[v1\], message: \[v2\], provider: \[v3\].