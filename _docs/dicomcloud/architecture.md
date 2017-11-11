---
title: Architecture
navigation: dicomcloud
---

The DICOMcloud is a web server that can interface with any DICOMweb client over the current implemented features (qido-rs, wado-uri, wado-rs and stow-rs).

An example DICOMweb client implementation with viewer support is provided [here](https://github.com/DICOMcloud/DICOMweb-js).

The implementation is customizable by using [StructureMap](https://github.com/structuremap/structuremap) as a DI (Dependency Injection) framework to provide a plug-in architecture.

The main layers of the DICOMcloud:

| Layer | Description | Project Name | Nuget Link |
| ------| ----------- | ------------ | -----------|
| **WebAPI RESTFUL Services** | The webservice implementation as an ASP.NET WebAPI | DICOMcloud.Wado.WebAPI | [![NuGet Pre Release](https://img.shields.io/nuget/vpre/DICOMcloud.Wado.WebApi.svg)](https://www.nuget.org/packages/DICOMcloud.Wado.WebApi/) |
| **DICOMweb Core Services** | The DICOMweb implementation for processing web requests and returning web responses. | DICOMcloud.Wado | [![NuGet Pre Release](https://img.shields.io/nuget/vpre/DICOMcloud.Wado.svg)](https://www.nuget.org/packages/DICOMcloud.Wado/) |
| **DICOM Services** | The core DICOM code and business services that process the DICOM datasets, perform query, retrieve and store. With interfaces to classes for storage and data access. | DICOMcloud | [![NuGet Pre Release](https://img.shields.io/nuget/vpre/DICOMcloud.svg)](https://www.nuget.org/packages/DICOMcloud/) |
| **Data Storage and Data Access** | The specific implementation layer that physically save the DICOM dataset media to a file system or Azure Blob and interface with Microsoft/Azure SQL database. | DICOMcloud <br> DICOMcloud.Azure <br> DICOMcloud.DataAccess.Database | [![NuGet Pre Release](https://img.shields.io/nuget/vpre/DICOMcloud.DataAccess.Database.svg)](https://www.nuget.org/packages/DICOMcloud.DataAccess.Database/) & [![NuGet Pre Release](https://img.shields.io/nuget/vpre/DICOMcloud.Azure.svg)](https://www.nuget.org/packages/DICOMcloud.Azure/) |

![DICOMcloud Architecture](https://raw.githubusercontent.com/DICOMcloud/DICOMcloud/master/Resources/Docs/DICOMcloud-Arch..png)
