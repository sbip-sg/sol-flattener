# sol-flattener
Mimimal solidity flattener script. No dependencies. 

Most analysis tools require the file to be self-contained and compilable directly with `solc`. This helps flatten solidity file from 
project folder structure to a single file to be used for tools or to be uploaded to etherscan.

# Requirements: 

* Python 3

# Usage:
Normal project:

* `python flatten.py --path yourfile.sol `
* `python flatten.py --path yourfile.sol --output /temp/`

Hardhat + truffle projects: 
* Install npm dependencies
  *  `cd project_folder`
  * `npm install` or `yarn install`
* `python flatten.py --path project_folder/contracts/Contract.sol --include project_folder/node_modules`

Test the flattened sol file with the correct solc version : `solc Contract_flattened.sol --binary`
