# CRaC JDK

## Build

CRaC JDK with Minicriu have extended build procedure.

1. Build the minicriu project
```
git clone https://github.com/CRaC/minicriu
make -C minicriu
```

2. Minicriu is not directly supported by the build system, you need to provide the path via C/C++ flags

```
bash configure --with-extra-cxxflags=-I$PWD/minicriu --with-extra-ldflags="-L$PWD/minicriu -lminicriu-client"
make images
```
