# Dataset Information and Statistics

## Dataset Name
PE File Dataset

## Description
This dataset contains information about various PE (Portable Executable) files. Each row represents a different PE file, and each column represents a different attribute of the file.

## Columns

| Column Name                | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| **Name**                   | The name of the PE file.                                                   |
| **md5**                    | The MD5 hash of the PE file.                                               |
| **Machine**                | The machine type (e.g., architecture) for which the PE file is intended.  |
| **SizeOfOptionalHeader**   | The size of the optional header in the PE file.                             |
| **Characteristics**        | Characteristics of the PE file (e.g., executable, DLL, etc.).             |
| **MajorLinkerVersion**     | The major version of the linker used to create the PE file.                 |
| **MinorLinkerVersion**     | The minor version of the linker used to create the PE file.                 |
| **SizeOfCode**             | The size of the code section in the PE file.                                |
| **SizeOfInitializedData**  | The size of the initialized data section in the PE file.                     |
| **SizeOfUninitializedData**| The size of the uninitialized data section in the PE file.                   |
| **AddressOfEntryPoint**   | The address of the entry point in the PE file.                              |
| **BaseOfCode**             | The base address of the code section in the PE file.                        |
| **BaseOfData**             | The base address of the data section in the PE file.                         |
| **ImageBase**              | The preferred base address of the PE file in memory.                        |
| **SectionAlignment**       | The alignment of sections in the PE file.                                   |
| **FileAlignment**          | The alignment of the PE file on disk.                                      |
| **MajorOperatingSystemVersion** | The major version of the operating system for which the PE file is intended.|
| **MinorOperatingSystemVersion** | The minor version of the operating system for which the PE file is intended.|
| **MajorImageVersion**       | The major version of the image (PE file).                                    |
| **MinorImageVersion**       | The minor version of the image (PE file).                                    |
| **MajorSubsystemVersion**   | The major version of the subsystem for which the PE file is intended.        |
| **MinorSubsystemVersion**   | The minor version of the subsystem for which the PE file is intended.        |
| **SizeOfImage**            | The size of the image (PE file) in memory.                                 |
| **SizeOfHeaders**          | The size of the headers in the PE file.                                     |
| **CheckSum**                | The checksum of the PE file.                                                |
| **Subsystem**               | The subsystem for which the PE file is intended (e.g., GUI, CUI).         |
| **DllCharacteristics**     | Characteristics specific to DLLs in the PE file.                           |
| **SizeOfStackReserve**     | The size of the stack to reserve for the PE file.                           |
| **SizeOfStackCommit**      | The size of the stack to commit for the PE file.                            |
| **SizeOfHeapReserve**      | The size of the heap to reserve for the PE file.                            |
| **SizeOfHeapCommit**       | The size of the heap to commit for the PE file.                              |
| **LoaderFlags**            | Flags used by the loader for the PE file.                                   |
| **NumberOfRvaAndSizes**    | The number of RVA (Relative Virtual Address) and sizes in the PE file.      |
| **SectionsNb**             | The number of sections in the PE file.                                       |
| **SectionsMeanEntropy**    | The mean entropy of the sections in the PE file.                             |
| **SectionsMinEntropy**     | The minimum entropy of the sections in the PE file.                          |
| **SectionsMaxEntropy**     | The maximum entropy of the sections in the PE file.                          |
| **SectionsMeanRawsize**    | The mean raw size of the sections in the PE file.                            |
| **SectionsMinRawsize**     | The minimum raw size of the sections in the PE file.                         |
| **SectionsMaxRawsize**     | The maximum raw size of the sections in the PE file.                         |
| **SectionsMeanVirtualsize**| The mean virtual size of the sections in the PE file.                         |
| **SectionsMinVirtualsize** | The minimum virtual size of the sections in the PE file.                     |
| **SectionsMaxVirtualsize** | The maximum virtual size of the sections in the PE file.                     |
| **ImportsNbDLL**           | The number of imported DLLs in the PE file.                                |
| **ImportsNb**               | The total number of imports in the PE file.                                 |
| **ImportsNbOrdinal**       | The number of ordinal imports in the PE file.                               |
| **ExportNb**               | The number of exports in the PE file.                                       |
| **ResourcesNb**            | The number of resources in the PE file.                                      |
| **ResourcesMeanEntropy**   | The mean entropy of the resources in the PE file.                            |
| **ResourcesMinEntropy**    | The minimum entropy of the resources in the PE file.                          |
| **ResourcesMaxEntropy**    | The maximum entropy of the resources in the PE file.                          |
| **ResourcesMeanSize**      | The mean size of the resources in the PE file.                               |
| **ResourcesMinSize**       | The minimum size of the resources in the PE file.                            |
| **ResourcesMaxSize**       | The maximum size of the resources in the PE file.                            |
| **LoadConfigurationSize**   | The size of the load configuration in the PE file.                            |
| **VersionInformationSize**  | The size of the version information in the PE file.                           |
| **legitimate**              | Indicates whether the PE file is considered legitimate.                     |

## Statistics

- **Total Number of Records**: 10541
- **File Size**: Approximately 560 KB

## Usage
This dataset can be used for various purposes, including:
- **Malware Analysis**: Analyzing the characteristics of PE files to identify malware.
- **Software Research**: Studying the properties of different PE files.
- **Machine Learning**: Training models to classify PE files as legitimate or malicious.

## Source
The dataset was compiled from various sources, including public repositories and malware analysis reports.

## License
This dataset is provided for educational and research purposes only. The use of this dataset is subject to the terms and conditions of the original sources.

## Contact
For any questions or further information, please contact the dataset maintainer.

