
In a folder of your choice, run mkdir my-upgradeable-contract && cd my-upgradeable-contract
Run npm init -y
Run npm install --save-dev hardhat
Run npm install @nomiclabs/hardhat-ethers @nomiclabs/hardhat-waffle @openzeppelin/contracts-upgradeable @openzeppelin/hardhat-upgrades
We will be verifying our contract on Etherscan! Run npm install @nomiclabs/hardhat-etherscan@3.0.1
We will be using dotenv to keep our project-wide environment variables safe and accessible! Run npm install dotenv
Run npx hardhat to initiate the Hardhat development environment - it will bring up some yes/no options, press Enter to select 'Create a sample project'
Press Enter to say yes to all of the options
You should now have a full sample Hardhat repo in your my-upgradeable-contract folder
Now let's delete some of the example stuff that we don't need!

In the contracts folder, delete Greeter.sol
In the scripts folder, delete sample-script.js
In the test folder, delete sample-test.js
Ok! We're almost there. We just need to add a couple of things to our hardhat.config.js.


In your project root folder, run npx hardhat run scripts/deployProxy.js --network rinkeby
Your terminal console will show the deployed proxy address. Plug this address into Rinkeby Etherscan.
If you go to the 'Contract' tab, you'll see this layout:
Rinkeby
