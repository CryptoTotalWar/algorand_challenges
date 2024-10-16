# Algorand Testnet Account Generator

This project demonstrates how to connect to the Algorand testnet, generate a new account, and manage the mnemonic phrase securely using a `.env` file. The code utilizes the `algosdk` library for interacting with the Algorand blockchain.

## Prerequisites

Before running this project, ensure you have the following installed:

- Python 3.12 or higher
- Pip (Python package manager)
- Algokit (pipx install algokit)

## Getting Started

Follow the instructions below to set up the project on your local machine.

### 1. Clone the Repository or skip setup and just enter a codespace!

```bash
git clone https://github.com/yourusername/use_algorand_testnet.git
cd use_algorand_testnet
```

### 2. Let dependencies install on codespace start

Wait for the dependencies to finish setting up.

### 3. Run the Script

To generate a new Algorand account or use an existing one, run the following command:

```bash
python main.py
```

### 4. Understanding the Output

- If a mnemonic phrase is not found in the `.env` file, a new Algorand account will be generated, and the mnemonic will be saved to the `.env` file.
- If the mnemonic already exists, the script will load the existing account and display the account address.
- The script will also confirm the connection to the Algorand testnet.

## Code Overview

- `main.py`: The main script that connects to the Algorand testnet, generates accounts, and manages the mnemonic phrase.
- `.env`: A file that stores the mnemonic phrase securely.

### Key Functions

- `connect_to_algorand_testnet()`: Initializes the Algorand client to connect to the testnet.
- `generate_new_account()`: Generates a new Algorand account and returns the address and mnemonic phrase.
- `write_mnemonic_to_env(mnemonic_phrase)`: Saves the generated mnemonic to a `.env` file.
- `load_passphrase_from_env()`: Loads the mnemonic from the `.env` file.
- `get_private_key_from_mnemonic(mnemonic_phrase)`: Converts the mnemonic back to the private key.

## How to fund your testnet account with AlgoKit CLI

To obtain ALGO for testing on the Algorand testnet, follow these steps:

1. **Login to the Dispenser**:
   ```bash
   algokit dispenser login
   ```

2. **Fund Your Account**:
   ```bash
   algokit dispenser fund -r <your-account-address> -a 10000000
   ```

3. **Confirm the Transaction**:
   After funding, you'll receive a transaction confirmation. You can view the transaction details at the provided link.

## Important Notes

- The mnemonic phrase is sensitive information. Store it securely and do not expose it publicly.
- The testnet is a simulated environment for testing purposes.

## Acknowledgments

- [Download AlgoKit!](https://developer.algorand.org/algokit/?utm_source=af_employee&utm_medium=social&utm_campaign=algokit_sarajane&utm_content=download&utm_term=EME)
- [Algorand Developer Documentation](https://developer.algorand.org/docs/)
- [Algorand SDK for Python](https://github.com/algorand/py-algorand-sdk)
- [Nodely](https://nodely.io/docs/free/start) 

## Join the AlgoDevs Community!

- [Join us on X](https://x.com/algodevs) 
- [Join us on Discord](https://discord.com/invite/algorand) 
