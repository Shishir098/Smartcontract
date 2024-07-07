SmartContract
This Solidity smart contract is a simple example demonstrating the use of require, assert, and revert statements to handle various conditions and errors.

Contract Overview
The SmartContract contract has the following functionalities:

Set a value with a requirement check.
Set a value with an assertion check.
Withdraw the current value with a revert condition.
Functions
setValueWithRequirement
solidity

function setValueWithRequirement(uint _value) external
Description: Sets the value state variable to the provided _value if _value is greater than zero. If _value is zero or less, the transaction is reverted with an error message "Value must be greater than zero."
Parameters:
uint _value: The new value to set. Must be greater than zero.
Usage:
solidity
contractInstance.setValueWithRequirement(10);
setValueWithAssertion
solidity
function setValueWithAssertion(uint _newValue) external
Description: Attempts to set the value state variable to _newValue only if the difference between _newValue and the current value is greater than zero and equal to the current value. If this assertion fails, the transaction is reverted.
Parameters:
uint _newValue: The new value to set. The difference between _newValue and the current value must be greater than zero and equal to the current value.
Usage:
solidity
contractInstance.setValueWithAssertion(20);
withdrawWithRevert
solidity
function withdrawWithRevert() external
Description: Attempts to withdraw the current value. It first sets amount to the current value, then resets value to zero. If amount is zero, it reverts the transaction with the error message "Withdraw reverted. Amount is Zero."
Usage:
solidity
contractInstance.withdrawWithRevert();
Deployment
Ensure you have Solidity and a suitable development environment installed (e.g., Remix, Truffle, or Hardhat).
Compile the SmartContract contract.
Deploy the contract to your desired Ethereum network.
Interact with the deployed contract using the provided functions.
Example
Here's an example of how to interact with the contract using Remix:

Open Remix and create a new file named SmartContract.sol.
Compile the contract.
Deploy the contract.
Use the deployed contract instance to call setValueWithRequirement, setValueWithAssertion, and withdrawWithRevert functions.

Author
Shishir gautam

GitHub: https://github.com/Shishir098 
Email: shishirgautam12345@gmail.com
License
This project is licensed under the MIT License.
