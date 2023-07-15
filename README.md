<<<<<<< HEAD
# Getting Started

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You can check if the git is already installed in the system by running the command `git --version` and you see a response like `git version x.x.x`
- [foundry](https://getfoundry.sh/)
  - You can check if the foundry is already installed in the system by running the command `forge --version` and you see a response like `orge 0.2.0 (816e00b 2023-03-16T00:05:26.396218Z)`

## Quickstart

```
git clone https://github.com/edsondsouza/foundry-fund-me-f23.git
cd foundry-fund-me-f23
forge build
```

### Optional Gitpod

If you can't or don't want to run and install locally, you can work with this repo in Gitpod. If you do this, you can skip the `clone this repo` part.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/edsondsouza/foundry-fund-me-f23.git)

# Usage

Deploy:

```
forge script scripts/DeployFundMe.s.sol
```

## Usage

Deploy:

```
forge script scripts/DeployFundMe.s.sol
```

## Testing

If you want to run test just run
`forge test`

for unit testing

```
forge test --match-test testFunctionName
```

or if you've the URL

```
forge test --fork-url $SEPOLIA_RPC_URL
```

### Test Coverage

To check how much you cover tests

```
forge coverage
```

# Deployment to a testnet or mainnet

1. Setup environment variables
   You'll want to set your `SEPOLIA_RPC_URL` and `PRIVATE_KEY` as environment variables. You can add them to a `.env` file.

   - `PRIVATE_KEY`: The private key of your account (like from [metamask](https://metamask.io/)). NOTE: FOR DEVELOPMENT, PLEASE USE A KEY THAT DOESN'T HAVE ANY REAL FUNDS ASSOCIATED WITH IT.

     - You can [learn how to export it here](https://support.metamask.io/hc/en-us/articles/360015289632-How-to-Export-an-Account-Private-Key).

   - `SEPOLIA_RPC_URL`: This is url of the sepolia testnet node you're working with. You can get setup with one for free from [Alchemy](https://www.alchemy.com/)

Optionally, add your `ETHERSCAN_API_KEY` if you want to verify your contract on [Etherscan](https://etherscan.io/).

2. Get testnet ETH
   Head over to [faucets.chain.link](https://faucets.chain.link/) and get some testnet ETH. You should see the ETH show up in your metamask.

3. Deploy
   ```
   forge script script/DeployFundMe.s.sol --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast
   ```

and this is to directly verify on Etherscan

```
forge script script/DeployFundMe.s.sol --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify --etherscan-api-key $ETHERSCAN_API_KEY
```

## Scripts

After deploying to a testnet or local net, you can run the scripts.

Using cast deployed locally example:

```
cast send <FUNDME_CONTRACT_ADDRESS> "fund()" --value 0.1ether --private-key <PRIVATE_KEY>
```

or

```
forge script script/FundFundMe.s.sol --rpc-url sepolia  --private-key $PRIVATE_KEY  --broadcast
```

Withdraw

```
cast send <FUNDME_CONTRACT_ADDRESS> "withdraw()"  --private-key <PRIVATE_KEY>
```

## Estimate Gas

You can estimate how much gas is cost by running:

```
forge snapshot
```

And you'll see an output file called `.gas-snapshot`

# Connect with me ❤️

[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=for-the-badge&logo=Twitter&logoColor=white)](https://twitter.com/edsondsouza) [![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/dsouzaedson/) [![Hashnode](https://img.shields.io/badge/Hashnode-2962FF?style=for-the-badge&logo=hashnode&logoColor=white)](https://edsondsouza.hashnode.dev/)
=======
