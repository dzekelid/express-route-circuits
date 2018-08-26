---
swagger: "2.0"
x-collection-name: Azure Virtual Network
x-complete: 1
info:
  title: NetworkManagementClient
  description: the-microsoft-azure-network-management-api-provides-a-restful-set-of-web-services-that-interact-with-microsoft-azure-networks-service-to-manage-your-network-resources--the-api-has-entities-that-capture-the-relationship-between-an-end-user-and-the-microsoft-azure-networks-service-
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits/{circuitName}
  : delete:
      summary: Express Route Circuits Delete
      description: Deletes the specified express route circuit.
      operationId: ExpressRouteCircuits_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitname-delete
      parameters:
      - in: path
        name: circuitName
        description: The name of the express route circuit
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
    get:
      summary: Express Route Circuits Get
      description: Gets information about the specified express route circuit.
      operationId: ExpressRouteCircuits_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitname-get
      parameters:
      - in: path
        name: circuitName
        description: The name of express route circuit
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
    put:
      summary: Express Route Circuits Create Or Update
      description: Creates or updates an express route circuit.
      operationId: ExpressRouteCircuits_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitname-put
      parameters:
      - in: path
        name: circuitName
        description: The name of the circuit
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters supplied to the create or update express route circuit
          operation
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits/{circuitName}/peerings/{peeringName}/arpTables/{devicePath}
  : post:
      summary: Express Route Circuits List Arp Table
      description: Gets the currently advertised ARP table associated with the express
        route circuit in a resource group.
      operationId: ExpressRouteCircuits_ListArpTable
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitnamepeeringspeeringnamearptablesdevicepath-post
      parameters:
      - in: path
        name: circuitName
        description: The name of the express route circuit
      - in: path
        name: devicePath
        description: The path of the device
      - in: query
        name: No Name
      - in: path
        name: peeringName
        description: The name of the peering
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits/{circuitName}/peerings/{peeringName}/routeTables/{devicePath}
  : post:
      summary: Express Route Circuits List Routes Table
      description: Gets the currently advertised routes table associated with the
        express route circuit in a resource group.
      operationId: ExpressRouteCircuits_ListRoutesTable
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitnamepeeringspeeringnameroutetablesdevicepath-post
      parameters:
      - in: path
        name: circuitName
        description: The name of the express route circuit
      - in: path
        name: devicePath
        description: The path of the device
      - in: query
        name: No Name
      - in: path
        name: peeringName
        description: The name of the peering
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits/{circuitName}/peerings/{peeringName}/routeTablesSummary/{devicePath}
  : post:
      summary: Express Route Circuits List Routes Table Summary
      description: Gets the currently advertised routes table summary associated with
        the express route circuit in a resource group.
      operationId: ExpressRouteCircuits_ListRoutesTableSummary
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitnamepeeringspeeringnameroutetablessummarydevicepath-post
      parameters:
      - in: path
        name: circuitName
        description: The name of the express route circuit
      - in: path
        name: devicePath
        description: The path of the device
      - in: query
        name: No Name
      - in: path
        name: peeringName
        description: The name of the peering
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits/{circuitName}/stats
  : get:
      summary: Express Route Circuits Get Stats
      description: Gets all the stats from an express route circuit in a resource
        group.
      operationId: ExpressRouteCircuits_GetStats
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitnamestats-get
      parameters:
      - in: path
        name: circuitName
        description: The name of the express route circuit
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits/{circuitName}/peerings/{peeringName}/stats
  : get:
      summary: Express Route Circuits Get Peering Stats
      description: Gets all stats from an express route circuit in a resource group.
      operationId: ExpressRouteCircuits_GetPeeringStats
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuitscircuitnamepeeringspeeringnamestats-get
      parameters:
      - in: path
        name: circuitName
        description: The name of the express route circuit
      - in: query
        name: No Name
      - in: path
        name: peeringName
        description: The name of the peering
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/expressRouteCircuits:
    get:
      summary: Express Route Circuits List
      description: Gets all the express route circuits in a resource group.
      operationId: ExpressRouteCircuits_List
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networkexpressroutecircuits-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
  /subscriptions/{subscriptionId}/providers/Microsoft.Network/expressRouteCircuits:
    get:
      summary: Express Route Circuits List All
      description: Gets all the express route circuits in a subscription.
      operationId: ExpressRouteCircuits_ListAll
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-networkexpressroutecircuits-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Express Route Circuits
---