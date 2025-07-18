# KeycloakRestClient for C#

A C# client library for Keycloak Admin REST API, automatically generated from official Keycloak Admin OpenAPI specifications using NSwag. This library uses System.Text.Json for JSON serialization and supports multiple .NET frameworks.

## Features

- **Auto-generated from Official OpenAPI Specs**: Built directly from Keycloak's official Admin API OpenAPI JSON specifications
- **System.Text.Json Support**: Uses the modern System.Text.Json library for high-performance JSON serialization
- **Multi-framework Support**: Targets .NET Standard 2.0, .NET 8.0, and .NET 9.0
- **Version Synchronization**: Library version matches the corresponding Keycloak version
- **Complete API Coverage**: Includes all Keycloak Admin API endpoints and operations

## Installation

```bash
dotnet add package KeycloakRestClient
```

## Supported Frameworks

- .NET Standard 2.0
- .NET 8.0
- .NET 9.0

## Usage

```csharp
using KeycloakRestClient;

// Create client instance
var client = new KeycloakClient(httpClient);

// Use the client to interact with Keycloak Admin API
// (Add specific usage examples based on your implementation)
```

## Library Generation Process

This library is generated using the following automated process:

### Obtain OpenAPI JSON

Get the OpenAPI JSON specification from the [Keycloak Documentation Archive](https://www.keycloak.org/documentation-archive) based on your desired Keycloak version (available for version 24 and above). Navigate to your target version → **API Documentation** → **Administration REST API** → find "OpenAPI definition in JSON format".

### Prerequisites

Install the NSwag CLI tool globally:

```bash
dotnet tool install --global NSwag.ConsoleCore
```

### Generation Command

```bash
nswag openapi2csclient /input:openapi.json /output:KeycloakClient.cs /namespace:KeycloakRestClient /className:KeycloakClient /jsonLibrary:SystemTextJson
```

### Project Configuration

The library targets multiple frameworks:

```xml
<TargetFrameworks>netstandard2.0;net8.0;net9.0</TargetFrameworks>
```

### Dependencies

```xml
<PackageReference Include="System.Text.Json" Version="4.7.2" />
```

## Versioning

**Important**: The version of this library is synchronized with the corresponding Keycloak version. For example:
- Library version 21.x.x corresponds to Keycloak 21.x.x
- Library version 22.x.x corresponds to Keycloak 22.x.x

This ensures API compatibility and feature alignment with your Keycloak server version.
ersion alignment between your Keycloak server and this client library.