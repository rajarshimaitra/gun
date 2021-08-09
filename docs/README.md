# Go Up Number!

`gun` is a CLI Bitcoin wallet for plebs, degenerates and revolutionaries.
Its distinguishing features is the ability to do peer-to-peer betting.

** ⚠ WARNING EXPERIMENTAL **

The wallet is alpha quality.
It will be buggy.
The underlying wallet functionality is built with the [Bitcoin Dev Kit](bitcoindevkit.org) but the betting functionality is freshly engineered.

Only put into it what you are willing to lose.
Thank you in advance for your sacrafice.

## Install

For now, just build the project yourself.

``` sh
git clone https://github.com/LLFourn/gun
cd gun
cargo install --path .
# or the edgy version if you are on nightly
cargo -Z avoid-dev-deps install --features=nightly --path .
# Make sure ~/.cargo/bin is in your $PATH
```
## Basic Wallet

The cli is decently documented with `--help` but here's a few things to get you started:

### Initialize wallet

``` sh
gun init bitcoin # or regtest or testnet
```

By default your wallet config and db will be stored in `~/.gun` and your seed words will be in `~/.gun/seed.txt`.

**save your seedwords somewhere else (don't delete them though)**

### Get an address

``` sh
gun address new
```

### Send coins


``` sh
gun send <address> 0.1BTC
```

Send all coins in your wallet

``` sh
gun send <address> all
```

### Check balance

Check your wallet's balance:

``` sh
gun -s balance
```

Check your wallet's balance but sync before:

``` sh
gun -s balance
```

Before any command you can put `-s` before it to tell the wallet it should sync with the blockchain before continuing.