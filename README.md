# ![LOGO](logo.png) RecoveryServicesBackupClient **flow**ground Connector

## Description

A generated **flow**ground connector for the RecoveryServicesBackupClient API (version 2016-06-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/recoveryservicesbackup/2016-06-01/swagger.json<br/>
Generated at: 2019-06-11T18:14:10+03:00

## API Description



## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### The backup management servers registered to a Recovery Services vault. This returns a pageable list of servers.

*Tags:* `BackupEngines`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `$filter` - _optional_ - Use this filter to choose the specific backup management server. backupManagementType { AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql }.
* `$skipToken` - _optional_ - The Skip Token filter.

### Provides the result of the refresh operation triggered by the BeginRefresh operation.

*Tags:* `ProtectionContainerRefreshOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the container.
* `operationId` - _required_ - The operation ID used for this GET operation.

### Gets details of the specific container registered to your Recovery Services vault.

*Tags:* `ProtectionContainers`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the container.
* `containerName` - _required_ - The container name used for this GET operation.

### Gets the result of any operation on the container.

*Tags:* `ProtectionContainerOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the container.
* `containerName` - _required_ - The container name used for this GET operation.
* `operationId` - _required_ - The operation ID used for this GET operation.

### Used to disable the backup job for an item within a container. This is an asynchronous operation. To learn the status of the request, call the GetItemOperationResult API.

*Tags:* `ProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ -  The fabric name associated with the backup item.
* `containerName` - _required_ - The container name associated with the backup item.
* `protectedItemName` - _required_ - The backup item to be deleted.

### Provides the details of the backup item. This is an asynchronous operation. To know the status of the operation, call the GetItemOperationResult API.

*Tags:* `ProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup item.
* `containerName` - _required_ - The container name associated with the backup item.
* `protectedItemName` - _required_ - The backup item name used in this GET operation.
* `$filter` - _optional_ - expand eq {extendedInfo}. This filter enables you to choose (or filter) specific items in the list of backup items.

### This operation enables an item to be backed up, or modifies the existing backup policy information for an item that has been backed up. This is an asynchronous operation. To learn the status of the operation, call the GetItemOperationResult API.

*Tags:* `ProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup item.
* `containerName` - _required_ - The container name associated with the backup item.
* `protectedItemName` - _required_ - The name of the backup item.

### Triggers the backup job for the specified backup item. This is an asynchronous operation. To know the status of the operation, call GetProtectedItemOperationResult API.

*Tags:* `Backups`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup item.
* `containerName` - _required_ - The container name associated with the backup item.
* `protectedItemName` - _required_ - The name of backup item used in this POST operation.

### Gets the result of any operation on the backup item.

*Tags:* `ProtectedItemOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup item.
* `containerName` - _required_ - The container name associated with the backup item.
* `protectedItemName` - _required_ - The name of backup item used in this GET operation.
* `operationId` - _required_ - The OperationID used in this GET operation.

### Gets the status of an operation such as triggering a backup or restore. The status can be: In progress, Completed, or Failed. You can refer to the OperationStatus enum for all the possible states of the operation. Some operations create jobs. This method returns the list of jobs associated with the operation.

*Tags:* `ProtectedItemOperationStatuses`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup item.
* `containerName` - _required_ - The container name associated with the backup item.
* `protectedItemName` - _required_ - The name of backup item used in this GET operation.
* `operationId` - _required_ - The OperationID used in this GET operation.

### Lists the recovery points, or backup copies, for the specified backup item.

*Tags:* `RecoveryPoints`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup item.
* `containerName` - _required_ - The container name associated with the backup item.
* `protectedItemName` - _required_ - The name of backup item used in this GET operation.
* `$filter` - _optional_ - startDate eq {yyyy-mm-dd hh:mm:ss PM} and endDate { yyyy-mm-dd hh:mm:ss PM}.

### Provides the backup data for the RecoveryPointID. This is an asynchronous operation. To learn the status of the operation, call the GetProtectedItemOperationResult API.

*Tags:* `RecoveryPoints`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with backup item.
* `containerName` - _required_ - The container name associated with backup item.
* `protectedItemName` - _required_ - The name of the backup item used in this GET operation.
* `recoveryPointId` - _required_ - The RecoveryPointID associated with this GET operation.

### Provisions a script which invokes an iSCSI connection to the backup data. Executing this script opens File Explorer which displays the recoverable files and folders. This is an asynchronous operation. To get the provisioning status, call GetProtectedItemOperationResult API.

*Tags:* `ItemLevelRecoveryConnections`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup items.
* `containerName` - _required_ - The container name associated with the backup items.
* `protectedItemName` - _required_ - The name of the backup item whose files or folders are to be restored.
* `recoveryPointId` - _required_ - The recovery point ID for backup data. The iSCSI connection will be provisioned for this backup data.

### Restores the specified backup data. This is an asynchronous operation. To know the status of this API call, use GetProtectedItemOperationResult API.

*Tags:* `Restores`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup items.
* `containerName` - _required_ - The container name associated with the backup items.
* `protectedItemName` - _required_ - The backup item to be restored.
* `recoveryPointId` - _required_ - The recovery point ID for the backup data to be restored.

### Revokes an iSCSI connection which can be used to download a script. Executing this script opens a file explorer displaying all recoverable files and folders. This is an asynchronous operation.

*Tags:* `ItemLevelRecoveryConnections`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the backup items. The value allowed is Azure.
* `containerName` - _required_ - The container name associated with the backup items.
* `protectedItemName` - _required_ - The name of the backup items whose files or folders will be restored.
* `recoveryPointId` - _required_ - The string that identifies the recovery point. The iSCSI connection will be revoked for this protected data.

### Discovers the containers in the subscription that can be protected in a Recovery Services vault. This is an asynchronous operation. To learn the status of the operation, use the GetRefreshOperationResult API.

*Tags:* `ProtectionContainers`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `fabricName` - _required_ - The fabric name associated with the container.

### Provides a pageable list of jobs.

*Tags:* `Jobs`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `$filter` - _optional_ - The following equation can be used to filter the list of jobs based on status, type, start date, and end date. status eq { InProgress , Completed , Failed , CompletedWithWarnings , Cancelled , Cancelling } and backupManagementType eq {AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql } and operation eq { ConfigureBackup , Backup , Restore , DisableBackup , DeleteBackupData } and jobId eq {guid} and startTime eq { yyyy-mm-dd hh:mm:ss PM } and endTime eq { yyyy-mm-dd hh:mm:ss PM }.
* `$skipToken` - _optional_ - The Skip Token filter.

### Gets the result of the operation triggered by the ExportJob API.

*Tags:* `ExportJobsOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `operationId` - _required_ - The ID associated with the export job.

### Gets extended information associated with the job.

*Tags:* `JobDetails`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `jobName` - _required_ - Name of the job associated with this GET operation.

### Cancels the job. This is an asynchronous operation. To know the status of the cancellation, call the GetCancelOperationResult API.

*Tags:* `JobCancellations`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `jobName` - _required_ - Name of the job to cancel.

### Gets the result of the operation.

*Tags:* `JobOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `jobName` - _required_ - Job name associated with this GET operation.
* `operationId` - _required_ - OperationID associated with this GET operation.

### Exports all jobs for a given Shared Access Signatures (SAS) URL. The SAS URL expires within 15 minutes of its creation.

*Tags:* `Jobs`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `$filter` - _optional_ - The OData filter options. status eq { InProgress , Completed , Failed , CompletedWithWarnings , Cancelled , Cancelling } and backupManagementType eq {AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql } and operation eq { ConfigureBackup , Backup , Restore , DisableBackup , DeleteBackupData } and jobId eq {guid} and startTime eq { yyyy-mm-dd hh:mm:ss PM } and endTime eq { yyyy-mm-dd hh:mm:ss PM }.

### Provides the status of the delete operations, for example, deleting a backup item. Once the operation starts, the response status code is Accepted. The response status code remains in this state until the operation reaches completion. On successful completion, the status code changes to OK. This method expects OperationID as an argument. OperationID is part of the Location header of the operation response.

*Tags:* `BackupOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `operationId` - _required_ - The ID of the operation.

### Gets the status of an operation such as triggering a backup or restore. The status can be In progress, Completed or Failed. You can refer to the OperationStatus enum for all the possible states of an operation. Some operations create jobs. This method returns the list of jobs when the operation is complete.

*Tags:* `BackupOperationStatuses`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `operationId` - _required_ - The ID of the operation.

### Lists the backup policies associated with the Recovery Services vault. The API provides parameters to Get scoped results.

*Tags:* `ProtectionPolicies`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `$filter` - _optional_ - The following equation can be used to filter the list of backup policies. backupManagementType eq {AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql}.

### Deletes the specified backup policy from your Recovery Services vault. This is an asynchronous operation. Use the GetPolicyOperationResult API to Get the operation status.

*Tags:* `ProtectionPolicies`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `policyName` - _required_ - The name of the backup policy to be deleted.

### Gets the details of the backup policy associated with the Recovery Services vault. This is an asynchronous operation. Use the GetPolicyOperationResult API to Get the operation status.

*Tags:* `ProtectionPolicies`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `policyName` - _required_ - The backup policy name used in this GET operation.

### Creates or modifies a backup policy. This is an asynchronous operation. Use the GetPolicyOperationResult API to Get the operation status.

*Tags:* `ProtectionPolicies`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `policyName` - _required_ - The backup policy to be created.

### Provides the result of an operation.

*Tags:* `ProtectionPolicyOperationResults`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `policyName` - _required_ - The backup policy name used in this GET operation.
* `operationId` - _required_ - The ID associated with this GET operation.

### Provides the status of the asynchronous operations like backup or restore. The status can be: in progress, completed, or failed. You can refer to the Operation Status enumeration for the possible states of an operation. Some operations create jobs. This method returns the list of jobs associated with the operation.

*Tags:* `ProtectionPolicyOperationStatuses`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `policyName` - _required_ - The backup policy name used in this GET operation.
* `operationId` - _required_ - The ID associated with this GET operation.

### Based on the query filter and the pagination parameters, this operation provides a pageable list of objects within the subscription that can be protected.

*Tags:* `ProtectableItems`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `$filter` - _optional_ - Using the following query filters, you can sort a specific backup item based on: type of backup item, status, name of the item, and more.  providerType eq { AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql } and status eq { NotProtected , Protecting , Protected } and friendlyName {name} and skipToken eq {string which provides the next set of list} and topToken eq {int} and backupManagementType eq { AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql }.
* `$skipToken` - _optional_ - The Skip Token filter.

### Provides a pageable list of all items in a subscription, that can be protected.

*Tags:* `ProtectedItems`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `$filter` - _optional_ -  itemType eq { VM , FileFolder , AzureSqlDb , SQLDB , Exchange , Sharepoint , DPMUnknown } and providerType eq { AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql } and policyName eq {policyName} and containerName eq {containername} and backupManagementType eq { AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql }.
* `$skipToken` - _optional_ -  The Skip Token filter.

### Lists the containers registered to the Recovery Services vault.

*Tags:* `ProtectionContainers`

#### Input Parameters
* `api-version` - _required_ - Client API version.
* `vaultName` - _required_ - The name of the Recovery Services vault.
* `resourceGroupName` - _required_ - The name of the resource group associated with the Recovery Services vault.
* `subscriptionId` - _required_ - The subscription ID.
* `$filter` - _optional_ - The following equation is used to sort or filter the containers registered to the vault. providerType eq {AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql} and status eq {Unknown, NotRegistered, Registered, Registering} and friendlyName eq {containername} and backupManagementType eq {AzureIaasVM, MAB, DPM, AzureBackupServer, AzureSql}.

## License

**flow**ground :- Telekom iPaaS / azure-com-recoveryservicesbackup-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
