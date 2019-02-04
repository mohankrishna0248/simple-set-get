# simple-set-get

Photo Contract
Simple sample project based on Truffle's react-app project to practice blockchain dev.

Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

Installation
Install Truffle globally.

npm install -g truffle
Download the box. This also takes care of installing the necessary dependencies.

truffle unbox react
Run the development console.

truffle develop
3.1 Optionally log chain details in new terminal tab using: javascript truffle develop --log

Compile and migrate the smart contracts. Note inside the development console we don't preface commands with truffle.

compile
migrate
Run the webpack server for front-end hot reloading (outside the development console). Smart contract changes must be manually recompiled and migrated.

// Serves the front-end on http://localhost:3000
npm run start
Truffle can run tests written in Solidity or JavaScript against your smart contracts. Note the command varies slightly if you're in or outside of the development console.

// If inside the development console.
test

// If outside the development console..
truffle test
Jest is included for testing React components. Compile your contracts before running Jest, or you may receive some file not found errors.

// Run Jest outside of the development console for front-end component tests.
npm run test
To build the application for production, use the build command. A production build will be in the build_webpack folder.

npm run build
Console Commands
PhotoContract.deployed().then(function(instance) {app = instance; })

var photoEvent = app.addedPhotoEvent({}, {fromBlock: 0,toBlock: 'latest'}).watch(function(error, event) {console.log(event);})
