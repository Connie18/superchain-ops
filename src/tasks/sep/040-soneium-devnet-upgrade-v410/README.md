# 040-soneium-devnet-upgrade-v410

Status: [EXECUTED](https://sepolia.etherscan.io/tx/0x73b5d8161fcf5763a11896a818861ade1c10ae1397686db5037eae13f210dd09)

```bash
cd src/tasks/sep/040-soneium-devnet-upgrade-v410

# Testing
SIMULATE_WITHOUT_LEDGER=1 just --dotenv-path $(pwd)/.env simulate

# Commands to execute
just --dotenv-path $(pwd)/.env sign

SIGNATURES=0x704c5488dbb0f13475d62a8be7bc02361a1fc3492563c26e5dd5a06004ec43837b4bc7f4bd92a0d44cbd810e5597dfddc6dde9b0d8cea5851a081f62965c4d201c just execute
```