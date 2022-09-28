# Governance

DAOs are governance structures for groups of people to come together and make decisions, which is one of its main distin- guishing features. Unlike traditional organizations (e.g., pri- vate companies, non-governmental organizations, charities, etc.) which have a centralized structure, these decisions are coordinated and enforced on a blockchain in a decentralized manner. Since DAOSYS proposes to be autonomous and fully decentralized, it has no top level governance.

AMMs are an essential part of the DeFi ecosystem. They allow digital assets to be traded in a permissionless and auto- matic way by using liquidity pools rather than a traditional market of buyers and sellers. Applying the AMM model to DAOs means that users create their own treasuries for specific ventures. These treasuries may apply a variety of governance solutions along with their treasuries. This allows for a compartmentalization of the politics that arise with any governance solution from the actual treasury management.

Under this model, the Syscoin Foundation behaves more like the software vendor. The factory makes open-source reference implementations of DeFi components available to compose into treasuries. Updates to these smart-contracts are available for deploying new pools that may be added to a DAO. Hence, this removes the need for top-level governance solutions that decides whether to include an update because users are free to create new pools.

A user creates a DAO by selecting which vaults and bond markets they would like to include. These vaults may come from one of four sources.

### Reuse an Existing Vault

This works best for when users wish to maintain their position in one DAO, but want to add more pools to form a new DAO.

### Recreate an Existing Vault

As the adage goes, _if it’s not broke, don’t fix it_. The investment strategy implemented in a vault can be used across several instances of vault pools. This works well for new DAOs that wish to replicate the financial strategies of an existing DAO. Also, this also works for when a new DAO would like to invest in other DAOs using the same strategy.

### New Pool with New Investment Strategy

A user may wish to create a new DAO reusing functionality available from the factory, but configured in a novel manner. The flexibility available in the ASE means that even a simple strategy has several configuration options. This is useful for when a DAO wishes to adopt a novel investment strategy that might not have been previously viable.

### New Pool with Custom Code

The Syscoin Foundation makes internal decisions regarding what smart-contracts are available through the factory similar to open source software development. Because this only concerns the software available from the foundation, this does not need to be open to public governance. When the community at large wishes to release custom code outside the foundation, a user may use the factory to deploy their own factory offering their custom code. This new factory inherits the offerings of the parent factory and may add their own modules.

These pools form the foundation of the DAO. Autonomous and permissionless liquidity pools that act as the agreed upon foundation for DAO treasury management. From there, users may launch further liquidity pools that may accept the DAO’s Treasury Token for deposit. These form the Roundtables for managing ventures within the DAO. The Roundtables compartmentalize management teams, Councillors, of the various ventures being executed under a DAO’s mission statement. A Roundtable typically does not have it’s own governance token, instead using a Council Token to resolve disputes by executing buyout options.

From the Roundtables, any Councillor may use their contribution to the Roundtable to launch a bond offering for a Quest. Quests define the bounty award and terms for completing a task. The Councillor that issues the Quest puts their share of the treasury in escrow to fund it. The interest being earned from that underlying position is then split to fund the bounty, compound into that position, and to sell on the bond market. This ensures that Questors know the payment for work they deliver is secured. And protects the Councillor from failure to deliver; see Fig. 2 for outline.

<figure><img src="../.gitbook/assets/governance.png" alt=""><figcaption><p>FIGURE 2: DAOSYS Governance Structure: new pool with custom code (ie, Quests)</p></figcaption></figure>

##
