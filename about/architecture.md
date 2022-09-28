# Architecture

The innovative software architecture that allows DAOSYS to pioneer a revolution in DAOs is the ASE. This introduces a revolution allowing DAOs to become more autonomous and fully decentralized. The ASE iterates on the Diamond proxy standard from EIP-2535 (see Appendix A) to apply AMM functionality for more flexible capabilities.

### ICREATE2METADATA

The `CREATE2` opcode is a low level human readable instruction used within the stack-based architecture of the Ethereum Virtual Machine (EVM) that was introduced in 2019 with EIP-1014 \[6]. This is the technology that enables AMMs in EVM implementations which allows a smart-contract to deploy another smart contract, and is typically called the Factory design pattern. Protocols like Balancer and Uniswap provide the ability to create permissionless liquidity pools. However, the limit of these implementations is the immutable nature of smart-contract bytecode as they can only deploy a single type of contract.

All contracts deployed through the ASE, new service proxies and delegate service, store the metadata for their deployment. This includes the factory address they were deployed from, and the value used to salt their deployment. Combined with the contract’s `codehash` this can be used to recalculate the contract’s address from the assertion of it’s `ICreate2Metadata` interface hook.

### IDELEGATESERVICE

Protocols like Aavegotchi have pioneered smart-contract architecture by iterating on the proxy capabilities of the EVM to advance the Factory design pattern. Smart-contract proxies take advantage of the `DELEGATECALL` opcode to allow a smart-contract to reuse the logic implemented in other smart-contracts. The Autonomous Service Engine advances this innovation with an infinitely flexible Diamond Factory design. The Diamond Factory design factory combines the Factory and Diamond design patterns to deploy configurable proxies. This allows for infinitely composable proxies.

Delegate Services replace the Facets defined in ERC-2535; see Fig. 3. Delegate Services define a strict storage allocation and access standard beyond the theory presented in ERC-2535. A Service is a smart-contract or library implemented following the Deterministically Dynamic Storage Allocation standard. A Service also reports the factory that deployed that contract and the salt used during deployment. This way the recalculation of the address from the factory init code hash and salt can be used to verify new Services as an implicit ACL.

\
This means that the deployment process for new Services deviates from industry standard. New Services are deployed as compiled bytecode passed to the Service Proxy Factory as the argument for the deployment function. The Service Proxy Factory then instantiates that bytecode as a new contract. ASE compliant Services must include the `ASEServiceBootstrapper` library to retrieve the address salt to initialize the Service. This should be done by delegating to the canonical external library deployment. ASE compliant external libraries may pre-calculate their address salt and store it as a constant. The standard Service initialization functions must still be implemented, but may hard code the values and return values since they can not store state.

All Services are required to implement ERC-165 including the Service extension that enumerates the functions. The Service extension to ERC-165 includes a per interface enumeration of the function selectors that define the interface ID. Additionally, there is an enumeration of all the function selectors across all interface IDs, and a `ServiceDef` struct that includes the information for initializing a Service Proxy to consume the Service.

<figure><img src="../.gitbook/assets/hyper_facet.png" alt=""><figcaption><p>FIGURE 3: Hyper-facet consisting of delegate Services that replace facets defined in ERC-2535</p></figcaption></figure>
