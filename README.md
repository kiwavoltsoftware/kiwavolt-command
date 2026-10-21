# Kiwavolt Command & Miner

Windows software for a private PRL solo-mining fleet. Kiwavolt Command includes its own mining engine, node and dashboard in one installed app. RTX 50-series CUDA engine, 0% developer fee.

## Download
Use the Windows installers under [Releases](https://github.com/kiwavoltsoftware/kiwavolt-command/releases/latest).

- **Host PC:** Kiwavolt Command 0.4.2 installer. Mining is built in; no separate Miner app.
- **Other GPU PCs:** use the same Command installer with your private `My-Kiwavolt-Pool.pearlpair` file beside it. Setup imports the connection, encrypts it locally and enables worker mode. Worker mode runs no blockchain node or Stratum server. Open Mining and press Start mining. PCs need LAN access to the existing host.
- This is a private-fleet edition configured for its owner's public reward address. It is not a general wallet or a public mining service. Check the displayed reward address before starting.

## Updates
Install this release once on older PCs to add the updater. In Command, open Settings > App updates. Older standalone Miner installations retain their own update check. Stop local mining before installation. Updates are downloaded from this repository and require a valid Ed25519 signature and matching SHA-256 digest before the installer runs. Installing is an explicit user action; releasing a version does not silently install software on other PCs.

Command removes the separate legacy Miner app on the host while retaining its data. Settings, encrypted pairing, worker names, chain data and logs remain in their existing Local AppData folders. Host updates briefly restart the pool dashboard; remote miners reconnect. The node stays running. The node binary is retained during routine app updates; node upgrades require separate maintenance.

Installers are not Authenticode signed. Signed update metadata is separate from Windows publisher signing.

Never upload pairing files, RPC passwords, wallet seeds or private keys to this repository. No such files are included in releases.

## Validation
46 automated tests passed, packaged RTX 5080 GPU self-test passed, and the packaged host/miner submitted two accepted blocks on an isolated test chain. Only one physical GPU was available; multi-GPU routing is tested with simulated devices. No mainnet block reward is claimed by these tests.

Third-party license notices are included with each installer. Mining performance and rewards are not guaranteed.
