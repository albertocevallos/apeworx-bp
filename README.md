# ApeWorx Boilerplate

## Installation

Install Dependencies

- [python3](https://www.python.org/downloads) - version 3.7 or greater
- Node.js, NPM, and Hardhat. See Hardhat's [installation](https://hardhat.org/getting-started/#installation) documentation for steps.

Note: Make sure hardhat is installed locally in the working directory. Run `npx hardhat` at the end of the installation and select `Create an empty hardhat.config.js`.

Setup virtual env:

```bash
python3 -m venv venv
source venv/bin/activate
```

Setup plugins:

```bash
ape plugins list -a
ape plugins install solidity vyper hardhat infura alchemy
```

Setup environment variables (where applicable):

```bash
export WEB3_INFURA_PROJECT_ID={YOUR_INFURA_PROJECT_ID}

export WEB3_ALCHEMY_API_KEY={YOUR_ALCHEMY_KEY}
```

Visit [infura](https://infura.io/) to get your free key.

# Console Usage

To interact with a deployed contract in a local environment, start by opening the console:

```bash
ape console --network :mainnet-fork:hardhat
```

# Testing

All tests must be stored under `tests/`. Each test must start with `test_` and end with the `.py` extension.

```bash
ape test
```

To test a particular contract use:

````bash
ape test test_my_contract
```

Additionally you can use `-I` to open interactive mode and `-s` to print logs.

```bash
ape test test_my_contract -I -s
````

# Deployments

To run a file in `scripts/` use:

```bash
ape run 1_deploy
```

# Additional info

The ApeWorx folder structure is generally:

```
project              # The root project directory
├── contracts/       # Project source files, such as '.sol' or '.vy' files
├── tests/           # Project tests, ran using the 'ape test' command
├── scripts/         # Project scripts, such as deploy scripts, ran using the 'ape run <name>' command
└── ape-config.yaml  # The ape project configuration file
```
