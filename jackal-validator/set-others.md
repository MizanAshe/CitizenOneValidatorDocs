# Set Others

For every new session, you will need to reset variables and set others before starting the node.

```
CHAIN="woof-2"
ALIAS="REPLACE_ME"
MONIKER="REPLACE_ME"
```

```
wget -O ~/.canine/config/genesis.json https://raw.githubusercontent.com/JackalLabs/woof/master/genesis/woof2.json
```

```
SEEDS=$(wget https://raw.githubusercontent.com/JackalLabs/woof/master/genesis/seeds.txt -q -O -)
```

```
PEERS=$(wget https://raw.githubusercontent.com/JackalLabs/woof/master/genesis/peers.txt -q -O -)
```

```
sed -i.bak -e "s/^seeds *=.*/seeds = \"$SEEDS\"/; s/^persistent_peers *=.*/persistent_peers = \"$PEERS\"/" ~/.canine/config/config.toml
```

Use the following to review .toml file to confirm peers and seeds are correct:

```
/sudo nano /root/.canine/config/config.toml
```

```
// These are the lines to review below. 
// If incorrect, you can manually add correct seeds and peers.
// Then, save and close file.

# Comma separated list of seed nodes to connect to
seeds = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"

# Comma separated list of nodes to keep persistent connections to
persistent_peers = "xxxxxxxxxxxxx,xxxxxxxxxxxxxx,xxxxxxxxxxxxxxx"

```

Note: \[Current seeds, peers, and related info are currently located at: [https://github.com/JackalLabs/woof](https://github.com/JackalLabs/woof)]

```
GAS="0.002ujkl"
```

```
sed -i.bak -e "s/^minimum-gas-prices *=.*/minimum-gas-prices = \"$GAS\"/" ~/.canine/config/app.toml
```

**/\*\* Stop here, ask for faucet funds, provide wallet address \*\*/**&#x20;

**Start node with following command**

```
canined start
```
