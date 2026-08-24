# DSCoin - Blockchain Cryptocurrency System

## Overview 
Complete Python implementation of a blockchain-based cryptocurrency with:
- Honest miner implementation (`DSCoinHonest`)
- Malicious miner handling (`DSCoinMalicious`)
- Full transaction lifecycle
- Merkle tree verification

## How to Use

1. Clone the repo:
```bash
git clone https://github.com/harshitaagrawal634/CryptoCoin.git
cd dscoin
```

2. Run the system:
```bash
python dscoin_system.py
```

## Key Components

| Class               | Description                          |
|---------------------|--------------------------------------|
| `DSCoinHonest`      | Standard blockchain implementation   |
| `DSCoinMalicious`   | Handles malicious mining scenarios   | 
| `Members`           | User accounts with coin wallets      |
| `Moderator`         | Initial coin distribution system     |
| `TransactionQueue`  | Pending transaction management       |

## Example Usage

```python
# Initialize
ds = DSCoinHonest()
alice = Members("101")
bob = Members("102")

# Distribute coins
mod = Moderator()
mod.initialize_dscoin(ds, 100)

# Send payment
alice.initiate_coinsend("102", ds)

# Mine block
bob.mine_coin(ds)
```

## Testing
The system includes built-in tests for:
- Coin distribution
- Transaction validation
- Block mining
- Chain verification

## License
MIT License
