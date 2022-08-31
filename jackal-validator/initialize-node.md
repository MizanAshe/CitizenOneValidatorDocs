# Initialize Node

**Initialize Variables**

* &#x20;_\[Replace REPLACE\_ME with desired alias and moniker]_

```
CHAIN="woof-2"
ALIAS="REPLACE_ME"
MONIKER="REPLACE_ME"
```

**Initiate chain**

```
canined init $MONIKER --chain-id=$CHAIN
```

```
canined keys add $ALIAS
```

**Get latest Woof JSON file**

```
wget -O ~/.canine/config/genesis.json https://raw.githubusercontent.com/JackalLabs/woof/master/genesis/woof2.json
```

**Add Genesis Account**

(Replaced "\<WALLETADDRESS>" with node wallet address as appropriate.) &#x20;

```
canined add-genesis-account <WALLETADDRESS> 250000000ujkl
```

The following node info will display something like this:

{% code overflow="wrap" %}
```
canined init $MONIKER --chain-id=$CHAIN 
moniker":"<MONIKER_NAME>","node_id":"xxxxxxxxxxxxxxxxxxxxxxxxxxxx"

keyring passphrase: xxxxxxxxxx

name: <name> 
type: local 
address: jklxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx 
pubkey: '{"@type":"/cosmos.crypto.secp256k1.PubKey","key":"xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"}' mnemonic: ""

Important write this mnemonic phrase in a safe place. 
It is the only way to recover your account if you ever forget your password.

[MNEMONIC PHRASE xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx]
```
{% endcode %}
