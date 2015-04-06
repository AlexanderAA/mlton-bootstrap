# C/assembly files to bootstrap MLton compiler on OpenBSD amd64

### Build instructions - with MLton compiler available on OpenBSD amd64 machine

```sh
    git clone https://github.com/MLton/mlton.git
    git checkout on-20130715-release
    cd mlton
    gmake
    cd mlton && mlton -stop g -target self mlton.mlb
```

### Build instructions - with MLton compiler available on Linux/other machine

```sh
    git clone https://github.com/MLton/mlton.git
    git checkout on-20130715-release
    cd mlton
    gmake
    bin/add-cross unknown amd64 openbsd localhost
    cd mlton && mlton -stop g -target unknown mlton.mlb
```

### To run tests

```sh
    bin/regression -cross unknown
```
