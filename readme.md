## Notice: This is a legacy repository and is no longer being supported.
If you have any questions or concerns, please contact XYO Network at **developer@xyo.network**. Please feel free to visit our ongoing projects at github.com/XYOracleNetwork. Thank you!
##

# Geo Node

![logo](https://raw.githubusercontent.com/GeoProof/geoproof.github.io/master/img/geo_3.png)

The code for a Node (a trusted device).

The Node provides the following functionality:

- Generate a private / public keypair, unique to each node
- Initialize itself with the backend, signing with the private key
- Act as a Bluetooth peripheral to receive verification requests from users. Sign messages using private key verifying presence of user at a certain timestamp.
- Communicate messages to backend

## Prerequisites
- npm
- Node.js

## Integrations

[Bleno](https://github.com/noble/bleno) - Act as Bluetooth peripheral

[Web3](https://github.com/ethereum/web3.js/) - Generate keypair

## Getting Started

1. Install requirements using `npm install`
1. Create the .env file: `cp .env.example .env`
1. Run using `node geo-node`

## Usage

Connect to the Geo Node by running the [Geo User Client](https://github.com/XYOracleNetwork/geo-user-client) on an iOS or Android device. Then, when in proximity of the device running Geo Node, the device will be discovered and you may connect to generate a signature.

Geo Node signs a message (using Web3) of the user's address, received via bluetooth, and the current timestamp in the form `address|timestamp`. Geo then sends the signature back to the user via bluetooth for the user to store.

Geo Node posts checkins to a [Geo Server](https://github.com/XYOracleNetwork/geo-server) running at the url specified in the `.env` file. This can be a server run by the user running the Geo Node.

<br><hr><br>
<p align="center">Made with  ❤️  by [<b>XY - The Persistent Company</b>] (https://xy.company)</p>
