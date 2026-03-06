# Nowa Chain

**Nowa** is an EVM-compatible Cosmos chain — built for developers who want the full power of Ethereum tooling with the interoperability and modularity of the Cosmos ecosystem.

Nowa runs on [Cosmos EVM](https://evm.cosmos.network/), giving it native EVM compatibility out of the box: Solidity smart contracts, Ethereum JSON-RPC, MetaMask support, and access to the entire Ethereum developer ecosystem — all while being a fully sovereign Cosmos SDK chain.

---

## What is Nowa?

Nowa is a Cosmos chain with full EVM support. It combines:

- **Ethereum compatibility** — Deploy any Solidity contract without modification. Connect any EVM wallet, use any Ethereum dev tool.
- **Cosmos interoperability** — Native IBC support for cross-chain asset transfers and messaging.
- **Native token: NOWA** — The chain's native staking and gas token, denominated as `anowa` at the base level (18 decimals, EVM-native).

Nowa is forward-compatible with Ethereum: it runs every valid Ethereum transaction, and adds features that go beyond what standard Ethereum offers.

---

## Features

- **EVM Smart Contracts** — Full Solidity support. Deploy and interact with contracts exactly as you would on Ethereum.
- **Ethereum JSON-RPC** — Compatible with MetaMask, Rabby, Blockscout, Hardhat, Foundry, and more.
- **IBC Integration** — Use any IBC asset inside the EVM via precompiles and extensions.
- **ERC-20 Module** — Native alignment between IBC assets and ERC-20 tokens for a seamless UX.
- **EIP-1559 Fee Market** — Self-regulating fee mechanism with configurable surge management.
- **EIP-712 Signing** — Sign Cosmos SDK messages with EVM wallets like MetaMask.
- **Governance-controlled** — All modules are controllable via on-chain governance.
- **Permissioned EVM** *(optional)* — Whitelist or blacklist addresses for contract interaction.

---

## Native Token

| Property | Value |
|---|---|
| Name | Nowa Token |
| Symbol | NOWA |
| Base denom | `anowa` |
| Alias | `attonowa` |
| Exponent | 18 |
| ERC-20 address | `0xEeeeeEeeeEeEeeEeEeEeeEEEeeeeEeeeeeeeEEeE` |

---

## Getting Started

### Run a local node

From the root of the repository:

```bash
./local_node.sh
```

This spins up a local Nowa chain with funded dev accounts (`dev0`–`dev3`) and a validator ready to go.

**Options:**

```
-y                       Overwrite existing chain data without prompt
-n                       Keep existing chain data and resume
--no-install             Skip 'make install'
--remote-debugging       Build without optimizations (for debuggers)
--additional-users N     Generate N extra funded accounts (dev4, dev5, ...)
--mnemonic-file PATH     Path to write generated mnemonics YAML
--mnemonics-input PATH   Provide custom dev mnemonics from a YAML file
```

### Migrations

Upgrade guides for moving between versions are available in [`./docs/migrations`](./docs/migrations).

---

## Testing

All test commands are available via `make`. From the root of the repository:

```bash
# Unit tests
make test-unit

# Unit tests with coverage report
make test-unit-cover

# Fuzz tests
make test-fuzz

# Solidity contract tests
make test-solidity

# Benchmarks
make benchmark
```

---

## Documentation & Resources

- **Official Cosmos EVM docs**: [evm.cosmos.network](https://evm.cosmos.network/)
- **Ethereum JSON-RPC reference**: [cosmos-docs.mintlify.app](https://cosmos-docs.mintlify.app/docs/api-reference/ethereum-json-rpc)
- **Cosmos SDK**: [github.com/cosmos/cosmos-sdk](https://github.com/cosmos/cosmos-sdk)
- **IBC**: [github.com/cosmos/ibc-go](https://github.com/cosmos/ibc-go)
- **CometBFT**: [github.com/cometbft/cometbft](https://github.com/cometbft/cometbft)

---

## Contributing

Contributions and discussions are welcome. See the [contributing guide](./CONTRIBUTING.md) to get started.

---

## License

Apache 2.0. Nowa is built on [Cosmos EVM](https://github.com/cosmos/evm), a fork of [evmOS](https://github.com/evmos/OS), originally developed by Tharsis with funding from the Interchain Foundation.