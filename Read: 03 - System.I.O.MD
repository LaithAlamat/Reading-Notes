# ***File and Stream I/O***
File and stream I/O (input/output) refers to the transfer of data either to or from a storage medium.

In .NET, the System.IO namespaces contain types that enable reading and writing, both synchronously and asynchronously, on data streams and files.


### ***File and Directory Classes:***

- File - provides static methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

- FileInfo - provides instance methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

- Directory - provides static methods for creating, moving, and enumerating through directories and subdirectories.

- DirectoryInfo - provides instance methods for creating, moving, and enumerating through directories and subdirectories.

- Path - provides methods and properties for processing directory strings in a cross-platform manner.

### ***Streams Fundamental Operations:***

- Reading - transferring data from a stream into a data structure, such as an array of bytes.

- Writing - transferring data to a stream from a data source.

- Seeking - querying and modifying the current position within a stream.


### ***Commonly Used Stream Classes:***

- FileStream – for reading and writing to a file.

- IsolatedStorageFileStream – for reading and writing to a file in isolated storage.

- MemoryStream – for reading and writing to memory as the backing store.

- BufferedStream – for improving performance of read and write operations.

- NetworkStream – for reading and writing over network sockets.

- PipeStream – for reading and writing over anonymous and named pipes.

- CryptoStream – for linking data streams to cryptographic transformations.

### ***Commonly Used Reader and Writer Classes:***

- BinaryReader and BinaryWriter – for reading and writing primitive data types as binary values.

- StreamReader and StreamWriter – for reading and writing characters by using an encoding value to convert the characters to and from bytes.

- StringReader and StringWriter – for reading and writing characters to and from strings.

- TextReader and TextWriter – serve as the abstract base classes for other readers and writers that read and write characters and strings, but not binary data.

### ***Asynchronous I/O Operations:***

We should use them to keep the application resposive to the user so tha the application does not have to read all of the data synchronously.

The asynchronous members contain Async in their names, such as the CopyToAsync, FlushAsync, ReadAsync, and WriteAsync methods. You use these methods with the async and await keywords.


### ***Compression:***

Compression refers to the process of reducing the size of a file for storage. Decompression is the process of extracting the contents of a compressed file so they are in a usable format. 

The following classes are frequently used when compressing and decompressing files and streams:

- ZipArchive – for creating and retrieving entries in the zip archive.

- ZipArchiveEntry – for representing a compressed file.

- ZipFile – for creating, extracting, and opening a compressed package.

- ZipFileExtensions – for creating and extracting entries in a compressed package.

- DeflateStream – for compressing and decompressing streams using the Deflate algorithm.

- GZipStream – for compressing and decompressing streams in gzip data format.

### ***Isolated storage:***

Isolated storage is a data storage mechanism that provides isolation and safety by defining standardized ways of associating code with saved data. 

The following classes are frequently used when implementing isolated storage:

- IsolatedStorage – provides the base class for isolated storage implementations.

- IsolatedStorageFile – provides an isolated storage area that contains files and directories.

- IsolatedStorageFileStream - exposes a file within isolated storage.



