# Capstone_Project: Revitalizing Capstone Research & Investment Company's Trading System

# Leverage Advanced AI Models for Enhanced Crypto Trading Success

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Intorduction](#introduction)
3. [Getting Started](#getting-started)
   - [Step 1: Setting Up Exchange](#step-1-setting-up-exchange)
   - [Step 2: Connecting to the Bot](#step-2-connecting-to-the-bot)
   - [Step 3: Configuring the Bot](#step-3-configuring-the-bot)
4. [Key Features](#key-features)
   - [Exchange Integration](#exchange-integration)
   - [User-Friendly Setup](#user-friendly-setup)
   - [Advanced Trading Configuration](#advanced-trading-configuration)
5. [Streamlit Application](https://github.com/TFITZ57/Capstone_Project/tree/main/streamlit)
6. [Benefits](#benefits)
   - [Efficiency](#efficiency)
   - [Accuracy](#accuracy)
   - [Security](#security)
   - [Risk Management](#risk-management)
7. [Support and Documentation](#support-and-documentation)
8. [On-Chain vs Off-Chain](#on-chain-vs-off-chain)
9. [Smart Contracts Explained](#smart-contracts-explained)
   - [TradingPlatform](#tradingplatform)
   - [TradingBot](#tradingbot)
   - [BotFactory](#botfactory)  
10. [Cryptocurrency Trading Process Flow](#cryptocurrency-trading-process-flow)
11. [Detailed Project Plan](#detailed-project-plan)
- [Project Overview](#project-overview)
- [Project Timeline](#project-timeline)
- [Project Team Roles](#project-team-roles)
- [Detailed Tasks and Team Allocation](#detailed-tasks-and-team-allocation)
- [Updated Resource Allocation](#updated-resource-allocation)
- [Time Distribution](#time-distribution)

## Executive Summary

The Crypto Trading Algo Bot is an advanced automated trading tool designed to streamline and enhance your cryptocurrency trading experience. Leveraging sophisticated algorithmic trading models, this bot allows users to efficiently manage trades and maximize returns while minimizing risk.

## Visual of what this model looks like
![image](https://github.com/TFITZ57/Capstone_Project/assets/154120290/cea07618-a6d8-48ba-8db1-382614e4ec78)

## Introduction
### Capstone Research & Investment Company: Challenges and Solutions

Capstone Research & Investment Company is facing significant challenges in the cryptocurrency trading market, marked by a decline in market share and increased competition. 

To address these challenges, Capstone Research has tasked its Technology Team with the development and advancement of an innovative trading system to regain its competitive edge and improve market positioning.

### Objective

Outline a plan to develop an integrated trading system that leverages AI and ML to improve trading success, increase market share, and minimize risk.

#### Targets / Key Performance Indicators

- Increase trading success rate by 20%.
- Reduce trading risk by 15%.
- Improve overall system performance and reliability.

#### Outcome

##### Integrated System
Development of a comprehensive trading system that utilizes a multi-layer perceptron (MLP) model, trained on every USDT market pair offered by the Binance Exchange.

#### Key Components

- **MLP Model:**
  - Provides advanced predictive signals for a broad range of assets and market trends.

- **ALGO Bot:**
  - Executes trades on both centralized and decentralized exchanges.


## Getting Started

---

### Step 1: Setting Up Exchange

1. Utilize platforms like Uniswap to set up and manage exchanges.
2. Select the list of coins you wish to trade and ensure they are supported on the exchange.

### Step 2: Connecting to the Bot

1. Obtain the bot's unique address.
2. Link your user address to the bot for secure fund deposits.
3. Transfer the desired amount of cryptocurrency to your user address.

### Step 3: Configuring the Bot

1. Decide whether to keep the bot idle initially to scan market data.
2. Configure the bot to detect buy, sell, and hold signals using the algorithmic trading model.
3. Set the position size and ensure the bot operates within a 3% risk tolerance parameter.

## Key Features

### Exchange Integration

- Seamlessly integrates with platforms like Uniswap to create and manage exchanges.
- Supports a diverse list of tradable coins, ensuring broad market access.

### User-Friendly Setup

- Provides a straightforward process to connect the user's address to the bot.
- Facilitates easy deposit of funds, ensuring quick and secure transaction processing.

### Advanced Trading Configuration

- Allows the bot to operate in an idle state initially, enabling comprehensive market data analysis.
- Utilizes a powerful algorithmic trading model to generate precise buy, sell, and hold signals.

## Benefits

### Efficiency

- Automates trading processes, reducing the need for constant manual monitoring.

### Accuracy

- Employs advanced algorithms to make data-driven trading decisions.

### Security

- Ensures secure fund management through a robust connection setup between the user and the bot.

### Risk Management

- Maintains strict risk parameters to protect against significant losses.

## Support and Documentation

For detailed instructions and troubleshooting, please refer to the provided documentation or contact support.

## On-Chain vs Off-Chain

### On-Chain

1. **Definition**: Transactions occur on the blockchain and are recorded on the public ledger.
2. **Transparency and Security**: High levels of transparency and security due to blockchain verification.
3. **Immutable Records**: Transactions are immutable once confirmed.
4. **Cost and Speed**: Typically slower and more expensive due to network consensus and fees.
5. **Examples**: Bitcoin transactions, Ethereum smart contracts.

### Off-Chain

1. **Definition**: Transactions occur outside the blockchain, recorded in databases or through agreements.
2. **Speed and Cost**: Faster and cheaper, without needing blockchain consensus.
3. **Privacy**: Offers more privacy as transactions are not publicly recorded.
4. **Trust and Security**: Relies on trust between parties or intermediaries.
5. **Examples**: Lightning Network, centralized exchange transactions.

## Smart Contracts Explained

### TradingPlatform

The `TradingPlatform` contract manages user deposits, preferences, and interactions with bot contracts. It provides functions for:

- Adding bot contracts.
- Connecting user wallets.
- Depositing and withdrawing funds.
- Setting trading preferences.
- Executing trades via bot contracts.
- Collecting fees by the contract owner.

This modular approach allows for scalable and flexible trading operations, enabling easy addition of new bot contracts and user-specific trading configurations.

#### State Variables:

- `owner`: Address of the contract owner.
- `usdt`: Instance of the USDT token.
- `feePercentage`: Fee percentage for using the platform (default is 1%).
- `User`: Struct to store user preferences and balances.
- `users`: Mapping from user address to User struct.
- `bots`: Array of addresses of bot contracts.

#### Events:

- `Deposit`: Emitted when a user deposits funds.
- `Withdraw`: Emitted when a user withdraws funds.
- `TradeExecuted`: Emitted when a trade is executed.

#### Modifiers:

- `onlyOwner`: Restricts function access to the contract owner.

#### Constructor:

- Initializes the contract with the USDT token address and sets the contract owner.

#### Functions:

1. **addBot**:

   - Adds a new bot contract to the platform.
   - Function Signature: `function addBot(address bot) external onlyOwner`

2. **connectWallet**:

   - Marks a user’s wallet as active, allowing them to interact with the platform.
   - Function Signature: `function connectWallet() external`

3. **deposit**:

   - Allows users to deposit funds (either USDT or a specific coin) into the platform.
   - Function Signature: `function deposit(uint amount, bool isUSDT) external`

4. **setPreferences**:

   - Allows users to set their trading preferences.
   - Function Signature: `function setPreferences(address coin, uint maxPositionSize, uint riskTolerance, uint stopLoss) external`

5. **executeTrade**:

   - Executes a trade using a specified bot.
   - Function Signature: `function executeTrade(address bot, string calldata action, uint amount) external`

6. **isBot**:

   - Checks if an address is a valid bot contract (internal function).
   - Function Signature: `function isBot(address bot) internal view returns (bool)`

7. **withdraw**:

   - Allows users to withdraw their funds (either USDT or a specific coin) from the platform.
   - Function Signature: `function withdraw(uint amount, bool isUSDT) external`

8. **collectFees**:

   - Allows the owner to collect fees from the contract.
   - Function Signature: `function collectFees() external onlyOwner`

9. **receive**:
   - Allows the contract to receive Ether.
   - Function Signature: `receive() external payable`

### TradingBot

The `TradingBot` contract interacts with the Uniswap router to execute buy and sell trades based on the user’s preferences stored in the main TradingPlatform contract. The contract includes the following functions:

1. **Constructor**:

   - Initializes the contract with the Uniswap router and the main trading platform contract addresses.

2. **executeTrade**:

   - Executes a trade based on the provided action (“buy” or “sell”) and amount.

3. **buy**:

   - Executes a buy trade on Uniswap.

4. **sell**:

   - Executes a sell trade on Uniswap.

5. **receive**:
   - Allows the contract to receive Ether.

This structure allows for a modular and scalable trading system where new bots can be added independently, each implementing their own trading logic.

### BotFactory

The `BotFactory` contract allows for the dynamic creation of TradingBot instances. This factory pattern enables the scalable deployment and management of multiple trading bots. The contract includes:

#### State Variables:

- `owner`: The owner of the factory contract.
- `router`: The Uniswap router address.
- `platform`: The main trading platform contract address.

#### Events:

- `BotCreated`: Emitted when a new bot instance is created.

#### Modifiers:

- `onlyOwner`: Ensures only the owner can call certain functions.

#### Constructor:

- Initializes the contract with the router and platform addresses and sets the owner.

#### Functions:

1. **createBot**:
   - Creates a new TradingBot instance and emits the BotCreated event.

This factory pattern is beneficial for managing multiple instances of trading bots, making the system modular and scalable.
## Cryptocurrency Trading Process Flow
![diagram (1)](https://github.com/TFITZ57/Capstone_Project/assets/154120290/503ada65-8178-4cee-be60-d11fae74ed08)

# Cryptocurrency Trading Process Flow

This repository details the process of developing and deploying a cryptocurrency trading model using machine learning.

## Components
- **Colab_MLP Model**
- **ALGO Bot**
- **User Interface**
- **Simulations (Strategy Results)**

## Detailed Flow of the Process

### 1. Colab_MLP Model

#### a. Data Ingestion
- **Sources:** Collect data from blockchain activity, market data, etc.
- **Storage:** Securely store data and ensure accessibility.

#### b. Data Preprocessing
- **Cleaning:** Handle missing values, remove noise, correct inconsistencies.
- **Normalization:** Scale data for consistent input.
- **SMOTE:** Balance the dataset by oversampling the minority class.
- **Random Undersampling and Oversampling.**
  
### Balanced Distribution 
![class_distributions_balanced](https://github.com/TFITZ57/Capstone_Project/assets/154120290/4b723b4e-0ce5-45eb-a914-d6a50bde3afb)
### Initial Distribution of Classes 
![class_distributions_initial](https://github.com/TFITZ57/Capstone_Project/assets/154120290/c48bd34c-0257-4c55-8af7-cc172ceefe48)

#### c. Feature Engineering
- **Creation:** Generate new features to improve model performance.
- **Selection:** Choose relevant features to reduce dimensionality and improve efficiency.

#### d. Hyperparameter Tuning
- **Hyperband:** Efficient hyperparameter optimization.
- **RandomSearch:** Explore a wide range of hyperparameter settings.
- **Bayesian Optimization:** Fine-tune an existing model.

#### e. Model Training
- **Architecture:** Build the model using the best hyperparameters.
- **Training:** Train on the entire dataset to learn patterns.
- **Validation:** Validate model performance with a separate dataset.
- **Cross-Validation:** Use strategies like k-fold to ensure robustness.

#### f. Model Evaluation
- **Metrics:** Evaluate using accuracy, precision, recall, F1 score.
- **Visualization:** Use classification reports, confusion matrix, ROC curve, and AUC score.

#### g. Prediction
- **Labeling Algorithm:** Calculate buy, sell, hold labels based on returns.
- **Softmax Activation:** Generate probabilistic outcomes.
- **Actionable Predictions:** Output predictions for buy (1), sell (2), hold (0).

#### h. Integration with ALGO Bot
- **Automated Trade Commands:** Feed predictions into the algorithm to trigger actions.

### 2. User Interface

#### a. User Interaction
- **Wallet Connection:** Enable deposits and interactions.
- **Preferences:** Set trading preferences and strategies.
- **Results View:** Display trading results and performance metrics.

#### b. Alerts
- **Notifications:** Alert users of buy, sell, or hold positions.

#### c. Feedback Loop
- **User Feedback:** Collect feedback to improve system performance.

### 3. ALGO Bot

#### a. Trade Execution
- **Execution:** Execute trades based on Colab_MLP Model predictions.

#### b. Integration with Exchanges
- **Interfaces:** Connect with centralized and decentralized exchanges.

### 4. Simulations (Strategy Results)

#### a. User Interaction
- **Preferences:** Set simulation parameters and view results.

#### b. Strategy Testing
- **Simulations:** Test different trading strategies using historical data.

#### c. Results Visualization
- **Visualization:** Display potential profits and losses from simulations.

## Visual Flow Chart Explanation

1. **Data Ingestion:** Collect data from various sources.
2. **Data Preprocessing:** Clean, normalize, and prepare data.
3. **Feature Engineering:** Create and select features.
4. **Hyperparameter Tuning:** Optimize model parameters.
5. **Model Training:** Train and validate the model.
6. **Model Evaluation:** Evaluate performance with metrics and visualizations.
7. **Prediction:** Generate actionable predictions.
8. **Output to ALGO Bot:** Send predictions to ALGO Bot for trade execution.
9. **User Interface:** Enable user interaction, wallet connection, and result viewing.
10. **Alerts:** Notify users of trading actions.
11. **Feedback Loop:** Collect user feedback.
12. **ALGO Bot:** Execute trades and connect with exchanges.
13. **Simulations:** Run strategy tests using historical data.
14. **Strategy Testing:** Evaluate different strategies.
15. **Results Visualization:** Display simulation results showing potential profits and losses.

## Detailed Project Plan

### Project Overview

**Project Title**: Cryptocurrency Trading Algorithm Model with Smart Contracts and Streamlit Integration

**Project Timeline**: June 3, 2024 - June 17, 2024

**Project Manager**: Randy Smith

### Project Team Roles

- **Data Scientists**: Tyler Fitzgerald, Antonio Papatzikos
- **NLP Specialists**: Ingrid Bendahan, Stephen Anderson
- **Software Developers**: Josue Vega, Victor Ordaz
- **Graphic Designer**: Diana Wang

### Detailed Tasks and Team Allocation

_All phases will be worked on concurrently. Each member will have a speaking part during the presentation. Phases are not dependent._

#### Data Sources

- Enterprise student plan: [Coinmetrics API](https://coinmetrics.io/api-v4/)

#### Phase 1: Model Completion (June 3 - June 5)

- **Debugging** (June 3 - June 4)
  - Ensure the trading model runs without errors.
  - Assigned to: Data Scientist 1, Data Scientist 2
- **Training Cycle** (June 4 - June 5)
  - Run additional training cycles to refine the model.
  - Assigned to: Data Scientist 1, Data Scientist 2
- **Validation** (June 5)
  - Validate the model using test data to ensure accuracy.
  - Assigned to: Data Scientist 1, Data Scientist 2
- **Results Analysis** (June 5)
  - Analyze the results from the validation phase.
  - Assigned to: Data Scientist 1, Data Scientist 2

#### Phase 2: Smart Contract Development (June 6 - June 10)

- **Develop Basic Smart Contracts** (June 6 - June 7)
  - Create a basic structure for the smart contracts.
  - Assigned to: Software Developer 1
- **Integrate Bot with Smart Contracts** (June 7 - June 8)
  - Connect the bot with the basic smart contracts.
  - Assigned to: Software Developer 1
- **Exchange Interaction** (June 8 - June 9)
  - Ensure the bot can interact with the exchange via the smart contracts.
  - Assigned to: Software Developer 2
- **Define Bot Logic** (June 9)
  - Outline the input, output, and execution logic for the bot.
  - Assigned to: Software Developer 2
- **Develop Variables and Functions** (June 10)
  - Create the necessary variables and functions for the smart contracts.
  - Assigned to: Software Developer 1, Software Developer 2

#### Phase 3: Streamlit Construction (June 11 - June 12)

- **Design User Interface** (June 11)
  - Design the user interface for the Streamlit app.
  - Assigned to: Software Developer 2, Graphic Designer
- **Develop Streamlit Code** (June 11 - June 12)
  - Code the Streamlit app to interact with the model and smart contracts.
  - Assigned to: Software Developer 2

#### Phase 4: Presentation Preparation (June 13 - June 14)

- **Define Presentation Purpose** (June 13 - June 14)
  - Outline the key points and purpose of the project presentation.
  - Assigned to: Project Manager
- **Create Slide Deck** (June 13 - June 14)
  - Design and structure the slides for the presentation.
  - Assigned to: Graphic Designer

#### Phase 5: GitHub Report/Update (June 15 - June 17)

- **Draft Comprehensive Report** (June 15 - June 16)
  - Write a detailed report covering all aspects of the project.
  - Assigned to: Project Manager, NLP Specialist 1, NLP Specialist 2
- **Update GitHub Repository** (June 15 - June 17)
  - Add the report, code, and any additional documentation to the GitHub repository.
  - Assigned to: Project Manager, NLP Specialist 1, NLP Specialist 2
- **Final Review and Edits** (June 16 - June 17)
  - Review all deliverables and make final edits.
  - Assigned to: All team members

### Updated Resource Allocation

| Resource            | Allocation (%) |
| ------------------- | -------------- |
| Project Manager     | 12.5           |
| Data Scientists     | 25             |
| NLP Specialists     | 25             |
| Software Developers | 25             |
| Graphic Designer    | 12.5           |

### Time Distribution

| Phase                      | Days |
| -------------------------- | ---- |
| Model Completion           | 3    |
| Smart Contract Development | 5    |
| Streamlit Construction     | 2    |
| Presentation Preparation   | 2    |
| GitHub Report/Update       | 3    |

### Project 3: Cryptocurrency Trading Algorithm Model Proposal: https://docs.google.com/document/d/1FoKmY_MA145YLXBN9Ot4ItV62mT_-kewTpmTO9eXahc/edit#heading=h.z5z7j71mgzxq
