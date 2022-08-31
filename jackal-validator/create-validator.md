# Create Validator

**Make sure node is running before moving forward.**

**Create Validator**

```
canined tx staking create-validator \
  --from "$ALIAS" \
  --amount "1000000ujkl" \
  --pubkey "$(canined tendermint show-validator)" \
  --chain-id=$CHAIN \
  --moniker="$MONIKER" \
  --commission-max-change-rate 0.01 \
  --commission-max-rate 0.20 \
  --commission-rate 0.05 \
  --min-self-delegation 1 \
  --details="XXXXXXX" \
  --security-contact="XXXXXXX" \
  --website="XXXXXXX" \
  --fees="2500ujkl" \
  --sequence=0
```

_(Replaced "XXXXXXX" values as appropriate.)_ &#x20;

You can then check status of node.

```
canineed status
```

You can also check balance.

```
canined q bank balances <wallet address>
```
