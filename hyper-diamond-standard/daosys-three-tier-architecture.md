---
description: Structure of the Hyper-diamond standard
---

# DAOSYS Three-Tier Architecture

Three-tier architecture is a well-established software architecture that organizes backend applications into three logical computing tiers, which include:

* **Presentation tier**: controller classes
* **Application tier**: services classes
* **Data tier**: repository classes

The utility of this is to manage properly structured code  to make it easier for other developers to work with. Thus, no matter what the application (eg, API, CLI, etc.), it is important to approach your software design in this way, which is what we are introducing into our DAOSYS smart contract implementations, namely the _Hyper Diamond Standard_.&#x20;

#### Presentation Tier

This is the user interface and communication layer, and is where the controller classes reside. These controllers are solely responsible for delegation, and do not contain any logic or direct data manipulation. The main purpose of a controller is to get the request, then pass it to the service that will process it and then return the response that is given from the service.

#### Application Tier

This is known as the logic or middle tier, and is considered the heart of the application. For instance this is where the DeFi setup would be established, which would be determined after running through several implementations of the design via the python simulator. This is where the services which get called by the controller classes and might call repositories or other services.&#x20;

#### Data Tier

This is the persistence or repository layer whose responsibilities are limited to Create, Retrieve, Update, and Delete (CRUD) operations on a data source; in the case of DAOSYS, it's the storage repositories.

### DAOSYS Package

This three-tier architecture is the structure by which the DAOSYS facet controller adheres to, which is defined as a package; see Fig 3. This well defined structure is the Hyper-diamond standard, and serves as an extension of EIP-2535. This is where we define each diamond facet as a fully functioning controller in accordance to well established protocols that have successfully served the software engineering process for the last number of decades.

<figure><img src="../.gitbook/assets/three_tier_package.png" alt=""><figcaption><p>FIGURE 3: Three-tier structure of the DAOSYS package</p></figcaption></figure>

The DAOSYS package are the templates that get deployed onto the network which represent a combination of management and deployment systems. These packages will serve as the no-code or low-code deployments onto the DAOSYS network. Thus allowing the DAOSYS protocol to serve as the first enterprise development system for the EVM. It is anticipated that these package deployments will consume more Gas than custom built deployments. However, since these will be utilized as layer-2 applications, Gas consumption will be far less than on layer 1. Hence, the benefits of fast seamless and secure deployments will far outweigh the additional incurred Gas costs.
