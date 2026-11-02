# What is Azure VNet or Virtual Network?

Imagine Azure is a giant city with millions of buildings (servers). Anyone could walk into any building, which would be chaos. A **Virtual Network (VNet)** is like our own private, fenced compound in that city. We decide:

- Who can enter
- Which of our buildings can talk to each other
- Which doors open to the outside world

Our virtual machines, databases, and apps live inside this compound and talk to each other privately.

## Where does a VNet live in Azure?

Think of Vnet as a set of nested boxes:

- **Azure account** → our whole account.
- **Subscription** → our billing and permission boundary. A VNet belongs to one subscription.
- **Resource Groups** → a folder that holds related things together. Your VNet sits in one.
- **Region (for example, South India)** → the physical location. A VNet lives in exactly one region and cannot stretch across two. To connect VNets in different regions, we use VNet peering.

```bash
Subscription → Resource Group → VNet (in one Region) → Subnets → your resources.
```

Address space is the total range of private IP addresses your compound owns. Example: `10.0.0.0/16`. Think of it as the “land” we bought. Subnet is a smaller section of that land. For example, `10.0.1.0/24` could be our web servers area and `10.0.2.0/24` our “database” area. We separate them so we can apply different rules to each.
