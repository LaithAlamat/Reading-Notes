# ***Azure Blobs***

Azure Blob storage is Microsoft's object storage solution for the cloud. Blob storage is optimized for storing massive amounts of unstructured data. Unstructured data is data that doesn't adhere to a particular data model or definition, such as text or binary data.

## ***Azure Blobs uses***

Blob storage is designed for:

- Serving images or documents directly to a browser.
- Storing files for distributed access.
- Streaming video and audio.
- Writing to log files.
- Storing data for backup and restore, disaster recovery, and archiving.
- Storing data for analysis by an on-premises or Azure-hosted service.

## ***Azure Data Lake Storage Gen2 advantages***

- Low-cost, tiered storage
- High availability
- Strong consistency
- Disaster recovery capabilities

## ***Blob storage types***

1. The storage account
2. A container in the storage account
3. A blob in a container

### ***Storage Accounts*** 
A storage account provides a unique namespace in Azure for your data. Every object that you store in Azure Storage has an address that includes your unique account name. The combination of the account name and the Blob Storage endpoint forms the base address for the objects in your storage account.

### ***Containers***
A container organizes a set of blobs, similar to a directory in a file system. A storage account can include an unlimited number of containers, and a container can store an unlimited number of blobs.

### ***Blobs***

1. Block blobs store text and binary data. Block blobs are made up of blocks of data that can be managed individually. Block blobs can store up to about 190.7 TiB.

2. Append blobs are made up of blocks like block blobs, but are optimized for append operations. Append blobs are ideal for scenarios such as logging data from virtual machines.

3. Page blobs store random access files up to 8 TiB in size. Page blobs store virtual hard drive (VHD) files and serve as disks for Azure virtual machines.

## ***Migrating existing data to Blob storage***

- AzCopy is an easy-to-use command-line tool for Windows and Linux that copies data to and from Blob storage, across containers, or across storage accounts.

- The Azure Storage Data Movement library is a .NET library for moving data between Azure Storage services. The AzCopy utility is built with the Data Movement library. 

- Azure Data Factory supports copying data to and from Blob storage by using the account key, a shared access signature, a service principal, or managed identities for Azure resources.

- Blobfuse is a virtual file system driver for Azure Blob storage. You can use blobfuse to access your existing block blob data in your Storage account through the Linux file system. 

- Azure Data Box service is available to transfer on-premises data to Blob storage when large datasets or network constraints make uploading data over the wire unrealistic. Depending on your data size, you can request Azure Data Box Disk, Azure Data Box, or Azure Data Box Heavy devices from Microsoft. You can then copy your data to those devices and ship them back to Microsoft to be uploaded into Blob storage.

- The Azure Import/Export service provides a way to import or export large amounts of data to and from your storage account using hard drives that you provide.

## ***Initialization***
- Azure Blob Storage client library for .NET package by using the dotnet add package command.

        dotnet add package Azure.Storage.Blobs

- Configure your storage connection string

 Replace <yourconnectionstring> with your actual connection string.

        setx AZURE_STORAGE_CONNECTION_STRING "<yourconnectionstring>"