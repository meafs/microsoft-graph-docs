---
title: "Work with the Microsoft Graph connectors API"
description: "Get an overview of the Microsoft Graph connectors API, including the External connection API, Schema API, External item API, and External group API."
author: mecampos
ms.localizationpriority: high
doc_type: conceptualPageType
ms.prod: search
---

# Work with the Microsoft Graph connectors API

Microsoft Graph connectors offer an intuitive way to bring external data into Microsoft Graph and enhance Microsoft 365 intelligent experiences. You might want to build a custom connector to integrate with services that aren't available as connectors built by Microsoft. To build custom connectors, you use the Microsoft Graph connectors REST APIs.

![Image showing the external data coming trough different types of connectors to Microsoft Graph](./images/connectors-images/api-overview.png)

You can use the Microsoft Graph connectors API to:

1. Create and manage external data connections.
2. Define and register the schema of the external data types.
3. Ingest external data items into Microsoft Graph.
4. Sync external groups.

## External connection API

The [externalConnection](/graph/api/resources/externalconnectors-externalconnection?view=graph-rest-1.0&preserve-view=true) resource is a logical container for your external data that you can manage as a single unit.

To learn more, see [Create, update, and delete connections in Microsoft Graph](connecting-external-content-manage-connections.md).

## Schema API

The connection [schema](/graph/api/resources/externalconnectors-schema?view=graph-rest-1.0&preserve-view=true) determines how your content is used in various Microsoft 365 experiences. The schema is a flat list of all the properties that you plan to add to the connection along with their attributes, labels, and aliases. You must register the schema before ingesting items into Microsoft Graph.

To learn more, see [Register and update schema for the Microsoft Graph connection](connecting-external-content-manage-schema.md).

## External item API

Items added by your application to the Microsoft Search service are represented by the [externalItem](/graph/api/resources/externalconnectors-externalitem?view=graph-rest-1.0&preserve-view=true) resource in Microsoft Graph.

To learn more, see [Create, update, and delete items added by your application via Microsoft Graph connectors](connecting-external-content-manage-items.md).

## External group API

Items in the external service can be granted or denied access via ACL to different types of non-Azure Active Directory groups. For example, Salesforce items might have permission sets and profiles, while ServiceNow items might have local groups. When you ingest these items into Microsoft Graph, you need to honor these ACLs.

You can use the External group API to set permissions on external items ingested into Microsoft Graph. An [externalGroup](/graph/api/resources/externalconnectors-externalgroup?view=graph-rest-1.0&preserve-view=true) represents a non-Azure Active Directory group or group-like construct (such as business units, teams, and so on) and determines permissions on the content in your external data source.

To learn more, see [Use external groups to manage permissions to Microsoft Graph connectors data sources](connecting-external-content-external-groups.md).
