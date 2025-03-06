## Crowdfunding Project

This project is a decentralized crowdfunding platform built on Ethereum using Solidity smart contracts.

### Contract Details

The main contract is `CrowdFunding.sol`, which allows users to create and donate to campaigns.

#### Campaign Structure

```solidity
struct Campaign {
    address owner;
    string title;
    string description;
    uint256 target;
    uint256 deadline;
    uint256 amountCollected;
    string image;
    address[] donators;
    uint256[] donations;
}
```

#### Functions

- `createCampaign(address _owner, string memory _title, string memory _description, uint256 _target, uint256 _deadline, string memory _image)`: Creates a new campaign.
- `donateToCampaign(uint256 _id)`: Allows users to donate to a campaign.
- `getDonators(uint256 _id)`: Returns the list of donators and their donations for a campaign.
- `getCampaigns()`: Returns all campaigns.

### Setup Instructions

1. Clone the repository:
    ```sh
    git clone https://github.com/your-repo/CrowdFunding.git
    ```

2. Navigate to the project directory:
    ```sh
    cd CrowdFunding/web3
    ```

3. Install dependencies:
    ```sh
    npm install
    ```

4. Compile the smart contracts:
    ```sh
    npx hardhat compile
    ```

5. Deploy the smart contracts:
    ```sh
    npx hardhat run scripts/deploy.js --network <network-name>
    ```

6. Run tests:
    ```sh
    npx hardhat test
    ```

### License

This project is licensed under the MIT License.