# Building-on-Avalanche---ETH-AVAX
# Description
For this project, you will write a smart contract to create your own ERC20 token and deploy it using HardHat or Remix. Once deployed, you should be able to interact with it for your walk-through video. From your chosen tool, the contract owner should be able to mint tokens to a provided address and any user should be able to burn and transfer tokens.
# Executing the Program
Avalanche HyperSDK Project: Create a Custom Subnet Description: In the previous section, we learned about pre-built subnets that can be deployed and interacted with. However, these templates may not always fit our specific use case. This is where the HyperSDK comes in.

The HyperSDK provides the ability to create a custom virtual machine, which offers complete control over a custom blockchain. With the HyperSDK, you can design a blockchain that perfectly suits your needs, such as creating and transferring tokens or implementing a traditional order book for asset trading. This level of customization provides a powerful tool for businesses and organizations seeking a tailored solution.

By using the HyperSDK, you have full control over the rules and functionality of your chain, allowing you to create a custom blockchain that is tailored to your startup's specific needs. This offers an unparalleled level of control and flexibility, making it a valuable tool for organizations seeking a custom solution.

This level of control allows your startup to create a unique solution that meets the needs of your users and provides a competitive edge in the market.

Challenge: Your startup has identified a need to create a custom virtual machine to enable users to mint and transfer tokens. The HyperSDK provides a powerful solution for this task by allowing you to build a custom blockchain tailored to your specific needs. With the HyperSDK, you can define the rules and functionality of your chain, including the ability to create and transfer tokens and manage order books for trading assets.
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import"@openzeppelin/contracts/access/Ownable.sol";
contract MyToken is ERC20, Ownable {

    mapping(uint256 => uint256) public productPrices;
    mapping(address => uint256) public userInventory;

    constructor() ERC20("MyToken", "MTK") Ownable(msg.sender) {
        productPrices[1] = 400;
        productPrices[2] = 350;
        productPrices[3] = 250;
        productPrices[4] = 50;
    }

  # Author 
  Timothy Macalalad MetaCrafters
  # License
  This project is licensed under the MIT License
