# Security

# Contracts

All contracts are immutable and not upgradable!

# Balancer Contracts
Balancer V2 uses an authorization mechanism which allows fine grained access control on a function level. At its core is the  contract which manages access to all protected function calls. 

## Default admin role

The default admin role does not give permission to execute any protected function but allows granting or revoking roles to other entities (or himself).

## Execution roles

All entities which are granted the default admin role can grant and revoke execution roles on a function level. For singleton contracts like the Vault, all roles granted on it are bound to its contract address. So if we would deploy another Vault contract, roles granted on the 'old' Vault would not apply on the new one. For contracts deployed via a factory like the pools, roles are bound to all pools created by the same factory address. So if a role is granted on a StablePool created by the StablePoolFactory contract, then the role applies to all other StablePools created by this factory. It's bound to the StablePoolFactory address. So if we were to deploy another StablePoolFactory, pools created by it would not share the same access roles.

Currently, all roles are only granted to the Balancer Admin Multisig.

# Audits

Embr uses Balancer V2 contracts verbatim, which have completed [several full audits](https://docs.balancer.fi/core-concepts/security/audits) and have a comprehensive [bug bounty](https://docs.balancer.fi/core-concepts/security/bug-bounties) program.

We created a script which compares all deployed contracts from beethovenx against balancer. Make sure to enter your ftmscan & etherscan api keys