### Environment Setup
1. Install Rust from https://rustup.rs/
2. Install Solana from https://docs.solana.com/cli/install-solana-cli-tools#use-solanas-install-tool

### Build and test for program compiled natively
```
$ cargo build
$ cargo test
```

### Build and test the program compiled for BPF
```
$ cargo build-bpf
$ cargo test-bpf
```

# Token Flow

create token -> create token account -> mint

### Create a token account
```
$ spl-token create-account [ TOKEN_ADDRESS ] --owner [ keypair.json | WALLET_ADDRESS ]
```

### Get token account info
Get token account info with `TOKEN_ADDRESS` and `OWNER_ADDRESS`
```
$ spl-token account-info [TOKEN_ADDRESS] [OWNER_ADDRESS]
```

Get token account info with a specific `TOKEN_ACCOUNT_ADDRESS`
```
$ spl-token account-info --address [TOKEN_ACCOUNT_ADDRESS]
```

### Mint token to token account
```
$ spl-token mint [TOKEN_ADDRESS] [TOKEN_AMOUNT] [RECIPIENT_TOKEN_ACCOUNT_ADDRESS] --mint-authority [token_owner_keypair.json]
```
