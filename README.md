# midas-chain config for testnet

MultiversX testnet configuration files used in conjunction with mx-chain-go project.
For more info how to connect to the testnet, please check [here](https://docs.multiversx.com/validators/nodes-scripts/config-scripts/)

## run an Midas observer/validator with docker

### build docker image
```docker image build . -t chain-testnet-local -f ./docker/Dockerfile```

### run node with docker
```
CONFIG_FOLDER=path/to/folder/with/pem/file
docker run --mount type=bind,source=${CONFIG_FOLDER}/,destination=/data chain-testnet-local --validator-key-pem-file="/data/validatorKey.pem" --log-level *:DEBUG
```