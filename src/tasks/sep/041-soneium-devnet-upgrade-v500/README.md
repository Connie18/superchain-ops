# 041-soneium-devnet-upgrade-v500

Status: [EXECUTED](https://sepolia.etherscan.io/tx/0x29555623eff4c66473c305ea651b22f188c58d12596066736aaa8f6102556e1c)

## Objective

Updates SONEIUM devnet to U17.

## Deploy OPCM

```bash
./bin/op-deployer bootstrap implementations \
  --l1-rpc-url=https://ethereum-sepolia-rpc.publicnode.com \
  --outfile=bootstrap_implementations.json \
  --private-key=$PRIVATE_KEY \
  --protocol-versions-proxy=0x59a3e4f7c89d2b2b824af42fd6e888726bdbce40 \
  --superchain-config-proxy=0xc92831eb4544053dc330ab2cd4164e1eb3157a8e \
  --superchain-proxy-admin=0x664e70e3d58eee0eef8b6b192015f43ab7323007 \
  --challenger=0x2D5cD08643086a42b0BCA5Adb1D755e80Cd5FE55 \
  --upgrade-controller=0xfb0f8937a0d6999c67e8a01310ebf7fe1859205f \
  --artifacts-locator file:///path/to/repo/optimism/packages/contracts-bedrock/forge-artifacts
```

```log
INFO [11-12|13:44:25.725] Load database journal from disk
INFO [11-12|13:44:25.725] State snapshot generator is not found
INFO [11-12|13:44:25.726] Initialized path database                readonly=true triecache=0.00B statecache=0.00B buffer=0.00B history="entire chain"
INFO [11-12|13:45:24.776] Running chain assertions on the DelayedWETH implementation at 0x33Dadc2d1aA9BB613A7AE6B28425eA00D44c6998 sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:25.113] Running chain assertions on the DisputeGameFactory implementation at 0x74Fac1D45B98bae058F8F566201c9A81B85C7D50 sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:26.444] Running chain assertions on the L1CrossDomainMessenger implementation at 0xb686F13AfF1e427a1f993F29ab0F2E7383729FE0 sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
WARN [11-12|13:45:28.392] Fault                                    addr=0xb686F13AfF1e427a1f993F29ab0F2E7383729FE0 label=L1CrossDomainMessengerImpl err="execution reverted" depth=2 op=253 byte4=0x3e47158c
WARN [11-12|13:45:28.392] callframe                                depth=1 byte4=0x329aa281 addr=0xfdAf657f7146c1AB9db4d70cEd5FDEa7dC4906c0 callsite= label=DeployImplementations
WARN [11-12|13:45:28.392] callframe                                depth=2 byte4=0x3e47158c addr=0xb686F13AfF1e427a1f993F29ab0F2E7383729FE0 callsite= label=L1CrossDomainMessengerImpl
WARN [11-12|13:45:28.392] Revert                                   addr=0xb686F13AfF1e427a1f993F29ab0F2E7383729FE0 label=L1CrossDomainMessengerImpl err="execution reverted" revertData=0x54e433cd depth=1
INFO [11-12|13:45:28.392] Running chain assertions on the L1ERC721Bridge implementation at 0x74f1aC50EB0BE98853805D381C884f5f9abDEcf9 sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
WARN [11-12|13:45:30.785] Fault                                    addr=0x74f1aC50EB0BE98853805D381C884f5f9abDEcf9 label=L1ERC721BridgeImpl         err="execution reverted" depth=2 op=253 byte4=0x3e47158c
WARN [11-12|13:45:30.785] callframe                                depth=1 byte4=0x329aa281 addr=0xfdAf657f7146c1AB9db4d70cEd5FDEa7dC4906c0 callsite= label=DeployImplementations
WARN [11-12|13:45:30.785] callframe                                depth=2 byte4=0x3e47158c addr=0x74f1aC50EB0BE98853805D381C884f5f9abDEcf9 callsite= label=L1ERC721BridgeImpl
WARN [11-12|13:45:30.785] Revert                                   addr=0x74f1aC50EB0BE98853805D381C884f5f9abDEcf9 label=L1ERC721BridgeImpl         err="execution reverted" revertData=0x54e433cd depth=1
INFO [11-12|13:45:30.785] Running chain assertions on the L1StandardBridge implementation at 0x61525EaaCDdB97D9184aFc205827E6A4fd0Bf62A sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:32.185] Running chain assertions on the MIPS at 0x6463dEE3828677F6270d83d45408044fc5eDB908 sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:32.186] Running chain assertions on the OPContractsManager at 0x704d236A529d7488669fF0627988E9fF7F3A1EcF sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:51.345] Running chain assertions on the OptimismMintableERC20Factory implementation at 0x8ee6fB13c6c9a7e401531168E196Fbf8b05cEabB sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:52.239] Running chain assertions on the OptimismPortal2 implementation at 0x7Cf803296662e8C72A6C1d6450572209aCF7f202 sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:55.783] Running chain assertions on the ETHLockbox implementation at 0x784d2F03593A42A6E4676A012762F18775ecbBe6 sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:45:56.644] Running chain assertions on the SystemConfig impl at 0x2fA28989fc559836E9d66dFf3010C7F7f41c65ED sender=0xb1c99bd22B5f80e553127a8565B6D11e51f351ad
INFO [11-12|13:46:11.420] transaction broadcasted                  id=0cfa7f..24829f nonce=0
INFO [11-12|13:46:11.421] Publishing transaction                   service=transactor tx=0x553ca83f444b4b45bfe0efb34f064ebbacbe30bb4fa7683cc5cb68a044d40bb5 nonce=308 gasTipCap=1,000,000,000 gasFeeCap=3,000,000,000 gasLimit=5,627,241
INFO [11-12|13:46:12.487] Transaction successfully published       service=transactor tx=0x553ca83f444b4b45bfe0efb34f064ebbacbe30bb4fa7683cc5cb68a044d40bb5 nonce=308 gasTipCap=1,000,000,000 gasFeeCap=3,000,000,000 gasLimit=5,627,241 tx=553ca8..d40bb5
WARN [11-12|13:46:12.790] Failed to create a transaction, will retry service=transactor err="failed to call: execution reverted, reason: 0x"
WARN [11-12|13:46:16.958] Failed to create a transaction, will retry service=transactor err="failed to call: execution reverted, reason: 0x"
WARN [11-12|13:46:23.225] Failed to create a transaction, will retry service=transactor err="failed to call: execution reverted, reason: 0x"
INFO [11-12|13:46:24.766] Transaction confirmed                    service=transactor tx=553ca8..d40bb5 block=f98877..7f548b:9611795 effectiveGasPrice=1,000,000,014
INFO [11-12|13:46:27.398] transaction broadcasted                  id=771250..7b3c91 nonce=0
INFO [11-12|13:46:27.398] transaction confirmed                    id=0cfa7f..24829f completed=1 total=2 hash=0x553ca83f444b4b45bfe0efb34f064ebbacbe30bb4fa7683cc5cb68a044d40bb5 nonce=0 creation=0x0000000000000000000000000000000000000000
INFO [11-12|13:46:27.398] Publishing transaction                   service=transactor tx=0x415e1db3efeddb2b19ba3b5cca26f6208c7be6cd61e1a28973e8c7decfc73282 nonce=309 gasTipCap=1,000,000,000 gasFeeCap=3,000,000,000 gasLimit=2,767,832
INFO [11-12|13:46:28.214] Transaction successfully published       service=transactor tx=0x415e1db3efeddb2b19ba3b5cca26f6208c7be6cd61e1a28973e8c7decfc73282 nonce=309 gasTipCap=1,000,000,000 gasFeeCap=3,000,000,000 gasLimit=2,767,832 tx=415e1d..c73282
INFO [11-12|13:46:37.166] Transaction confirmed                    service=transactor tx=415e1d..c73282 block=011618..aa68cc:9611796 effectiveGasPrice=1,000,000,015
INFO [11-12|13:46:37.166] transaction confirmed                    id=771250..7b3c91 completed=2 total=2 hash=0x415e1db3efeddb2b19ba3b5cca26f6208c7be6cd61e1a28973e8c7decfc73282 nonce=0 creation=0x0000000000000000000000000000000000000000
INFO [11-12|13:46:37.166] deployed implementations
```

## Simulation & Signing

```bash
cd src/tasks/sep/041-soneium-devnet-upgrade-v500

# Testing
SIMULATE_WITHOUT_LEDGER=1 just --dotenv-path $(pwd)/.env simulate

# Commands to execute
just --dotenv-path $(pwd)/.env sign

SIGNATURES=0xb9228a676319006bfecd5b0f833c7ca38991342e8e3db05bf9d669fc1410f13f37124ccdbe459b647b165d3d8a761411d2e4a28332731269b1beb7d995271c661c just execute
```
