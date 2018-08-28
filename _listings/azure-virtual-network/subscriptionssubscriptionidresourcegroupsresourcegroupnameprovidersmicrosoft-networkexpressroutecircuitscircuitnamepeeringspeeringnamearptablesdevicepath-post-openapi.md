---
swagger: "2.0"
x-collection-name: Azure Virtual Network
x-complete: 0
info:
  title: Azure Virtual Network API Express Route Circuits List Arp Table
  description: Gets the currently advertised ARP table associated with the express
    route circuit in a resource group.
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---