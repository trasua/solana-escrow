### Environment Setup
1. Install Rust from https://rustup.rs/
2. Install Solana from https://docs.solana.com/cli/install-solana-cli-tools#use-solanas-install-tool

### Build and test for program compiled natively
```
cargo build
cargo test
```

### Build and test the program compiled for BPF
```
cargo build-bpf
cargo test-bpf
```

# Get token currently owned
```
spl-token accounts --verbose
```

# Create fungible token and non-fungible token
### Create a fungible token
```
spl-token create-token [--decimals 9]
```

### Create a non-fungible token
```
spl-token create-token --decimals 0
```

# Token Flow

create token -> create token account -> mint or transfer

### Create a token account
```
spl-token create-account [ TOKEN_ADDRESS ] --owner [ keypair.json | WALLET_ADDRESS ]
```

### Get token account info
Get token account info with `TOKEN_ADDRESS` and `OWNER_ADDRESS`
```
spl-token account-info [TOKEN_ADDRESS] [OWNER_ADDRESS]
```

Get token account info with a specific `TOKEN_ACCOUNT_ADDRESS`
```
spl-token account-info --address [TOKEN_ACCOUNT_ADDRESS]
```

### Mint token to token account
```
spl-token mint [TOKEN_ADDRESS] [TOKEN_AMOUNT] [RECIPIENT_TOKEN_ACCOUNT_ADDRESS] --mint-authority [token_owner_keypair.json]
```

### Transfer to specific recipient token account
```
spl-token transfer [TOKEN_ADDRESS] [TOKEN_AMOUNT] [RECIPIENT_TOKEN_ACCOUNT_ADDRESS]
```
### Create a token account for recipient and transfer token to it
```
spl-token transfer --fund-recipient [TOKEN_ADDRESS] [TOKEN_AMOUNT] [RECIPIENT_ACCOUNT_ADDRESS]
```
