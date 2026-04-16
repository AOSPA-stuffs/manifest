# Paranoid Android #

### Creating workspace folder ###

```bash
mkdir AOSPA
cd AOSPA
```

### Initializing repo ###

```bash
repo init -u https://github.com/AOSPA-stuffs/manifest -b vauxite
```

### Initializing depth repo ###

```bash
repo init --depth=1 -u https://github.com/AOSPA-stuffs/manifest -b vauxite
```

### Downloading the source tree ###

```bash
repo sync -c --force-sync --current-branch --no-tags -j$(nproc --all)
```

## Building ##

```bash
./rom-build.sh DEVICE -j$(nproc --all)
```
