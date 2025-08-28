# Azure Cosmos DB Management SDK Samples for C# V2

This folder contains Azure Management SDK samples for Azure Cosmos DB using the stable version of `Azure.ResourceManager.CosmosDB` SDK.

## Overview

These samples demonstrate how to create and manage Azure Cosmos DB resources using the Azure Resource Manager SDK for .NET. The samples use the stable version of the `Azure.ResourceManager.CosmosDB` package (v1.3.2) instead of preview/beta versions.

## Features Demonstrated

- **Account Management**: Create or update Cosmos DB accounts with serverless capabilities and security configurations
- **Database Operations**: Create and manage SQL databases
- **Container Management**: Configure containers with hierarchical partition keys, indexing policies, unique keys, TTL, and conflict resolution
- **Throughput Management**: Update autoscale throughput settings
- **Role-Based Access Control (RBAC)**: 
  - Create custom role definitions
  - Assign built-in and custom roles
  - Manage data plane permissions

## Prerequisites

- .NET 8.0 or later
- Azure subscription
- Azure CLI or appropriate authentication setup

## Configuration

Update the `appsettings.json` file with your Azure subscription details:

```json
{
    "SubscriptionId": "your-subscription-id",
    "ResourceGroupName": "your-resource-group-name", 
    "AccountName": "your-cosmos-account-name",
    "Location": "East US",
    "DatabaseName": "your-database-name",
    "ContainerName": "your-container-name",
    "MaxAutoScaleThroughput": 1000
}
```

## Running the Samples

1. Ensure you're authenticated with Azure (using Azure CLI, Visual Studio, or environment variables)
2. Update the configuration file with your Azure details
3. Build and run the project:

```bash
dotnet build
dotnet run
```

## Key Differences from Beta Versions

This version uses the stable `Azure.ResourceManager.CosmosDB` package and excludes preview features such as:
- Computed Properties (available in beta versions)
- Other preview-only features

## SDK Reference

- Package: [Azure.ResourceManager.CosmosDB](https://www.nuget.org/packages/Azure.ResourceManager.CosmosDB) (v1.3.2)
- Documentation: [Azure SDK for .NET - Cosmos DB](https://learn.microsoft.com/en-us/dotnet/api/azure.resourcemanager.cosmosdb)
- Source: [GitHub - Azure SDK for .NET](https://github.com/Azure/azure-sdk-for-net/tree/main/sdk/cosmosdb/Azure.ResourceManager.CosmosDB)