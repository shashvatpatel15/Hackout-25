**Green Hydrogen Subsidy Portal - Judge's Guide**
Welcome to the Green Hydrogen Subsidy Portal, a blockchain-powered platform for transparent and automated subsidy disbursement. This guide provides the technical steps required to set up and demonstrate the application's core functionality.

Core Concept
This project uses a combination of a traditional web server with a database and a decentralized smart contract on the blockchain.

Web Application (Node.js & MySQL): Manages user accounts (Government, Producer, Auditor), roles, and provides the user interface.

Blockchain (Solidity & Sepolia Testnet): The smart contract acts as the ultimate source of truth. It securely holds the rules for vendor registration, progress tracking, and fund withdrawal, ensuring all actions are transparent and irreversible.

Required First Step: Create a Government Account
The system is designed with a secure, role-based architecture. To begin using the portal, a Government user must be created first, as only this role has the authority to register vendors and initiate the subsidy lifecycle.

Instructions:

Navigate to the main page of the application.

Click the "Sign Up" button.

In the sign-up form, enter your details and make sure to select the "Government" role from the dropdown menu.

Complete the sign-up process.

You can now log in as the Government user to access the main dashboard.

Demonstration Workflow
Once the Government account is created, you can proceed with the full demonstration flow:

Log in as Government: Access the dashboard.

Register a Vendor: Use the "Register New Vendor" button to create a producer account, link their wallet address, and set their production goals on the blockchain. Note: Each vendor's wallet address must be unique.

Update Progress: As the Government user, you can update a vendor's production progress. This action is recorded in the database and logged for auditing.

Log in as Producer: Log out and sign in using the producer's credentials. The producer can view their real-time progress toward the milestone.

Withdraw Subsidy: Once the production milestone is met, the status will change to "Payout Ready." The producer can then click "Withdraw Subsidy," which will trigger a real-time MetaMask transaction on the Sepolia testnet to transfer the funds.

Audit the Trail: Finally, log in as an Auditor. The audit dashboard provides a complete, time-stamped log of all major events, including vendor registrations and progress updates, showcasing the system's transparency.

Technical Setup Overview
For a complete local setup, the following components are required:

Node.js Environment: To run the backend server.

MySQL Database: To store user and off-chain project data.

.env File: A configuration file in the project root is needed to store the database URL and the blockchain connection details (RPC URL, Private Key of the contract owner, and the deployed Contract Address).

*Sepolia Testnet: The SubsidyAutomator.sol smart contract is deployed on this public test network.*

*MetaMask: The browser extension is required for producers to interact with the smart contract and withdraw their funds.*

***Developed by Team: Error 404***
