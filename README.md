# Lottery_smart_contract
This is a lottery smart contract deployed on blockchain using solidity

**Description-**
This is a simple lottery smart contract written in Solidity. It allows users to participate in a lottery by sending ETH to the contract. A manager, who is the person deploying the contract, can randomly select a winner from the participants and transfer the entire balance of the contract to the winner.

**Features-**
- Lottery Participation: Users can join the lottery by sending ETH to the contract.
- Manager Role: The manager, who deployed the contract, can pick a winner.
- Random Winner Selection: The winner is selected randomly from the participants.

**Contract Details-**
- _State Variables:_
  - address payable[] public players: A dynamic array to store the addresses of the participants.
  - address public manager: The address of the manager who deployed the contract.

- _Constructor:_
  - Initializes the manager to the address deploying the contract.

- _Functions:_
  - receive() external payable: Allows the contract to receive ETH.
  - getBalance() public view returns (uint): Returns the current balance of the contract.
  - random() private view returns (uint): Generates a pseudo-random number.
  - pickWinner() public: Allows the manager to pick a winner and transfer the funds.
  - getPlayers() public view returns (address payable[]): Returns the list of participants.
 
**Usage-**
1. Deploy the contract to a blockchain network (e.g., Ethereum).
2. Users can participate by sending ETH to the contract address.
3. The manager can call the pickWinner() function to randomly select a winner.

**Prerequisites-**
- Solidity version >=0.5.0 <0.9.0.
- Ethereum wallet (e.g., MetaMask) for deploying and interacting with the contract.

**Security Considerations-**
- Ensure only the manager can call the pickWinner() function to prevent unauthorized access.
- The random function is not truly random; it is vulnerable to manipulation in a real-world scenario.




  
