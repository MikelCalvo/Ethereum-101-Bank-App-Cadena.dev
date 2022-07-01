# 💰 MK Bank Project -> [https://mkbank.vercel.app/](https://mkbank.vercel.app/) 💰

Rinkeby ETH decentralized bank for storing your ETH.

This website is part of the course Ethereum 101 from [cadena.dev](https://cadena.dev)

## Screenshots

- Default Layout

![Deployer Layout](https://raw.githubusercontent.com/MikelCalvo/Ethereum-101-Bank-App-Cadena.dev/main/screenshots/main_lowres.png)

- Admin Layout

![Deployer Layout](https://raw.githubusercontent.com/MikelCalvo/Ethereum-101-Bank-App-Cadena.dev/main/screenshots/admin_lowres.png)

## Installation

Install dependencies with npm

```bash
  npm install
```

Create a .env file in the root directory with the following variables:

```
POKT_RINKEBY_URL=https://....
RINKEBY_PRIVATE_KEY=000000....
```

POKT_RINKEBY_URL is your [POKT Rinkeby app endpoint](https://mainnet.portal.pokt.network/#/).

RINKEBY_PRIVATE_KEY is your ETH private key to deploy the bank contract into rinkeby.

## Contract Compilation & Deployment

You can compile the bank contract using the following command:

```
npx hardhat compile
```

And then you have to deploy it to the Rinkeby network using:

```
npx hardhat run scripts/deploy.js --network rinkeby
```

You should see the following message as a result:

```
BankContract deployed to: 0x5AF770cB1928726B07573b688483B72eE11B144F
BankContract owner address: 0x7Ed4D8f4195da9993b66600F0f2DeA420FB42978
```

Copy the contract address and paste it into webapp/src/App.js:19

## Frontend Local Deployment

To create a local instance of the frontend, cd into webapp and use the following command

```
cd webapp
npm start
```

## go to [http://localhost:3000/](http://localhost:3000/) & you should see you decentralized bank.

by mikelcalvo.eth
