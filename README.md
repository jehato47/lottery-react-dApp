# Lottery Contract

This is a simple React app that allows users to interact with a smart contract on the Ethereum blockchain. The contract is a lottery where users can enter by sending Ether to the contract address, and a winner is picked at random by the contract manager.

## Installation

To run this app locally, you need to have Node.js and npm installed. Clone this repository, navigate to the project directory, and run the following command:

`npm install`


## Usage

To start the app, run the following command:

`npm start`


This will start the development server and open the app in your default browser.

### Interacting with the contract

The app allows you to interact with the contract by entering an amount of Ether you want to enter the lottery with, and picking a winner.

When you enter the amount of Ether, it will be sent to the contract address and you will be notified that you have been entered into the lottery. When the manager picks a winner, you will be notified if you won or not.

## Code documentation

### App Component

This is the main component of the app that handles the state and user interactions.

#### State

The state of the app is managed by the following variables:

- `manager`: the Ethereum address of the contract manager
- `players`: an array of Ethereum addresses of the players who entered the lottery
- `balance`: the balance of the contract in Ether
- `value`: the amount of Ether the user wants to enter the lottery with
- `message`: a message that is displayed to the user after an interaction with the contract

#### componentDidMount()

This function is called after the component mounts, and it retrieves the initial state of the contract from the blockchain. It retrieves the manager address, the list of players, and the balance of the contract.

#### onSubmit()

This function is called when the user submits the form to enter the lottery. It retrieves the user's Ethereum account, sends the entered amount of Ether to the contract address, and updates the state of the app with the new balance and a message that the user has been entered into the lottery.

#### onClick()

This function is called when the user clicks the button to pick a winner. It retrieves the user's Ethereum account and calls the `pickWinner()` function of the contract. It then updates the state of the app with a message that a winner has been picked.

