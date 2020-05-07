# Digging into Rubrik APIs

APIs unlock unlimited opportunity to extend and automate functionality across the data center and cloud. This session will delve into Rubrik's API architecture, authentication, how to explore and consume APIs, versioning, and more. Walk away with tangible examples of how Rubrik’s APIs can be used to automate data protection.

Code and slides in repo. This is from a session at Rubrik Forward (Digital Summit) 2020.

# REST API Demos

## Prerequisites
The following pre-requisites are required for this example:

* Access to a Rubrik CDM cluster
* Postman

## Use Rubrik REST API Explorer
The Rubrik REST API Explorer can be accessed by navigating to `https://${var.ip_address}/docs/v1/playground`.

1. Authenicate (token or basic)
2. Take an on-demand snapshot
    * `GET /vmware/vm`. Specify a value in the `name` field
    * Copy the virtual machine ID
    * `POST /vmware/vm/{id}/snapshot` and input the string value of the virtual machine `id`
3. Validate on-demand snapshot

## Use Postman to navigate Rubrik REST API
Live Mount a vSphere virtual machine:

1. GET List of VM Live Mounts
2. GET VM UUID
3. GET snapshot UUID
4. POST VM Live Mount
5. GET List of VM Live Mounts
6. DEL VM Live Mount
7. GET List of VM Live Mounts

Postman collection for this function available [here](/Postman%20Collection%20-%20Demo%20-%20VM%20Live%20Mount). 

# GraphQL API Demos

## Prerequisites
The following pre-requisites are required for this example:

* Access to a Rubrik CDM cluster
* Postman

## Use Postman to interact with Rubrik GraphQL API
Live Mount a vSphere virtual machine:

1. Retrieve count of number of vCenters
2. Retrieve count of protected and unprotected VMs
3. Retrieve the names of 5 VMs
4. Retrieve information about a specified VM
5. Retrieve multiple VMs using aliases and a fragment
6. Retrieve multiple VMs, including SLA info, using aliases and a fragment
7. Retrieve information about the applied SLA

Postman collection for this function available [here](/Postman Collection - Demo - GraphQL/Rubrik Forward GraphQL API Demo.postman_collection.json). 
