# Full instructions for setup

Welcome to MaximizeAI Validator 🔥

## Setup environment
```bash
git clone https://github.com/maximizeai-dev/maximizeai-subnet
```

### Install system dependencies
You can directly use our one-click installation script to create the environment
```bash
cd script
bash setup_btcli.sh
```
Or you can install the dependencies manually
```bash
# creat venv 
python3 -m venv btcli_venv
source btcli_venv/bin/activate

# setup bittensor sdk
pip install bittensor
pip install -e .
```

### Get hot and coldkeys onto your machine
Securely move them onto your machine as usual. Either with the btcli or with a secure method of your choosing
```bash
btcli wallet create
```
## Register your validator
```bash
btcli subnet register --netuid 367 --subtensor.network test --wallet.name Your Coldkey Name --wallet.hotkey Your Hotkey Name
```

## Start validator
```bash
python neurons/miner.py --netuid 367 --subtensor.network test --wallet.name Your Coldkey Name --wallet.hotkey Your Hotkey Name --logging.debug
```

