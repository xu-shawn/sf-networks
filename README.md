# networks (private directory)

This repository contains the networks as required by the NNUE evaluation in Stockfish:

https://github.com/official-stockfish/Stockfish/

It is intended to preserve all networks used in the master branch of Stockfish, to ensure this branch can always be built,
irrespective of the state of the stockfish infrastructure that usually provides these networks.

https://tests.stockfishchess.org/nns

This website also documents who authored the network, and when and how it was tested.

For a given Stockfish version, the default network name (UCI option `EvalFile`),
specifies the compatible and tested network file name. Other combinations may or may not work.

The preferred way to obtain the networks is to rely on the integration in the build process of stockfish,
i.e. either using `make net` or by building the code. This will automatically download the net from

`https://tests.stockfishchess.org/api/nn/nn-<SHA>.nnue`

where `<SHA>` are the first 12 digits of the sha256sum of the nn.nnue data file (`sha256sum nn.nnue | cut -c1-12`).

All networks in this repository were [uploaded](https://tests.stockfishchess.org/upload) by the authors under the CC0 license.
