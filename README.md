# HyperspaceAI-Node

## Linux CLI
[Official repository](https://github.com/hyperspaceai/aios-cli?tab=readme-ov-file) with all of the commands (if needed)
### Install
```
curl https://download.hyper.space/api/install | bash

source /root/.bashrc
```

### Start your node
```console
# Create a screen ro run it in background for later
screen -S hyperspace

# Run node
aios-cli start
```
* To continue, minimize your screen using `CTRL+A+D` or Open second terminal

### Config Node
```console
# Run this to see what models are required
aios-cli hive select-tier 5
# Download a required model
aios-cli models add hf:TheBloke/phi-2-GGUF:phi-2.Q4_K_M.gguf
# Import your private key - Create a .pem file using nano .pem and input a privatekey (You can get a privatekey from browser version)
aios-cli hive import-keys ./my.pem
# Set those keys as the preferred keys for this session
aios-cli hive login
# Make sure the model is registered
aios-cli hive connect
aios-cli hive select-tier 5
# To check your current multiplier and points
aios-cli hive points
```

# Usefull commands
```console
# Update node
aios-cli version
# Stop node
aios-cli kill
```
