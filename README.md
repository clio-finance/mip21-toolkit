# Equipment for MIP21: Off-chain Asset Backed Lending in MakerDAO

## Components

- `RwaLiquidationOracle`: acts as a liquidation beacon for an off-chain enforcer.
- `RwaUrn`: facilitates borrowing of DAI, delivering to a designated account.
- `RwaOutputConduit`: disburses DAI 
- `RwaInputConduit`: repays DAI
- `RwaToken`: represents the RWA collateral in the system

## Spells

**⚠️*ATTENTION:** Spells are being moved to the [`ces-spells-goerli` repo](https://github.com/clio-finance/ces-spells-goerli/tree/master/template/rwa-onboarding), once the migration is completed, these files are going to be removed.

The following can be found in `src/RwaSpell.sol`:
- `RwaSpell`: which deploys and configures the RWA collateral in MakerDAO in accordance with MIP21 

The following can be found in `src/test/RwaSpell.t.sol`:

- `TellSpell`: which allows MakerDAO governance to initiate liquidation proceedings.
- `CureSpell`: which allows MakerDAO governance to dismiss liquidation proceedings.
- `CullSpell`: which allows MakerDAO governance to write off a loan which was in liquidation.

## Deploy

### kovan
```
make deploy-kovan
```

### goerli
```
make deploy-goerli
```

### mainnet
```
make deploy-mainnet
```