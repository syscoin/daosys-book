# Three-Tier Architecture

Three-tier architecture is a well-established software architecture that organizes backend applications into three logical computing tiers, which include:

* **Presentation tier**: controller classes
* **Application tier**: services classes
* **Data tier**: repository classes

The utility of this is to manage properly structured code  to make it easier for other developers to work with. Thus, no matter what the application (eg, API, CLI, etc.), it is important to approach your software design in this way, which is what we are introducing into our DAOSYS smart contract implementations.&#x20;

### Presentation Tier

This is the user interface and communication layer, and is where the controller classes reside. These controllers are solely responsible for delegation, and do not contain any logic or direct data manipulation. The main purpose of a controller is to get the request, then pass it to the service that will process it and then return the response that is given from the service.

### Application Tier

This is known as the logic or middle tier, and is considered the heart of the application. For instance this is where our DeFi setup would be established, which would be determined after running through several implementations of our design via the python simulator.
