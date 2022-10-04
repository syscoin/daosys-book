---
description: Diamond hardened security for the EVM
---

# Diamond Hardened Security

Since runtime cryptographic security is naturally done in the EVM, we are surfacing this feature using the Hyper-diamond standard within the functionality in DAOSYS. We call this Diamond hardened security for the EVM. By enforcing this design standard through our templates, this will cut-down on auditing tasks and significantly speed-up the security auditing process, and the development costs in general. For instance, a major concern with deploying on DeFi protocols like Aave is that they have a governance system that once changed, will change how Aave works, thus affecting anything security-wise that runs on that system.

However, with the Hyper-diamond standard, we are looking at the EVM as a secure shared run-time, much like how standard enterprise software applications are secure. For instance, if we were to make the analogy to the JVM, this would akin to every application sharing the same JVM where each application is building these low level hooks to ensure security. This is what's currently happening on the EVM, as nobody is building applications like its a shared run-time. Essentially, DAOSYS is borrowing these ideas from applications like Java with its layered software architecture, which is well defined and well structured. Hence, DAOSYS eliminates redundancy by exposing access to all the layers of our logic.&#x20;
