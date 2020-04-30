# How to deploy contracts.

**Checkout contracts code from repository**

```shell
git checkout https://github.com/mcdexio/mai-protocol-v2.git

cd mai-protocol-v2
```

**Build**

```
# install dependencies
npm install

# compile contracts
./node_modules/.bin/truffle compile --all
```

**Test**

> Running unit tests is an optional step. It requires an ethereum node like ganache or testrpc.

```shell
# run test
./node_modules/.bin/truffle test
```

**Deploy**

```shell
# deploy
./node_modules/.bin/truffle migrate --network [network to deploy]
```

There are some hints if you want to customize your deployment:

- Default we use a fake price feeder for test purpose, switch to what ever your like to use another feeder. Find out more in file migrations/6_chainlink_inverse_price.js and migrations/14_amm_eth.js;

- Modify configuration in truffle.js to choose your target network;

**Done**

Feel free to try your fresh Mai Protocol V2.
