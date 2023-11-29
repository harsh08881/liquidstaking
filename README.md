
# Liquid Staking Smart Contract

## Overview
This Solidity smart contract implements a liquid staking mechanism, allowing users to stake their tokens and earn rewards. It supports staking and unstaking functionalities with a specified staking duration.

## Features
- Staking: Users can stake their tokens by calling the stake function.
- Unstaking: Users can unstake their tokens and claim rewards after the staking period using the unstake function.
- Reward Calculation: Rewards are calculated based on a fixed annual interest rate.

## Contract Structure
- LiquidStaking contract is deployed with addresses of the staking and reward tokens.
- Staked balances and timestamps are tracked for each user.
- Staking duration is set to 30 days by default.

## Usage

### Deployment
Deploy the contract by providing the addresses of the staking and reward tokens.

solidity
// Example deployment
LiquidStaking myStakingContract = new LiquidStaking(stakingTokenAddress, rewardTokenAddress);


### Staking
Users can stake their tokens using the stake function.

solidity
// Example staking
uint256 amountToStake = 100; 
// Adjust the amount accordingly
myStakingContract.stake(amountToStake);


### Unstaking
Users can unstake their tokens and claim rewards after the staking period.

solidity
// Example unstaking
myStakingContract.unstake();


## Customization
- Adjust the staking duration and annual interest rate in the contract constructor and reward calculation function.

solidity
// Example customization
uint256 customStakingDuration = 60 days; 
// Change the staking duration to 60 days
uint256 customAnnualInterestRate = 10; 
// Change the annual interest rate to 10%
LiquidStaking myCustomStakingContract = new LiquidStaking(stakingTokenAddress, rewardTokenAddress, customStakingDuration, customAnnualInterestRate);


## License
This smart contract is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

Feel free to customize this template based on your specific project details and requirements.
